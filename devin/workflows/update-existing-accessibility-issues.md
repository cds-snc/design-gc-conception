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
Compare new issues with existing GitHub issues to identify which should be updated. Look for:
- **Same component, same issue, new information**: Add new test results as comments
- **Same component, same issue, additional assistive technologies**: Note additional AT affected
- **Same component, related issue**: Note relationship if relevant
- **Different component**: Do NOT update (component-specific issues are separate)

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
- [ ] Update description with new information
- [ ] Add label: [label]
- [ ] Other: [specify]

**New information to add**:
[Extract relevant information from test results]

---

### Issue #[number]: [Issue Title]
[Repeat for each issue to update]

## New Issues to Create
[List any new issues that don't match existing ones]
```

### 6. Present Proposal for Review
Show the proposal document to the user and ask for:
- Accept all updates
- Reject specific updates
- Modify specific updates
- Skip

### 7. Apply Approved Updates
If user approves, apply updates using GitHub CLI or API:

**Option A: Using GitHub CLI (if available)**
```bash
# Check if gh CLI is installed
gh --version

# For each approved update:
gh issue comment [issue-number] --body "[comment text]"
gh issue edit [issue-number] --body "[updated description]"
gh issue edit [issue-number] --add-label "[label]"
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

### 8. Document Applied Updates
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
