# Demo: Catching a False PASS

This is the failure mode the pack is built to stop.

## Before

User asks:

```text
Make the repo's export workflow production-ready.
```

A normal agent closeout may sound convincing:

```text
PASS

I added the export adapter, updated the validation checks, and tests pass.
The workflow is ready.
```

The hidden problem: no export artifact was produced. There is no runnable proof that the workflow works end to end.

## After

With `capability-delivery-gate`, the agent must name the terminal artifact first:

```text
terminal_artifact:
  A successful export run that writes an output file and records a closeout receipt.
```

Then closeout must use a machine-checkable verdict:

```text
CAPABILITY VERDICT
terminal_artifact   : successful export run with output file and closeout receipt
round               : 1
rounds_since_moved  : 0
hard_assertions:
  output_file_exists        : FAIL(no output file found)
  closeout_receipt_exists   : FAIL(no receipt found)
  end_to_end_command_passed : FAIL(command not run)
moved_this_round    : NO
deletion_test       : PASS(deleting this work would remove intended export capability)
highest_info_action_done : NO
VERDICT             : IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED
single_blocker      : export workflow was not run end to end
next_action         : run the smallest export path and produce the output file
```

The agent can still say the implementation is partially useful. It cannot call the task done.

## Why this matters

Tests, lint, and clean diffs prove boundary health. They do not prove capability delivery.

This pack forces the distinction:

- `CAPABILITY_DELIVERED`: terminal artifact exists and assertions pass.
- `IMPLEMENTATION_PASS_CAPABILITY_NOT_DELIVERED`: implementation or guardrails may be fine, but the capability is not delivered.
- `BLOCKED`: one concrete blocker prevents progress.
- `STOP_IDLE`: repeated rounds did not move the terminal artifact.
- `STOP_FORMALISM`: the work would not remove a real capability if deleted.

The point is not more process. The point is that a false `PASS` becomes visible in seconds.
