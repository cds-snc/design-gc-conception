---
name: Accessibility Issue
about: Voice Control cannot scroll within filter menu
title: "[A11y] Voice Control - Scrolling not working in filter menu"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,development,High Priority | Haute priorité'
assignees: ''

---

## 📇 User story
As a user using Voice Control, I want to be able to scroll within filter menus, so that I can access all filter options.

## ✅ Definition of Done / Outcomes
Filter menus can be scrolled using Voice Control commands, allowing users to access all options.

## 📜 Acceptance criteria
- [ ] Voice Control scrolling commands work within filter menus
- [ ] Users can reach all filter options using Voice Control
- [ ] Tested with Voice Control on Chrome

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-14
- Assistive technology: Voice Control on Chrome

### Issue description
The scrolling up and down within the filter menu section is not working with Voice Control. Because the user cannot scroll to the bottom, they cannot complete tasks that require accessing options at the bottom of the filter menu. The user was unable to get past this step, marking it as a blocker.

### Priority
**High** - Issue is related to component and blocks task success. Users cannot complete tasks when they cannot access all filter options.

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not a known limitation of Voice Control - it appears to be an issue with how the component is implemented. Voice Control should be able to scroll within scrollable containers.

**. 🚫 Out of scope**
Fixing Voice Control behavior itself - this is about ensuring the component works properly with Voice Control.
