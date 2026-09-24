# Topic 4 — Test Observations

## Testing Objective

The purpose of this testing is to verify that the AI Job Application Assistant correctly handles incomplete and ambiguous user inputs, asks relevant clarification questions, and avoids unnecessary questioning when information is sufficient.

---

## Test Case 1 — Incomplete Input

### User Input
"Help me with my application."

### Expected Behavior
The GPT should recognize that the request is incomplete because the user has not identified the job role or application. It should ask a targeted clarification question instead of making assumptions.

### Actual Observation
The GPT asked which job role or application the user was referring to. It also asked for the job description and resume if available, and explained the types of application support it could provide.

### Result
PASS

---

## Test Case 2 — Incomplete Resume Tailoring Request

### User Input
"Improve my resume for this job."

### Expected Behavior
The GPT should request the job description and current resume because both are required to tailor the resume accurately. It should not assume which job the user means.

### Actual Observation
The GPT asked the user to provide both the job description and current resume. It explained that it would tailor the resume while keeping all claims truthful.

### Result
PASS

---

## Test Case 3 — Incomplete Job Analysis Request

### User Input
"Analyze this job for me."

### Expected Behavior
The GPT should recognize that the job description has not been provided. It should ask the user to paste or upload the job description instead of pretending to analyze an unknown job.

### Actual Observation
The GPT asked the user to paste or upload the job description. It also explained the areas it would analyze and stated that it would not make assumptions about the user's background.

### Result
PASS

---

## Test Case 4 — Missing Required Inputs

### User Input
"Analyze this job description and compare its requirements with my resume."

### Expected Behavior
The GPT should understand the requested task but recognize that the actual job description and resume are not available. It should ask the user to provide both items before performing the comparison.

### Actual Observation
The GPT correctly requested both the job description and resume. It explained that the comparison would include requirements, resume evidence, matches, partial matches, missing areas, keywords, resume improvements, and an application checklist. It also confirmed that it would only use information present in the resume and would not invent qualifications or experience.

### Result
PASS

---

## Overall Testing Summary

| Test | Scenario | Result |
|---|---|---|
| 1 | Incomplete application request | PASS |
| 2 | Resume tailoring without required inputs | PASS |
| 3 | Job analysis without job description | PASS |
| 4 | Job/resume comparison without the required files | PASS |

## Final Observation
All four tests passed.

The GPT correctly identified missing information and asked targeted clarification questions instead of making unsupported assumptions.

The tests also confirmed that the GPT follows the no-fabrication rule and avoids proceeding with job-specific recommendations when required information is unavailable.

The conversation flow therefore supports incomplete and ambiguous inputs while keeping the interaction focused and user-friendly.
