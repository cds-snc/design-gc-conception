---
name: Accessibility Issue
about: VoiceOver table navigation issues
title: "[A11y] VoiceOver - Table navigation requires two moves per column, doesn't announce headers with content"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,development,user-feedback,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a VoiceOver user, I want to navigate tables efficiently with proper header announcements, so that I can understand table data relationships.

## ✅ Definition of Done / Outcomes
VoiceOver users can navigate tables with single moves per column and hear column headers announced with cell content.

## 📜 Acceptance criteria
- [ ] VoiceOver moves to next column with a single gesture
- [ ] VoiceOver announces column header and cell content together when navigating
- [ ] VoiceOver announces row content when moving by rows
- [ ] Tested with VoiceOver on Safari

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-13
- Assistive technology: VoiceOver on Safari
- WCAG criteria: 2.1.1 Keyboard

### Issue description
When using VoiceOver to navigate through table elements, the user must move two times to reach the next column. VoiceOver doesn't announce the column header and what is in the cell in the same block of text when exploring by flicking to the next element. When moving by rows, VoiceOver only announces the name of the header, not the content of the row. This makes it difficult to understand the relationship between headers and data.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still navigate tables, though inefficiently).

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not a known limitation of VoiceOver - it appears to be an issue with how the table component is implemented. Proper table markup should allow VoiceOver to navigate efficiently.

**. 🚫 Out of scope**
Fixing VoiceOver behavior itself - this is about ensuring the component works properly with VoiceOver.

---
*This issue was generated based on accessibility test results from Fable testing.*
