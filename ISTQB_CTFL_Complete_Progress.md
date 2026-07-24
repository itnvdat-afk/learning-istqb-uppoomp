# ISTQB CTFL v4.0 — Lộ Trình Học Toàn Bộ

**Status:** Đã học Q#1-Q#26/40 (65%)  
**Date:** 2026-07-23  
**Next:** Q#27-Q#40  

---

## 📚 Mục Lục

1. [Tuần 1-3 Learning Overview](#tuần-1-3-learning-overview)
2. [Q#1-Q#26 Quick Reference](#quick-reference-tất-cả-câu-hỏi)
3. [7 Testing Principles (ISTQB)](#7-testing-principles)
4. [Key Concepts & Formulas](#key-concepts--formulas)
5. [Common Exam Traps](#common-exam-traps)
6. [Study Tips & Mnemonics](#study-tips--mnemonics)

---

## 📖 Tuần 1-3 Learning Overview

### **Tuần 1: Fundamentals (Ch.1)**
- Error-Defect-Failure causal chain
- 7 Testing Principles (Presence, Exhaustive, Early, Cluster, Pesticide, Context, Fallacy)
- 5 Test Levels (Component, Integration, System, Acceptance, Alpha/Beta)
- V-Model pairing (Requirements↔Acceptance, Design↔System, etc.)
- QA vs QC distinction
- Test objectives vs test proof

### **Tuần 2: Testing in SDLC (Ch.2) & Static Testing (Ch.3)**
- SDLC Models (Waterfall, Iterative, Incremental, Agile, DevOps)
- Shift-Left approach (test early)
- Test Approach selection (8 types: Analytical, Model-based, Methodical, Process-Compliant, Reactive, Risk-Based, Consultative, Regression-Averse)
- Static Testing (code review, inspection, analysis)
- 4 Review Types: Informal < Walkthrough < Technical < Inspection
- Review success factors

### **Tuần 3: Test Techniques (Ch.4) & Managing Test (Ch.5)**
- Black-box: EP, 2/3-value BVA, Decision Table, State Transition
- White-box: Statement Coverage, Branch Coverage
- Experience-based: Error Guessing, Exploratory Testing, Checklist-based
- Test Planning: Entry/Exit Criteria
- Risk-based Testing (Probability × Impact)
- Test Monitoring vs Control
- Defect Management
- ATDD (Acceptance Test-Driven Development)

---

## 🎯 Quick Reference: Tất Cả Câu Hỏi

### **Q#1-Q#10**

| Q# | Topic | Đáp án | Key Point |
|----|-------|--------|-----------|
| 1 | Test Objectives | C | Reduce risk + build confidence (NOT prove no defects) |
| 2 | Early Testing | A | Tester involved throughout SDLC → detect early |
| 3 | Pesticide Paradox | A | Tests wear out → need to evolve |
| 4 | Test Analysis | B | Identify test CONDITIONS (not estimate/design/execute) |
| 5 | Test Approach Factors | B | i, iii, iv (SDLC, risks, regulatory) |
| 6 | Testing Role (Technical) | a+e | Configure env + Analyze basis (NOT managerial d) |
| 7 | Tester Skills | b | i, iii, v (Domain, Team player, Critical thinking) |
| 8 | Whole Team Approach | d | Tester + Business collaborate on acceptance tests |
| 9 | SDLC Models | d | Sequential, Incremental, Iterative all have tests |
| 10 | ATDD | c | Tests DRIVE development (not after-the-fact) |

### **Q#11-Q#20**

| Q# | Topic | Đáp án | Key Point |
|----|-------|--------|-----------|
| 11 | Shift-Left | c | Performance test at component level ≠ shift-left |
| 12 | Retrospectives | c | Process weaknesses → analyzed → improvement |
| 13 | Test Levels & Failures | a | 1D, 2B, 3A, 4C (match failure types to levels) |
| 14 | Regression Testing | b | (5), (7) = transition state changes (fail→pass) |
| 15 | Static Testing Benefits | a | NOT less expensive due to detecting LATER (logic sai) |
| 17 | Review Types | b | Walkthrough = author-led (key distinction) |
| 18 | Review Success | d | "Appreciate failures" = post-review, NOT success factor |
| 19 | Experience-based | c | Rely on tester's KNOWLEDGE of software + domain |
| 20 | 2-Value BVA Coverage | b | 4 test cases (Ground+Small, Ground+Large, First+No, Second++No) |
| 21 | Statement Coverage BVA | a | 50% coverage (6/12 boundary values) |

### **Q#22-Q#26**

| Q# | Topic | Đáp án | Key Point |
|----|-------|--------|-----------|
| 23 | Transitions Coverage | d | 3 test cases (cover all 7 transitions) |
| 24 | 100% Statement | a | Defective statements EXECUTED (NOT detected) |
| 25 | White-box Testing | d | KHÔNG identify requirement gaps (BLACK-box job) |
| 26 | Error Guessing | a | Use knowledge + experience of PAST defects |

---

## 🔟 7 Testing Principles (ISTQB)

### **1. Testing shows PRESENCE of defects**
- Testing finds bugs, không prove "vô lỗi"
- Absence of defects ≠ high quality

### **2. Exhaustive testing is IMPOSSIBLE**
- Can't test all input combinations (infinite)
- Can't test all paths (with loops)
- Risk-based: prioritize high-risk areas

### **3. EARLY testing** (shift-left)
- Test từ requirements phase (không chờ code ready)
- Find defects early → cheaper to fix

### **4. Defects CLUSTER**
- Lỗi tập trung ở một số modules
- Focus testing on risky areas

### **5. Pesticide PARADOX**
- Same tests chạy lại lần lần → không tìm lỗi mới
- Tests must EVOLVE to stay effective
- Change test data, change approaches

### **6. Testing is CONTEXT-DEPENDENT**
- E-commerce testing ≠ healthcare testing
- Test approach phụ thuộc project factors

### **7. Absence of errors FALLACY**
- No defects found ≠ system is good
- May miss requirements
- May have poor performance/usability

---

## 💡 Key Concepts & Formulas

### **Error-Defect-Failure Chain**
```
Error (người mắc sai)
  ↓
Defect (bug trong code)
  ↓
Failure (system không hoạt động như kỳ vọng)
```

### **Test Levels & V-Model Pairing**
```
Requirements ←→ Acceptance Test
System Design ←→ System Test
Detailed Design ←→ Integration Test
Code ←→ Unit/Component Test
```

### **4 Review Types (Formality)**
```
Informal < Walkthrough < Technical < Inspection
```

### **Coverage Hierarchy**
```
Statement Coverage
  ↓
Branch Coverage (stronger)
  ↓
Path Coverage (strongest, often impossible)
```

### **2-Value BVA Formula**
```
For each boundary [min, max]:
- Test: min-1, min (lower)
- Test: max, max+1 (upper)
= 4 values per range
= 2-value coverage
```

### **Risk Calculation**
```
Risk = Probability × Impact
(But Impact can override Probability)
```

### **Test Approach Factors (SIGNIFICANT)**
```
✅ SDLC model
✅ Product risks
✅ Regulatory requirements
✅ Budget/timeline
✅ Requirement clarity

❌ NOT significant:
- Historical defect counts
- Test environment setup (technical detail)
```

---

## ⚠️ Common Exam Traps

### **1. Test Objectives**
- ❌ TRAP: "Tests prove no defects"
- ✅ REAL: Tests reduce risk + build confidence

### **2. Testing Role**
- ❌ TRAP: Test Manager role = testing role
- ✅ REAL: Testing = technical (analyze, design, execute)

### **3. Test Analysis Phase**
- ❌ TRAP: Analysis = estimate time/effort
- ✅ REAL: Analysis = identify test CONDITIONS

### **4. Pesticide Paradox**
- ❌ TRAP: Run same test → find same bugs
- ✅ REAL: Tests must EVOLVE

### **5. V-Model Pairing**
- ❌ TRAP: System Design ↔ Integration Test
- ✅ REAL: System Design ↔ System Test (scope match)

### **6. 100% Statement Coverage**
- ❌ TRAP: Means all branches tested
- ✅ REAL: All STATEMENTS executed (not branches/paths)

### **7. White-box Testing**
- ❌ TRAP: Identifies requirement gaps
- ✅ REAL: Identifies code logic gaps

### **8. State Transition**
- ❌ TRAP: "Coverage" = state coverage by default
- ✅ REAL: Default = transition coverage (more comprehensive)

### **9. Review Success Factors**
- ❌ TRAP: "Appreciate defects" = review success
- ✅ REAL: That's post-review culture, not success factor

### **10. Shift-Left**
- ❌ TRAP: Any early testing = shift-left
- ✅ REAL: Test must be EARLIER than expected phase

---

## 🎓 Study Tips & Mnemonics

### **ISTQB Mindset**
- Testing ≠ Proving correctness
- Coverage metrics ≠ Test effectiveness
- Execution ≠ Detection
- Statement ≠ Branch ≠ Path

### **Test Level Memory (CIASAA)**
- **C**omponent
- **I**ntegration
- **S**ystem
- **A**ccept (+ **A**lpha/**A**lpha)

### **Review Type Memory (IWTI)**
- **I**nformal
- **W**alkthrough (author-led ← KEY)
- **T**echnical
- **I**nspection (most formal)

### **Test Approach Factors (SDR+BC)**
- **S**DLC model ✅
- **D**efect counts ❌
- **R**egulatory ✅
- **B**udget ✅
- **C**larity ✅

### **7 Principles Quick Check**
1. Shows PRESENCE (not absence)
2. Exhaustive IMPOSSIBLE
3. EARLY testing
4. Defects CLUSTER
5. Pesticide PARADOX (evolve)
6. Context-DEPENDENT
7. Absence of errors FALLACY

### **Statement vs Branch**
```
100% Statement ✓ 100% Branch? ✗
100% Branch → 100% Statement? ✓ (one-way guarantee)
```

### **Edge vs Node Coverage (State Transition)**
```
keyword "transition" → EDGE
keyword "state" (alone) → NODE
Default: EDGE (more common)
```

---

## 📋 Exam Readiness Checklist

### **Sau Khi Xong Q#1-Q#26:**
- ✅ Hiểu 7 Principles (có thể giải thích mỗi cái)
- ✅ Biết phân biệt: Test Analysis vs Planning vs Design vs Execution
- ✅ Biết phân biệt: Testing role vs Managerial role
- ✅ Hiểu V-Model pairing (scope match)
- ✅ Hiểu 4 Review Types (formality order)
- ✅ Hiểu 2-value BVA (calculate coverage %)
- ✅ Hiểu Statement ≠ Branch ≠ Path coverage
- ✅ Hiểu Edge vs Node coverage (state transition)
- ✅ Biết Black-box vs White-box (WHAT vs HOW)
- ✅ Biết Error Guessing = anticipate bugs (knowledge-based)

### **Q#27-Q#40 (Còn Lại):**
- Ch.1: Thêm test levels, acceptance testing chi tiết
- Ch.2: Agile testing, DevOps testing, maintenance
- Ch.4: Decision Table, State Transition detailed
- Ch.5: Entry/Exit criteria, Monitoring vs Control, Defect closure
- Ch.6: Test tools, automation

---

## 🚀 Next Steps

**Khi sang máy tính bảng:**
1. Upload file này lên Claude Web
2. Nói: "Tôi đã học Q#1-Q#26, hãy hỏi Q#27"
3. Claude sẽ đọc file → continue session

**Hoặc:**
1. Copy content file vào chat message
2. Nói: "Based on this progress, hỏi Q#27"

---

## 📝 Notes

- **Language:** Song ngữ (Tiếng Anh + Tiếng Việt)
- **Format:** Always translate question first, then explain
- **Exam Style:** Multiple choice, select ONE option
- **Passing Score:** ≥ 26/40 (65%)

---

**Good luck! 😥**  
**Bệ hạ cố gắng lên!**