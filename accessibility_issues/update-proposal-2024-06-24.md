# Accessibility Issues Update Proposal

Generated on: June 24, 2026
Based on test requests: https://app.makeitfable.com/requests/CDS-GT_1-14, https://app.makeitfable.com/requests/CDS-GT_1-13, https://app.makeitfable.com/requests/CDS-GT_1-11, https://app.makeitfable.com/requests/CDS-GT_1-12

## Summary
- Total existing issues reviewed: 10
- Issues proposed for update: 1 (add comment to #2092)
- New issues to create: 14

## Analysis

After comparing the 15 drafted accessibility issues in `accessibility_issues/` with the existing GitHub accessibility issues, **1 duplicate was found**. 14 drafted issues are new and should be created as separate GitHub issues.

### Comparison Results

**Similar but distinct issues (not duplicates):**

1. **006_focus_visibility_table_cells.md** vs **#2119 (Styling element outlines and borders in a way that removes or renders non-visible the visual focus indicator)**
   - Different scope: #2119 is a general focus indicator issue across various components
   - Drafted issue is specific to table cells (Reviewer and Status columns)
   - **Recommendation**: Create as new issue

2. **010_voice_control_filter_button_commands.md** vs **#2122 (Dictation doesn't work on search component)**
   - Different issue: #2122 is about dictating search terms into input field
   - Drafted issue is about selecting buttons by name using voice commands
   - **Recommendation**: Create as new issue

3. **012_keyboard_filter_button_inconsistent.md** vs **#2498 (Table filter does not respond to Enter key; lacks affordance for applying filter)**
   - Different issue: #2498 is about Enter key in filter input field not applying filter
   - Drafted issue is about Enter vs Space key behavior on the filter button itself
   - **Recommendation**: Create as new issue

**Duplicate found:**

1. **001_voice_control_radio_button_numbers.md** vs **#2092 (Too many items have an interactive label on Holiday app and doc site)**
   - #2092 specifically mentions: "there were two numbers assigned by voice control for each option. One of them was close to the radio button and the other one was covering the text slightly."
   - This is the same issue as 001 (multiple numbers assigned to radio buttons, with one overlaying text)
   - #2092 is broader but already covers this specific issue
   - **Recommendation**: Skip creating issue 001, add comment to #2092 with test request URL

**No matches found for:**
- 002_voice_control_filter_menu_scrolling.md
- 003_voiceover_table_navigation.md
- 004_update_submission_button_nonfunctional.md
- 005_filter_field_unclear_label.md
- 006_focus_visibility_table_cells.md
- 007_sorting_controls_not_visible.md
- 008_color_contrast_issues.md
- 009_link_underline_spacing.md
- 010_voice_control_filter_button_commands.md
- 011_excessive_scrolling_voice_control.md
- 012_keyboard_filter_button_inconsistent.md
- 013_voiceover_date_read_twice.md
- 014_voice_control_numbers_not_reassigned.md
- 015_status_count_indicator.md

## Proposed Updates

### Issue #2092: Too many items have an interactive label on Holiday app and doc site
**Current status**: Open
**Component**: Multiple (Holiday app, doc site)
**Proposed update**: Add comment with additional test request URL

**Rationale**: Issue 001 (Voice Control assigns multiple number sets to radio buttons) is a duplicate of #2092. #2092 already covers this specific issue. Adding the new test request URL provides additional evidence.

**Proposed action**:
- [x] Add comment with new test results

**New information to add**:
This issue was also observed in test request: https://app.makeitfable.com/requests/CDS-GT_1-14
- Voice Control assigns multiple number sets to radio buttons that switch rapidly
- Numbers overlay the beginning of text, making it difficult to read
- This creates a visually busy interface and makes it extremely difficult to know which number to say

## New Issues to Create

14 drafted issues should be created as new GitHub issues:

1. 002_voice_control_filter_menu_scrolling.md - Voice Control cannot scroll within filter menu
2. 003_voiceover_table_navigation.md - VoiceOver table navigation issues
3. 004_update_submission_button_nonfunctional.md - Update submission button doesn't work for screen reader users
4. 005_filter_field_unclear_label.md - Filter field lacks clear labeling
5. 006_focus_visibility_table_cells.md - Focus not visible on all table cells
6. 007_sorting_controls_not_visible.md - Sorting controls only appear on hover
7. 008_color_contrast_issues.md - Poor color contrast for text and status indicators
8. 009_link_underline_spacing.md - Link underline spacing insufficient at high magnification
9. 010_voice_control_filter_button_commands.md - Dragon NaturallySpeaking cannot select filter button by name
10. 011_excessive_scrolling_voice_control.md - Excessive scrolling required with Voice Control
11. 012_keyboard_filter_button_inconsistent.md - Filter button reacts inconsistently to Enter vs Space key
12. 013_voiceover_date_read_twice.md - VoiceOver reads date twice in table
13. 014_voice_control_numbers_not_reassigned.md - Voice Control numbers not reassigned after scrolling
14. 015_status_count_indicator.md - No numerical indicator to count filtered results

## Recommendation

1. Add a comment to issue #2092 with the additional test request URL (https://app.makeitfable.com/requests/CDS-GT_1-14) and details about the radio button number issue
2. Create the remaining 14 drafted issues as new GitHub issues using the content from the markdown files in `accessibility_issues/`. Each issue already has:
   - Proper labels (Accessiblity | Accessibilité, Bug | Bogue, New | Nouveau, type labels, priority labels)
   - User stories and acceptance criteria
   - Test request URLs
   - Issue descriptions
   - Type of change required
   - Adaptive technology limitation notes
