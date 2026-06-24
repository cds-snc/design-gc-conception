---
name: Accessibility Issue
about: Excessive scrolling required with Voice Control
title: "[A11y] Voice Control - Excessive scrolling makes finding records tedious"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,design,development,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a Voice Control user, I want to find records without excessive scrolling, so that I can complete tasks efficiently without fatigue.

## ✅ Definition of Done / Outcomes
Users can find specific records without excessive scrolling through improved search/filter functionality.

### Note
This may be addressed by improving the filter field labeling (see issue #005) and ensuring users understand they can search by ID.

## 📜 Acceptance criteria
- [ ] Users can search for specific records by ID or name
- [ ] Filter field is clearly labeled as a search field
- [ ] Users don't need to scroll through multiple pages to find specific records
- [ ] Tested with Voice Control

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-11
- Assistive technology: Voice Control on Chrome

### Issue description
There is a lot of scrolling and page flipping which makes it tiring and tedious to find a specific name. When using Voice Control, users must verbally give commands to scroll repetitively, which gets tiring. If the record is at the bottom, users must use voice commands for pagination and continue scrolling. While sorting filters exist, a search field should be included to enter specific text and display only those results.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still complete tasks, though with difficulty). This may be partially addressed by improving filter field labeling.

### Type of change required
- [x] Both design and code changes
- [ ] Code change only
- [ ] Design change only
- [ ] Content design change only
- [ ] Both design and content design changes
- [ ] Both code and content design changes
- [ ] All three: design, code, and content design changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is partially a limitation of Voice Control (requiring verbal scroll commands), but can be mitigated by better search/filter functionality. The component should provide efficient search/filter options to reduce the need for scrolling.

**. 🚫 Out of scope**
Fixing Voice Control scrolling behavior itself - this is about reducing the need for scrolling through better search functionality.
