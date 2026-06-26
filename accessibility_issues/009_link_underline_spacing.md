---
name: Accessibility Issue
about: Link underline too close to text, cutting it off at high magnification
title: "[A11y] Link underline spacing insufficient at high magnification"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,design,user-feedback,Low Priority | Faible priorité'
assignees: ''

---

## 📇 User story
As a screen magnification user, I want sufficient spacing between link underlines and text, so that I can read link text clearly.

## ✅ Definition of Done / Outcomes
Link underlines have sufficient spacing from text to prevent interference at high magnification.

## 📜 Acceptance criteria
- [ ] Link underlines have adequate spacing from text
- [ ] Text is readable at magnifications over 400%
- [ ] Underline does not cut off text
- [ ] Tested with screen magnification

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-12
- Assistive technology: OS Magnification on Safari

### Issue description
The ID links have underlines beneath the text. The underline does not have enough space between it and the text, resulting in the underline "cutting off" the text of the actual ID number. This makes the text hard to read at all magnifications, especially over 400%. Adding more pixels between the underline and text would help ensure the link and text do not interfere with each other.

### Priority
**Low** - Issue may be specific to the application of the design system component rather than the component itself, and doesn't block task success.

### Type of change required
- [ ] Code change only
- [x] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not an adaptive technology limitation - it's a styling issue with the component.

**. 🚫 Out of scope**
N/A

---
*This issue was generated based on accessibility test results from Fable testing.*
