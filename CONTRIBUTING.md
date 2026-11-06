# Contributing

Work in this sandbox is done by agents through GitHub issues.

## Workflow

1. **Open an issue** describing the task and add the `agent-task` label.
2. **The Router sweeps** open `agent-task` issues. It only accepts issues
   opened by the repo owner. Each accepted issue is handed to a Worker in an
   isolated cloud session, and its label changes to `agent-working`.
3. **The Worker** does one of two things:
   - Opens a **draft pull request** from branch `agent/issue-N`
     (where `N` is the issue number), or
   - Comments on the issue starting with `QUESTION:` if the issue is unclear.
4. **The owner** replies to any question with a comment starting with
   `ANSWER:`, then reviews and merges the pull request.

## Rules

- Only the repo owner merges pull requests. Workers never merge.
- One issue, one branch, one draft pull request.
