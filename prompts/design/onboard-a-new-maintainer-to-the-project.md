---
title: "Onboard a New Maintainer to the Project"
slug: onboard-a-new-maintainer-to-the-project
stage: Design
category: "Documentation"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/onboard-a-new-maintainer-to-the-project
---
# Onboard a New Maintainer to the Project

Draft a Markdown onboarding guide for a new open-source maintainer with a welcome message, access checklist, and review and triage responsibilities.

Variables: contributor_username, project_name, repo_url, mentor_username

## Prompt

A long-time, trusted contributor, `{{contributor_username}}`, has accepted our invitation to become a maintainer for our open-source project, `{{project_name}}`. I need to create a structured onboarding plan and a welcome package for them.

Generate a comprehensive onboarding guide for new maintainers in Markdown format. This document should be stored in the project's private maintainer repository or wiki.

The guide should include:

1.  **Welcome Message**: A personal message congratulating the new maintainer and expressing excitement about them joining the team.

2.  **Phase 1: Setting Up Permissions and Access**
    *   A checklist of access to be granted:
        *   [ ] Grant write access to the GitHub repository: `{{repo_url}}`.
        *   [ ] Add to the maintainers team in the GitHub organization.
        *   [ ] Invite to the private maintainer communication channel (e.g., Slack or Discord).
        *   [ ] Grant access to the project's cloud services or other infrastructure if applicable.

3.  **Phase 2: Understanding Maintainer Responsibilities**
    *   **Triage**: Explain the process for triaging new issues (labeling, prioritizing, asking for more information).
    *   **Pull Request Reviews**: Outline the project's standards for code reviews. What should they look for? (e.g., correctness, style, tests, documentation). When is it okay to approve a PR?
    *   **Merging**: Explain the policy for merging PRs. (e.g., "Requires at least one approval from another maintainer", "Ensure CI is green").
    *   **Release Process**: Briefly describe the release process and link to the detailed release checklist.

4.  **Phase 3: Your First Month as a Maintainer**
    *   **Week 1**: Suggest they focus on triaging new issues and performing secondary reviews on PRs already reviewed by another maintainer.
    *   **Weeks 2-3**: Encourage them to take the lead on reviewing a few non-trivial PRs.
    *   **Week 4**: Suggest they lead the triage for a week or help prepare a minor release.
    *   **Mentorship**: Assign an existing maintainer (`{{mentor_username}}`) as their dedicated mentor for the first month to answer questions.

5.  **Code of Conduct and Values**: Reiterate the importance of upholding the project's Code of Conduct in all interactions and acting as a role model for the community.

6.  **A Note on Burnout**: Include a brief, supportive section about the importance of setting boundaries, taking breaks, and avoiding burnout. Encourage them to communicate if they feel overwhelmed.

Constraint Checklist & Confidence Score:
1.  Is the onboarding plan structured and phased? Yes.
2.  Does it clearly outline the responsibilities of a maintainer? Yes.
3.  Does it provide a clear, gradual plan for the first month? Yes.
4.  Does it include important cultural aspects like the CoC and burnout? Yes.
5.  Is the tone welcoming and supportive? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the comprehensive onboarding guide for new maintainers.

## Tips

A structured onboarding process helps new maintainers become effective quickly and sets them up for long-term success, which is vital for the project's sustainability.
