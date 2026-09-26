# Useful Bug Reports for Scoutly Issues

When reporting an issue with Scoutly, providing a [minimal, reproducible example](https://stackoverflow.com/help/minimal-reproducible-example) enables the team to isolate the root cause and release fixes significantly faster.

Here is how you can write high-quality, actionable bug reports for different components of Scoutly:

---

## 1. Web Application & Dashboard Issues

If an issue occurs while using the Scoutly web platform (e.g. applications table, resume tailor, settings, document viewer):

- **Page URL & Route:** Note the exact page route (e.g. `/tailor/abc-123` or `/settings`).
- **Browser & OS:** State your browser name and version (e.g. Chrome 133, Safari 18, Arc) and operating system.
- **Console Errors:** Open browser DevTools (`Cmd + Option + I` or `F12`), switch to the **Console** tab, and copy any red error traces.

---

## 2. Chrome Extension & Autofill Issues

When reporting an issue with the Scoutly Chrome Extension on job boards:

- **Target Job Board / ATS:** Mention the specific ATS (e.g. Greenhouse, Lever, Workday, Ashby, LinkedIn, Internshala, Unstop).
- **Job Posting URL:** Provide the public job listing URL where autofill or logging failed.
- **Specific Field Failures:** Note which fields failed to autofill (e.g. "Work Experience dates were left blank" or "Resume upload button was not triggered").
- **Extension Version:** Provide the extension version installed in your browser.

---

## 3. Resume Tailoring & ATS Scoring Issues

For issues related to AI resume tailoring or ATS keyword match evaluation:

- **Job Description Snippet:** Provide the relevant requirements text from the job description.
- **Expected vs Actual Output:** Explain what content was expected (e.g. "Expected STAR bullet points reflecting Docker experience") versus what was generated.
- **Redaction:** Always redact personal phone numbers, physical addresses, or confidential employer information before sharing.

---

## 4. Inspecting Network Logs

If an API call fails or displays an error banner:

1. Open **DevTools** (`F12`) and select the **Network** tab.
2. Reproduce the action (e.g. click "Save", "Generate", or "Autofill").
3. Find the failed request highlighted in red.
4. Click on it, view the **Response** tab, and copy the RFC 7807 Problem Details JSON payload (e.g. `{"type": "...", "title": "...", "detail": "..."}`).

---

## 5. Security & Sensitive Data

> [!CAUTION]
> **Never include passwords, session cookies, Bearer tokens, or confidential company secrets in public GitHub issues.**
>
> If you discover a vulnerability or security bypass, report it privately via email to **[security@scoutly.in](mailto:security@scoutly.in)**.
