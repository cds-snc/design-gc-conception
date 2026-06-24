---
name: Accessibility Issue
about: Filter button reacts differently to Enter vs Space key
title: "[A11y] Filter button reacts inconsistently to Enter vs Space key"
labels: 'accessibility,low-priority'
assignees: ''

---

## 📇 User story
As an on-screen keyboard user, I want consistent behavior when activating buttons with different keys, so that I can predict the outcome.

## ✅ Definition of Done / Outcomes
The filter button behaves consistently when activated with Enter or Space key.

## 📜 Acceptance criteria
- [ ] Filter button behaves consistently with Enter key
- [ ] Filter button behaves consistently with Space key
- [ ] Both keys produce the same expected behavior
- [ ] Tested with on-screen keyboard

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-11
- Assistive technology: On-screen keyboard on Chrome

### Issue description
When navigating with the Tab key on an on-screen keyboard, activating the "Filter and Sort" button reacts differently based on keyboard input. When focus is on the button, pressing "Enter" makes the dialog box briefly appear then disappear a few moments later, with focus automatically shifting to the forms. However, pressing "Space Bar" makes the dialog box appear normally without disappearing. This inconsistent behavior is confusing.

### Priority
**Low** - Issue may be specific to the application of the design system component rather than the component itself, and doesn't block task success (users can still activate the button with Space).

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Content design change only
- [ ] Both design and code changes
- [ ] Both design and content design changes
- [ ] Both code and content design changes
- [ ] All three: design, code, and content design changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not an adaptive technology limitation - it's an inconsistent keyboard behavior issue.

**. 🚫 Out of scope**
N/A
