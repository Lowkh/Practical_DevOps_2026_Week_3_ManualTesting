# Manual Testing Practical

> A guided, hands-on introduction to positive testing, negative testing, equivalence partitioning, and boundary value analysis.

This practical helps you learn manual testing by using existing demonstration websites. You will prepare test cases, interact with the websites, compare expected and actual results, and document your findings.

The focus is on understanding how to select meaningful tests and record evidence—not on writing code or automating tests.

| Item | Details |
|---|---|
| Duration | 2.5 hours |
| Mode | Individual testing with paired discussion |
| Prerequisites | Basic web browsing and document editing |
| Tools | Web browser, text editor or spreadsheet, screenshot tool |
| Websites | SauceDemo and Test Pages |
| Output | Completed test records, a findings report, and a reflection |

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

> [!IMPORTANT]
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

## 2. Practical Schedule

| Activity | Duration |
|---|---:|
| Preparation and key concepts | 15 minutes |
| Activity 1: Positive and negative login testing | 25 minutes |
| Activity 2: Equivalence partitioning | 25 minutes |
| Activity 3: 2-point boundary testing | 20 minutes |
| Activity 4: 3-point boundary testing | 25 minutes |
| Activity 5: Findings and peer reproduction | 25 minutes |
| Review and reflection | 15 minutes |
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

Manual testing means that you perform the test steps yourself rather than running an automated test script.

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

### 4.4 Positive and Negative Do Not Mean Pass and Fail

The test type describes the input or scenario. The test status describes whether the actual behaviour matches the expected behaviour.

| Test type | Input | Expected behaviour | Actual behaviour | Status |
|---|---|---|---|---|
| Positive | Valid credentials | Allow login | Login allowed | Pass |
| Positive | Valid credentials | Allow login | Login rejected | Fail |
| Negative | Incorrect password | Reject login | Login rejected | Pass |
| Negative | Incorrect password | Reject login | Login allowed | Fail |

> [!TIP]
> A negative test passes when the application handles the invalid input correctly.
>
> An error message is not automatically evidence of a failed test.

### 4.5 Equivalence Partitioning and Boundary Testing

| Technique | What it helps you do |
|---|---|
| Equivalence partitioning | Divide inputs into groups expected to receive similar treatment |
| 2-point boundary testing | Test adjacent values on opposite sides of a boundary transition |
| 3-point boundary testing | Test identified boundary values and their immediate neighbours |

These techniques help you choose test data. Each selected case can then be classified as positive or negative.

***

## 5. Prepare Your Working Files

### 5.1 Create a Folder

In your local working directory or practical repository, create this structure:

```text
manual-testing/
├── test-results.md
├── findings.md
├── reflection.md
└── evidence/
```

| File or folder | Purpose |
|---|---|
| `test-results.md` | Environment details, test cases, and results |
| `findings.md` | One reproducible finding |
| `reflection.md` | Your answers to the reflection questions |
| `evidence/` | Relevant screenshots |

Git does not track empty folders. The `evidence/` folder will appear in the repository after you add a screenshot or another file.

### 5.2 Record Your Test Environment

