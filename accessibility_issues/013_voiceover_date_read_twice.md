---
name: Accessibility Issue
about: VoiceOver reads date twice in table
title: "[A11y] VoiceOver - Date read twice in table cells"
labels: 'accessibility,low-priority'
assignees: ''

---

## 📇 User story
As a VoiceOver user, I want dates to be read once, so that I can efficiently understand table content.

## ✅ Definition of Done / Outcomes
Dates in table cells are read once by VoiceOver.

## 📜 Acceptance criteria
- [ ] Date is read once by VoiceOver
- [ ] No redundant "invalid date" or "end of" announcements
- [ ] Tested with VoiceOver on Safari

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-14
- Assistive technology: VoiceOver on Safari

### Issue description
When reviewing the table, the date gets read twice by VoiceOver. For example, it says the date and possibly the time it was submitted. If scrolling with Control+Option+rightarrow keys, VoiceOver says "invalid date," then says "end of," date. It's unclear whether this redundant reading is necessary.

### Priority
**Low** - Issue could be specific to the application of the design system component (how dates are formatted in this specific table) rather than the component itself.

### Type of change required
- [ ] Code change only
- [ ] Design change only
- [ ] Content design change only
- [ ] Both design and code changes
- [ ] Both design and content design changes
- [ ] Both code and content design changes
- [ ] All three: design, code, and content design changes
- [x] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This appears to be a VoiceOver behavior related to how dates are formatted in the table. This may be a limitation of VoiceControl's date handling that cannot be fixed through component design changes.

**. 🚫 Out of scope**
N/A
