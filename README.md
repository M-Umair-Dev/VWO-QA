# VWO Application (Login & Dashboard) — QA Test Documentation

Welcome to the official QA test repository for the **VWO Web Application (`app.vwo.com`)**. This repository showcases structured manual and performance testing artifacts governed under professional Software Testing Life Cycle (STLC) standards[cite: 5].

---

## 📂 Repository File Directory

* **`README.md`**: Central repository overview outlining project scope, test execution metrics, bug summaries, and QA triage workflows.
* **`VWO_Master_Test_Plan_Complete.docx`**: Master Test Plan structured from a QA Team Lead perspective. It includes a detailed multi-level Table of Contents, scope boundaries (Login and Dashboard modules), black-box test design techniques, environment matrices, execution schedules, and STLC gate criteria.
* **`Test cases -App-VWO.xlsx`**: Master test execution workbook containing 48 total test cases across three primary sheets:
  * **Login Page (`TS1` - 19 cases):** Validates authentication, password masking, SSO integration, CAPTCHA triggers, keyboard navigation, HTTPS security, responsive UI, and JMeter performance testing.
  * **Dashboard (`TS2` - 29 cases):** Validates page loading, widget data rendering, active navigation states, browser history consistency, campaign search, sorting, and filtering.
  * **Bug Report Sheet:** Detailed defect logs mapping failures directly to test case IDs (`TS1-TC8` and `TS1-TC19`).
* **`VWO_Test_Metrics_Updated.xlsx`**: Quantitative execution analytics tracking test coverage and outcomes (48 test cases written, 48 executed, 46 passed, 2 failed, 95.83% pass rate, and defect distribution across P0 and P1 severities).

---

## 📊 Executive QA Summary & Highlights

| Metric Category | Count / Performance KPI |
| :--- | :--- |
| **Total Test Coverage** | **48 Test Cases** across Login (`TS1`) & Dashboard (`TS2`)|
| **Execution Rate** | **100.00%** (48 / 48 Executed) |
| **Pass Rate** | **95.83%** (46 Passed) |
| **Defect Density Rate** | **4.17%** (2 Failed / Logged Bugs) |
| **Test Environment** | Windows 11, macOS, Android, (Chrome, Firefox, Edge) |

---

## 🐞 Logged Defects & Triage Summary

| Bug ID / Ref | Title & Description | Severity / Priority |
| :--- | :--- | :--- |
| **TS1-TC8** | **UI/UX Responsiveness Defect:** Right-side banner text and section overflow/cutoff on small mobile viewports. | **P0 (Critical / Blocker)** |
| **TS1-TC19** | **Web Server Load Testing Defect:** Apache JMeter concurrency test showed that at 21+ concurrent threads, server response time peaked at **3,362ms** (breaching the <3,000ms threshold). | **P1 (High / Performance)** |

---

## 🧪 Test Strategy & Black-Box Design Techniques
The test suite was designed and executed utilizing industry-standard testing methodologies:
* **Equivalence Partitioning:** Partitioning valid and invalid credential inputs (numeric-only emails, blank fields, and spaces).
* **Boundary Value Analysis:** Testing length limits (>255 characters) and thread concurrency thresholds.
* **Decision Table Testing:** Evaluating multi-condition authentication outcomes and CAPTCHA triggers after 3 invalid attempts.
* **State Transition Testing:** Validating unauthorized URL manipulation (`accountId` tampering).
* **Performance Testing:** Apache JMeter thread group configuration for server concurrency and response time monitoring.

---

## 🚀 Execution Timeline & STLC Milestones

| Project Milestone | Target Execution Date | Status |
| :--- | :---: | :---: |
| **Test Plan Creation & Strategy Sign-off** | 07/09/2026 | ✅ Completed |
| **Test Case Authoring (Login & Dashboard)** | 09/09/2026 | ✅ Completed |
| **Test Execution & Defect Logging** | 09/09/2026 | ✅ Completed |
| **Test Summary & Metrics Submission** | 11/09/2026 | ✅ Completed |

---

## 👤 Author & QA Leadership
* **Prepared By:** Muhammad Umair
* **Target Environment:** `app.vwo.com` (Staging / QA)
