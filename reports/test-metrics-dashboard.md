# Test Metrics Dashboard

## 1. Purpose
This dashboard provides a centralized view of key quality metrics across recent development cycles, helping stakeholders evaluate release readiness, automation progress, and overall product stability.

## 2. Pass Rate
Tracks the testing execution success rate over recent sprint cycles to monitor stability trends.

| Sprint | Passed | Failed | Blocked | Pass Rate |
|---|---:|---:|---:|---:|
| Sprint 1 | 92 | 6 | 2 | 92% |
| Sprint 2 | 96 | 3 | 1 | 96% |

## 3. Automation Coverage
Measures the percentage of test cases that have been successfully converted from manual execution to automated scripts.

| Area | Manual Tests | Automated Tests | Coverage |
|---|---:|---:|---:|
| API | 120 | 95 | 79% |
| UI | 80 | 40 | 50% |
| Regression | 150 | 100 | 67% |

## 4. Escaped Defects
Tracks defects found in production by end-users after a release, which helps measure the effectiveness of our QA regression safety net.

| Release | Critical | High | Medium | Low |
|---|---:|---:|---:|---:|
| v1.0 | 0 | 1 | 3 | 5 |
| v1.1 | 0 | 0 | 2 | 4 |

## 5. Bug Severity
Distribution of active bugs currently found during the active testing cycle.

| Blocked | Critical | Major | Minor | Total Active |
|---|---|---|---|---|
| 1 | 3 | 8 | 14 | 26 |

## 6. Test Execution
A snapshot of testing progress for the current, active cycle.

* **Total Planned Tests:** 350
* **Executed:** 280 (80%)
* **Remaining:** 70 (20%)

## 7. Requirements Coverage
Ensures every documented business requirement maps to at least one validation test case.

| Component | Total Requirements | Covered by Tests | Coverage % |
|---|---|---|---|
| User Auth | 12 | 12 | 100% |
| Checkout | 25 | 24 | 96% |
| Profile Mgmt | 10 | 8 | 80% |

## 8. Summary
* **Quality Trend:** Testing stability increased significantly in Sprint 2 with a 96% pass rate.
* **Focus Area:** UI automation remains our bottleneck at 50% coverage; next sprint will prioritize converting the core checkout path to automated UI scripts.