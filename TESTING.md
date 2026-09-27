# System Testing & Verification Guide (دليل الفحص والتحقق)

> Authority: Global CTO Governance Directive (Rule 6)  
> Scope: Quality Assurance, Ledger Verification & CI/CD Testing  

---

## 1. Quick Verification Command
To run the automated verification test suite locally:
```bash
python AI/test_suite.py
```

Expected output:
```text
ALL TESTS PASSED WITH 100% SUCCESS
```

---

## 2. Test Coverage & Verification Gates

### A. Ledger Mathematical Integrity
- Formula: `Net Balance = (Base Capital + Total Deposits) - Total Withdrawals - Education Reserve + Net Trading PnL`
- Loss-compensation deposits ($311.00) are classified as deposits (+), not withdrawals.
- Total net balance must equal `-$1,215.00` with 100% precision.

### B. Empirical Trading Week Reconciliation
- Reconciles all 19 September trading days into four 5-day market weeks:
  - Week 1 (`01 - 05 Sep`): `-$212.00`
  - Week 2 (`07 - 11 Sep`): `-$119.00`
  - Week 3 (`14 - 18 Sep`): `-$78.68`
  - Week 4 (`21 - 25 Sep`): `-$56.80`

### C. UI & Attribution Cleanliness
- Confirms zero developer attribution in `index.html` or visible UI elements (Rule 1).
- Confirms presence of all 23 core interactive element IDs.

### D. File Governance & Quarantine Security
- Verifies `.gitignore` protects the `/AI/` quarantine zone from remote exposure.
- Verifies existence of `developer.md` (Rule 7) and `AI/project-map.md` (Rule 5).

---

## 3. Detailed Audit Logs
For detailed test outputs and metric breakdowns, refer to:
[test-results.md](file:///c:/Users/Admin/Desktop/Gold%20Tracker/AI/test-results.md)
