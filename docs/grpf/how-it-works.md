# How It Works

## Step 1 — Configure
Use `grpf_layout.fmb` to design the layout and save metadata.

## Step 2 — Execute
Use `grpf_runtime.fmx` to load the form dynamically based on the selected Report ID.

## Step 3 — Publish
Promote the tested configuration and make it available to end users.

```sql
CALL_FORM('grpf_runtime.fmx', NO_HIDE, DO_REPLACE, PARAMLIST => 'p_report_id=12345');
```
