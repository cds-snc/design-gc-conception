---
name: Accessibility Issue
about: No numerical indicator to count filtered results
title: "[A11y] No numerical indicator to count filtered results by status"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,design,development,user-feedback,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a screen magnification user, I want a numerical indicator showing how many results match each status, so that I can quickly understand the count without manual counting.

## ✅ Definition of Done / Outcomes
A numerical indicator displays the count of results for each status when filtering.

## 📜 Acceptance criteria
- [ ] Numerical indicator shows count of results for each status
- [ ] Count is visible when applying status filters
- [ ] Count is accessible to screen readers
- [ ] Tested with screen magnification

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-12, https://app.makeitfable.com/requests/CDS-GT_1-13
- Assistive technology: OS Magnification on Safari, NVDA on Chrome

### Issue description
When applying status filters, there is no way to review how many applications have a specific status (e.g., Approved). Users must manually count the results, which is very difficult at high magnification (around 600%). If the cursor drifts while counting, users may get the wrong count. A numerical indicator that counts how many applications have each status would be helpful.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still complete tasks, though with difficulty).

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
This is not an adaptive technology limitation - it's a missing feature in the component design.

**. 🚫 Out of scope**
N/A

---
*This issue was generated based on accessibility test results from Fable testing.*