Add the following to `test-results.md`:

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
```

Use a fictional or class-assigned identifier if the repository is public.

### 5.3 Use a Consistent Results Table

```markdown
| Test ID | Type | Test data | Expected result | Actual result | Status | Evidence |
|---|---|---|---|---|---|---|
| | Positive / Negative | | | | Not run | |
```

Use these statuses:

| Status | Meaning |
|---|---|
| Pass | Actual behaviour matches the expected result |
| Fail | Actual behaviour differs from the expected result |
| Blocked | Another issue prevents you from completing the test |
| Not run | You have not executed the test |

### 5.4 Add Screenshot Evidence

Save screenshots using descriptive names:

```text
evidence/login-p01.png
evidence/login-n01.png
evidence/age-18.png
```

From `test-results.md`, link to a screenshot using a relative path:

```markdown
[View screenshot](evidence/login-n01.png)
```

Do not capture unrelated browser tabs, personal account details, or other sensitive information.

***

## 6. Activity 1 — Positive and Negative Login Testing

Time: 25 minutes

Open [SauceDemo](https://www.saucedemo.com/).

Use these demonstration credentials:

```text
Username: standard_user
Password: secret_sauce
```

For this activity, use these acceptance criteria:

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

#### Step 1 — Prepare the Page

1. Open SauceDemo.
2. If you are already logged in, use the website’s logout option.
3. Confirm that the username and password fields are visible.
4. Clear both fields.

Why: every test should begin from a known state.

#### Step 2 — Enter Valid Data

Enter:

```text
Username: standard_user
Password: secret_sauce
```

#### Step 3 — Perform the Action

Select `Login`.

#### Step 4 — Check the Result

Expected result:

```text
Login succeeds and the product inventory page appears.
```

Check that products are visible. Do not assume login succeeded simply because the page changed.

#### Step 5 — Record the Result

Record:

- The page reached.
- Whether products are visible.
- Any unexpected message.
- The test status.
- Relevant screenshot evidence.

| ID | Type | Expected result | Actual result | Status |
|---|---|---|---|---|
| LOGIN-P01 | Positive | Product inventory appears | | Not run |

### 6.2 Test LOGIN-N01 — Incorrect Password

| Item | Details |
|---|---|
| Type | Negative |
| Purpose | Check that an incorrect password is rejected |
| Starting state | Logged-out login page |

#### Step 1 — Reset the Page

1. Log out if necessary.
2. Return to the login page.
3. Clear both fields.

#### Step 2 — Enter the Test Data

```text
Username: standard_user
Password: wrong_password
```

Keep the username valid. Change only the password.

Why: changing one input helps isolate the condition being tested.

#### Step 3 — Select Login

Observe the page and any error feedback.

#### Step 4 — Compare the Result

Expected result:

```text
Login is rejected.
The inventory page is not reached.
Error feedback is displayed.
```

#### Step 5 — Record the Result

Copy the error message accurately.

If the application rejects the incorrect password as expected, mark the test Pass.

| ID | Type | Expected result | Actual result | Status |
|---|---|---|---|---|
| LOGIN-N01 | Negative | Login rejected with feedback | | Not run |

### 6.3 Test LOGIN-N02 — Missing Password

1. Return to the logged-out login page.
2. Clear both fields.
3. Enter `standard_user` as the username.
4. Leave the password empty.
5. Select `Login`.
6. Observe the feedback.
7. Confirm that the inventory page is not reached.
8. Record the actual result and status.

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
7. Confirm that the inventory page is not reached.
8. Record the actual result and status.

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

Expected result:

```text
After correcting the credentials, the user can log in successfully.
```

### 6.6 Complete Your Login Test Record

| ID | Type | Scenario | Expected result | Actual result | Status |
|---|---|---|---|---|---|
| LOGIN-P01 | Positive | Valid credentials | Allow login | | Not run |
| LOGIN-N01 | Negative | Incorrect password | Reject login | | Not run |
| LOGIN-N02 | Negative | Missing password | Reject login | | Not run |
| LOGIN-N03 | Negative | Missing username | Reject login | | Not run |
| LOGIN-R01 | Recovery | Correct invalid credentials | Reject first attempt; accept corrected attempt | | Not run |

### Checkpoint

Discuss with your partner:

1. Why can a negative test pass?
2. Why did you change only one credential in each negative test?
3. What did the recovery scenario check that the other tests did not?

***

## 7. Activity 2 — Equivalence Partitioning

Time: 25 minutes

Open:

- [Test Pages validation form](https://testpages.eviltester.com/apps/client-server-form-validation/)
- [Validation instructions](https://testpages.eviltester.com/apps/client-server-form-validation/client-server-form-validation-instructions/)

### 7.1 Step 1 — Read the Requirements

Check the current website instructions before testing.

The requirements used in this practical include:

| Field | Requirement |
|---|---|
| First name | Required and fewer than 90 characters |
| Surname | Between 11 and 79 characters |
| Age | Between 18 and 80 |
| Country | Selected from the available list |
| Notes | No more than 2,000 characters |

For the core age exercises, use this classroom test model:

```text
Age is a whole number from 18 to 80 inclusive.
```

Therefore:

```text
18 ≤ age ≤ 80
```

Decimal ages are outside the core exercise. If their treatment is not specified, record a requirement question.

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
The form accepts the baseline data and submits successfully.
```

