---
name: Flowchart Design
description: Create professional, consistent, client-facing flowcharts, process diagrams, and software architecture visualizations using HTML, CSS, and SVG. Defines visual semantics, colors, shapes, connectors, layout, typography, accessibility, and rendering standards.
---

# Flowchart Design Skill

## 1. Purpose

Create visually polished, professional, easy-to-understand diagrams for client-facing technical reports.

Diagrams must communicate system architecture, business processes, data flows, integrations, and system transformations.

The visual style should resemble modern enterprise consulting documentation: clean, minimal, structured, and consistent.

Prioritize:
1. Clarity over decoration.
2. Consistent visual semantics.
3. Accurate representation of the actual system.
4. Readability for non-technical stakeholders.
5. Professional HTML rendering and PDF export.

## 2. General Design Principles

- Use a clean white canvas.
- Use a restrained semantic color palette.
- Maintain consistent component dimensions.
- Use clear directional arrows.
- Avoid unnecessary visual complexity.
- Group related components into logical boundaries.
- Use whitespace to establish visual hierarchy.
- Prefer short labels and concise descriptions.
- Never use color as the only indicator of meaning.
- Never invent system components, dependencies, or data flows.

Every diagram must have:
- A descriptive title.
- An optional short subtitle explaining its purpose.
- Clearly identifiable components.
- Directional connections.
- A legend when multiple semantic colors or connector types are used.

## 3. Color System

Use the following semantic color palette consistently across all diagrams.

### 3.1 Semantic Colors

| Semantic role | Color | Hex | Usage |
|---|---|---|---|
| Legacy | Slate | #64748B | Existing, old, or deprecated components |
| Primary | Blue | #2563EB | Active internal services and main components |
| Success | Green | #16A34A | Successful outcomes and improvements |
| Warning | Amber | #D97706 | Manual operations, bottlenecks, warnings |
| Error | Red | #DC2626 | Failures, critical errors, failure paths |
| External | Violet | #7C3AED | Third-party systems and external integrations |

### 3.2 Background Colors

Use light tinted backgrounds rather than saturated solid fills.

| Role | Background | Border |
|---|---|---|
| Legacy | #F1F5F9 | #94A3B8 |
| Primary | #EFF6FF | #93C5FD |
| Success | #F0FDF4 | #86EFAC |
| Warning | #FFFBEB | #FCD34D |
| Error | #FEF2F2 | #FCA5A5 |
| External | #F5F3FF | #C4B5FD |
| Neutral | #F8FAFC | #CBD5E1 |

### 3.3 Color Usage Rules

LEGACY / SLATE:
- Previous system components.
- Deprecated services.
- Old infrastructure.
- Components being replaced.

PRIMARY / BLUE:
- Active application components.
- Backend services.
- Internal APIs.
- Main processing operations.
- Current architecture components.

SUCCESS / GREEN:
- Successful outcomes.
- Completed operations.
- Improved processes.
- Verified improvements.
- Successful output paths.

WARNING / AMBER:
- Manual operations.
- Human approval.
- Manual data entry.
- Bottlenecks.
- Potential risks.
- Conditional attention points.

ERROR / RED:
- Failed operations.
- Error handling paths.
- Critical failures.
- Invalid data.
- Unresolved critical problems.

EXTERNAL / VIOLET:
- Third-party APIs.
- External SaaS providers.
- Payment gateways.
- External systems.
- Vendor integrations.

IMPORTANT:
- Do not color every new component green. New components should normally use blue.
- Green represents positive outcomes or verified improvements, not simply newly created components.
- Red must represent actual errors or critical risks, not ordinary processing.
- Amber must not be used for generic visual decoration.
- Use neutral colors for elements without a meaningful semantic state.

## 4. Flowchart Shape Standards

Use standard flowchart notation.

### 4.1 Terminator

Shape: Rounded rectangle / pill.

Meaning:
- Start.
- End.
- Workflow entry point.
- Workflow completion.

Appearance:
- Fully rounded corners.
- Light blue background.
- Blue border.
- Centered label.

Example labels:
- Start
- Request received
- Process completed
- Workflow finished

### 4.2 Process

Shape: Rectangle with rounded corners.

Meaning:
- Operation.
- Computation.
- API execution.
- Business operation.
- Service processing.

Appearance:
- 10px border radius.
- 1.5px border.
- Light blue background for active internal operations.
- Optional icon.

Example labels:
- Validate request
- Process payment
- Generate report
- Transform data
- Send notification

### 4.3 Decision

Shape: Diamond.

