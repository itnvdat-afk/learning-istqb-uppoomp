# ISTQB CTFL v4.0 — Thống Kê Lý Thuyết Q#1–Q#26

**Tổng hợp toàn bộ lý thuyết đã học qua 26 câu hỏi**
**Progress:** 65% (26/40) · **Ngày:** 2026-07-24

---

## 📊 Bản Đồ Câu Hỏi → Chương

| Chương | Câu hỏi liên quan | Chủ đề |
|--------|-------------------|--------|
| **Ch.1 — Fundamentals** | Q1, Q2, Q3, Q4, Q6, Q7, Q8 | Mục tiêu test, 7 nguyên tắc, vai trò tester, whole-team |
| **Ch.2 — Testing in SDLC** | Q5, Q9, Q10, Q11, Q12, Q13, Q14 | SDLC models, ATDD, shift-left, retrospective, test levels |
| **Ch.3 — Static Testing** | Q15, Q17, Q18 | Review types, review success factors |
| **Ch.4 — Test Techniques** | Q19, Q20, Q21, Q23, Q24, Q25, Q26 | BVA, statement/transition coverage, black/white-box, error guessing |

---

## 📖 CHƯƠNG 1 — Fundamentals of Testing

### 1.1 Mục tiêu của Testing (Q1)
- Testing để **giảm rủi ro (reduce risk)** + **xây dựng sự tự tin (build confidence)**.
- ❌ KHÔNG phải để "chứng minh không còn lỗi" (prove no defects — bất khả thi).
- Test tìm ra lỗi, cung cấp thông tin cho quyết định, ngăn lỗi (defect prevention).

### 1.2 Error – Defect – Failure (chuỗi nhân quả)
```
Error (con người mắc sai lầm)
   ↓ gây ra
Defect (lỗi nằm trong code/tài liệu)
   ↓ khi thực thi
Failure (hệ thống chạy sai kỳ vọng)
```
> Lưu ý: 1 defect chưa chắc gây failure (phải được thực thi đúng điều kiện). Failure cũng có thể do môi trường (bức xạ, từ trường...).

### 1.3 Bảy Nguyên Tắc Testing (7 Principles)
| # | Nguyên tắc | Ý nghĩa cốt lõi |
|---|-----------|-----------------|
| 1 | **Testing shows presence of defects** | Chỉ chứng minh CÓ lỗi, không chứng minh VÔ lỗi |
| 2 | **Exhaustive testing is impossible** | Không thể test hết mọi tổ hợp → ưu tiên theo rủi ro |
| 3 | **Early testing (shift-left)** (Q2) | Test sớm từ pha requirement → lỗi rẻ hơn khi sửa |
| 4 | **Defects cluster together** | Lỗi tập trung ở vài module → dồn lực vào đó |
| 5 | **Pesticide paradox** (Q3) | Test lặp lại mãi sẽ "chai" → phải làm mới test |
| 6 | **Testing is context-dependent** | E-commerce ≠ y tế → cách test khác nhau |
| 7 | **Absence-of-errors fallacy** | Không tìm thấy lỗi ≠ sản phẩm tốt/dùng được |

### 1.4 Test Process — Test Analysis (Q4)
- **Test Analysis** = xác định **test conditions** ("test cái gì").
- Phân biệt các pha:
  - **Planning** → lập kế hoạch, ước lượng effort.
  - **Analysis** → xác định test conditions (WHAT to test).
  - **Design** → thiết kế test cases (HOW to test).
  - **Implementation** → chuẩn bị testware, môi trường.
  - **Execution** → chạy test, so sánh kết quả.

### 1.5 Vai trò của Tester (Q6, Q7)
- Testing là công việc **kỹ thuật** (technical): configure môi trường, phân tích test basis, thiết kế, thực thi.
- ❌ KHÔNG bao gồm việc **quản lý** (managerial) như phân bổ ngân sách, quyết định nhân sự.
- **Kỹ năng tester cần (Q7):** kiến thức domain, tinh thần đồng đội (team player), tư duy phản biện (critical thinking).

### 1.6 Whole-Team Approach (Q8)
- Cả team cùng chịu trách nhiệm chất lượng.
- Tester + Business Representative **cộng tác** viết acceptance tests.

---

## 📖 CHƯƠNG 2 — Testing Throughout the SDLC