If it does not:

1. Recheck every value.
2. Read the current validation instructions.
3. Record any discrepancy.
4. Consult your Tutor before continuing.

> [!IMPORTANT]
> Keep every other field valid when testing age.
>
> Otherwise, a rejection caused by another field could be mistaken for an age-validation result.

### 7.3 Step 3 — Identify the Partitions

Divide whole-number ages into three groups:

| Partition | Input group | Representative | Type | Expected result |
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

Why: values within each group are expected to receive similar acceptance or rejection treatment.

### 7.4 Step 4 — Execute the Positive Test

Test ID: `AGE-EP-P01`

1. Restore the form.
2. Enter the valid baseline.
3. Set age to `30`.
4. Submit.
5. Check whether submission succeeds.
6. Where displayed, confirm that the submitted age is `30`.
7. Record the actual result and status.

Expected result:

```text
Age 30 is accepted.
```

### 7.5 Step 5 — Execute the Lower Invalid Test

Test ID: `AGE-EP-N01`

1. Restore the form.
2. Enter the valid baseline.
3. Change only age to `10`.
4. Submit.
5. Observe any validation feedback.
6. Confirm that age 10 is not successfully accepted.
7. Record the actual result and status.

Expected result:

```text
Age 10 is rejected because it is below the minimum.
```

### 7.6 Step 6 — Execute the Upper Invalid Test

Test ID: `AGE-EP-N02`

Repeat the same procedure using age `90`.

Expected result:

```text
Age 90 is rejected because it exceeds the maximum.
```

### 7.7 Step 7 — Complete Your Results

| ID | Type | Age | Expected result | Actual result | Status |
|---|---|---:|---|---|---|
| AGE-EP-P01 | Positive | 30 | Accept | | Not run |
| AGE-EP-N01 | Negative | 10 | Reject | | Not run |
| AGE-EP-N02 | Negative | 90 | Reject | | Not run |

### 7.8 Step 8 — Observe Input-Format Handling

Try these inputs separately:

| Input | What to observe |
|---|---|
| Empty age | Is the field required? What feedback appears? |
| `abc` | Can it be entered? Is it prevented, cleared, or rejected? |

Record observations separately from the numeric partitions.

If the browser prevents `abc` from being entered, record that prevention. Do not claim that the server rejected data that was never submitted.

Where the required behaviour is unclear, record a requirement question rather than inventing an expected result.

### Checkpoint

Explain why selecting only `25`, `40`, and `60` would leave important partitions untested.

***

## 8. Activity 3 — 2-Point Boundary Testing

Time: 20 minutes

### 8.1 Step 1 — Locate the Boundary Transitions

The accepted range is:

```text
18 to 80 inclusive
```

The transitions are:

```text
17 → 18     Invalid → Valid
80 → 81     Valid → Invalid
```

### 8.2 Step 2 — Select Two Values per Transition

Choose the adjacent values on opposite sides of each transition:

```text
Lower transition: 17, 18
Upper transition: 80, 81
```

### 8.3 Step 3 — Classify Each Test

| Age | Position | Type | Expected result |
|---:|---|---|---|
| 17 | Immediately below the minimum | Negative | Reject |
| 18 | Minimum accepted value | Positive | Accept |
| 80 | Maximum accepted value | Positive | Accept |
| 81 | Immediately above the maximum | Negative | Reject |

Boundary testing includes both positive and negative cases.

### 8.4 Step 4 — Execute the Tests

For each value:

1. Restore the form.
2. Enter the valid baseline.
3. Change only age.
4. Write the expected result before submitting.
5. Submit the form.
6. Observe the actual behaviour.
7. Record relevant feedback.
8. Assign a status.

