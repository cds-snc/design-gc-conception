---
name: Accessibility Issue
about: Poor color contrast for text and status indicators
title: "[A11y] Poor color contrast for text and status indicators"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,design,Medium Priority  | Priorité moyenne'
assignees: ''

---

## 📇 User story
As a user with screen magnification and color inversion, I want sufficient color contrast, so that I can read and understand all content.

## ✅ Definition of Done / Outcomes
All text and status indicators have sufficient color contrast, including when using color inversion settings.

## 📜 Acceptance criteria
- [ ] Grey text has sufficient contrast against background
- [ ] Status indicators (green, red, blue) have sufficient contrast against black background
- [ ] All important information is visible at high magnification
- [ ] Tested with color inversion and high magnification

## 📝 More info

### Source
- Test request: https://app.makeitfable.com/requests/CDS-GT_1-12
- Assistive technology: OS Magnification on Safari
- WCAG criteria: 1.4.3 Contrast (Minimum)

### Issue description
The bright white background washes away content. When using Classic Invert (color inversion), there is grey text and very dark highlights (green on black, red on black, blue on black) that are challenging to see even at magnification over 400%. Important information like status and filters are difficult to see due to poor color contrast.

### Priority
**Medium** - Issue is related to component and impacts readability but doesn't block task success (users can still access information with difficulty).

### Type of change required
- [ ] Code change only
- [x] Design change only
- [ ] Both design and code changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
This is not an adaptive technology limitation - it's a color contrast issue with the component design.

**. 🚫 Out of scope**
N/A