### 2.1 SDLC Models (Q5, Q9)
- Các mô hình: **Sequential (Waterfall, V-model)**, **Iterative**, **Incremental**, **Agile**.
- Mọi mô hình đều có hoạt động test — chỉ khác thời điểm & cách tổ chức.
- **Yếu tố ảnh hưởng test approach (Q5):** SDLC model, product risks, regulatory requirements (KHÔNG phải số lượng defect lịch sử, KHÔNG phải chi tiết cấu hình môi trường).

### 2.2 ATDD — Acceptance Test-Driven Development (Q10)
- Viết acceptance tests **TRƯỚC** khi code → test **dẫn dắt** (drive) phát triển.
- ❌ KHÔNG phải viết test sau khi code xong.

### 2.3 Shift-Left (Q11)
- Đưa hoạt động test **sớm hơn** vị trí thông thường trong vòng đời.
- ⚠️ Bẫy: test performance ở component level KHÔNG tự động = shift-left (nếu vốn đã ở đó thì không phải "dịch trái").

### 2.4 Retrospectives (Q12)
- Cuối iteration/dự án → phân tích **điểm yếu quy trình** → đề xuất cải tiến.
- Mục tiêu: process improvement, không phải đổ lỗi cá nhân.

### 2.5 Test Levels & Failure Types (Q13)
| Test Level | Kiểm tra | Loại failure phát hiện |
|-----------|----------|------------------------|
| **Component (Unit)** | 1 module đơn lẻ | Logic sai trong 1 hàm |
| **Integration** | Giao tiếp giữa các module | Sai interface/dữ liệu truyền |
| **System** | Toàn hệ thống, end-to-end | Sai chức năng/luồng tổng thể |
| **Acceptance** | Đáp ứng nhu cầu người dùng | Không đúng yêu cầu nghiệp vụ |

### 2.6 Regression Testing (Q14)
- Chạy lại test khi có thay đổi để đảm bảo **không phát sinh lỗi mới** ở phần đang chạy tốt.
- Regression phù hợp cho các transition có thay đổi trạng thái (fail→pass).

---

## 📖 CHƯƠNG 3 — Static Testing

### 3.1 Static Testing Benefits (Q15)
- Phát hiện lỗi **sớm** ngay trên tài liệu/code mà không cần chạy → rẻ hơn.
- ⚠️ Bẫy logic: static testing rẻ vì tìm lỗi SỚM, KHÔNG phải vì "tìm lỗi muộn".

### 3.2 Bốn Loại Review (theo mức formal tăng dần) (Q17)
```
Informal  <  Walkthrough  <  Technical Review  <  Inspection
(ít formal)                                      (formal nhất)
```
| Loại | Đặc điểm chính |
|------|----------------|
| **Informal** | Không quy trình, không tài liệu |
| **Walkthrough** | **Tác giả dẫn dắt (author-led)** ← điểm phân biệt Q17 |
| **Technical** | Chuyên gia kỹ thuật, có thể có moderator |
| **Inspection** | Formal nhất, có vai trò & metrics, moderator dẫn |

### 3.3 Review Success Factors (Q18)
- Yếu tố thành công: mục tiêu rõ, đúng người, chuẩn bị kỹ, không khí tích cực.
- ⚠️ Bẫy: "Appreciate/biết ơn khi tìm ra lỗi" là **văn hóa sau review**, KHÔNG phải success factor.

---

## 📖 CHƯƠNG 4 — Test Techniques

### 4.1 Phân loại kỹ thuật
| Nhóm | Dựa trên | Ví dụ |
|------|----------|-------|
| **Black-box** | Đặc tả/hành vi (WHAT) | EP, BVA, Decision Table, State Transition |
| **White-box** | Cấu trúc code (HOW) | Statement Coverage, Branch Coverage |
| **Experience-based** | Kinh nghiệm tester | Error Guessing, Exploratory, Checklist |

### 4.2 Experience-based Testing (Q19, Q26)
- Dựa vào **kiến thức + kinh nghiệm** của tester về phần mềm và domain.
- **Error Guessing (Q26):** dùng kinh nghiệm về **các lỗi ĐÃ TỪNG xảy ra** để đoán chỗ dễ lỗi.

