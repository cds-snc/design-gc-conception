---
name: Dev Card template
about: Template to use when creating development tasks
title: ''
labels: ''
assignees: ''

---
**Summary:** Development of the XXXXX component.
Develop on component branch, push to staging and flag ready to merge when reviwed.

Owner : dev assigned on the card 

**Definition of done:**  
- [ ] Prior to doing work, clarify scope of ticket with the designers (dev design sync or slack) and adjust if necessary
- [ ] Check with DTO if there are upcoming changes to this component or potential impact if we were to update the component
- [ ] Consider edge cases
- [ ] Describe component properties
- [ ] Update Requirements doc with agreed specifications
- [ ] Develop the component according to the requirements doc and design specs
- [ ] Add component to storybook
- [ ] Write draft of dev guidance
- [ ] Handoff from draft dev guidance to documentation lead and tag the content owner 
- [ ] Code review
- [ ] After PR approval, merge component to staging

**Acceptance criteria:** 
- [ ] Sync dev properties with Figma properties (design + dev)
- [ ] Passes storybook a11y test without any violation
- [ ] WCAG Goal can be completed using a screen reader.
- [ ] WCAG Visual elements observe color contrast requirements.
- [ ] WCAG Manual accessibility testing meets WCAG 2.1 AA requirements.
- [ ] Provides equal service in French and English.
- [ ] Dev peer reviews 

**Deliverables:** 
- [ ]Proposal guidance handed off to content
- [ ]Requirement doc updated 
- [ ]Pull request, with approvals. Do not merge. 
