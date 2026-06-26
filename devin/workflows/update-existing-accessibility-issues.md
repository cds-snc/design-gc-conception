---
description: Update existing GitHub accessibility issues with new test results
---

# Workflow: Update Existing Accessibility Issues

This workflow reviews existing GitHub accessibility issues and proposes updates based on new Fable test results.

## Prerequisites
- New Fable test result documents (.docx files) in Downloads folder
- Test request URLs (e.g., https://app.makeitfable.com/requests/CDS-GT_1-12)

## Steps

### 1. Fetch Existing Accessibility Issues
Fetch all existing accessibility-labeled issues from GitHub:
```bash
read_url_content https://github.com/cds-snc/design-gc-conception/issues?q=is%3Aissue%20label%3A%22Accessiblity%20%7C%20Accessibilit%C3%A9%22
```

### 2. Read New Test Results
Convert and read new Fable test documents:
```bash
textutil -convert txt -stdout "/path/to/test-result.docx"
```

### 3. Extract New Issues
Extract issues from new test results:
- Issue type and category
- Assistive technology used
- Issue description
- Component affected
- WCAG criteria (if provided)

### 4. Compare and Identify Updates
Compare new issues with existing GitHub issues to identify which should be updated. This requires careful analysis:

**Step 4a: Read existing GitHub issue content**
For each existing GitHub issue, read the full description to understand:
- The specific component affected
- The exact issue description
- The assistive technologies mentioned
- Any test request URLs or references

**Step 4b: Compare against new issues**
For each new issue, check for:
- **Exact duplicate**: Same component, same issue, same assistive technology
  - Action: Skip creating new issue, add comment to existing issue with new test request URL
- **Partial duplicate**: Same component, same issue, but existing issue is broader
  - Action: Skip creating new issue, add comment to existing issue with new test request URL
  - Example: Existing issue covers general interactive labeling, new issue is specific to radio button numbers
- **Same component, same issue, new information**: Add new test results as comments
- **Same component, same issue, additional assistive technologies**: Note additional AT affected
- **Same component, related issue**: Note relationship if relevant
- **Different component**: Do NOT update (component-specific issues are separate)

**Step 4c: Document comparison results**
For each potential duplicate, document:
- Existing issue number and title
- New issue file name
- Why they are similar or different
- Recommendation (skip, update, or create new)

**Important**: Be conservative. When in doubt, create a new issue rather than updating an existing one. Only mark as duplicate when the issues are clearly the same problem.

### 5. Generate Proposal Document
Create a proposal document at `accessibility_issues/update-proposal-[YYYY-MM-DD].md` (with the current date) with the following structure:

```markdown
# Accessibility Issues Update Proposal

Generated on: [Date]
Based on test requests: [List of test request URLs]

## Summary
- Total existing issues reviewed: [number]
- Issues proposed for update: [number]
- New issues to create: [number]

## Proposed Updates

### Issue #[number]: [Issue Title]
**Current status**: [Open/Closed/etc.]
**Component**: [Component name]
**Proposed update**: [Description of what to add/change]

**Rationale**: [Why this update is needed based on new test results]

**Proposed action**:
- [ ] Add comment with new test results
- [ ] Other: [specify]

**IMPORTANT**: Do not edit existing issue descriptions or labels. Only add comments to provide additional information.

**Draft comment for verification**:
```
This issue was also observed in test request: [Test request URL]

**Additional test results:**
- [Key observation 1]
- [Key observation 2]
- Test configuration: [Assistive technology on browser]

---
*This comment was generated based on accessibility test results from Fable testing.*
```

**New information to add**:
[Extract relevant information from test results]

---

### Issue #[number]: [Issue Title]
[Repeat for each issue to update]

## New Issues to Create
[List any new issues that don't match existing ones]

**Important**: When creating new issues, add the following note at the end of the issue description:
```
---
*This issue was generated based on accessibility test results from Fable testing.*
```

### 6. Present Proposal for Review
Show the proposal document to the user and ask for:
- Accept all updates
- Reject specific updates
- Modify specific updates
- Skip

### 7. Apply Approved Updates
If user approves, apply updates using GitHub CLI or API:

**IMPORTANT RESTRICTION**: Do not edit existing issue descriptions or labels. Only add comments to provide additional information.

**Option A: Using GitHub CLI (if available)**
```bash
# Check if gh CLI is installed
gh --version

# For each approved update (only add comments):
gh issue comment [issue-number] --body "[comment text]"
```

**Option B: Using GitHub API (if gh CLI not available)**
```bash
# Requires GitHub personal access token with repo scope
curl -X POST \
  -H "Authorization: token [GITHUB_TOKEN]" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/cds-snc/design-gc-conception/issues/[issue-number]/comments \
  -d '{"body": "[comment text]"}'
```

### 8. Create New Issues
For each new issue to create, use GitHub CLI:
```bash
gh issue create --title "[title]" --body-file [issue-file] -l [label1] -l [label2] ...
```

Record the GitHub issue number assigned to each created issue.

### 9. Update Cross-References
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

### 10. Document Applied Updates
After applying updates, create a summary document at `accessibility_issues/applied-updates-[YYYY-MM-DD].md` (with the current date):
```markdown
# Applied Updates Summary

Date: [Date]
Proposal: [Link to proposal document]

## Updates Applied
- Issue #[number]: [Summary of update]
- Issue #[number]: [Summary of update]

## Updates Skipped
- Issue #[number]: [Reason]
```

## Important Notes
- **Component-specific**: Only update issues for the SAME component with the SAME or VERY SIMILAR issue
- **Conservative approach**: When in doubt, create a new issue rather than updating an existing one
- **Preserve history**: Add new information as comments rather than replacing existing content
- **User approval required**: Never apply updates without explicit user approval

## Example Usage
Ask: "Update existing accessibility issues based on these test results: [list of document paths]"
