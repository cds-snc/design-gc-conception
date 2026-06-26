---
description: Create accessibility issues from Fable test results
---

# Workflow: Create Accessibility Issues from Fable Test Results

This workflow creates accessibility issues from Fable testing reports, following the established process for GCDS accessibility issue tracking.

## Prerequisites
- Fable test result documents (.docx files) in Downloads folder, with names and other PII removed (Download files and remove PII on secure device first)
- Test request URLs (e.g., https://app.makeitfable.com/requests/CDS-GT_1-12)

## Steps

### 1. Read and Convert Test Documents
Convert .docx files to text format for analysis:
```bash
textutil -convert txt -stdout "/path/to/test-result.docx"
```

### 2. Extract and Categorize Issues
Review each test document and extract:
- Issue type and category
- Assistive technology used
- Issue description
- WCAG criteria (if provided)
- Whether it blocks task completion

### 3. Check for Existing Issues
Fetch existing accessibility issues from GitHub to avoid duplicates:
```bash
# Fetch accessibility-labeled issues from GitHub
read_url_content https://github.com/cds-snc/design-gc-conception/issues?q=is%3Aissue%20label%3A%22Accessiblity%20%7C%20Accessibilit%C3%A9%22
```

Review the fetched issues and compare against new findings to identify potential duplicates. Look for:
- Same component (e.g., table, filter, button)
- Similar assistive technology (e.g., VoiceOver, NVDA, Voice Control)
- Similar issue description (e.g., focus visibility, keyboard navigation, screen reader announcements)

**Important**: Since the team works with components individually and each component has different use cases and specific needs, do NOT mark issues as related just because they deal with the same general accessibility concern (e.g., color contrast) if they are for different components. Component-specific issues should be treated as separate.

If a duplicate is found (same component and same issue), either:
- Note the existing issue number in the new issue file for reference
- Skip creating a new issue if it's completely redundant

### 4. Create Issue Files
For each unique issue, create a markdown file in `accessibility_issues/` directory with the following structure:

```markdown
---
name: Accessibility Issue
about: [Brief description]
title: "[A11y] [Descriptive title]"
labels: 'Accessiblity | Accessibilité,Bug | Bogue,New | Nouveau,[type-labels],[priority-label]'
assignees: ''
```

**Label mapping based on type of change required**:
- Design change only → `design`
- Code change only → `development`
- Content design change only → `content`
- Both design and code → `design,development`
- Both design and content design → `design,content`
- Both code and content design → `development,content`
- All three → `design,development,content`
- Adaptive technology limitation → no additional type labels

**Label mapping based on priority**:
- High → `High Priority | Haute priorité`
- Medium → `Medium Priority | Priorité moyenne`
- Low → `Low Priority | Faible priorité`
---

## 📇 User story
As a [user type], I want to [goal], so that [benefit].

## ✅ Definition of Done / Outcomes
[Expected outcome]

## 📜 Acceptance criteria
- [ ] [Criterion 1]
- [ ] [Criterion 2]

## 📝 More info

### Source
- Test request: [URL from app.makeitfable.com]
- Assistive technology: [Technology used, e.g., Voice Control on Chrome]
- WCAG criteria: [If provided]

### Related Issues
[Only include if there is an existing issue for the SAME component with the SAME or VERY SIMILAR issue]
- [URL to related GitHub issue] - [Brief note on how it's related]

### Issue description
[Detailed description from test report]

### Priority
**[High/Medium/Low]** - [Justification based on task completion impact]

### Type of change required
- [ ] Design change only
- [ ] Code change only
- [ ] Content design change only
- [ ] Both design and code changes
- [ ] Both design and content design changes
- [ ] Both code and content design changes
- [ ] All three: design, code, and content design changes
- [ ] Adaptive technology limitation (no fix possible)

### Adaptive technology limitation
[Note if this is a confirmed adaptive technology limitation that cannot be fixed through component design]

**. 🚫 Out of scope**
[What is not included in this fix]

---
*This issue was generated based on accessibility test results from Fable testing.*
```

### 5. Assign Priorities
- **High**: Only for issues that completely block task completion (user cannot use the component as intended)
- **Medium**: Issues that impact usability but don't block task success
- **Low**: Issues specific to application of component rather than component itself (e.g. implementation of Table component on test site vs. Table component API)

### 6. Validate Adaptive Technology Limitations
Mark issues as adaptive technology limitations only when:
- The issue is a known behavior of the assistive technology
- It cannot be fixed through component design changes
- Examples: Voice Control accessibility overlay labels not changing or lagging after scrolling

### 7. Create GitHub Issues
For each unique issue file, create a GitHub issue using GitHub CLI:
```bash
gh issue create --title "[title]" --body-file [issue-file] -l [label1] -l [label2] ...
```

Record the GitHub issue number assigned to each created issue.

### 8. Update Cross-References
After creating all issues, check for cross-references within the issue descriptions:
- Search for references like "see issue #005" or "issue #XXX" where XXX is the local file number
- Replace these with the actual GitHub issue numbers
- Update the GitHub issues using `gh issue edit` with the corrected body

Example:
```bash
# If issue 011 references issue 005, and 005 became #2541
# Update the reference in the markdown file
gh issue edit [new-issue-number] --body-file [updated-issue-file]
```

### 9. Create review summary
Create a summary in `accessibility_issues/README.md` with:
  - Date of review
  - Test tasks (found in the reports)
  - Test request URLs reviewed
  - Total unique issues count
  - Priority breakdown
  - Confirmed adaptive technology limitations

## Important Notes
- **Always include test request links** in format: https://app.makeitfable.com/requests/CDS-GT-XX
- **Be conservative with High priority** - only for true blockers
- **Validate adaptive technology claims** - don't assume limitations without confirmation

## Example Usage
Ask: "Create accessibility issues from these Fable test results: [list of document paths]"
