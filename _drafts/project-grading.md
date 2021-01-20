---
title: Project Functionality
navbar: Guides
layout: guides
key: 1.3

blurb: |
  <p>Each project grade is split into two components: functionality (passing tests) and design (passing code review). This guide details both the process for getting credit for project functionality.</p>
---

This guide assumes you have already [setup your project](project-setup.html) and [tested your project](project-testing.html). This includes making a release of your project that passes the verification process on Github.

## Eligibility
{: .page-header }

Before making a request, you should make sure you are eligible to have your functionality verified:

  - Do you have credit for the functionality of the previous project? You can check your grades on [Canvas]({{ site.data.info.links.canvas.link }}). If you are missing a grade you should already have, please reach out to us on [Piazza]({{ site.data.info.links.piazza.link }})

      *For example, if you are on project 3, you must already have a non-zero functionality grade for project 2. If you are on project 1, you can skip this check.*

  - Are you working only 1 project ahead?

      *For example, if you are on project 3, you must already have completed project 1 (both functionality and design) and have a non-zero functionality grade for project 2. If you are on project 1 or 2, you can skip this check.*

  - Do you have a release for this project that passed the verification action on Github? If not, see the [Creating Releases](project-testing.html#creating-releases) section of the testing guide.

If you answered yes to all of the above, you can request to have your functionality grade updated.

## Requesting Grade
{: .page-header }

To request an update to your functionality grade, you must create a **project verification issue** on Github.

  1. Click the "Issues" tab on Github and click the green "New issue" button.

  1. Click the "Get started" button for the "Project Verification Issue" template:

      ![Screenshot]({{ "/images/verification-issue.png" | relative_url }}){: style="width: 500px;"}

  1. Verify the issue is automatically assigned to `josecorella`. Jose is the teacher assistant that will process these issues.

  1. Verify the issue has the `verify` label automatically applied. We use this to tell the difference between (functionality) verification and code review requests.

  1. Add the project label, either `project1`, `project2`, `project3`, or `project4`, in all lowercase with no spaces. These labels should already exist. We use these labels to track how long it takes to progress on specific projects.

  1. Add the issue to a project [milestone](https://guides.github.com/features/issues/#filtering), either `Project 1`, `Project 2`, `Project 3`, or `Project 4`, with proper capitalization and spacing. You will likely have to create this milestone.

  1. Fill in the `[FIELD_NAME]` fields in the issue title and body. Replace the `[` and `]` square bracket symbols. For example, `[FULL_NAME]` might be replaced with `Sophie Engle` instead.

  1. Check the boxes for the checklist at the bottom of the issue.

Save and open the issue. For an example, see the [example issue](https://github.com/usf-cs212-fall2020/project-template/issues/1) in the `project-template` repository.

Within 10 minutes, the github-actions bot should add a comment to the issue. The bot will check for any issues with the issue title, assignees, labels, and milestone. If everything looks good, the bot will also attempt to verify whether the release passed the tests.

If there are any issues, the github-actions bot will close the issue.
If your issue gets closed by the bot, you must **make the required changes and re-open the issue ASAP** to continue. **You will not get credit for functionality until you do so.**

If there are no issues, the issue will remain open for the teacher assistant. The teacher assistant will respond once your grade is updated on Canvas. If you haven't received a response in 48 hours, please post on Piazza.

If you do not receive a comment from the bot within 10 minutes, try closing and re-opening the issue. If that still doesn't work, please reach out to us on Piazza with a link to your issue.

You only need to do this once per project.

### Functionality Grade

Your functionality grade will be based on the **date you created the issue** that passed verification. If the issue date is before the checkpoint deadline, you will earn 100% on the project functionality. If the issue date is after the checkpoint deadline, your grade will be deducted 10% (up to a maximum of 30%) per week.

See the [Schedule](schedule.html) for the functionality deadlines.

## Other Considerations
{: .page-header }

Concerned about your grade or falling behind?

Regardless, **don't cheat**. I *often* catch it. It gets messy. There are consequences. You do NOT end up saving time, effort, reputation, or stress. You DO miss one of the few (if not only) one-on-one personalized learning experiences you'll ever get in college.

Instead, please see below.

### Working Ahead

Worried about the deadline schedule and how slow code reviews progress?

You *can* work ahead on the functionality of the next project after passing verification, just **not in the `main` branch** used for the current project and code reviews.

If you want to work ahead, [create a separate branch](/guides/general/using-branches.html) for the next project. You can even create releases from that branch, allowing you to pass functionality for the next project while still undergoing code review for the current project.

However, you have to be comfortable with branching and merging in `git` if you choose this route. It is very easy to cause merge conflicts that can be difficult to resolve.

You **cannot** work more than one project ahead than the project currently under code review. Your efforts at that point are better spent on passing code review for the current project.

<i class="fas fa-exclamation-triangle"></i>
If your `main` branch includes functionality for the next project, you'll be asked to remove it and reschedule the code review. This could cost you a week, and undo your efforts to work ahead!
{: .notification }

### Extra Credit

Worried about those project points you missed due to late submissions? You can request extra credit opportunities in a **public post** on Piazza. These opportunities will be specific to the project, can be completed at any time, and are open to all students that missed points on that project.

Examples of extra credit opportunities include: creating unit tests for one of your classes, adding the ability to output compact JSON files, adding a new (but minor) feature, generating the actual Javadoc files for your project, and more.

Extra credit is not meant to be time consuming---especially given that many students that need it have already fallen behind in class.

Extra credit must be pre-approved on Piazza before it will be awarded. To receive credit, make a private post to the "Instructors" group confirming you completed the extra credit with a link to the public post that has the approval.
