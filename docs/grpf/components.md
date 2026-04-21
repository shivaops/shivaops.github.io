# Core Components

## `grpf_layout.fmb`
This is the runtime designer interface used by developers to configure layouts and parameter behavior.

## `grpf_runtime.fmx`
This is the runtime engine that reads metadata and renders the configured form dynamically.

## Why this split matters
The designer and the runtime engine have separate roles, which helps keep development flexible while keeping execution standardized.
