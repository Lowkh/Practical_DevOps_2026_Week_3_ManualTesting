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
| Output | Team plan, test results, self-designed tests, evidence, reflections, and contribution history |

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

### SauceDemo

[https://www.saucedemo.com/](https://www.saucedemo.com/)

Use this website for positive, negative, and recovery login scenarios.

### Test Pages Validation Form

[https://testpages.eviltester.com/apps/client-server-form-validation/](https://testpages.eviltester.com/apps/client-server-form-validation/)

Use this website for equivalence partitioning and boundary testing.

### Test Pages Validation Instructions

[https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/)

Read this page to check the form’s current validation requirements.

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

#### Member A — Team Coordination

- Keep track of time.
- Help the team follow the activity sequence.
- Confirm that every member has an assigned task.

#### Member B — Requirements and Baseline

- Check the published requirements.
- Record the agreed baseline data.
- Highlight unclear or changed requirements.

#### Member C — Guided Test Coverage

- Check that all required guided test values are covered.
- Identify missing or unexecuted cases.

#### Member D — Evidence Organisation

- Help the team use consistent evidence filenames.
- Check that screenshots contain no sensitive information.
- Check that evidence links work.

#### Member E — Repository Integration

- Coordinate pull-request merging.
- Maintain the team summary.

For a four-member team, Members A and D share the repository integration responsibility.

> [!NOTE]
> These are coordination responsibilities, not exclusive jobs.
>
> Every member must test, record results, design additional tests, commit their own work, and complete a reflection.
>
> The repository coordinator must not commit everyone else’s work on their behalf.

### 4.3 Agree on How to Work Together

Before testing, agree on:

1. The shared repository.
2. The branch naming convention.
3. The baseline data.
4. Where each member will record results.
5. How the team will communicate progress.
6. Who will coordinate merging pull requests.

Members may discuss ideas and help one another. Each person must still identify their own executions and contributions.

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

#### Positive Test Example

```text
Input:
Valid credentials.

Expected:
Login succeeds.

If login succeeds:
Pass.

If login is rejected:
Fail.
```

#### Negative Test Example

```text
Input:
Incorrect password.

Expected:
Login is rejected.

If login is rejected:
Pass.

If login succeeds:
Fail.
```

> [!TIP]
> A negative test passes when the application handles invalid input correctly.
>
> An error message does not automatically mean the test failed.

### 5.5 Techniques for Selecting Test Data

#### Equivalence Partitioning

Divide inputs into groups expected to receive similar treatment. Select representative values from those groups.

#### 2-Point Boundary Testing

Select adjacent values on opposite sides of each boundary transition.

#### 3-Point Boundary Testing

Select identified boundary values and their immediate neighbours.

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
| `summary.md` | Links to completed work and a short team conclusion |
| `results/` | Guided test cases and results |
| `exploratory/` | Self-designed tests and observations |
| `reflections/` | Individual reflections |
| `evidence/` | Relevant screenshots |

Git does not track empty directories. Evidence folders will appear after files are added.

The coordinator commits and pushes the starting structure before members begin their individual branches.

### 6.3 Complete the Team Plan

Add the following structure to `team-plan.md`:

```markdown
# Team Plan

## Team Identifier

## Members

### Member A
- GitHub username:
- Coordination responsibility:

### Member B
- GitHub username:
- Coordination responsibility:

### Member C
- GitHub username:
- Coordination responsibility:

### Member D
- GitHub username:
- Coordination responsibility:

### Member E — If Applicable
- GitHub username:
- Coordination responsibility:

## Guided Test Allocation

## Agreed Baseline Data

## Open-Ended Testing Allocation

## Repository Integration Arrangements
```

Each member should primarily edit their own files.

The coordinator maintains the shared plan and summary.

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

### 7.2 Use a Separate Record for Each Test

Do not place long steps and results in a wide table.

Use a test-case block with:

- A short details table.
- Preconditions.
- Test data.
- Numbered steps.
- Expected result.
- Actual result.
- Evidence.

Copy this template for each test:

```markdown
### Test ID: YOUR-TEST-ID

| Item | Details |
|---|---|
| Test type | Positive / Negative / Recovery |
| Tester | Your member identifier |
| Website | Website name |
| Status | Not run |

#### Purpose

What does this test check?

#### Preconditions

What must be true before the test starts?

#### Test Data

| Field | Value |
|---|---|
| Input name | Input value |

#### Steps

1.
2.
3.

#### Expected Result

Write this before executing the test.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---
```

After executing the test:

1. Replace the actual-result placeholder with your observation.
2. Update the status.
3. Add relevant evidence.
4. Save, commit, and push the changes.

### 7.3 Use Consistent Statuses

| Status | Meaning |
|---|---|
| Pass | Actual result matches the expected result |
| Fail | Actual result differs from the expected result |
| Blocked | Another issue prevents completion |
| Not run | The test has not been executed |

For an exploratory observation without a clear expected result, explain the uncertainty rather than forcing a Pass or Fail. You may label it `Observation only`.

Avoid vague descriptions such as:

```text
Works.
```

Instead, record:

```text
After selecting Login, the inventory page appeared and
the product list was visible.
```

### 7.4 Save Evidence in Your Own Folder

Example:

```text
manual-testing/evidence/member-a/login-p01.png
```

From `results/member-a.md`, link using:

```markdown
[View screenshot](../evidence/member-a/login-p01.png)
```

Capture useful evidence, particularly for unexpected behaviour.

A screenshot is not required for every passing test. Written actual results are still required.

Do not capture sensitive information or unrelated personal browser content.

### 7.5 Use This Git Workflow at Every Checkpoint

Run commands from the repository root.

#### Step 1 — Save and Review

```bash
git status
git diff
```

Review new files and screenshots directly.

Normal `git diff` does not display untracked files or the visual contents of screenshots.

#### Step 2 — Stage Your Intended Files

Example for Member A:

```bash
git add manual-testing/results/member-a.md
```

If you added screenshots:

```bash
git add manual-testing/evidence/member-a/
```

When you edit your exploratory or reflection files, stage those paths as well.

#### Step 3 — Review the Staged Changes

```bash
git diff --cached
git status
```

Confirm that only your intended work is staged.

#### Step 4 — Commit

```bash
git commit -m "Prepare individual testing record"
```

Use a message that accurately describes the changes.

#### Step 5 — Push

For the first push:

```bash
git push -u origin testing/member-a
```

For subsequent pushes:

```bash
git push
```

Other members substitute their own branch names.

#### Step 6 — Verify on GitHub

Open your branch and check that:

1. The latest commit appears.
2. The expected files are present.
3. Markdown displays correctly.
4. Evidence links work.

> [!WARNING]
> A local commit does not upload your work to GitHub.
>
> Push and verify your work online. If a push is rejected, read the message and consult your Tutor if needed. Do not force push.

### Git Checkpoint — Preparation

Commit and push your environment details and initial test record.

Suggested message:

```text
Prepare individual testing record
```

***

## 8. Activity 1 — Positive and Negative Login Testing

Time: 20 minutes

Open:

[https://www.saucedemo.com/](https://www.saucedemo.com/)

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

| Member | Test ID | Scenario |
|---|---|---|
| A | LOGIN-P01 | Valid credentials |
| B | LOGIN-N01 | Incorrect password |
| C | LOGIN-N02 | Missing password |
| D | LOGIN-N03 | Missing username |
| E | LOGIN-R01 | Correct an invalid attempt |

For four members, Member A also performs LOGIN-R01.

### 8.3 Shared Starting Procedure

Before each independent test:

1. Open the login page.
2. Log out if already logged in.
3. Clear both input fields.
4. Confirm that you are starting from the logged-out state.

Do not reset between the two attempts within the recovery scenario.

### 8.4 LOGIN-P01 — Valid Credentials

Test type: Positive.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | `secret_sauce` |

#### Steps

1. Follow the shared starting procedure.
2. Enter the username.
3. Enter the password.
4. Select `Login`.
5. Observe the page reached.
6. Check that products are visible.

#### Expected Result

The inventory page appears and products are visible.

#### Record Your Result

In your own test record:

- Describe the actual page reached.
- Record whether products were visible.
- Assign a status.
- Add relevant evidence.

### 8.5 LOGIN-N01 — Incorrect Password

Test type: Negative.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | `wrong_password` |

#### Steps

1. Follow the shared starting procedure.
2. Enter the valid username.
3. Enter the incorrect password.
4. Select `Login`.
5. Observe the page and feedback.

#### Expected Result

Login is rejected, error feedback appears, and the inventory is not reached.

Keep the username valid to isolate the incorrect-password condition.

If rejection occurs as expected, mark the test Pass.

### 8.6 LOGIN-N02 — Missing Password

Test type: Negative.

#### Test Data

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | Empty |

#### Steps

1. Follow the shared starting procedure.
2. Enter the username.
3. Leave the password empty.
4. Select `Login`.
5. Observe the feedback.

#### Expected Result

The attempt is rejected with validation feedback. The inventory is not reached.

### 8.7 LOGIN-N03 — Missing Username

Test type: Negative.

#### Test Data

| Field | Value |
|---|---|
| Username | Empty |
| Password | `secret_sauce` |

#### Steps

1. Follow the shared starting procedure.
2. Leave the username empty.
3. Enter the password.
4. Select `Login`.
5. Observe the feedback.

#### Expected Result

The attempt is rejected with validation feedback. The inventory is not reached.

### 8.8 LOGIN-R01 — Recovery After an Invalid Attempt

Test type: Recovery.

#### Steps

1. Follow the shared starting procedure.
2. Enter `standard_user` and `wrong_password`.
3. Select `Login`.
4. Confirm rejection.
5. Replace the password with `secret_sauce`.
6. Keep the username unchanged.
7. Select `Login` again.
8. Check whether the inventory appears.

#### Expected Result

The invalid attempt is rejected. After correcting the password, login succeeds.

Record both stages in the actual result.

### 8.9 Discuss as a Team

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

Open the validation form and its instructions.

### 9.1 Step 1 — Read the Requirements

Check the current website instructions.

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

The whole-number restriction defines the classroom model.

If decimal behaviour is unspecified, record a requirement question rather than inventing an expected result.

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
3. Resolve the issue with your team or Tutor before proceeding.

Record the baseline in `team-plan.md`.

> [!IMPORTANT]
> When testing age, keep every other field valid and unchanged.
>
> Otherwise, rejection caused by another field could be mistaken for an age-validation result.

### 9.3 Step 3 — Identify Numeric Partitions

| Partition | Whole-number age group | Representative |
|---|---|---:|
| EP-01 | Below 18 | 10 |
| EP-02 | 18–80 inclusive | 30 |
| EP-03 | Above 80 | 90 |

Classify the selected values:

| Representative | Test type | Expected result |
|---:|---|---|
| 10 | Negative | Reject |
| 30 | Positive | Accept |
| 90 | Negative | Reject |

```text
       Negative                 Positive                 Negative
         <18                     18–80                     >80
─────────────────┬──────────────────────────────┬─────────────────
                 18                             80
```

### 9.4 Step 4 — Allocate Tests

| Member | Task |
|---|---|
| A | Test age 30 |
| B | Test age 10 |
| C | Test age 90 |
| D | Observe blank age handling |
| E | Observe non-numeric input handling using `abc` |

For four members, Member D performs both input-format observations.

### 9.5 Step 5 — Execute Numeric Tests

For each assigned numeric case:

1. Restore the form.
2. Enter the valid baseline.
3. Change only age.
4. Write the expected result.
5. Submit.
6. Observe acceptance or rejection.
7. Where displayed, verify the submitted age.
8. Record the actual result and status in a separate test-case block.

Suggested test IDs:

```text
AGE-EP-30-A
AGE-EP-10-B
AGE-EP-90-C
```

For this practical:

- Accept means the form successfully submits with the intended age.
- Reject means successful submission is prevented or a validation error is returned for that age.

### 9.6 Step 6 — Observe Input-Format Handling

For blank age and `abc`, record:

- Whether the input can be entered.
- Whether it is prevented, cleared, or rejected.
- What feedback appears.
- Whether the requirement clearly defines the expected behaviour.

These observations are separate from the three numeric partitions.

Do not claim that the server rejected input that the browser prevented from being entered.

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

Select values on opposite sides of each transition:

```text
17, 18, 80, 81
```

### 10.3 Step 3 — Allocate Tests

| Member | Assigned age |
|---|---|
| A | 17 |
| B | 18 |
| C | 80 |
| D | 81 |
| E | Independently repeat 18 and 81 |

For four members, omit the additional independent repetitions.

| Age | Test type | Expected result |
|---:|---|---|
| 17 | Negative | Reject |
| 18 | Positive | Accept |
| 80 | Positive | Accept |
| 81 | Negative | Reject |

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

Use separate records with IDs such as:

```text
AGE-2P-17-A
AGE-2P-18-B
AGE-2P-80-C
AGE-2P-81-D
```

The final letter identifies the tester.

### 10.5 Example Boundary Test Record

```markdown
### Test ID: AGE-2P-17-A

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-a |
| Website | Test Pages validation form |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check that an age immediately below the minimum is rejected.

#### Preconditions

The validation form is open.
All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| Age | `17` |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `17`.
4. Submit.
5. Observe the response.

#### Expected Result

Age 17 is rejected because it is below the minimum age of 18.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---
```

### 10.6 Step 5 — Interpret the Results

Consider this hypothetical implementation mistake:

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

| Boundary value | Values to consider |
|---:|---|
| 17 | 16, 17, 18 |
| 18 | 17, 18, 19 |
| 80 | 79, 80, 81 |
| 81 | 80, 81, 82 |

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

| Member | Additional age |
|---|---|
| A | 16 |
| B | 19 |
| C | 79 |
| D | 82 |
| E | Independently repeat 16 and 79 |

Classify the additional values:

| Age | Test type | Expected result |
|---:|---|---|
| 16 | Negative | Reject |
| 19 | Positive | Accept |
| 79 | Positive | Accept |
| 82 | Negative | Reject |

Use the same baseline and execution procedure as Activity 3.

Record each execution in its own test-case block.

### 11.5 Step 5 — Reference Existing Results

The team may reuse results for `17`, `18`, `80`, and `81` if the environment, baseline, and procedure remain applicable.

Identify the original tester, file, and test ID.

Example from `results/member-b.md`:

```markdown
### Age 17 — Reused Execution

- Original test: `AGE-2P-17-A`
- Tester: `member-a`
- Record: [Member A’s results](member-a.md)
- Reason for reuse: The baseline, environment, and procedure remain applicable.
```

Do not copy another member’s execution and present it as your own.

### 11.6 Step 6 — Compare Coverage

#### Equivalence Partitioning

```text
Positive:
30

Negative:
10, 90
```

#### 2-Point Boundary Testing

```text
Positive:
18, 80

Negative:
17, 81
```

#### 3-Point Boundary Testing

```text
Positive:
18, 19, 79, 80

Negative:
16, 17, 81, 82
```

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

Update `team-plan.md` with a short block for each member:

```markdown
### Member A — Open-Ended Testing

- Chosen area:
- Question to investigate:

### Member B — Open-Ended Testing

- Chosen area:
- Question to investigate:
```

Repeat for the remaining members.

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

Record any assumptions or unclear requirements.

## Approach

How will I choose data and perform the tests?

## Test Cases

### Test ID: OWN-A-01

| Item | Details |
|---|---|
| Test type | Positive / Negative / Recovery / Exploratory |
| Tester | member-a |
| Status | Not run |

#### Purpose

What does this individual test check?

#### Preconditions

What starting state is required?

#### Test Data

List the exact inputs or actions.

#### Steps

1.
2.
3.

#### Expected Result

State the expected behaviour and its basis.

If the behaviour is unspecified, record the question being investigated.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## Overall Observations

What did the tests show?

## Next Question

What would I investigate next?
```

Duplicate the test-case block for additional tests.

You may adapt the structure, but keep enough detail for another person to understand what you did.

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

The aim is to create useful tests, not the largest collection.

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

Formal peer approval and reproduction are not required.

Before merging, confirm that:

- Files are in the intended locations.
- Another member’s work is not overwritten.
- Relevant evidence links are included.
- No sensitive information is present.

Use a merge method that preserves individual commits for this practical.

If a merge conflict appears, resolve it with the affected member. Consult your Tutor if needed.

Do not overwrite work blindly.

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

Use short sections and links rather than a wide contribution table.

### 15.1 Guided Testing Coverage

Copy and complete:

```markdown
# Team Summary

## Guided Testing Coverage

### Login Testing

Required coverage:
- Valid credentials.
- Incorrect password.
- Missing password.
- Missing username.
- Recovery after an invalid attempt.

Results:
Add links to the relevant member records.

### Equivalence Partitioning

Required coverage:
- Age below the accepted range.
- Age within the accepted range.
- Age above the accepted range.

Results:
Add links to the relevant member records.

### Input-Format Observations

Required observations:
- Blank age.
- Non-numeric age input.

Results:
Add links to the relevant member records.

### 2-Point Boundary Testing

Required values:
17, 18, 80, 81.

Results:
Add links to the relevant member records.

### 3-Point Boundary Testing

Required values:
16, 17, 18, 19, 79, 80, 81, 82.

Results:
Add links to new executions and identify reused evidence.
```

### 15.2 Member Contributions

Add a block for each member:

```markdown
## Member Contributions

### Member A

- Guided results: [View results](results/member-a.md)
- Self-designed tests: [View tests](exploratory/member-a.md)
- Reflection: [View reflection](reflections/member-a.md)
- Chosen investigation:
- Main observation:
- Pull request: Add the actual pull-request link.

### Member B

- Guided results: [View results](results/member-b.md)
- Self-designed tests: [View tests](exploratory/member-b.md)
- Reflection: [View reflection](reflections/member-b.md)
- Chosen investigation:
- Main observation:
- Pull request: Add the actual pull-request link.
```

Repeat for the remaining members.

### 15.3 Team Conclusion

Finish with a short conclusion:

- What did the guided activities help you understand?
- How did members extend the testing in different directions?
- What would the team investigate next?

Commit and push the summary, then merge it through a pull request.

> [!TIP]
> Count a reused execution once, even if it supports multiple techniques.
>
> Identify independent repetitions separately.
>
> Preserve differing observations rather than silently replacing one result with another.

***

## 16. Final Completion Checklist

### Every Member

- [ ] I used my own working branch.
- [ ] I completed my assigned guided tests.
- [ ] I used separate, readable test-case blocks.
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

If Git reports unfinished changes or refuses the update, stop and consult your Tutor.

Do not discard work or force the operation.

Verify the final repository on GitHub.

> [!TIP]
> Capture genuine progress. Do not create empty commits or split completed work artificially just to increase the commit count.
>
> Your history should help another person understand what you prepared, executed, and learned.

***

## 17. Troubleshooting

### Website Is Unavailable

Record the time and mark affected tests `Blocked`.

Continue designing cases, but do not claim that they were executed.

### Baseline Is Rejected

Recheck the current requirements and every baseline field, especially surname length and country selection.

### Browser Prevents Input

Record the prevention as the actual behaviour.

Do not describe it as a server response.

### Expected Behaviour Is Unclear

State the assumption or record a requirement question.

Do not invent a requirement.

### Members Observe Different Results

Compare:

- Baseline values.
- Starting state.
- Browser.
- Exact steps.
- Timing of the observation.

Preserve both observations while investigating the difference.

### No Defects Are Found

Record passing results and what they demonstrate.

You do not need to find a defect to complete the practical.

### Evidence Link Does Not Work

Check:

- Relative path.
- Filename.
- File extension.
- Letter case.
- Whether the image was committed and pushed.

### Git Reports Nothing to Commit

Check that:

- Your files were saved.
- You are in the correct repository.
- You edited the intended files.
- The changes have not already been committed.

### Push Is Rejected

Read the message and consult your Tutor if needed.

Do not force push.

### Merge Conflict Appears

Coordinate with the affected member.

Resolve the conflicting content carefully. Do not overwrite work blindly.

### One Member Is Doing All Git Work

Pause and redistribute responsibilities.

Every member must commit and push their own contribution.

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

Remember that negative text lengths are outside the input domain.

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
