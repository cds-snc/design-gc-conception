---
name: Accessibility Issue
about: Dragon NaturallySpeaking cannot select filter button by name
title: "[A11y] Dragon NaturallySpeaking - Cannot select filter button by name"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,development,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a Dragon NaturallySpeaking user, I want to select buttons by their visible text/label, so that I can interact with controls efficiently.

## ✅ Definition of Done / Outcomes
Dragon NaturallySpeaking users can select the filter button using commands like "click filter and sort".

## 📜 Acceptance criteria
- [ ] Filter button can be selected by name using Dragon NaturallySpeaking
- [ ] Radio buttons in filter menu can be selected by voice commands
- [ ] Users don't need to use mouse grid command
- [ ] Tested with Dragon NaturallySpeaking on Chrome

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-11
- Assistive technology: Dragon NaturallySpeaking on Chrome
- WCAG criteria: 2.1.1 Keyboard

### Issue description
Dragon NaturallySpeaking users cannot select the "filter and sort" menu button using the command "click filter and sort". They had to use the command "click button" to select it. Additionally, they cannot interact with any of the radio buttons inside the pop-up menu and had to manually select them using the mouse grid command. This makes the component very difficult to use with Dragon NaturallySpeaking.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still complete tasks using mouse grid, though inefficiently).

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not a known limitation of Dragon NaturallySpeaking - it appears to be an issue with how the component is labeled or implemented. Dragon NaturallySpeaking should be able to select buttons by their visible text/label.

**. 🚫 Out of scope**
Fixing Dragon NaturallySpeaking behavior itself - this is about ensuring the component works properly with Dragon NaturallySpeaking.
