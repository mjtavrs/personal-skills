---
name: component-split-enforcer
description: Use this skill when building or refactoring UI components, pages, layouts, or feature modules to prevent monster files and enforce smaller, reusable pieces.
---

# Component Split Enforcer

## Goal
Prevent oversized components and encourage small, focused, maintainable UI building blocks.

## When to use
Use this skill for:
- new pages
- new components
- refactoring large components
- feature modules with growing UI complexity
- files with mixed rendering, state, side effects, and business logic

## Hard rules
- avoid components growing beyond 500–600 lines
- split responsibilities early
- extract reusable pieces even if reuse is only likely in the future
- keep naming in English
- avoid mixing too many concerns in one file

## Always verify
- rendering logic is not overloaded
- business logic is not buried inside large UI files
- repeated UI blocks are extracted
- repeated behavior is moved to hooks, composables, or helpers when appropriate
- props and responsibilities are clear
- state ownership is deliberate
- files remain readable from top to bottom

## Good split candidates
- form sections
- table toolbars
- filters
- modals
- cards
- empty states
- loading states
- repeated button groups
- status badges
- data transformation helpers
- hooks/composables for stateful behavior

## Anti-patterns to avoid
- page files doing everything
- components with many unrelated local states
- giant templates or JSX blocks
- deeply nested conditionals in the render layer
- extracting too late, after the file is already hard to reason about

## Output format
Always provide:
1. Why the current structure is too large or risky
2. Suggested split boundaries
3. Proposed smaller components/helpers
4. Why the new structure is easier to maintain
5. Plain-language summary for non-technical readers