Meaning:
- Conditional branching.
- Boolean conditions.
- Validation results.
- Business rules.

Appearance:
- Amber background.
- Amber border.
- Centered short question.

Example labels:
- Is data valid?
- Payment successful?
- User authorized?
- Record exists?

Rules:
- Always label outgoing branches.
- Use YES / NO or meaningful condition labels.
- Avoid more than three outgoing branches unless necessary.
- Never use diamonds for ordinary processing operations.

### 4.4 Database / Persistent Storage

Shape: Cylinder.

Meaning:
- Relational databases.
- Data warehouses.
- Persistent data stores.
- Object storage when appropriate.

Appearance:
- Green-tinted background.
- Green border.
- Database icon optional.

Example labels:
- PostgreSQL
- Data warehouse
- Object storage
- Redis (persistent only if applicable)

IMPORTANT:
Do not represent queues, caches, or temporary storage as persistent databases unless that accurately describes their role.

### 4.5 External System

Shape: Rounded rectangle with external-service icon.

Meaning:
- Third-party services.
- External APIs.
- Vendor platforms.
- External integrations.

Appearance:
- Violet-tinted background.
- Violet border.
- Cloud or integration icon.

Example labels:
- Stripe API
- SendGrid
- External CRM
- Payment provider

A cloud shape is optional. Do not use cloud shapes for every service.

### 4.6 Manual Operation

Shape: Trapezoid or rounded rectangle with a person icon.

Meaning:
- Manual data entry.
- Human approval.
- Administrator intervention.
- Manual file upload.
- Manual reporting.

Appearance:
- Amber-tinted background.
- Amber border.
- Person icon.
- Clear indication of the responsible actor.

Example labels:
- Administrator uploads CSV
- Manual approval
- Operator reviews results

Manual operations should be visually distinguishable from automated processing.

### 4.7 Document / File

Shape: Document shape with a wavy bottom or a file-style rectangle.

Meaning:
- Input files.
- Generated reports.
- CSV / Excel files.
- PDF documents.
- Exported data.

Appearance:
- Neutral or blue-tinted background.
- File icon.
- Clearly identified file type.

Example labels:
- Input CSV
- Generated PDF
- Excel export

### 4.8 Subprocess

Shape: Rectangle with double vertical side lines.

Meaning:
- A nested workflow.
- A complex process represented separately.
- A reusable operation.

Appearance:
- Standard process styling.
- Two vertical internal boundary lines.

Example labels:
- Authentication workflow
- Data aggregation
- Payment processing

Use a separate diagram for complex subprocesses when necessary.

## 5. Connector Standards

Connectors must communicate the relationship between components.

### 5.1 Connector Types

| Connector | Style | Meaning |
|---|---|---|
| Standard flow | Solid arrow | Normal process flow |
| Data transfer | Solid arrow | Data movement |
| API request | Solid blue arrow | API communication |
| Async event | Dashed arrow | Asynchronous communication |
| Error flow | Red dashed arrow | Failure or exception path |
| Manual action | Amber arrow | Human intervention |
| Optional dependency | Dotted arrow | Optional relationship |

### 5.2 Connector Styling

- Default stroke width: 2px.
- Arrowhead: Filled triangle.
- Use orthogonal routing where possible.
- Prefer horizontal and vertical segments.
- Avoid unnecessary diagonal connections.
- Avoid overlapping connectors.
- Use rounded line joins.
- Place labels near the relevant connection.
- Connector labels should have a white background.

### 5.3 Direction

Default flow direction:
- Left to right for process flows.
- Top to bottom for layered architecture.
- Top to bottom for simple vertical workflows.

Do not mix directions unnecessarily.

### 5.4 Branch Labels

Decision branches must have explicit labels.

Good:
- YES
- NO
- SUCCESS
- FAILURE
- VALID
- INVALID

Bad:
- Unlabeled arrows.
- Ambiguous abbreviations.
- Labels placed far from their connectors.

## 6. Architecture Grouping

For system architecture diagrams, group components into logical boundaries.

Possible grouping categories:

- Presentation Layer.
- API Layer.
- Application Layer.
- Business Logic.
- Data Layer.
- Infrastructure.
- External Services.
- Third-party Integrations.

Grouping appearance:
- Background: #F8FAFC.
- Border: #E2E8F0.
- Border radius: 14px.
- Padding: 20px.
- Section title: 13px semibold.
- Optional small descriptive subtitle.

Group boundaries must not imply separate deployments unless that is factually correct.

Use labels such as:
- Internal System.
- External Provider.
- Cloud Infrastructure.
- Client Environment.

## 7. Component Status Labels

