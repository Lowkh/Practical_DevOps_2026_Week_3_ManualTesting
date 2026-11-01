# Manual Testing Practical

> A guided, hands-on introduction to positive testing, negative testing, equivalence partitioning, and boundary value analysis.

This practical helps you learn manual testing by using existing demonstration websites. You will prepare test cases, interact with the websites, compare expected and actual results, and document your findings.

The focus is on selecting meaningful tests, recording accurate observations, and maintaining a clear record of your work.

> [!IMPORTANT]
> ## Record Your Practical Using Git
>
> You must use **Git** to capture your work throughout this practical.
>
> Store your test cases, actual results, screenshots, findings, and reflection in your practical repository. Make meaningful commits as you complete each activity rather than uploading everything only at the end.
>
> Your repository should show how your work developed: preparing tests, recording observations, adding evidence, and improving your findings after peer review.
>
> Follow your Tutor’s instructions on which repository and branch to use. Commit and push your work at the checkpoints identified in this practical.

| Item | Details |
|---|---|
| Duration | 2.5 hours |
| Mode | Individual testing with paired discussion |
| Prerequisites | Basic web browsing, document editing, and Git skills from the earlier practical |
| Tools | Web browser, text editor, Git, GitHub, and screenshot tool |
| Websites | SauceDemo and Test Pages |
| Output | A GitHub repository containing test records, evidence, findings, reflection, and meaningful commit history |

> [!NOTE]
> ## Educational Practice Repository
>
> This repository has been created solely for an introductory manual testing practical.
>
> All names, accounts, examples, and test data prepared by students must be fictional and used only for educational purposes. Any resemblance to actual persons, organisations, events, or circumstances is purely coincidental.
>
> Do not include personal, confidential, sensitive, or commercially sensitive information in this repository.
>
> Use only the demonstration websites and normal browser interactions described in this practical. Do not conduct security attacks, generate excessive traffic, or test unrelated production websites.

> [!WARNING]
> Public demonstration websites may change or become unavailable. If the current page or its published requirements differ from this practical, record the difference and consult your Tutor.
>
> Never claim that a test was executed if you only designed the test case.

***

## 1. Learning Outcomes

By the end of this practical, you should be able to:

1. Explain the difference between positive and negative testing.
2. Write test cases with clear steps and expected results.
3. Execute tests manually and record actual behaviour.
4. Select representative inputs using equivalence partitioning.
5. Apply 2-point and 3-point boundary testing.
6. Decide whether a test passes or fails.
7. Describe a finding so another person can reproduce it.
8. Use Git and GitHub to capture testing progress and revisions.

## 2. Practical Schedule

The time for each activity includes its Git checkpoint.

| Activity | Duration |
|---|---:|
| Preparation and key concepts | 20 minutes |
| Activity 1: Positive and negative login testing | 25 minutes |
| Activity 2: Equivalence partitioning | 25 minutes |
| Activity 3: 2-point boundary testing | 20 minutes |
| Activity 4: 3-point boundary testing | 25 minutes |
| Activity 5: Findings and peer reproduction | 25 minutes |
| Reflection and final repository check | 10 minutes |
| Total | 150 minutes |

## 3. Websites Used

