# Style Guide: Personal Boundary Repository (PBR)

## 1. Goal & Philosophy

The goal of this repository is to provide a **single source of truth** for personal conduct, interpersonal expectations, and self-preservation.

- **Precision over Politeness:** Use clear, declarative language.
- **Version Control:** All changes to boundaries must be tracked via commit history to understand personal growth.
- **Separation of Concerns:** Keep core values separate from situational implementation.

## 2. File Naming & Structure

- **Format:** All files must be `.md` (Markdown).
- **Naming Convention:** Use kebab-case.
  - *Correct:* `social-media-consumption.md`
  - *Incorrect:* `Social Media Consumption.md`
- **Directory Mapping:**
  - `/core`: Fundamental rights and non-negotiables.
  - `/professional`: Workplace and career boundaries.
  - `/relational`: Friends, family, and partner-specific logic.
  - `/templates`: Blank specs for new boundary creation.

## 3. The Boundary Specification Template

Every boundary document must follow this standardized section hierarchy:

### 3.1 Required Sections

1. `# Boundary Title` — A high-level name for the boundary.
2. `## 1. The Line` — A single-sentence bold statement of the rule.
3. `## 2. Rationale` — The "Why." Link to core values or past incidents that necessitated this rule.
4. `## 3. Implementation` — A bulleted list of technical or physical steps taken to enforce the boundary.
5. `## 4. Communication (Signals)` — Standardized phrases to use when the boundary is tested.
6. `## Metadata` — YAML block at the end of the file tracking status and scope.

### 3.2 Metadata Block (End of File)

Place a fenced YAML code block at the end of each document under a `## Metadata` heading:

````markdown
## Metadata

```yaml
id: BND-001
status: Draft | Active | Deprecated
severity: Low | Medium | High | Critical
review_frequency: Quarterly | Annual | Event-Driven
scope: Relational | Internal | Operational
```
````

## 4. Formatting Components

### The "[SIGNAL]" Callout

Use `**[SIGNAL - Name]:**` inline in bullet lists for pre-scripted responses. This reduces the cognitive load of finding the right words in the moment.

**[SIGNAL]:** "I appreciate the invite, but I don't do social events on weeknights to ensure I get enough sleep."

### The "[!WARNING]" Enforcement Block

For high-severity boundaries, use a MkDocs admonition block to define what happens if the line is crossed:

```markdown
!!! warning "Enforcement Step"
    If [Person] continues to [Action] after the Signal is given, I will remove myself from the environment immediately.
```

### Typography Rules

- **Keywords:** Use **bold** for absolute negatives (e.g., **No**, **Never**, **Will not**).
- **Internal Notes:** Use *italics* for personal reflections or notes to self regarding the difficulty of the boundary.

## 5. Vocabulary Standards

To maintain the "Code Project" feel, avoid vague or deferential language:

| Avoid | Use Instead |
| :---- | :---- |
| I try not to... | I do not... |
| I would prefer if... | I require... |
| Maybe we can... | The policy is... |
| I feel like... | The boundary is... |
