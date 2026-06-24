---
name: Accessibility Issue
about: Focus not visible on all table cells when using keyboard navigation
title: "[A11y] Focus not visible on all table cells (Reviewer, Status columns)"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,development,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a keyboard user with screen magnification, I want to see focus indicators on all interactive table cells, so that I can navigate efficiently.

## ✅ Definition of Done / Outcomes
All table cells that contain interactive content have visible focus indicators when navigating with keyboard.

## 📜 Acceptance criteria
- [ ] Focus outline is visible on Reviewer column cells
- [ ] Focus outline is visible on Status column cells
- [ ] Focus outline is visible on all interactive table cells
- [ ] Tested with keyboard navigation and screen magnification

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-12
- Assistive technology: OS Magnification on Safari
- WCAG criteria: 2.4.7 Focus Visible

### Issue description
When using the Tab key to navigate through the table, only the ID and Action details receive focus outlines. The Reviewer details and Status columns were not visible with a focus outline. This made it difficult for keyboard users to know where focus was and which elements were interactive. Users had to use hover text at high magnification to figure out the details, which was much harder than expected.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still navigate, though with difficulty).

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not an adaptive technology limitation - it's a focus visibility issue with the component.

**. 🚫 Out of scope**
N/A
