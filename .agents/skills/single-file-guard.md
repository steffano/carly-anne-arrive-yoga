---
name: single-file-guard
description: Enforces single-file integrity and prevents agents from splitting index.html into external dependencies.
---

# Single-File Guardrail Skill

When instructed to modify or extend features:
1. NEVER suggest creating `styles.css`, `app.js`, `script.js`, or external modular components.
2. Custom CSS animations and rules must be placed inside the existing `<style>` block inside `<head>`.
3. Tailwind theme modifications MUST be placed inside the inline script `tailwind.config = { ... }`.
4. Client-side JS logic, data structures, modal handlers, and event listeners MUST be placed inside the `<script>` tag at the bottom of `<body>`.
