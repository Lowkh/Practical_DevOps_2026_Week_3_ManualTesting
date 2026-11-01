# Manual Testing Team Practical

> A guided, hands-on introduction to positive testing, negative testing, equivalence partitioning, and boundary value analysis, followed by an open-ended testing activity.

Work in a team of 4–5 members to test existing demonstration websites. Complete the guided activities first, then apply what you have learned by designing and executing your own tests.

Each member must perform tests, record actual results, and contribute through Git. Your team will combine these contributions into one shared repository.

The focus is on selecting meaningful tests, recording accurate observations, and maintaining a clear history of your work.

> [!IMPORTANT]
> ## Capture Your Practical Using Git
>
> Every member must use **Git** throughout this practical.
>
> Work on your own branch, make meaningful commits, push to GitHub, and use pull requests to combine your contributions.
>
> Do not wait until the end to upload everything. Your repository history should show the progression from test preparation to execution and reflection.
>
> A formal findings report, assigned peer review, and peer-reproduction exercise are not required. During the open-ended activity, members decide what additional tests to create.

| Item | Details |
|---|---|
| Duration | 2.5 hours |
| Team size | 4–5 members |
| Prerequisites | Basic web browsing, Markdown editing, and Git/GitHub skills from the earlier practical |
| Tools | Web browser, text editor, Git, GitHub, and screenshot tool |
| Websites | SauceDemo and Test Pages |
| Collaboration | Shared repository, individual branches, commits, and pull requests |
| Output | A shared repository containing the team plan, guided test results, self-designed tests, evidence, reflections, and contribution history |

> [!NOTE]
> ## Educational Practice Repository
>
> This repository has been created solely for an introductory manual testing and collaboration practical.
>
> All names, accounts, examples, and test data prepared by students must be fictional and used only for educational purposes. Any resemblance to actual persons, organisations, events, or circumstances is purely coincidental.
>
> Do not include personal, confidential, sensitive, or commercially sensitive information.
>
> Use only the demonstration websites and normal browser interactions described in this practical. Do not conduct security attacks, generate excessive traffic, or test unrelated production websites.

> [!WARNING]
> Public demonstration websites may change or become unavailable. Record any differences and consult your Tutor.
>
> Never claim that a test was executed if it was only designed.

***

## 1. Learning Outcomes

By the end of this practical, you should be able to:

1. Distinguish positive testing from negative testing.
2. Write test cases with clear steps and expected results.
3. Execute tests manually and record actual behaviour.
4. Select representative inputs using equivalence partitioning.
5. Apply 2-point and 3-point boundary testing.
6. Design additional tests based on your own ideas and observations.
7. Collaborate through branches, commits, and pull requests.
8. Use Git history to show the development of your testing work.

## 2. Practical Schedule

Git updates and collaboration are included in the activity times.

| Activity | Duration |
|---|---:|
| Team setup, repository preparation, and concepts | 25 minutes |
| Activity 1: Positive and negative login testing | 20 minutes |
| Activity 2: Equivalence partitioning | 20 minutes |
| Activity 3: 2-point boundary testing | 20 minutes |
| Activity 4: 3-point boundary testing | 20 minutes |
| Activity 5: Design and execute your own tests | 30 minutes |
| Reflections and final repository check | 15 minutes |
| Total | 150 minutes |

## 3. Websites Used

