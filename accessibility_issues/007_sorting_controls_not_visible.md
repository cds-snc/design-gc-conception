---
name: Accessibility Issue
about: Sorting controls in table headers only appear on hover
title: "[A11y] Sorting controls in table headers not visible by default"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,design,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a screen magnification user, I want sorting controls to be visible by default, so that I can sort columns without navigating to the Filter and Sort menu.

## ✅ Definition of Done / Outcomes
Sorting controls in table headers are visible by default, allowing users to sort columns directly.

## 📜 Acceptance criteria
- [ ] Sorting icons are visible in table headers by default
- [ ] Sorting functionality is discoverable without mouse hover
- [ ] Users can sort columns directly from headers
- [ ] Tested with screen magnification

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-12
- Assistive technology: OS Magnification on Chrome

### Issue description
The sorting controls in the table headers were not visible by default and only appeared when hovering with a mouse. As a result, users did not realize that sorting functionality was available directly within the column headers. Instead, each time they wanted to sort a column, they had to open the Filter and Sort menu, navigate through options, and select the desired sorting criteria. This was cumbersome and time-consuming, especially for screen magnification users who had to repeatedly move back and forth between the table and the Filter and Sort menu.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still sort through the Filter and Sort menu).

### Type of change required
- [ ] Code change only
- [x] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not an adaptive technology limitation - it's a discoverability issue with the component design.

**. 🚫 Out of scope**
N/A