Use small status badges where necessary.

| Label | Meaning |
|---|---|
| NEW | Newly introduced component |
| MODIFIED | Existing component changed |
| REMOVED | Removed component |
| UNCHANGED | Existing component retained |
| AUTOMATED | Previously manual process automated |
| DEPRECATED | Scheduled for removal |
| OPTIONAL | Optional component |

Badge styling:
- Font size: 10px.
- Font weight: 600.
- Small horizontal padding.
- Rounded pill shape.
- Light semantic background.

Do not use badges on every component. Use them only when status adds useful information.

## 8. Layout and Dimensions

### 8.1 Canvas

| Property | Value |
|---|---|
| Background | #FFFFFF |
| Padding | 40px |
| Minimum width | 900px |
| Recommended width | 1200px |
| Height | Content-dependent |
| Grid spacing | 24px |

### 8.2 Nodes

| Property | Value |
|---|---|
| Width | 180–220px |
| Height | 76–100px |
| Border radius | 10px |
| Border width | 1.5px |
| Internal padding | 12–16px |
| Title font size | 14px |
| Description font size | 11–12px |
| Title weight | 600 |

Allow larger nodes when descriptions require additional space.

### 8.3 Groups

| Property | Value |
|---|---|
| Border radius | 14px |
| Border width | 1px |
| Padding | 20px |
| Internal spacing | 16–24px |
| Background | #F8FAFC |

### 8.4 Typography

Preferred font:
- Inter.

Fallback:
- system-ui
- -apple-system
- Segoe UI
- sans-serif

Hierarchy:
- Diagram title: 20px / 600.
- Diagram subtitle: 13px / 400.
- Group title: 13px / 600.
- Node title: 14px / 600.
- Node description: 11–12px / 400.
- Connector label: 11px / 500.
- Legend: 11px / 400.

