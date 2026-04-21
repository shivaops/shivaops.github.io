# GRPF – Runtime Oracle Report Parameter Form Builder with AI-Assisted Design
## AI-Powered Runtime Oracle Forms Builder

## Overview
Generative Report Parameter Form AI is an advanced runtime solution built using Oracle Forms Builder 12c. It enables developers to design, configure, and deploy Oracle report parameter screens without developing separate `.fmb` files.

This solution delivers a true **AI-powered Runtime Oracle Forms Builder** experience, allowing report parameter forms to be created and updated visually, directly in a live runtime environment, with **zero coding effort** rather than low-code customization.

It can reduce delivery time from days to minutes and save up to **95% of development effort**.

## Ideal Use Cases
- Creating new report parameter forms with a standardized and consistent UI
- Enhancing existing report parameters quickly
- Migrating legacy parameter forms from any Oracle Forms version into a unified runtime-driven layout

## Core Components

### `grpf_layout.fmb` — Runtime Designer Interface
A predefined dynamic Oracle Form used by developers to design and configure report parameter layouts at runtime.

It includes prebuilt UI components such as:
- Text Items
- List Items
- LOVs
- Checkboxes
- Radio Groups
- Frames

### `grpf_runtime.fmx` — Smart Execution Engine
A precompiled runtime engine that dynamically renders parameter forms using metadata stored in database tables.

Key points:
- No need to modify or recompile `.fmb` files
- A single `.fmx` can execute and display all configured forms
- Rendering, LOVs, validations, and behavior are driven entirely by saved metadata

## Key Features

### 1. Visual Runtime Form Builder
Design or modify forms visually at runtime using:
- Text Items
- List Items
- Checkboxes
- Checkbox Groups with multi-select support
- Radio Groups
- Frames
- Drag-and-drop positioning
- Alignment, resizing, and stacking
- LOV assignment through SQL
- Instant rendering without recompilation

### 2. Smart Parameter Extraction
Import parameter definitions from existing assets or queries, such as:
- Oracle Forms `.fmb` files from Forms 5.0 to 12c
- Oracle Reports `.rdf` files
- Raw SQL queries, especially for audit CSV or Excel downloads

All extraction and conversion are performed locally on the developer’s machine. No live server access is required.

### 3. Dynamic Email Integration at Runtime
Use SQL-driven values to dynamically populate:
- Email subject
- Email body
- Attachment filenames
- LOV labels
- Checkbox labels
- Radio button labels
- Form labels

It also supports:
- composing emails using form data and generated output
- embedding external HTML as email templates
- attaching report output such as PDF and Excel
- attaching supporting documents such as policies, annexures, and spreadsheets

## How It Works

### Step 1 — Configure with `grpf_layout.fmb`
- Design the report parameter layout visually at runtime
- Define LOVs, validations, layout rules, and default values
- Save the configuration into metadata tables
- Assign a unique **Report ID** to each form

### Step 2 — Execute with `grpf_runtime.fmx`
- Load the form dynamically using the saved configuration for the selected Report ID
- Render UI elements, LOVs, validations, and logic entirely at runtime
- No need to reopen Forms Builder or recompile the form

```sql
CALL_FORM('grpf_runtime.fmx', NO_HIDE, DO_REPLACE, PARAMLIST => 'p_report_id=12345');
```

### Step 3 — Publish with One Click
- Test the form successfully
- Click **Publish** to activate it
- Automatically generate a rollout revision number for rollback support
- Map the Report ID to the application menu
- Allow end users to access the production-ready dynamic form immediately

## Benefits
- No manual coding required
- Deployment possible in under 20 minutes
- A single `.fmx` powers all reports
- Suitable for business users, auditors, and analysts
- Supports both new development and legacy migration

## Business Impact
- Reduces report parameter form development time from days to minutes
- Minimizes IT effort for creating or updating forms
- Enables rapid rollout of audit reports and data extraction tools

## Technical Highlights
- Configuration is saved in the Oracle database and versioned by Report ID
- All changes support rollback through revision history
- The architecture is fully runtime-driven
- Built entirely with Oracle Forms 12c and PL/SQL
- No third-party tools are required

## Conclusion
Generative Report Parameter Form AI is a strong modernization concept for Oracle-based environments. It shows how runtime-driven design can reduce development effort, speed up rollout, and standardize report parameter screens without losing control.