| Website | Purpose |
|---|---|
| [SauceDemo](https://www.saucedemo.com/) | Positive and negative login testing |
| [Test Pages validation form](https://testpages.eviltester.com/apps/client-server-form-validation/) | Equivalence partitioning and boundary testing |
| [Test Pages validation instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/) | Checking the form’s published requirements |

***

## 4. Understand the Testing Concepts

### 4.1 Manual Testing

In this practical, you perform the test steps yourself rather than running automated test scripts.

For each test:

1. Read the requirement.
2. Choose the test data.
3. Write the expected result.
4. Perform the steps.
5. Record the actual result.
6. Compare the results.
7. Assign a status.

```text
Requirement → Test data → Expected result → Execute
            → Actual result → Compare → Record
```

Write the expected result before performing the test. Do not assume that whatever the website does must be correct.

### 4.2 Positive Testing

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

### 4.3 Negative Testing

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

### 4.4 Test Type Is Different from Test Status

| Test type | Input | Expected behaviour | Actual behaviour | Status |
|---|---|---|---|---|
| Positive | Valid credentials | Allow login | Login allowed | Pass |
| Positive | Valid credentials | Allow login | Login rejected | Fail |
| Negative | Incorrect password | Reject login | Login rejected | Pass |
| Negative | Incorrect password | Reject login | Login allowed | Fail |

> [!TIP]
> A negative test passes when the application handles invalid input correctly.
>
> An error message is not automatically evidence of a failed test.

### 4.5 Selecting Test Data

| Technique | Purpose |
|---|---|
| Equivalence partitioning | Divide inputs into groups expected to receive similar treatment and select representatives |
| 2-point boundary testing | Test adjacent values on opposite sides of a boundary transition |
| 3-point boundary testing | Test identified boundary values and their immediate neighbours |

These techniques help you choose data. Each selected case can then be classified as positive or negative.

***

## 5. Prepare Your Repository and Test Records

### 5.1 Open the Correct Repository

Use the repository and branch specified by your Tutor.

If the repository has not been cloned:

1. Open its GitHub page.
2. Select `Code`.
3. Select `HTTPS`.
4. Copy the repository URL.
5. Open a terminal where you keep your practical work.
6. Replace `REPOSITORY_URL` below with the copied URL and run:

```bash
git clone REPOSITORY_URL
```

7. Move into the cloned folder, replacing `REPOSITORY_FOLDER` with its actual name:

```bash
cd REPOSITORY_FOLDER
```

If the repository is already cloned, open a terminal inside its existing local folder. Do not clone it again.

Check your current state:

```bash
git status
git branch --show-current
```

Confirm that you are in the correct repository and on the branch specified by your Tutor.

> [!NOTE]
> If you have unfinished changes from another activity or are unsure which branch to use, consult your Tutor. Do not discard existing work.

### 5.2 Create Your Working Files

Inside the repository, create:

```text
manual-testing/
├── test-results.md
├── findings.md
├── reflection.md
└── evidence/
```

| File or folder | What to record |
|---|---|
| `test-results.md` | Environment, test cases, expected results, actual results, and statuses |
| `findings.md` | One finding and changes made after peer reproduction |
| `reflection.md` | Reflection answers |
| `evidence/` | Relevant screenshots |

Git does not track empty folders. The `evidence/` folder will appear in the repository after you add a screenshot or another file.

Run the Git commands in this practical from the repository root.

### 5.3 Prepare `test-results.md`

Add:

```markdown
# Manual Testing Results

## Test Environment

| Item | Details |
|---|---|
| Tester identifier | |
| Date and time | |
| Browser and version | |
| Operating system | |
| Website URL | |

## Login Tests

## Equivalence Partitioning

## 2-Point Boundary Tests

## 3-Point Boundary Tests

## Execution Summary
```

Use a fictional or class-assigned tester identifier if the repository is public.

### 5.4 Record Results Consistently

Use a table such as:

```markdown
| Test ID | Type | Test data | Expected result | Actual result | Status | Evidence |
|---|---|---|---|---|---|---|
| | Positive / Negative | | | | Not run | |
```

| Status | Meaning |
|---|---|
| Pass | Actual behaviour matches the expected result |
| Fail | Actual behaviour differs from the expected result |
| Blocked | Another issue prevents completion |
| Not run | The test has not been executed |

Avoid vague actual results such as “works” or “does not work.” Describe what appeared, what changed, or what was prevented.

### 5.5 Save Screenshot Evidence

Use descriptive filenames:

```text
evidence/login-p01.png
evidence/login-n01.png
evidence/age-18.png
```

From `test-results.md`, link to a screenshot using:

```markdown
[View screenshot](evidence/login-n01.png)
```

Capture relevant evidence, particularly for failures, unexpected behaviour, and your reported finding. You do not need a screenshot for every passing case.

Check that screenshots do not expose personal information or unrelated browser content.

### 5.6 Use This Git Workflow at Every Checkpoint

#### Step 1 — Save and Review

Save your files, then run:

```bash
git status
git diff
```

Open new files and screenshots directly to review them. Untracked files do not appear in normal `git diff` output, and image contents are not displayed as a text diff.

#### Step 2 — Stage Your Practical Work

```bash
git add manual-testing/
```

#### Step 3 — Review the Staged Changes

```bash
git diff --cached
git status
```

Confirm that only intended files are staged.

#### Step 4 — Commit

Use the checkpoint message provided or another accurate description:

```bash
git commit -m "Prepare manual testing records"
```

#### Step 5 — Push

If your branch already has an upstream:

```bash
git push
```

For the first push of a new branch:

```bash
git push -u origin YOUR_BRANCH_NAME
```

Replace `YOUR_BRANCH_NAME` with your actual branch name.

#### Step 6 — Verify on GitHub

Open your repository and select your working branch.

Check that:

1. Your commit appears.
2. The intended files are present.
3. Markdown displays correctly.
4. Evidence links work when evidence has been added.

> [!IMPORTANT]
> A local commit does not upload your work to GitHub. You must push and verify it online.
>
> If a push is rejected, read the message and consult your Tutor if needed. Do not use a force push to bypass the problem.

### Git Checkpoint — Preparation

Commit and push your initial files and environment details.

Suggested message:

```text
Prepare manual testing records
```

***

## 6. Activity 1 — Positive and Negative Login Testing

Time: 25 minutes

Open [SauceDemo](https://www.saucedemo.com/).

Use:

```text
Username: standard_user
Password: secret_sauce
```

For this exercise, use these acceptance criteria:

1. Valid demonstration credentials allow access to the product inventory.
2. Incorrect credentials do not allow access.
3. Missing required credentials do not allow access.
4. After correcting an invalid attempt, valid credentials allow login.

### 6.1 Test LOGIN-P01 — Valid Credentials

| Item | Details |
|---|---|
| Type | Positive |
| Purpose | Check that valid credentials allow login |
| Starting state | Logged-out login page |

#### Steps

1. Open the login page.
2. If already logged in, use the logout option.
3. Clear both input fields.
4. Enter `standard_user` as the username.
5. Enter `secret_sauce` as the password.
6. Select `Login`.
7. Check the page reached and whether products are visible.
8. Record the actual result and status.

Expected result:

```text
Login succeeds and the product inventory page appears.
```

Do not assume success merely because the page changed. Check that the expected inventory is available.

### 6.2 Test LOGIN-N01 — Incorrect Password

| Item | Details |
|---|---|
| Type | Negative |
| Purpose | Check that an incorrect password is rejected |

#### Steps

1. Return to the logged-out login page.
2. Clear both fields.
3. Enter `standard_user`.
4. Enter `wrong_password`.
5. Select `Login`.
6. Observe the page and feedback.
7. Copy the error text accurately.
8. Record the actual result and status.

Expected result:

```text
Login is rejected.
The inventory is not reached.
Error feedback is displayed.
```

Keep the username valid so that this test isolates the incorrect password.

If the incorrect password is rejected as expected, mark the test Pass.

### 6.3 Test LOGIN-N02 — Missing Password

1. Return to the login page.
2. Clear both fields.
3. Enter `standard_user`.
4. Leave the password empty.
5. Select `Login`.
6. Observe the feedback.
7. Confirm that the inventory is not reached.
8. Record the result.

Expected result:

```text
The application rejects the attempt and displays validation feedback.
```

### 6.4 Test LOGIN-N03 — Missing Username

1. Return to the login page.
2. Clear both fields.
3. Leave the username empty.
4. Enter `secret_sauce` as the password.
5. Select `Login`.
6. Observe the feedback.
7. Confirm that the inventory is not reached.
8. Record the result.

Expected result:

```text
The application rejects the attempt and displays validation feedback.
```

### 6.5 Test LOGIN-R01 — Recovery After an Invalid Attempt

This scenario contains a negative attempt followed by a positive attempt.

1. Enter `standard_user` and `wrong_password`.
2. Select `Login`.
3. Confirm that the attempt is rejected.
4. Replace the password with `secret_sauce`.
5. Keep the username as `standard_user`.
6. Select `Login` again.
7. Check whether the inventory appears.
8. Record both stages of the scenario.

Expected result:

```text
The invalid attempt is rejected.
After correcting the password, login succeeds.
```

### 6.6 Complete Your Results

| ID | Type | Scenario | Expected result | Actual result | Status |
|---|---|---|---|---|---|
| LOGIN-P01 | Positive | Valid credentials | Allow login | | Not run |
| LOGIN-N01 | Negative | Incorrect password | Reject login | | Not run |
| LOGIN-N02 | Negative | Missing password | Reject login | | Not run |
| LOGIN-N03 | Negative | Missing username | Reject login | | Not run |
| LOGIN-R01 | Recovery | Correct invalid credentials | Reject first attempt; accept corrected attempt | | Not run |

### Discussion Checkpoint

1. Why can a negative test pass?
2. Why did you change only one credential in each negative test?
3. What additional behaviour did the recovery scenario check?

### Git Checkpoint — Login Testing

Save your results and relevant evidence. Review, stage, commit, push, and verify your work.

Suggested message:

```text
Record positive and negative login test results
```

***

## 7. Activity 2 — Equivalence Partitioning

Time: 25 minutes

Open the [validation form](https://testpages.eviltester.com/apps/client-server-form-validation/) and its [instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/).

### 7.1 Step 1 — Read the Requirements

Check the current instructions before testing.

The requirements used in this practical are:

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

Therefore:

```text
18 ≤ age ≤ 80
```

Decimal ages are outside this core model. If their treatment is unspecified, record a requirement question.

### 7.2 Step 2 — Establish a Valid Baseline

Enter:

| Field | Baseline value |
|---|---|
| First name | `Alex` |
| Surname | `TestingStudent` |
| Age | `30` |
| Country | Select an available country |
| Notes | `Manual testing classroom exercise` |

Submit the form.

Expected result:

```text
The baseline data is accepted and the form submits successfully.
```

If not:

1. Recheck every value.
2. Read the current instructions.
3. Record any discrepancy.
4. Consult your Tutor before continuing.

> [!IMPORTANT]
> Keep all other fields valid while testing age.
>
> Otherwise, a rejection caused by another field could be mistaken for an age-validation result.

### 7.3 Step 3 — Identify the Partitions

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

The purpose is to sample each group rather than choose several values from only one group.

### 7.4 Step 4 — Execute the Tests

For each representative:

1. Restore the form.
2. Enter the valid baseline.
3. Change only age to the selected value.
4. Write the expected result.
5. Submit.
6. Observe whether submission succeeds or validation rejects the age.
7. Where displayed, verify the submitted age.
8. Record the actual result and status.

| ID | Type | Age | Expected result | Actual result | Status |
|---|---|---:|---|---|---|
| AGE-EP-P01 | Positive | 30 | Accept | | Not run |
| AGE-EP-N01 | Negative | 10 | Reject | | Not run |
| AGE-EP-N02 | Negative | 90 | Reject | | Not run |

Here:

- Accept means the form successfully submits with the intended age.
- Reject means successful submission is prevented or a validation error is returned for that age.

### 7.5 Step 5 — Observe Input-Format Handling

Try these separately:

| Input | Observation to record |
|---|---|
| Empty age | Is input required? What feedback appears? |
| `abc` | Can it be entered? Is it prevented, cleared, or rejected? |

These are separate observations, not additional numeric ranges.

If the browser prevents `abc` from being entered, record that prevention. Do not report that the server rejected data that was never submitted.

If the expected behaviour is unclear, document a requirement question rather than inventing a rule.

### Discussion Checkpoint

Why would testing only `25`, `40`, and `60` leave important partitions untested?

### Git Checkpoint — Equivalence Partitioning

Save your partitions, results, and input-format observations. Review, commit, push, and verify.

Suggested message:

```text
Record equivalence partitioning tests
```

***

## 8. Activity 3 — 2-Point Boundary Testing

Time: 20 minutes

### 8.1 Step 1 — Locate the Transitions

The accepted range is:

```text
18 to 80 inclusive
```

The transitions are:

```text
17 → 18     Invalid → Valid
80 → 81     Valid → Invalid
```

### 8.2 Step 2 — Select Adjacent Values

For 2-point testing, select adjacent values on opposite sides of each transition:

```text
Lower transition: 17, 18
Upper transition: 80, 81
```

### 8.3 Step 3 — Classify and Execute

| ID | Type | Age | Position | Expected result |
|---|---|---:|---|---|
| AGE-2P-N01 | Negative | 17 | Immediately below minimum | Reject |
| AGE-2P-P01 | Positive | 18 | Minimum accepted value | Accept |
| AGE-2P-P02 | Positive | 80 | Maximum accepted value | Accept |
| AGE-2P-N02 | Negative | 81 | Immediately above maximum | Reject |

For each case:

1. Restore the form.
2. Enter the valid baseline.
3. Change only age.
4. Confirm the expected result before submitting.
5. Submit.
6. Observe the actual behaviour.
7. Record feedback and evidence where relevant.
8. Assign a status.

| ID | Actual result | Status | Evidence |
|---|---|---|---|
| AGE-2P-N01 | | Not run | |
| AGE-2P-P01 | | Not run | |
| AGE-2P-P02 | | Not run | |
| AGE-2P-N02 | | Not run | |

### 8.4 Step 4 — Interpret the Results

Consider this hypothetical implementation mistake:

```text
Incorrect:
age > 18

Required:
age >= 18
```

Testing `30` would not reveal the difference. Testing `18` would.

| Observation | Interpretation |
|---|---|
| Age 17 is rejected | Negative test passes |
| Age 18 is accepted | Positive test passes |
| Age 18 is rejected | Positive test fails |
| Age 81 is accepted | Negative test fails |

### Discussion Checkpoint

Explain why testing only `18` and `80` does not complete this 2-point boundary set.

### Git Checkpoint — 2-Point Boundary Testing

Save the four results. Review, commit, push, and verify.

Suggested message:

```text
Record 2-point boundary test results
```

***

## 9. Activity 4 — 3-Point Boundary Testing

Time: 25 minutes

### 9.1 Step 1 — Understand the Convention

This practical uses the ISTQB CTFL v4.0 interpretation of 3-value boundary value analysis.

For every identified boundary value, test:

```text
One below → Boundary value → One above
```

This includes boundary values belonging to adjacent invalid partitions.

### 9.2 Step 2 — Identify Boundary Values

| Partition | Boundary value or values |
|---|---|
| Below 18 | 17 |
| 18–80 inclusive | 18 and 80 |
| Above 80 | 81 |

The identified boundary values are:

```text
17, 18, 80, 81
```

### 9.3 Step 3 — Add Immediate Neighbours

| Boundary value | One below | Boundary | One above |
|---:|---:|---:|---:|
| 17 | 16 | 17 | 18 |
| 18 | 17 | 18 | 19 |
| 80 | 79 | 80 | 81 |
| 81 | 80 | 81 | 82 |

### 9.4 Step 4 — Remove Duplicates

The unique values are:

```text
16, 17, 18, 19, 79, 80, 81, 82
```

> [!NOTE]
> Some introductory materials use a simplified convention that tests only around the valid minimum and maximum:
>
> ```text
> 17, 18, 19, 79, 80, 81
> ```
>
> This practical uses the convention described above, producing eight unique values. State the convention clearly rather than mixing the two approaches.

### 9.5 Step 5 — Execute and Record

| ID | Age | Type | Expected result | Actual result | Status |
|---|---:|---|---|---|---|
| AGE-3P-N01 | 16 | Negative | Reject | | Not run |
| AGE-3P-N02 | 17 | Negative | Reject | | Not run |
| AGE-3P-P01 | 18 | Positive | Accept | | Not run |
| AGE-3P-P02 | 19 | Positive | Accept | | Not run |
| AGE-3P-P03 | 79 | Positive | Accept | | Not run |
| AGE-3P-P04 | 80 | Positive | Accept | | Not run |
| AGE-3P-N03 | 81 | Negative | Reject | | Not run |
| AGE-3P-N04 | 82 | Negative | Reject | | Not run |

Use the same execution procedure as Activity 3.

You may reference existing results for `17`, `18`, `80`, and `81` if the environment, baseline, and procedure are unchanged. Identify the original test IDs in your record.

Execute these additional values:

```text
16, 19, 79, 82
```

### 9.6 Step 6 — Compare the Techniques

| Technique | Positive values | Negative values |
|---|---|---|
| Equivalence partitioning | 30 | 10, 90 |
| 2-point boundary testing | 18, 80 | 17, 81 |
| 3-point boundary testing | 18, 19, 79, 80 | 16, 17, 81, 82 |

### Discussion Checkpoint

Explain:

1. Why `18` is a positive boundary test.
2. Why `17` is a negative boundary test.
3. Which additional values the 3-point set introduces.
4. Why these tests do not prove that every possible input works correctly.

### Git Checkpoint — 3-Point Boundary Testing

Save your results and identify any reused evidence. Review, commit, push, and verify.

Suggested message:

```text
Record 3-point boundary test results
```

***

## 10. Activity 5 — Document and Reproduce a Finding

Time: 25 minutes

### 10.1 Step 1 — Select a Finding

Choose one:

- A mismatch between a requirement and actual behaviour.
- An unclear requirement.
- A usability observation.
- A passed positive or negative test.

Do not invent a defect if every test passes.

### 10.2 Step 2 — Complete `findings.md`

```markdown
# Findings Report

## Finding ID
FINDING-01

## Title
A short, specific description.

## Classification
Potential defect / Requirement question /
Usability observation / Passed test

## Related Test ID

## Test Type
Positive / Negative / Recovery

## Requirement
State the rule being checked.

## Environment
- Browser:
- Operating system:
- Date and time:
- Website URL:

## Preconditions
State the starting page and valid baseline data.

## Steps to Reproduce
1.
2.
3.

## Expected Result

## Actual Result

## Evidence
Add a relative link to relevant evidence, if available.

## Reproduction
Observed on __ out of __ attempts.

## Impact
Explain why the finding matters.

## Peer Reproduction
- Outcome:
- Missing or unclear details:
- Changes made after feedback:
```

### 10.3 Step 3 — Review This Hypothetical Example

This example illustrates report structure. It is not a claim that the website contains this defect.

```text
Title:
Age 81 is accepted despite a maximum age of 80

Classification:
Potential defect

Test type:
Negative

Preconditions:
The form is open.
All other fields contain valid baseline values.

Steps:
1. Enter Alex as the first name.
2. Enter TestingStudent as the surname.
3. Enter 81 as the age.
4. Select an available country.
5. Enter Manual testing classroom exercise in Notes.
6. Submit the form.

Expected:
Age 81 is rejected because it exceeds the maximum.

Actual:
[Insert only what you actually observed.]

Impact:
The form may accept data outside the stated age range.
```

### Git Checkpoint — Initial Finding

Before exchanging reports, commit and push your initial finding.

Suggested message:

```text
Document initial testing finding
```

### 10.4 Step 4 — Exchange Reports

Ask your partner to:

1. Read your report.
2. Follow the steps without verbal guidance.
3. Record whether they observe the same behaviour.
4. Identify missing or ambiguous details.
5. Return the report for revision.

If your finding is a passed test, your partner should reproduce the pass.

### 10.5 Step 5 — Improve the Report

Record the reproduction outcome and make necessary improvements.

Avoid:

```text
The form does not work.
```

Use a specific observation:

```text
After submitting age 18 with the valid baseline data,
the form remains on the input page and displays:
[exact message].
```

If no changes to the steps are needed, still record the peer reproduction outcome.

### Git Checkpoint — Peer Review

Commit and push the peer reproduction outcome and any revisions.

Suggested message:

```text
Record peer reproduction and revise finding
```

Your history should now preserve both the initial report and the follow-up work.

***

## 11. Reflection and Execution Summary

### 11.1 Complete `reflection.md`

Write one or two sentences for each question:

```markdown
# Reflection

## 1. What makes a test positive or negative?

## 2. Why can a negative test pass?

## 3. How did equivalence partitioning help you select test data?

## 4. Why did you keep other fields valid when testing age?

## 5. What additional values did 3-point boundary testing introduce?

## 6. What did your partner need clarified to reproduce your finding?

## 7. How does your Git history show the progress of your testing work?
```

### 11.2 Summarise Your Tests

Add a summary to `test-results.md`:

| Status | Number of distinct test cases |
|---|---:|
| Pass | |
| Fail | |
| Blocked | |
| Not run | |
| Total | |

Do not count reused evidence as an additional execution. Identify reruns separately if you performed them.

### Git Checkpoint — Completion

Save your reflection and summary. Review, commit, push, and verify.

Suggested message:

```text
Add testing reflection and execution summary
```

***

## 12. Final Completion Checklist

### Testing Records

- [ ] Test environment details are recorded.
- [ ] Expected results were written before execution.
- [ ] One positive login test is complete.
- [ ] Three negative login tests are complete.
- [ ] One recovery scenario is complete.
- [ ] Three numeric equivalence partitions are identified.
- [ ] Equivalence test results are recorded.
- [ ] Four 2-point boundary results are recorded.
- [ ] Eight 3-point results are recorded or linked to reused evidence.
- [ ] Blank and non-numeric observations are recorded.
- [ ] A findings report is complete.
- [ ] Peer reproduction feedback is recorded.
- [ ] Reflection answers are complete.
- [ ] Evidence links work.
- [ ] Screenshots contain no sensitive information.

### Git and GitHub

- [ ] I used the repository and branch specified by my Tutor.
- [ ] My practical files are stored inside `manual-testing/`.
- [ ] I recorded progress throughout the session.
- [ ] My commit messages describe actual changes.
- [ ] My initial finding was committed before peer review.
- [ ] Peer feedback and revisions appear in a later commit.
- [ ] My reflection and execution summary are committed.
- [ ] My latest commits are pushed to GitHub.
- [ ] I verified the files on the correct GitHub branch.
- [ ] No intended practical work remains uncommitted.

### Final Git Check

Run:

```bash
git status
git log --oneline -10
```

Then verify your latest commit on GitHub.

> [!TIP]
> Capture genuine progress. Do not create empty commits or split finished work artificially just to increase the commit count.
>
> Your history should help another person understand what you completed and what you improved.

***

## 13. Troubleshooting

| Situation | What to do |
|---|---|
| Website is unavailable | Record the time and mark affected tests Blocked. Continue designing cases without claiming execution. |
| Website differs from this practical | Read the current instructions and consult your Tutor. |
| Every age test is rejected | Recheck the valid baseline, especially surname length and country selection. |
| Browser prevents an input | Record the prevention as the actual behaviour. |
| No result page appears | Check for validation feedback before assuming success. |
| Expected behaviour is unclear | Record a requirement question rather than inventing a rule. |
| No defects are found | Document a passed test or requirement question. |
| Partner gets a different result | Compare starting state, input data, browser, and exact steps. |
| Screenshot link does not work | Check the relative path, filename, and letter case. |
| Git says there is nothing to commit | Check that your files were saved and that you are in the correct repository. |
| Commit exists locally but not on GitHub | Push and check the correct remote branch. |
| Push is rejected | Read the message and consult your Tutor if needed. Do not force push. |

***

## 14. Optional Extensions — Outside the In-Class Practical

These activities are not required during the 2.5-hour session. Attempt them in your own time if you have the bandwidth.

Capture any extension work using Git as well.

### 14.1 First-Name Length Testing

Using the requirement that the first name is required and contains fewer than 90 characters:

1. Identify valid and invalid length partitions.
2. Select positive and negative representative tests.
3. Derive the 2-point boundary values.
4. Derive the 3-point values using this practical’s convention.
5. Keep every other field valid.
6. Explain why negative text lengths are outside the input domain.

### 14.2 Surname Length Testing

Using the stated surname range of 11–79 characters:

1. Select a typical valid length.
2. Select a below-range invalid length.
3. Select an above-range invalid length.
4. Prepare a complete 2-point boundary set.
5. Prepare a complete 3-point boundary set.
6. Verify character counts before execution.

### 14.3 Requirement Questions

Investigate whether the current requirements clarify:

- Decimal ages.
- Spaces around an age.
- First names containing only spaces.

If behaviour is unspecified, document a question rather than assigning an unsupported Pass or Fail.

***

## 15. Final Testing Habit

The goal is not simply to make an error message appear. It is to determine whether the application behaves correctly for valid and invalid inputs, then preserve clear evidence of your work.

```text
Read → Design → Execute → Observe → Record
     → Review changes → Commit → Push → Verify
```
