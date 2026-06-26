---
name: Accessibility Issue
about: Voice Control assigns multiple number sets to radio buttons that switch rapidly
title: "[A11y] Voice Control - Multiple number sets assigned to radio buttons with rapid switching"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,development,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a user using Voice Control, I want to be able to select radio buttons reliably without numbers switching rapidly, so that I can complete form interactions efficiently.

## ✅ Definition of Done / Outcomes
Radio buttons in filter menus work reliably with Voice Control, with stable number assignments that don't switch rapidly or overlay text.

## 📜 Acceptance criteria
- [ ] Voice Control assigns a single, stable number to each radio button
- [ ] Numbers do not switch between consecutive values rapidly
- [ ] Numbers do not overlay text content
- [ ] Tested with Voice Control on Chrome

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-14
- Assistive technology: Voice Control on Chrome
- WCAG criteria: 2.1.1 Keyboard

### Issue description
When using Voice Control with filter menus, multiple sets of numbers are assigned to each radio button option. The numbers by the radio buttons switch very quickly between two different sets of consecutive numbers (e.g., switching between 93 and 94). Additionally, a second set of numbers overlays the beginning of the text for each option, making it difficult to read. This creates a visually busy interface and makes it extremely difficult to know which number to say to Voice Control to select the desired option.

### Priority
**Medium** - Issue is related to component and impacts usability but doesn't block task success (users can still complete tasks, though with difficulty and frustration).

### Type of change required
- [x] Code change only
- [ ] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not a known limitation of Voice Control - it appears to be an issue with how the component is implemented. Voice Control should assign stable numbers to interactive elements.

**. 🚫 Out of scope**
Fixing Voice Control behavior itself - this is about ensuring the component works properly with Voice Control.