| ID | Type | Age | Expected result | Actual result | Status |
|---|---|---:|---|---|---|
| AGE-2P-N01 | Negative | 17 | Reject | | Not run |
| AGE-2P-P01 | Positive | 18 | Accept | | Not run |
| AGE-2P-P02 | Positive | 80 | Accept | | Not run |
| AGE-2P-N02 | Negative | 81 | Reject | | Not run |

### 8.5 Step 5 — Understand What the Tests Can Reveal

Consider this hypothetical implementation mistake:

```text
Incorrect:
age > 18

Required:
age >= 18
```

Age `30` would satisfy both conditions, so it would not reveal this mistake.

Age `18` would reveal the difference.

| Observation | Interpretation |
|---|---|
| Age 17 is rejected | Negative test passes |
| Age 18 is accepted | Positive test passes |
| Age 18 is rejected | Positive test fails |
| Age 81 is accepted | Negative test fails |

### Checkpoint

Explain why testing only `18` and `80` does not complete this 2-point boundary set.

***

## 9. Activity 4 — 3-Point Boundary Testing

Time: 25 minutes

### 9.1 Step 1 — Understand the Convention

This practical uses the ISTQB CTFL v4.0 interpretation of 3-value boundary value analysis.

For each identified boundary value, test:

```text
One below → Boundary value → One above
```

This includes boundary values belonging to the adjacent invalid partitions.

### 9.2 Step 2 — Identify the Boundary Values

| Partition | Boundary value or values |
|---|---|
| Below 18 | 17 |
| 18–80 inclusive | 18 and 80 |
| Above 80 | 81 |

The identified boundary values are:

```text
17, 18, 80, 81
```

### 9.3 Step 3 — Add Their Immediate Neighbours

| Boundary value | One below | Boundary | One above |
|---:|---:|---:|---:|
| 17 | 16 | 17 | 18 |
| 18 | 17 | 18 | 19 |
| 80 | 79 | 80 | 81 |
| 81 | 80 | 81 | 82 |

### 9.4 Step 4 — Remove Duplicates

The unique test values are:

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
> This practical uses the convention described above, producing eight unique values. Do not mix the two conventions without explaining which one you are applying.

### 9.5 Step 5 — Classify and Execute the Tests

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

You may reference existing results for `17`, `18`, `80`, and `81` if the environment, baseline, and procedure are unchanged. Identify the original test IDs.

Execute the additional values:

```text
16, 19, 79, 82
```

### 9.6 Step 6 — Compare the Techniques

| Technique | Positive values | Negative values |
|---|---|---|
| Equivalence partitioning | 30 | 10, 90 |
| 2-point boundary testing | 18, 80 | 17, 81 |
| 3-point boundary testing | 18, 19, 79, 80 | 16, 17, 81, 82 |

### Checkpoint

Explain:

1. Why age `18` is a positive boundary test.
2. Why age `17` is a negative boundary test.
3. What additional values the 3-point set introduces.
4. Why passing these tests does not prove that every possible input works correctly.

***

## 10. Activity 5 — Document and Reproduce a Finding

Time: 25 minutes

### 10.1 Step 1 — Select a Finding

Choose one:

- A mismatch between the requirement and actual behaviour.
- An unclear requirement.
- A usability observation.
- A passed positive or negative test.

You do not need to find a defect to complete this practical.

### 10.2 Step 2 — Complete `findings.md`

Use this template:

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
State the starting page and required baseline data.

## Steps to Reproduce
1.
2.
3.

## Expected Result

## Actual Result

## Evidence
[View screenshot](evidence/example.png)

## Reproduction
Observed on __ out of __ attempts.

