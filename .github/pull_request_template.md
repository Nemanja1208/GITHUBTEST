<!--
  📍 Location: .github/pull_request_template.md
  Text inside <!-- --> is guidance only and won't show in the rendered PR. Leave it or delete it.

  PR TITLE FORMAT (Conventional Commits):
    feat: add filter by status to JobManager
    fix: prevent status change from Rejected to Offer
    refactor: move console input helpers to ConsoleUI
    docs: update user flow diagram
    test: add unit tests for GetStatistics
    chore: update CI workflow
-->

## 🔗 Linked Issue

Closes #<!-- issue number, e.g. Closes #12 -->

## 🏷️ Type of Change

- [ ] ✨ Feature (new functionality)
- [ ] 🐛 Fix (bug fix)
- [ ] ♻️ Refactor (no behavior change)
- [ ] ✅ Test (adding or updating tests)
- [ ] 📝 Docs (README, diagrams, comments)
- [ ] 🔧 Chore (CI, config, dependencies)

## 📝 Description

### What
<!-- What does this PR do? 1–3 sentences. -->

### Why
<!-- Why is this change needed? What problem does it solve? -->

### How
<!-- How did you solve it? Key decisions, trade-offs, and alternatives you considered. -->

## 📸 Screenshots / Demo

<!--
  REQUIRED for any change that affects what the user sees in the console.
  Show the menu, input, and output. For fixes, show Before and After.
  Tip: drag and drop images straight into this text box.
-->

| Before | After |
|--------|-------|
| <!-- screenshot --> | <!-- screenshot --> |

## 🧪 How to Test

<!-- Exact steps a reviewer can follow to verify this works. -->

1. `git checkout <branch-name>`
2. `dotnet run --project JobApplicationManager`
3. Choose menu option `...`
4. Expected result: `...`

**Edge cases tested:**
<!-- e.g. empty list, invalid input, non-existent application, invalid status transition -->
- [ ] ...

---

## ✅ Developer Checklist

> Every box must be checked before requesting review. If something doesn't apply, check it and write `N/A` next to it.

### 🌿 Branch Naming
- [ ] Branch follows `<type>/<issue-number>-<short-description>` in lowercase kebab-case
  <!-- Examples: feature/12-filter-by-status · fix/18-invalid-status-transition · refactor/21-console-ui-helpers · docs/9-user-flow-diagram -->
- [ ] Branch is up to date with `main` (rebased or merged, no conflicts)

### 🧹 Clean Code
- [ ] Names are clear and follow C# conventions: `PascalCase` for classes, methods, and properties, `camelCase` for locals and parameters, `_camelCase` for private fields
- [ ] Methods are small and do one thing
- [ ] No duplicated logic (DRY)
- [ ] No business logic in `ConsoleUI` and no `Console` calls in `JobManager` or `JobApplication`
- [ ] No dead code, commented-out code, unused `using` statements, or leftover debug output
- [ ] No magic numbers or strings. Use constants or enums.
- [ ] User input is validated, and errors are handled with clear messages (no crashes)

### 🎨 Formatting
- [ ] Ran `dotnet format` locally
- [ ] Project builds with no new warnings (`dotnet build`)
- [ ] CI **Build & Check** is green ✅

### 💬 Comments & Documentation
- [ ] Public classes and methods have XML doc comments (`/// <summary>`)
- [ ] Comments explain **why**, not what. The code itself should explain what.
- [ ] No outdated or misleading comments
- [ ] README, UML class diagram, or user flow updated if structure or behavior changed

### 🧪 Testing
- [ ] Tested manually by following the steps above
- [ ] Unit tests added or updated for new logic (if a test project exists)
- [ ] All existing tests pass

### 📦 PR Quality
- [ ] PR title follows Conventional Commits (`feat:`, `fix:`, `refactor:` …)
- [ ] PR is focused on **one** issue or feature. Unrelated changes go in a separate PR.
- [ ] Commits are meaningful (no `fix`, `asdf`, or `wip`). Squash if needed.
- [ ] Description explains What, Why, and How, with screenshots
- [ ] I self-reviewed my own diff before requesting review
- [ ] No secrets, personal data, or local config files committed

---

## 👀 Notes for Reviewer

<!-- Anything specific you want feedback on? Areas you're unsure about? Known limitations or follow-up issues? -->