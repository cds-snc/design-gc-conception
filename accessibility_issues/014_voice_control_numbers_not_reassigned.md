---
name: Accessibility Issue
about: Voice Control numbers not reassigned after scrolling
title: "[A11y] Voice Control - Numbers not reassigned after scrolling"
labels: 'accessibility,medium-priority'
assignees: ''

---

## 📇 User story
As a Voice Control user, I want numbers to be automatically reassigned to newly visible interactive elements after scrolling, so that I can continue navigating efficiently.

## ✅ Definition of Done / Outcomes
Voice Control automatically reassigns numbers to interactive elements when they become visible after scrolling.

## 📜 Acceptance criteria
- [ ] Voice Control reassigned numbers to newly visible buttons after scrolling
- [ ] Users don't need to manually request number reassignment
- [ ] Tested with Voice Control on Chrome

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-14
- Assistive technology: Voice Control on Chrome

### Issue description
After scrolling down, Voice Control did not easily reassign the numbers to the newly available interactive buttons on the page. Users needed to tell Voice Control to show the numbers again before it appropriately adjusted to the available buttons. This process made it take longer to go through the results.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still complete tasks by manually requesting number reassignment).

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
This appears to be a Voice Control behavior limitation where numbers are not automatically reassigned to newly visible elements after scrolling. This is a known limitation of Voice Control that cannot be fixed through component design changes.

**. 🚫 Out of scope**
Fixing Voice Control behavior itself - this is about ensuring the component doesn't interfere with Voice Control's automatic number reassignment.
