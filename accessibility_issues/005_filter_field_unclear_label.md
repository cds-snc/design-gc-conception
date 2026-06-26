---
name: Accessibility Issue
about: Filter field lacks clear labeling and instructions
title: "[A11y] Filter field lacks clear labeling and placeholder text"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,design,user-feedback,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a user, I want clear labeling and instructions for the filter field, so that I understand how to use it effectively.

## ✅ Definition of Done / Outcomes
The filter field has clear labeling, placeholder text, and instructions that explain its search functionality.

## 📜 Acceptance criteria
- [ ] Filter field has clear label indicating it can be used for search
- [ ] Placeholder text explains what can be entered (e.g., "Search by ID, name, etc.")
- [ ] Suggestions appear when typing in the filter field
- [ ] Tested with screen readers

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-12
- Assistive technology: Multiple configurations
- WCAG criteria: 3.3.2 Labels or Instructions

### Issue description
The "Filter" field appeared to function as a search field, but this was not clear. It did not have any hint or placeholder text to clarify its search capability. Since it was labeled as a filter, users initially relied on sorting and manually reviewed multiple pages. No suggestions appeared when typing in the filter field, so users were unsure what to type. This created confusion about when to use sorting vs. filtering/searching.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still complete tasks through alternative methods).

### Type of change required
- [ ] Code change only
- [x] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not an adaptive technology limitation - it's a labeling and instruction issue.

**. 🚫 Out of scope**
N/A

---
*This issue was generated based on accessibility test results from Fable testing.*