Use dark slate for titles (#0F172A) and muted slate for secondary text (#64748B).

## 9. Diagram Complexity

Keep diagrams easy to understand.

Rules:
- Prefer 5–12 nodes per diagram.
- Avoid exceeding 15 nodes unless necessary.
- Split complex systems into multiple diagrams.
- Avoid crossing connectors.
- Avoid excessively long connector paths.
- Avoid unnecessary icons.
- Avoid paragraphs inside nodes.
- Use separate detailed diagrams for complex subprocesses.

If a diagram becomes difficult to read, split it into logical sections rather than shrinking all components.

## 10. Before vs. After Visualization

When documenting system transformation, use consistent visual conventions.

### BEFORE

Represent:
- Previous architecture.
- Existing components.
- Manual operations.
- Previous integrations.
- Previous limitations.

Use slate for legacy components.

Use amber for manual operations and bottlenecks.

Use red only for actual critical failures or problems.

### AFTER

Represent:
- Current architecture.
- Active components.
- New integrations.
- Automated operations.
- Improved data flows.

Use blue for active internal components.

Use violet for external integrations.

Use green for verified successful outcomes and improvements.

### Component Comparison

Where possible, preserve the identity and position of unchanged components between before and after diagrams.

This makes architectural changes easier to recognize.

Use status labels to identify NEW, MODIFIED, REMOVED, and UNCHANGED components.

Do not imply that a component was removed simply because it is absent from the new diagram. Only mark REMOVED when confirmed.

## 11. HTML / CSS / SVG Implementation

Prefer HTML + SVG for diagrams embedded in client-facing reports.

Responsibilities:

HTML:
- Page structure.
- Titles and descriptions.
- Diagram containers.
- Legends.
- Supporting explanations.

SVG:
- Shapes.
- Connectors.
- Arrowheads.
- Icons.
- Precise positioning.

CSS:
- Colors.
- Typography.
- Borders.
- Spacing.
- Responsive presentation.
- Print styles.

### SVG Requirements

- Use viewBox for scalable rendering.
- Use semantic SVG groups where practical.
- Use reusable arrowhead definitions.
- Keep text readable when scaled.
- Use explicit stroke and fill values.
- Avoid excessively complicated SVG paths.
- Ensure connectors remain behind nodes.
- Use accessible titles and descriptions when appropriate.

### CSS Design Tokens

Use these variables as the default design system:

```css
:root {
  /* Semantic colors */
  --flow-legacy: #64748B;
  --flow-primary: #2563EB;
  --flow-success: #16A34A;
  --flow-warning: #D97706;
  --flow-error: #DC2626;
  --flow-external: #7C3AED;

  /* Backgrounds */
  --flow-canvas: #FFFFFF;
  --flow-surface: #F8FAFC;

  --flow-legacy-bg: #F1F5F9;
  --flow-primary-bg: #EFF6FF;
  --flow-success-bg: #F0FDF4;
  --flow-warning-bg: #FFFBEB;
  --flow-error-bg: #FEF2F2;
  --flow-external-bg: #F5F3FF;

  /* Borders */
  --flow-border: #E2E8F0;
  --flow-border-strong: #CBD5E1;

  /* Typography */
  --flow-text: #0F172A;
  --flow-muted: #64748B;
  --flow-font: Inter, system-ui, sans-serif;

  /* Dimensions */
  --flow-node-radius: 10px;
  --flow-group-radius: 14px;
  --flow-node-border: 1.5px;
  --flow-connector-width: 2px;

  /* Spacing */
  --flow-node-gap: 24px;
  --flow-group-padding: 20px;
}
```

## 12. Accessibility and Export

Diagrams must remain understandable when exported or viewed in different environments.

Requirements:
- Maintain sufficient text contrast.
- Do not communicate status using color alone.
- Use explicit labels for conditional paths.
- Ensure font sizes remain readable.
- Avoid relying on hover interactions.
- Provide meaningful SVG titles and descriptions.
- Use a white background for print.
- Avoid clipping nodes or connectors.
- Preserve aspect ratios.
- Support high-resolution PDF rendering.

For PDF export:
- Prefer vector SVG.
- Avoid rasterizing diagrams unnecessarily.
- Use print-specific CSS.
- Prevent diagram elements from being split across pages.
- Use landscape layout for wide diagrams when appropriate.

## 13. Legend Standards

Include a legend whenever multiple semantic colors or connector types appear.

Example:

- Blue: Internal service.
- Slate: Legacy component.
- Green: Improvement / successful outcome.
- Amber: Manual operation / warning.
- Red: Error / failure.
- Violet: External integration.

Connector legend:
- Solid: Synchronous flow.
- Dashed: Asynchronous flow.
- Dotted: Optional dependency.

Keep the legend compact and position it below or beside the diagram.

## 14. AI Diagram Generation Workflow

When asked to generate a diagram:

1. Understand the system or process being described.
2. Identify all components, actors, operations, and dependencies.
3. Determine the diagram type: process flowchart, architecture diagram, sequence diagram, or data flow diagram.
4. Identify the correct standard shape for each component.
5. Assign semantic colors based on component roles.
6. Determine flow direction.
7. Arrange components into logical groups.
8. Create connectors and labels.
9. Check for overlapping nodes and crossing connectors.
10. Verify that the diagram accurately represents the supplied information.
11. Add a title, subtitle, and legend where appropriate.
12. Render and inspect the resulting HTML/SVG.

If information is missing:
- Do not invent details.
- Use neutral placeholders only when necessary.
- Clearly identify assumptions.
- Ask for clarification when missing information materially affects the diagram.

## 15. Final Quality Checklist

Before delivering a diagram, verify:

### Visual quality
- [ ] Clean, professional appearance.
- [ ] Consistent semantic colors.
- [ ] Consistent typography.
- [ ] Consistent component dimensions.
- [ ] Sufficient whitespace.
- [ ] No unnecessary decoration.

### Diagram semantics
- [ ] Correct shapes for each operation.
- [ ] Correct decision diamonds.
- [ ] Correct database representations.
- [ ] External systems clearly distinguished.
- [ ] Manual operations clearly identified.
- [ ] Every connector has a meaningful direction.
- [ ] Conditional branches are labeled.

### Layout
- [ ] Logical flow direction.
- [ ] No overlapping nodes.
- [ ] No unnecessary crossing connectors.
- [ ] No clipped content.
- [ ] Readable labels.
- [ ] Logical grouping.

### Accuracy
- [ ] No invented components.
- [ ] No invented integrations.
- [ ] No unsupported improvements.
- [ ] No misleading relationships.
- [ ] Before/after differences accurately represented.

### HTML output
- [ ] SVG scales correctly.
- [ ] HTML renders without layout issues.
- [ ] Print layout is supported.
- [ ] Diagram remains readable in PDF export.

## 16. Design Philosophy

The purpose of a flowchart is not to show how many technical components exist.

Its purpose is to help the reader understand how the system works.

Do a Less text and more visualisations.

A successful client-facing diagram should allow a non-technical stakeholder to understand:

1. Where information comes from.
2. What happens to that information.
3. Which systems participate.
4. Where decisions are made.
5. Where manual intervention is required.
6. What happens when something fails.
7. What the final result looks like.

Always optimize for comprehension, not technical density.