| Website | Purpose |
|---|---|
| [SauceDemo](https://www.saucedemo.com/) | Positive and negative login testing |
| [Test Pages validation form](https://testpages.eviltester.com/apps/client-server-form-validation/) | Equivalence partitioning and boundary testing |
| [Test Pages validation instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/) | Checking published validation requirements |

***

## 4. Organise Your Team

### 4.1 Assign Member Identifiers

Use these identifiers consistently:

```text
member-a
member-b
member-c
member-d
member-e
```

For a four-member team, omit `member-e`.

Use your identifier in branch names, filenames, evidence folders, and test records.

### 4.2 Assign Coordination Responsibilities

| Responsibility | Five-member team | Four-member team |
|---|---|---|
| Coordinate timing and task allocation | Member A | Member A |
| Check requirements and baseline data | Member B | Member B |
| Check guided testing coverage | Member C | Member C |
| Check evidence organisation | Member D | Member D |
| Coordinate repository integration and summary | Member E | Shared by A and D |

These are coordination responsibilities, not exclusive jobs.

Every member must still:

- Execute assigned tests.
- Record their own results.
- Design additional tests.
- Commit and push their own work.
- Complete an individual reflection.

The repository coordinator must not commit everyone else’s work on their behalf.

### 4.3 Agree on How to Work Together

Before testing, agree on:

1. The repository and branch naming convention.
2. The shared baseline data.
3. Where each member will record results.
4. How the team will communicate progress.
5. Who will coordinate merging pull requests.

Members may discuss ideas and help one another. However, each member must identify their own executions and contributions.

***

## 5. Understand the Testing Concepts

### 5.1 Manual Testing

In this practical, you perform the test steps yourself rather than running automated test scripts.

Use this sequence:

```text
Read the requirement
        ↓
Select test data
        ↓
Write the expected result
        ↓
Execute from a known starting state
        ↓
Record the actual result
        ↓
Compare and assign a status
        ↓
Capture the work using Git
```

Write the expected result before executing the test.

### 5.2 Positive Testing

Positive testing uses valid inputs and expected actions.

Example:

```text
Action:
Enter valid login credentials.

Expected result:
The application allows login.
```

The question is:

> Does the application behave correctly when the user provides valid information?

### 5.3 Negative Testing

Negative testing uses invalid inputs or unexpected actions.

Example:

```text
Action:
Enter an incorrect password.

Expected result:
The application rejects the login attempt.
```

The question is:

> Does the application handle invalid information correctly?

### 5.4 Test Type Is Different from Test Status

| Test type | Input | Expected behaviour | Actual behaviour | Status |
|---|---|---|---|---|
| Positive | Valid credentials | Allow login | Login allowed | Pass |
| Positive | Valid credentials | Allow login | Login rejected | Fail |
| Negative | Incorrect password | Reject login | Login rejected | Pass |
| Negative | Incorrect password | Reject login | Login allowed | Fail |

> [!TIP]
> A negative test passes when the application handles invalid input correctly.
>
> An error message does not automatically mean the test failed.

### 5.5 Techniques for Selecting Test Data

| Technique | Purpose |
|---|---|
| Equivalence partitioning | Divide inputs into groups expected to receive similar treatment and select representatives |
| 2-point boundary testing | Select adjacent values on opposite sides of each boundary transition |
| 3-point boundary testing | Select identified boundary values and their immediate neighbours |

These techniques help you choose test data. A selected case is positive or negative according to whether its input is valid.

***

## 6. Prepare the Shared Repository

### 6.1 Create One Team Repository

One member creates the repository according to your Tutor’s instructions.

Suggested name:

```text
manual-testing-team-XX
```

Replace `XX` with your assigned team identifier.

1. Initialise the repository with a `README.md`.
2. Use the visibility specified by your Tutor.
3. Add every team member as a collaborator.
4. Add your Tutor using the account provided.
5. Ensure everyone accepts their invitation.

Do not create separate unrelated repositories for individual submissions.

### 6.2 Prepare the Starting Structure

The repository coordinator creates:

```text
README.md
manual-testing/
├── team-plan.md
├── summary.md
├── results/
│   ├── member-a.md
│   ├── member-b.md
│   ├── member-c.md
│   ├── member-d.md
│   └── member-e.md
├── exploratory/
│   ├── member-a.md
│   ├── member-b.md
│   ├── member-c.md
│   ├── member-d.md
│   └── member-e.md
├── reflections/
│   ├── member-a.md
│   ├── member-b.md
│   ├── member-c.md
│   ├── member-d.md
│   └── member-e.md
└── evidence/
```

Omit Member E’s files for a four-member team.

The initial member files may contain only a heading.

| Location | Purpose |
|---|---|
| `team-plan.md` | Members, responsibilities, baseline data, and task allocation |
| `summary.md` | Links to completed work and a short team summary |
| `results/` | Guided test cases and results |
| `exploratory/` | Self-designed tests and observations |
| `reflections/` | Individual reflections |
| `evidence/` | Relevant screenshots |

Git does not track empty directories. Evidence folders will appear after files are added.

The coordinator commits and pushes the starting structure before members begin their individual branches.

### 6.3 Complete the Team Plan

In `team-plan.md`, record:

```markdown
# Team Plan

## Team Identifier

## Members

| Identifier | GitHub username | Coordination responsibility |
|---|---|---|
| member-a | | |
| member-b | | |
| member-c | | |
| member-d | | |
| member-e, if applicable | | |

## Guided Test Allocation

## Agreed Baseline Data

## Open-Ended Testing Allocation

## Repository Integration Arrangements
```

Each member should primarily edit their own files. The coordinator maintains the shared plan and summary.

### 6.4 Clone the Repository

Each member:

1. Opens the shared repository.
2. Selects `Code`.
3. Selects `HTTPS`.
4. Copies the repository URL.
5. Opens a terminal.
6. Replaces the placeholders below and runs:

```bash
git clone REPOSITORY_URL
cd REPOSITORY_FOLDER
```

If the repository is already cloned, open the existing local folder instead.

Check:

```bash
git status
git branch --show-current
```

Confirm that the starting structure is present.

### 6.5 Create Your Own Branch

Member A runs:

```bash
git switch -c testing/member-a
```

Other members use their own identifier:

```text
testing/member-b
testing/member-c
testing/member-d
testing/member-e
```

> [!IMPORTANT]
> Work on your own branch.
>
> Do not edit another member’s files without agreeing first. Use pull requests to combine contributions into `main`.

***

## 7. Prepare Your Individual Test Record

### 7.1 Add Your Environment Details

In your file under `manual-testing/results/`, add:

```markdown
# Manual Testing Results — Member A

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-a |
| Date and time | |
| Browser and version | |
| Operating system | |

## Login Tests

## Equivalence Partitioning

## 2-Point Boundary Tests

## 3-Point Boundary Tests
```

Replace Member A’s details with your own identifier.

### 7.2 Use Consistent Test Records

Use a table such as:

```markdown
| Test ID | Type | Test data | Expected result | Actual result | Status | Evidence |
|---|---|---|---|---|---|---|
| | | | | | Not run | |
```

For longer scenarios, write the numbered steps above the results table.

| Status | Meaning |
|---|---|
| Pass | Actual result matches the expected result |
| Fail | Actual result differs from the expected result |
| Blocked | Another issue prevents completion |
| Not run | The test has not been executed |

Avoid vague actual results such as “works” or “does not work.” Describe the page, message, or behaviour observed.

### 7.3 Save Evidence in Your Own Folder

Example:

```text
manual-testing/evidence/member-a/login-n01.png
```

From `results/member-a.md`, link using:

```markdown
[View screenshot](../evidence/member-a/login-n01.png)
```

Capture useful evidence, particularly for unexpected behaviour. A screenshot is not required for every passing test.

Do not capture sensitive information or unrelated personal browser content.

### 7.4 Use This Git Workflow at Each Checkpoint

Save your files, then:

```bash
git status
git diff
```

Review new files and screenshots directly. Normal `git diff` does not display untracked files or the visual contents of screenshots.

Stage only your intended files. For example:

```bash
git add manual-testing/results/member-a.md
```

If you added screenshots, stage your evidence folder as well:

```bash
git add manual-testing/evidence/member-a/
```

Review the staged changes:

```bash
git diff --cached
git status
```

Commit with a meaningful message:

```bash
git commit -m "Prepare member A testing record"
```

For the first push:

```bash
git push -u origin testing/member-a
```

For subsequent pushes:

```bash
git push
```

Other members substitute their own paths and branch names.

Open GitHub and verify that your latest commit and files appear on your branch.

> [!WARNING]
> A local commit does not upload your work to GitHub.
>
> Push your commits and verify them online. If a push is rejected, read the message and consult your Tutor if needed. Do not force push.

### Git Checkpoint — Preparation

Commit and push your environment details and initial test record.

Suggested message:

```text
Prepare individual testing record
```

***

## 8. Activity 1 — Positive and Negative Login Testing

Time: 20 minutes

Open [SauceDemo](https://www.saucedemo.com/).

Demonstration credentials:

```text
Username: standard_user
Password: secret_sauce
```

### 8.1 Acceptance Criteria

For this exercise:

1. Valid credentials allow access to the product inventory.
2. Incorrect credentials do not allow access.
3. Missing required credentials do not allow access.
4. Correcting an invalid attempt allows a subsequent valid login.

### 8.2 Allocate Tests

| Member | Assigned scenario |
|---|---|
| A | LOGIN-P01: Valid credentials |
| B | LOGIN-N01: Incorrect password |
| C | LOGIN-N02: Missing password |
| D | LOGIN-N03: Missing username |
| E | LOGIN-R01: Recovery after invalid login |

For four members, Member A also performs LOGIN-R01.

### 8.3 Execute the Assigned Login Test

1. Start from the logged-out login page.
2. Clear both fields.
3. Enter the assigned data.
4. Write the expected result before selecting `Login`.
5. Select `Login`.
6. Observe the page and feedback.
7. Record the actual result.
8. Assign a status.

| ID | Type | Username | Password | Expected result |
|---|---|---|---|---|
| LOGIN-P01 | Positive | `standard_user` | `secret_sauce` | Inventory appears |
| LOGIN-N01 | Negative | `standard_user` | `wrong_password` | Login rejected with feedback |
| LOGIN-N02 | Negative | `standard_user` | Empty | Login rejected with feedback |
| LOGIN-N03 | Negative | Empty | `secret_sauce` | Login rejected with feedback |

For the positive case, confirm that products are visible.

For negative cases:

- Confirm that the inventory is not reached.
- Copy relevant feedback accurately.
- Mark the test Pass if rejection matches the expected result.

### 8.4 Execute the Recovery Scenario

For LOGIN-R01:

1. Enter `standard_user` and `wrong_password`.
2. Select `Login`.
3. Confirm rejection.
4. Replace the password with `secret_sauce`.
5. Select `Login` again.
6. Check whether the inventory appears.
7. Record both stages.

Expected result:

```text
The invalid attempt is rejected.
The corrected attempt succeeds.
```

### 8.5 Discuss as a Team

Each member briefly explains:

- Which test they performed.
- Why it is positive, negative, or a recovery scenario.
- What happened.
- Why the test passed or failed.

### Git Checkpoint — Login Testing

Save, review, commit, and push your results.

Suggested message:

```text
Record assigned login testing results
```

***

## 9. Activity 2 — Equivalence Partitioning

Time: 20 minutes

Open the [validation form](https://testpages.eviltester.com/apps/client-server-form-validation/) and its [instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/).

### 9.1 Step 1 — Read the Requirements

Check the current instructions.

The requirements used in this practical include:

| Field | Requirement |
|---|---|
| First name | Required and fewer than 90 characters |
| Surname | Between 11 and 79 characters |
| Age | Between 18 and 80 |
| Country | Selected from the available list |
| Notes | No more than 2,000 characters |

For the core age exercises, use this classroom model:

```text
Age is a whole number from 18 to 80 inclusive.
```

```text
18 ≤ age ≤ 80
```

The whole-number restriction defines the classroom model. If decimal behaviour is unspecified, record a requirement question.

### 9.2 Step 2 — Establish a Valid Baseline

Every member enters:

| Field | Baseline value |
|---|---|
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | The same available country agreed by the team |
| Notes | `Manual testing classroom exercise` |

Submit and verify that the baseline succeeds.

If it does not:

1. Recheck the values.
2. Read the current requirements.
3. Resolve the issue with your team or Tutor before continuing.

> [!IMPORTANT]
> When testing age, keep every other field valid and unchanged.
>
> Otherwise, a rejection caused by another field could be mistaken for an age-validation result.

### 9.3 Step 3 — Identify the Partitions

| Partition | Whole-number age group | Representative | Type | Expected result |
|---|---|---:|---|---|
| EP-01 | Below 18 | 10 | Negative | Reject |
| EP-02 | 18–80 inclusive | 30 | Positive | Accept |
| EP-03 | Above 80 | 90 | Negative | Reject |

```text
       Negative                 Positive                 Negative
         <18                     18–80                     >80
─────────────────┬──────────────────────────────┬─────────────────
                 18                             80
```

### 9.4 Step 4 — Allocate Tests

| Member | Assigned task |
|---|---|
| A | Age 30: valid numeric partition |
| B | Age 10: below-range partition |
| C | Age 90: above-range partition |
| D | Observe blank age handling |
| E | Observe non-numeric input handling using `abc` |

For four members, Member D performs both input-format observations.

### 9.5 Step 5 — Execute and Record

For numeric cases:

1. Restore the form.
2. Enter the valid baseline.
3. Change only age.
4. Record the expected result.
5. Submit.
6. Observe acceptance or rejection.
7. Where displayed, verify the submitted age.
8. Record the actual result and status.

For input-format observations, record:

- Whether the input can be entered.
- Whether it is prevented, cleared, or rejected.
- What feedback appears.

Do not claim that the server rejected input that the browser prevented from being entered.

If the expected behaviour is unclear, record a requirement question rather than inventing a rule.

### Discussion Checkpoint

Why would testing only `25`, `40`, and `60` leave important numeric partitions untested?

### Git Checkpoint — Equivalence Partitioning

Commit and push your results and observations.

Suggested message:

```text
Record equivalence and input-format testing
```

***

## 10. Activity 3 — 2-Point Boundary Testing

Time: 20 minutes

### 10.1 Step 1 — Locate the Transitions

```text
17 → 18     Invalid → Valid
80 → 81     Valid → Invalid
```

### 10.2 Step 2 — Select Adjacent Values

Select the values on opposite sides of each transition:

```text
17, 18, 80, 81
```

### 10.3 Step 3 — Allocate Tests

| Member | Age | Type | Expected result |
|---|---:|---|---|
| A | 17 | Negative | Reject |
| B | 18 | Positive | Accept |
| C | 80 | Positive | Accept |
| D | 81 | Negative | Reject |
| E | Independently repeat 18 and 81 | Positive and negative | Accept 18; reject 81 |

For four members, omit the additional independent repetitions.

### 10.4 Step 4 — Execute and Record

Each assigned tester:

1. Restores the form.
2. Enters the valid baseline.
3. Changes only age.
4. Writes the expected result.
5. Submits.
6. Observes the actual behaviour.
7. Records relevant feedback.
8. Assigns a status.

Use IDs such as:

```text
AGE-2P-17-A
AGE-2P-18-B
AGE-2P-80-C
AGE-2P-81-D
```

The final letter identifies the tester.

### 10.5 Step 5 — Interpret the Results

Consider:

```text
Incorrect:
age > 18

Required:
age >= 18
```

Testing `30` would not reveal the difference. Testing `18` would.

Discuss:

1. Why is age 18 a positive boundary test?
2. Why is age 17 a negative boundary test?
3. Why is testing only 18 and 80 incomplete?

### Git Checkpoint — 2-Point Boundaries

Commit and push your results.

Suggested message:

```text
Record assigned 2-point boundary tests
```

***

## 11. Activity 4 — 3-Point Boundary Testing

Time: 20 minutes

### 11.1 Step 1 — Understand the Convention

This practical uses the ISTQB CTFL v4.0 interpretation of 3-value boundary value analysis.

For each identified boundary value, test:

```text
One below → Boundary value → One above
```

This includes boundary values belonging to adjacent invalid partitions.

### 11.2 Step 2 — Identify Boundary Values

| Partition | Boundary value or values |
|---|---|
| Below 18 | 17 |
| 18–80 inclusive | 18 and 80 |
| Above 80 | 81 |

### 11.3 Step 3 — Add Immediate Neighbours

| Boundary value | One below | Boundary | One above |
|---:|---:|---:|---:|
| 17 | 16 | 17 | 18 |
| 18 | 17 | 18 | 19 |
| 80 | 79 | 80 | 81 |
| 81 | 80 | 81 | 82 |

Remove duplicates:

```text
16, 17, 18, 19, 79, 80, 81, 82
```

> [!NOTE]
> Some introductory materials use a simplified six-value convention:
>
> ```text
> 17, 18, 19, 79, 80, 81
> ```
>
> This practical uses the eight-value convention derived above. State the convention clearly rather than mixing the two approaches.

### 11.4 Step 4 — Allocate Additional Executions

| Member | Additional age | Type | Expected result |
|---|---:|---|---|
| A | 16 | Negative | Reject |
| B | 19 | Positive | Accept |
| C | 79 | Positive | Accept |
| D | 82 | Negative | Reject |
| E | Independently repeat 16 and 79 | Negative and positive | Reject 16; accept 79 |

Use the same baseline and execution procedure as Activity 3.

### 11.5 Step 5 — Reference Existing Results

The team may reuse results for `17`, `18`, `80`, and `81` if the environment, baseline, and procedure remain applicable.

Identify the original tester, file, and test ID.

Example from `results/member-b.md`:

```markdown
Age 17:
See AGE-2P-17-A in [Member A’s results](member-a.md).
```

Do not copy another member’s execution and present it as your own.

### 11.6 Step 6 — Compare Coverage

| Technique | Positive values | Negative values |
|---|---|---|
| Equivalence partitioning | 30 | 10, 90 |
| 2-point boundary testing | 18, 80 | 17, 81 |
| 3-point boundary testing | 18, 19, 79, 80 | 16, 17, 81, 82 |

### Discussion Checkpoint

What did 3-point testing add, and why do these tests still not prove that every possible input works correctly?

### Git Checkpoint — 3-Point Boundaries

Commit and push your new results and references.

Suggested message:

```text
Record assigned 3-point boundary tests
```

***

## 12. Activity 5 — Design and Execute Your Own Tests

Time: 30 minutes

You have practised positive testing, negative testing, equivalence partitioning, and boundary testing.

Now decide what else is worth investigating.

There is no prescribed set of scenarios for this activity. Your team chooses the direction, and every member designs and executes their own additional tests.

### 12.1 Step 1 — Choose What to Investigate

Continue using SauceDemo or the Test Pages validation form.

Choose a manageable feature, input, or sequence of actions that you have not already tested in exactly the same way.

Possible starting questions include:

- What other valid inputs should work?
- What invalid inputs have we not considered?
- Are there other boundaries worth investigating?
- What happens when the user corrects an error and tries again?
- What happens when actions are repeated?
- What happens when actions are performed in a different sequence?

These are prompts, not a required checklist. You may develop a different testing idea.

### 12.2 Step 2 — Agree on the Team’s Approach

Update the allocation in `team-plan.md`:

| Member | Chosen area | What they want to investigate |
|---|---|---|
| A | | |
| B | | |
| C | | |
| D | | |
| E, if applicable | | |

Members may investigate the same feature if they ask different questions or use different test data.

### 12.3 Step 3 — Record Your Testing Idea

In your own file under `manual-testing/exploratory/`, use:

```markdown
# Self-Designed Testing — Member A

## Testing Idea
What do I want to investigate?

## Reason
Why is this worth testing?

## Test Basis
What requirement or stated expectation am I checking?

## Approach
How will I choose data and perform the tests?

## Test Cases and Results

| ID | Type | Steps and data | Expected result | Actual result | Status |
|---|---|---|---|---|---|
| OWN-A-01 | | | | | Not run |

## Observations
What did I learn or notice?

## Evidence
Add relevant screenshot links.

## Next Question
What would I investigate next?
```

You may adapt the structure. Keep enough detail for another person to understand what you did.

> [!NOTE]
> If the website does not specify the expected behaviour, state your assumption or record the result as an observation.
>
> Do not label behaviour as a confirmed defect simply because it differs from your personal preference.

### 12.4 Step 4 — Create Your Test Cases

Before executing a test:

1. Identify the starting state.
2. Choose the input or action.
3. Write the steps.
4. State the expected result.
5. Identify whether the case is positive or negative, where applicable.

Choose enough cases to investigate your idea meaningfully within the available time. There is no fixed test count.

The aim is to create useful tests, not the largest table.

### Git Checkpoint — Self-Designed Test Preparation

Commit and push your testing idea and planned cases before recording execution results.

Suggested message:

```text
Add self-designed test scenarios
```

### 12.5 Step 5 — Execute and Adapt

1. Perform the tests manually.
2. Record actual behaviour accurately.
3. Assign a status where the expected behaviour is clear.
4. Capture relevant evidence.
5. Add follow-up tests if your observations suggest another useful question.

You may change direction. Record why you changed your approach.

Leave unexecuted cases marked `Not run`.

### 12.6 Step 6 — Summarise What You Learned

Record:

- What you investigated.
- What the results showed.
- Any uncertainty or unanswered question.
- What you would test next.

A formal defect or findings report is not required. Passing results, unexpected observations, and requirement questions are all valid outcomes.

### Git Checkpoint — Self-Designed Test Execution

Commit and push your results and evidence.

Suggested message:

```text
Record self-designed testing results
```

***

## 13. Complete Your Individual Reflection

Each member answers the following in their own file under `manual-testing/reflections/`:

1. What makes a test positive or negative?
2. Why can a negative test pass?
3. How did equivalence partitioning help you select data?
4. What did boundary testing help you investigate?
5. What did you choose to test during the open-ended activity, and why?
6. Did your observations lead to follow-up tests?
7. How does your Git history show your contribution?

Write one or two sentences for each answer.

Commit and push:

```text
Add individual testing reflection
```

***

## 14. Combine Your Contributions Using Pull Requests

### 14.1 Open a Pull Request

Each member opens a pull request from their branch into `main`.

Suggested title:

```text
Add member A manual testing work
```

Include:

```markdown
## Guided Testing
What I executed and recorded.

## Self-Designed Testing
What I chose to investigate.

## Main Observation
What I learned.

## Files
Links to my results, exploratory work, and reflection.
```

You may open the pull request earlier and continue pushing commits to the same branch as you work.

### 14.2 Check Before Merging

Your team decides who merges each pull request.

Formal peer approval and reproduction are not required. Before merging, confirm that:

- Files are in the intended locations.
- Another member’s work is not overwritten.
- Relevant evidence links are included.
- No sensitive information is present.

Use a merge method that preserves individual commits for this practical.

If a merge conflict appears, resolve it with the affected member. Consult your Tutor if needed. Do not overwrite work blindly.

### 14.3 Verify Integration

After merging:

1. Open `main` on GitHub.
2. Confirm that the member’s files are present.
3. Open the Markdown files.
4. Check evidence links.
5. Confirm that the contribution appears in repository history.

***

## 15. Complete the Team Summary

The coordinator updates `summary.md` after members’ contributions are available.

### 15.1 Guided Testing Coverage

| Area | Required coverage | Links to results |
|---|---|---|
| Login | Positive, negative, and recovery scenarios | |
| Equivalence partitioning | Below range, valid range, above range | |
| Input format | Blank and non-numeric observations | |
| 2-point boundaries | 17, 18, 80, 81 | |
| 3-point boundaries | 16, 17, 18, 19, 79, 80, 81, 82 | |

### 15.2 Self-Designed Testing

| Member | Chosen investigation | Main observation | Link |
|---|---|---|---|
| A | | | |
| B | | | |
| C | | | |
| D | | | |
| E, if applicable | | | |

### 15.3 Contribution Summary

| Member | Guided results | Self-designed tests | Reflection | Pull request |
|---|---|---|---|---|
| A | | | | |
| B | | | | |
| C | | | | |
| D | | | | |
| E, if applicable | | | | |

### 15.4 Team Conclusion

Write a short conclusion:

- What did the guided activities help you understand?
- How did members extend the testing in different directions?
- What would the team investigate next?

Commit and push the summary, then merge it through a pull request.

> [!TIP]
> Count a reused execution once, even if it supports multiple techniques.
>
> Identify independent repetitions separately. Preserve differing observations rather than silently replacing one result with another.

***

## 16. Final Completion Checklist

### Every Member

- [ ] I used my own working branch.
- [ ] I completed my assigned guided tests.
- [ ] I recorded actual results and accurate statuses.
- [ ] I designed and executed additional tests.
- [ ] I explained why I chose those tests.
- [ ] I recorded assumptions or unclear requirements.
- [ ] I added relevant evidence.
- [ ] I committed progress throughout the practical.
- [ ] I opened my own pull request.
- [ ] I completed my reflection.
- [ ] My work is pushed and included in the shared repository.

### Team

- [ ] Every member contributed directly.
- [ ] The agreed baseline and task allocation are documented.
- [ ] All guided testing areas are covered.
- [ ] Every member’s self-designed testing is included.
- [ ] Evidence links work.
- [ ] The summary links to the supporting records.
- [ ] No member’s work was overwritten during integration.
- [ ] No intended work remains only on a local computer.
- [ ] The repository contains no sensitive information.

### Final Git Check

Each member runs:

```bash
git status
git log --oneline -10
```

After all their work is committed, pushed, and merged, each member updates local `main`:

```bash
git switch main
git pull --ff-only
```

If Git reports unfinished changes or refuses the update, stop and consult your Tutor. Do not discard work or force the operation.

Verify the final repository on GitHub.

> [!TIP]
> Capture genuine progress. Do not create empty commits or split completed work artificially just to increase the commit count.
>
> Your history should help another person understand what you prepared, executed, and learned.

***

## 17. Troubleshooting

| Situation | What to do |
|---|---|
| Website is unavailable | Record the time and mark affected tests Blocked. Do not claim execution. |
| Baseline is rejected | Recheck the current requirements and every baseline field. |
| Browser prevents input | Record the prevention as the actual behaviour. |
| Expected behaviour is unclear | State the assumption or record a requirement question. |
| Members observe different results | Compare baseline, starting state, browser, and exact steps. Preserve both observations. |
| No defects are found | Record passing results and what they demonstrate. |
| Evidence link fails | Check the relative path, filename, and letter case. |
| Git reports nothing to commit | Check that files were saved and that you are in the correct repository. |
| Push is rejected | Read the message and consult your Tutor. Do not force push. |
| Merge conflict appears | Coordinate with the affected member. Do not overwrite work blindly. |
| One member is doing all Git work | Redistribute responsibilities. Every member must commit and push their own contribution. |

***

## 18. Optional Extensions — Outside the In-Class Practical

These activities are not required during the 2.5-hour session. Attempt them in your own time if you have the bandwidth.

Continue capturing your work using Git.

### 18.1 Extend Your Investigation

Choose an unanswered question from your self-designed testing.

1. Explain why it matters.
2. Design follow-up cases.
3. Execute and record them.
4. Update your conclusion.

### 18.2 Test Another Field

Apply equivalence partitioning and boundary testing to first-name or surname length.

Check the current requirements and verify character counts before executing.

### 18.3 Compare Browsers

Repeat selected tests in another browser.

Separate differences in:

- Input prevention.
- Validation timing.
- Feedback presentation.
- Final acceptance or rejection.

***

## 19. Final Team Workflow

```text
Understand → Allocate → Design → Execute → Observe
           → Record → Commit → Push → Combine → Reflect
```

The goal is not simply to produce screenshots or discover errors. It is to build a shared, traceable record of what your team tested, what happened, and what you learned.