## Impact
Explain why the finding matters.
```

Replace the example screenshot path with an actual file, or remove the link if no screenshot was captured.

### 10.3 Step 3 — Review the Example

The following is hypothetical. It is not a claim that the website contains this defect.

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

### 10.4 Step 4 — Exchange Reports

Ask your partner to:

1. Follow your report without verbal guidance.
2. Record whether they observe the same behaviour.
3. Identify missing or ambiguous details.
4. Return the report for revision.

If the finding is a passed test, your partner should reproduce the pass.

### 10.5 Step 5 — Improve the Report

Replace vague statements with specific observations.

Avoid:

```text
The form does not work.
```

Use:

```text
After submitting age 18 with the valid baseline data,
the form remains on the input page and displays:
[exact message].
```

***

## 11. Review Your Test Records

### 11.1 Completion Checklist

- [ ] Environment details are recorded.
- [ ] Expected results were written before execution.
- [ ] One positive login test is complete.
- [ ] Three negative login tests are complete.
- [ ] One recovery scenario is complete.
- [ ] Three numeric equivalence partitions are identified.
- [ ] Equivalence test results are recorded.
- [ ] Four 2-point boundary results are recorded.
- [ ] Eight 3-point boundary results are recorded or linked to reused evidence.
- [ ] Blank and non-numeric input observations are recorded.
- [ ] One findings report is complete.
- [ ] A partner has attempted to reproduce the finding.
- [ ] Reflection answers are complete.
- [ ] Screenshots contain no sensitive information.
- [ ] Relative evidence links work.

### 11.2 Summarise Execution

| Status | Number of distinct executed tests |
|---|---:|
| Pass | |
| Fail | |
| Blocked | |

Record not-run cases separately:

| Status | Number |
|---|---:|
| Not run | |

Do not count reused evidence as a new execution. If a test result appears in two technique tables but was executed once, count one execution.

***

## 12. Reflection

Add your answers to `reflection.md`:

```markdown
# Reflection

## 1. What makes a test positive or negative?

## 2. Why can a negative test pass?

## 3. How did equivalence partitioning help you select test data?

## 4. Why did you keep the other form fields valid when testing age?

## 5. What additional values did 3-point boundary testing introduce?

## 6. What did your partner need clarified to reproduce your finding?
```

Write one or two sentences for each answer.

***

## 13. Troubleshooting

| Situation | What to do |
|---|---|
| Website is unavailable | Record the time and mark affected tests as Blocked. Continue designing cases without claiming execution. |
| Website differs from the practical | Read its current instructions and consult your Tutor. |
| Every age test is rejected | Recheck the valid baseline, especially surname length and country selection. |
| Browser prevents an input | Record the prevention as the actual behaviour. |
| No result page appears | Check for validation feedback before assuming success. |
| Expected behaviour is unclear | Record a requirement question rather than inventing a rule. |
| No defects are found | Document a passed test or requirement question. |
| Partner gets a different result | Compare starting state, data, browser, and exact steps. |
| Screenshot link does not work | Check the relative path, filename, and letter case. |

***

## 14. Optional Extensions — Outside the In-Class Practical

These activities are not required during the 2.5-hour session. Attempt them in your own time if you have the bandwidth.

### 14.1 First-Name Length Testing

Using the requirement that the first name is required and contains fewer than 90 characters:

1. Identify the valid and invalid length partitions.
2. Select positive and negative representative tests.
3. Derive the 2-point boundary values.
4. Derive the 3-point boundary values using this practical’s convention.
5. Keep every other field valid.
6. Explain why negative text lengths are outside the input domain.

### 14.2 Surname Length Testing

Using the stated surname range of 11–79 characters:

1. Select a typical valid length.
2. Select a below-range invalid length.
3. Select an above-range invalid length.
4. Prepare a complete 2-point boundary set.
5. Prepare a complete 3-point boundary set.
6. Verify your character counts before executing.

### 14.3 Requirement Questions

Investigate whether the published requirements clarify:

- Decimal ages.
- Spaces around an age.
- First names containing only spaces.

If the required behaviour is unspecified, document the question rather than assigning an unsupported Pass or Fail.

***

## 15. Final Testing Habit

The goal of **testing** is not simply to make an error message appear. It is to determine whether the application behaves correctly for valid and invalid inputs.

```text
Read → Select data → Predict → Execute
     → Observe → Compare → Record → Review
```
