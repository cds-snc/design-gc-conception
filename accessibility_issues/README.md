# Accessibility Issues Summary

This directory contains accessibility issues identified from Fable testing results for GCDS components. Each review session is documented below with its date, test reports, and findings.

---

## June 23, 2026

These are the test tasks: Table component accessibility testing with various assistive technologies

The test reports reviewed:
- https://app.makeitfable.com/requests/CDS-GT_1-14 (Screen Reader & Alt Nav)
- https://app.makeitfable.com/requests/CDS-GT_1-13 (Screen Reader 1)
- https://app.makeitfable.com/requests/CDS-GT_1-11 (Alt Nav)
- https://app.makeitfable.com/requests/CDS-GT_1-12 (Screen Magnification)

Total unique issues after deduplication: 15

### Priority Breakdown

**High (2 issues)**: Issues that completely block task completion
- 002_voice_control_filter_menu_scrolling.md - Voice Control cannot scroll within filter menu
- 004_update_submission_button_nonfunctional.md - Update submission button doesn't work for screen reader users

**Medium (10 issues)**: Issues that impact usability but don't block task success
- 001_voice_control_radio_button_numbers.md - Voice Control assigns multiple number sets to radio buttons
- 003_voiceover_table_navigation.md - VoiceOver table navigation issues
- 005_filter_field_unclear_label.md - Filter field lacks clear labeling
- 006_focus_visibility_table_cells.md - Focus not visible on all table cells
- 007_sorting_controls_not_visible.md - Sorting controls only appear on hover
- 008_color_contrast_issues.md - Poor color contrast for text and status indicators
- 010_voice_control_filter_button_commands.md - Dragon NaturallySpeaking cannot select filter button by name
- 011_excessive_scrolling_voice_control.md - Excessive scrolling required with Voice Control
- 014_voice_control_numbers_not_reassigned.md - Voice Control numbers not reassigned after scrolling
- 015_status_count_indicator.md - No numerical indicator to count filtered results

**Low (3 issues)**: Issues specific to application of component rather than component itself
- 009_link_underline_spacing.md - Link underline too close to text at high magnification
- 012_keyboard_filter_button_inconsistent.md - Filter button reacts differently to Enter vs Space
- 013_voiceover_date_read_twice.md - VoiceOver reads date twice in table

### Adaptive Technology Limitations

The following issues are confirmed adaptive technology limitations that cannot be fixed through component design changes:
- 013_voiceover_date_read_twice.md - VoiceOver behavior related to date formatting in tables
- 014_voice_control_numbers_not_reassigned.md - Voice Control behavior where numbers are not automatically reassigned to newly visible elements after scrolling

---

## [Date]

These are the test tasks: [Description of test tasks]

The test reports reviewed:
- [Test request URL] ([Brief description])
- [Test request URL] ([Brief description])

Total unique issues after deduplication: [Number]

### Priority Breakdown

**High ([X] issues)**: [Description]
- [Filename] - [Brief description]
- [Filename] - [Brief description]

**Medium ([X] issues)**: [Description]
- [Filename] - [Brief description]
- [Filename] - [Brief description]

**Low ([X] issues)**: [Description]
- [Filename] - [Brief description]
- [Filename] - [Brief description]

### Adaptive Technology Limitations

The following issues are confirmed adaptive technology limitations that cannot be fixed through component design changes:
- [Filename] - [Description]
- [Filename] - [Description]

---

## Next Steps

1. Review each issue file to confirm accuracy
2. Create GitHub issues using the content from these files
3. Assign appropriate team members
4. Prioritize based on impact and severity
5. Track resolution and retest with affected assistive technologies