### 4.3 Boundary Value Analysis — BVA (Q20, Q21)
- Test tại **biên** của các phân vùng (nơi lỗi hay xuất hiện).
- **2-value BVA:** với mỗi biên → test giá trị biên + giá trị liền kề ngoài.
  - Công thức: mỗi range → thường 2 giá trị/biên.
- **Q20:** cần **4 test cases** để phủ 2-value cho bài toán đã cho.
- **Q21:** Statement coverage đạt **50%** (6/12 boundary values).

### 4.4 State Transition Testing (Q23)
- Mô hình gồm: **states (nút)**, **transitions (cạnh)**, events, actions.
- **Transition coverage (Q23):** cần **3 test cases** để phủ hết **7 transitions**.
- ⚠️ Từ khóa quan trọng:
  - `"transition"` → **EDGE** (cạnh) coverage.
  - `"state"` (đứng riêng) → **NODE** (nút) coverage.
  - **Mặc định** khi nói "coverage" → **transition/edge coverage** (mạnh hơn).

### 4.5 Statement vs Branch Coverage (Q24, Q25)
- **100% Statement Coverage (Q24):** mọi câu lệnh được **THỰC THI** (executed) — KHÔNG có nghĩa lỗi được **phát hiện** (detected). Execution ≠ detection.
- **Quan hệ một chiều:**
  ```
  100% Branch  →  đảm bảo 100% Statement  ✅
  100% Statement  →  KHÔNG đảm bảo 100% Branch  ❌
  ```
- **White-box (Q25):** tìm lỗ hổng **logic code**, KHÔNG phát hiện **thiếu requirement** (đó là việc của black-box).

---

## ⚠️ 10 Cái Bẫy Thường Gặp (rút ra từ Q1–Q26)

| # | Bẫy (SAI) | Đúng |
|---|-----------|------|
| 1 | Test để chứng minh vô lỗi | Test để giảm rủi ro + build confidence |
| 2 | Testing = vai trò quản lý | Testing = kỹ thuật (analyze/design/execute) |
| 3 | Analysis = ước lượng effort | Analysis = xác định test conditions |
| 4 | Pesticide: chạy lại tìm lỗi mới | Test phải TIẾN HÓA |
| 5 | System Design ↔ Integration Test | System Design ↔ **System Test** |
| 6 | 100% Statement = phủ mọi branch | Chỉ phủ mọi **câu lệnh** |
| 7 | White-box tìm thiếu requirement | White-box tìm lỗi **logic code** |
| 8 | "Coverage" mặc định = state coverage | Mặc định = **transition** coverage |
| 9 | "Biết ơn lỗi" = review success factor | Đó là văn hóa hậu-review |
| 10 | Mọi test sớm = shift-left | Phải SỚM HƠN vị trí thông thường |

---

## 🧠 Mnemonics Nhanh

- **7 Principles:** Presence · Exhaustive · Early · Cluster · Pesticide · Context · Fallacy
- **Test Levels (CISA):** Component · Integration · System · Acceptance
- **Review formality (IWTI):** Informal · Walkthrough · Technical · Inspection
- **Approach factors ✅:** SDLC · Regulatory · Budget · Risk · Clarity — (❌ defect-count, môi trường)
- **Coverage 1 chiều:** Branch ⇒ Statement (không có chiều ngược)
- **State transition:** "transition"→edge, "state"→node, default→edge

---

## ✅ Đáp Án Gốc (tra ngược nhanh)

| Q | Đáp án | Q | Đáp án | Q | Đáp án |
|---|--------|---|--------|---|--------|
| 1 | C | 10 | c | 20 | b |
| 2 | A | 11 | c | 21 | a |
| 3 | A | 12 | c | 23 | d |
| 4 | B | 13 | a (1D 2B 3A 4C) | 24 | a |
| 5 | B (i,iii,iv) | 14 | b (5,7) | 25 | d |
| 6 | a+e | 15 | a | 26 | a |
| 7 | b (i,iii,v) | 17 | b | | |
| 8 | d | 18 | d | | |
| 9 | d | 19 | c | | |

> *Ghi chú: file gốc không có Q16 và Q22 trong bảng — có thể là câu lý thuyết/đã bỏ qua.*

---

**Tiếp theo:** Q#27–Q#40 (Decision Table, State Transition chi tiết, Entry/Exit criteria, Monitoring vs Control, Defect closure, Test tools).
