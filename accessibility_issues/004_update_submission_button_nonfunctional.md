---
name: Accessibility Issue
about: Update submission button doesn't work for screen reader users
title: "[A11y] Update submission button non-functional for screen reader users"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,development,High Priority | Haute priorité'
assignees: ''

---

## 📇 User story
As a screen reader user, I want the update submission button to work when activated, so that I can perform required actions.

## ✅ Definition of Done / Outcomes
The update submission button functions correctly when activated by screen reader users.

## 📜 Acceptance criteria
- [ ] Update submission button works when activated
- [ ] Appropriate feedback is provided when button is activated
- [ ] Tested with VoiceOver on Safari and NVDA on Chrome

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-13
- Assistive technology: VoiceOver on Safari, NVDA on Chrome

### Issue description
When screen reader users select the "update submission" button, nothing happens. No error message, no modal, no visible feedback. The button appears to be non-functional. This prevents users from completing required actions.

### Priority
**High** - Issue is related to component and blocks task success. Users cannot complete required actions when the button doesn't work.

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not a known limitation of screen readers - it appears to be a functional bug with the button. The button should work when activated by any method.

**. 🚫 Out of scope**
Fixing screen reader behavior itself - this is about ensuring the button works correctly.
