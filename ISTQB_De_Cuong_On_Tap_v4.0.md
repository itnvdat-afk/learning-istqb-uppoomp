# ISTQB CTFL v4.0.1 — Đề Cương Ôn Tập (Bản Đồ Syllabus)

**Nguồn:** Đề cương ISTQB® Certified Tester Foundation Level — **Phiên bản 4.0.1 (bản tiếng Việt, 2024-09-15)**
**Mục đích:** Bản đồ toàn syllabus để tra cứu & ôn tập — 6 chương, mọi section, mọi Learning Objective (LO) kèm K-level.
**Đối chiếu tiến độ:** Đã học Q#1–26 (65%). Cột **"Đã học?"** đánh dấu chủ đề đã cover.

> **K-level là gì?**
> - **K1 = Ghi nhớ (Remember)** — nhớ/nhận biết thuật ngữ, khái niệm. → học thuộc.
> - **K2 = Hiểu (Understand)** — giải thích, phân biệt, so sánh, phân loại. → hiểu bản chất.
> - **K3 = Áp dụng (Apply)** — thực hiện kỹ thuật để tạo ra kết quả (thiết kế test case, tính toán). → **luyện bài tập**.

---

## 📊 Thông Tin Kỳ Thi & Trọng Số

| Hạng mục | Chi tiết |
|----------|----------|
| Số câu hỏi | **40 câu** trắc nghiệm |
| Điểm đậu | **≥ 26/40 (65%)** |
| Thời gian | **60 phút** (75 phút cho thí sinh thi bằng ngôn ngữ không phải tiếng mẹ đẻ) |
| Phạm vi thi | Toàn bộ đề cương, **trừ** phần Giới thiệu (Ch.0) và các Phụ lục |
| K-level tối đa | K3 (Foundation Level dừng ở mức Áp dụng) |

### Trọng số theo chương

| Chương | Tên chương | Thời lượng đào tạo | Số câu thi* |
|--------|-----------|:------------------:|:-----------:|
| **1** | Nền tảng Kiểm thử | 180 phút | 8 |
| **2** | Kiểm thử Trong suốt Vòng đời PTPM | 130 phút | 6 |
| **3** | Kiểm thử tĩnh | 80 phút | 4 |
| **4** | Phân tích và Thiết kế Test case | 390 phút | 11 |
| **5** | Quản lý các Hoạt động Kiểm thử | 335 phút | 9 |
| **6** | Công cụ Kiểm thử | 20 phút | 2 |
| | **TỔNG** | **1.135 phút** (~18h55) | **40** |

> \* Thời lượng đào tạo lấy trực tiếp từ đề cương v4.0.1. Số câu thi mỗi chương theo **"Bảng Cấu trúc Kỳ thi" (Exam Structure Table)** chuẩn của ISTQB (đề cương chỉ định phạm vi, không in số câu). → **Chương 4 & 5 nặng nhất (20/40 câu)** — ưu tiên chắc 2 chương này.

---

## 📘 CHƯƠNG 1 — Nền tảng Kiểm thử *(180 phút · 8 câu)*

| Mục | Learning Objective (LO) | K | Đã học? |
|-----|-------------------------|:-:|:-------:|
| **1.1** | **Kiểm thử là gì?** | | |
| 1.1.1 | Xác định các mục tiêu kiểm thử điển hình | K1 | ✅ Q1 |
| 1.1.2 | Phân biệt kiểm thử và gỡ lỗi (debugging) | K2 | 🔸 |
| **1.2** | **Tại sao cần kiểm thử?** | | |
| 1.2.1 | Minh họa lý do kiểm thử là cần thiết | K2 | 🔸 |
| 1.2.2 | Ghi nhớ mối quan hệ giữa kiểm thử và Đảm bảo Chất lượng (QA) | K1 | 🔸 |
| 1.2.3 | Phân biệt nguyên nhân gốc rễ, sai sót, lỗi phần mềm, và sự cố (root cause/error/defect/failure) | K2 | 🔸 |
| **1.3** | **Các nguyên tắc kiểm thử** | | |
| 1.3.1 | Giải thích **bảy nguyên tắc kiểm thử** | K2 | ✅ Q2,Q3 |
| **1.4** | **Hoạt động, sản phẩm & vai trò kiểm thử** | | |
| 1.4.1 | Giải thích các hoạt động kiểm thử và công việc liên quan | K2 | ✅ Q4 |
| 1.4.2 | Giải thích ảnh hưởng của ngữ cảnh đến quy trình kiểm thử | K2 | 🔸 |
| 1.4.3 | Phân biệt các sản phẩm kiểm thử (testware) hỗ trợ hoạt động kiểm thử | K2 | 🔸 |
| 1.4.4 | Giải thích giá trị của khả năng truy xuất nguồn gốc (traceability) | K2 | 🔸 |
| 1.4.5 | So sánh các vai trò khác nhau trong kiểm thử | K2 | ✅ Q6 |
| **1.5** | **Kỹ năng cốt lõi & thực hành tốt** | | |
| 1.5.1 | Đưa ra ví dụ về các kỹ năng chung cần thiết cho kiểm thử | K2 | ✅ Q7 |
| 1.5.2 | Ghi nhớ lợi ích của cách tiếp cận toàn đội (whole team) | K1 | ✅ Q8 |
| 1.5.3 | Phân biệt lợi ích và hạn chế của tính độc lập trong kiểm thử | K2 | 🔸 |

---

## 📗 CHƯƠNG 2 — Kiểm thử Trong suốt Vòng đời PTPM *(130 phút · 6 câu)*

| Mục | Learning Objective (LO) | K | Đã học? |
|-----|-------------------------|:-:|:-------:|
| **2.1** | **Kiểm thử theo ngữ cảnh vòng đời PTPM (SDLC)** | | |
| 2.1.1 | Giải thích ảnh hưởng của mô hình PTPM được chọn đến kiểm thử | K2 | ✅ Q5,Q9 |
| 2.1.2 | Ghi nhớ các thực hành kiểm thử tốt áp dụng cho mọi mô hình PTPM | K1 | 🔸 |
| 2.1.3 | Ghi nhớ ví dụ về các phương pháp phát triển hướng kiểm thử trước (test-first) | K1 | ✅ Q10 (ATDD) |
| 2.1.4 | Tóm tắt cách DevOps ảnh hưởng đến kiểm thử | K2 | 🔸 |
| 2.1.5 | Giải thích khái niệm **shift left** | K2 | ✅ Q11 |
| 2.1.6 | Giải thích retrospective như một cơ chế cải tiến quy trình | K2 | ✅ Q12 |
| **2.2** | **Các mức & các loại kiểm thử** | | |
| 2.2.1 | Phân biệt các **mức kiểm thử** (Component/Integration/System/Acceptance) | K2 | ✅ Q13 |
| 2.2.2 | Phân biệt các **loại kiểm thử** (functional/non-functional/…) | K2 | 🔸 |
| 2.2.3 | Phân biệt kiểm thử **xác nhận** (confirmation) và kiểm thử **hồi quy** (regression) | K2 | ✅ Q14 |
| **2.3** | **Kiểm thử bảo trì** | | |
| 2.3.1 | Tóm tắt kiểm thử bảo trì và các yếu tố kích hoạt (triggers) | K2 | 🔸 |

---

## 📙 CHƯƠNG 3 — Kiểm thử tĩnh *(80 phút · 4 câu)*

| Mục | Learning Objective (LO) | K | Đã học? |
|-----|-------------------------|:-:|:-------:|
| **3.1** | **Cơ bản về kiểm thử tĩnh** | | |
| 3.1.1 | Nhận biết các sản phẩm công việc có thể kiểm tra bằng kiểm thử tĩnh | K1 | 🔸 |
| 3.1.2 | Giải thích giá trị của kiểm thử tĩnh | K2 | ✅ Q15 |
| 3.1.3 | So sánh và đối chiếu kiểm thử tĩnh vs kiểm thử động | K2 | 🔸 |
| **3.2** | **Phản hồi & quy trình rà soát (review)** | | |
| 3.2.1 | Xác định lợi ích của phản hồi sớm và thường xuyên từ các bên liên quan | K1 | 🔸 |
| 3.2.2 | Tóm tắt các hoạt động trong quy trình rà soát | K2 | 🔸 |
| 3.2.3 | Ghi nhớ trách nhiệm của các vai trò chính khi rà soát | K1 | 🔸 |
| 3.2.4 | So sánh và đối chiếu các **loại rà soát** (Informal/Walkthrough/Technical/Inspection) | K2 | ✅ Q17 |
| 3.2.5 | Ghi nhớ các yếu tố góp phần vào buổi rà soát thành công | K1 | ✅ Q18 |

---

## 📕 CHƯƠNG 4 — Phân tích và Thiết kế Test case *(390 phút · 11 câu)* — **NẶNG NHẤT**

| Mục | Learning Objective (LO) | K | Đã học? |
|-----|-------------------------|:-:|:-------:|
| **4.1** | **Tổng quan kỹ thuật kiểm thử** | | |
| 4.1.1 | Phân biệt kỹ thuật hộp đen / hộp trắng / dựa vào kinh nghiệm | K2 | ✅ Q19,Q25 |
| **4.2** | **Kỹ thuật hộp đen (black-box)** | | |
| 4.2.1 | **Áp dụng** phân vùng tương đương (Equivalence Partitioning) để thiết kế test case | **K3** | 🔸 |
| 4.2.2 | **Áp dụng** phân tích giá trị biên (Boundary Value Analysis) để thiết kế test case | **K3** | ✅ Q20,Q21 |
| 4.2.3 | **Áp dụng** kiểm thử bảng quyết định (Decision Table) để thiết kế test case | **K3** | 🔸 (đang học Q27) |
| 4.2.4 | **Áp dụng** kiểm thử chuyển đổi trạng thái (State Transition) để thiết kế test case | **K3** | ✅ Q23 (một phần) |
| **4.3** | **Kỹ thuật hộp trắng (white-box)** | | |
| 4.3.1 | Giải thích kiểm thử câu lệnh & độ bao phủ câu lệnh (Statement) | K2 | ✅ Q24 |
| 4.3.2 | Giải thích kiểm thử nhánh & độ bao phủ nhánh (Branch) | K2 | 🔸 |
| 4.3.3 | Giải thích giá trị của kiểm thử hộp trắng | K2 | ✅ Q25 |
| **4.4** | **Kỹ thuật dựa vào kinh nghiệm** | | |
| 4.4.1 | Giải thích đoán lỗi (error guessing) | K2 | ✅ Q26 |
| 4.4.2 | Giải thích kiểm thử khám phá (exploratory testing) | K2 | 🔸 |
| 4.4.3 | Giải thích kiểm thử dựa vào checklist | K2 | 🔸 |
| **4.5** | **Cách tiếp cận dựa trên hợp tác (collaboration)** | | |
| 4.5.1 | Giải thích cách viết user story qua hợp tác với dev & đại diện nghiệp vụ | K2 | 🔸 |
| 4.5.2 | Phân loại một số cách viết tiêu chí chấp nhận (acceptance criteria) | K2 | 🔸 |
| 4.5.3 | **Sử dụng** ATDD (Acceptance Test-Driven Development) để thiết kế test case | **K3** | ✅ Q10 (một phần) |

---

## 📓 CHƯƠNG 5 — Quản lý các Hoạt động Kiểm thử *(335 phút · 9 câu)* — **NẶNG**

| Mục | Learning Objective (LO) | K | Đã học? |
|-----|-------------------------|:-:|:-------:|
| **5.1** | **Lập kế hoạch kiểm thử** | | |
| 5.1.1 | Minh hoạ mục đích và nội dung của kế hoạch kiểm thử (test plan) | K2 | 🔸 |
| 5.1.2 | Nhận biết đóng góp của tester trong lập kế hoạch iteration & release | K1 | 🔸 |
| 5.1.3 | So sánh và đối chiếu tiêu chí bắt đầu (entry) và tiêu chí kết thúc (exit) | K2 | 🔸 |
| 5.1.4 | **Sử dụng** các kỹ thuật ước lượng để tính công sức kiểm thử | **K3** | 🔸 |
| 5.1.5 | **Áp dụng** ưu tiên hóa test case | **K3** | 🔸 |
| 5.1.6 | Ghi nhớ khái niệm tháp kiểm thử (test pyramid) | K1 | 🔸 |
| 5.1.7 | Tóm tắt các góc phần tư kiểm thử (testing quadrants) & quan hệ với mức/loại kiểm thử | K2 | 🔸 |
| **5.2** | **Quản lý rủi ro** | | |
| 5.2.1 | Xác định mức rủi ro dựa vào khả năng xảy ra × mức độ ảnh hưởng | K1 | 🔸 |
| 5.2.2 | Phân biệt rủi ro dự án (project) và rủi ro sản phẩm (product) | K2 | 🔸 |
| 5.2.3 | Giải thích cách phân tích rủi ro sản phẩm ảnh hưởng mức độ & phạm vi kiểm thử | K2 | 🔸 |
| 5.2.4 | Giải thích các biện pháp ứng phó với rủi ro sản phẩm đã phân tích | K2 | 🔸 |
| **5.3** | **Giám sát, kiểm soát & hoàn tất kiểm thử** | | |
| 5.3.1 | Ghi nhớ các chỉ số (metrics) dùng trong kiểm thử | K1 | 🔸 |
| 5.3.2 | Tóm tắt mục đích, nội dung, đối tượng của báo cáo kiểm thử | K2 | 🔸 |
| 5.3.3 | Minh hoạ cách truyền đạt trạng thái kiểm thử | K2 | 🔸 |
| **5.4** | **Quản lý cấu hình (configuration management)** | | |
| 5.4.1 | Tóm tắt cách quản lý cấu hình hỗ trợ kiểm thử | K2 | 🔸 |
| **5.5** | **Quản lý lỗi (defect management)** | | |
| 5.5.1 | **Chuẩn bị** báo cáo lỗi (defect report) | **K3** | 🔸 |

---

## 📔 CHƯƠNG 6 — Công cụ Kiểm thử *(20 phút · 2 câu)*

| Mục | Learning Objective (LO) | K | Đã học? |
|-----|-------------------------|:-:|:-------:|
| **6.1** | **Hỗ trợ kiểm thử bằng công cụ** | | |
| 6.1.1 | Giải thích cách các loại công cụ khác nhau hỗ trợ hoạt động kiểm thử | K2 | 🔸 |
| **6.2** | **Lợi ích & rủi ro của tự động hóa** | | |
| 6.2.1 | Ghi nhớ các lợi ích và rủi ro của tự động hóa kiểm thử | K1 | 🔸 |

---

## 🎯 Tổng Hợp Theo K-level

**Tổng cộng 64 Learning Objectives** trên 6 chương.

### 🔴 8 LO mức K3 — BẮT BUỘC luyện bài tập (dạng tính toán / thiết kế test case)
> Đây là nhóm dễ mất điểm nhất nếu không luyện tay. Chiếm phần lớn câu khó của đề.

| LO | Chủ đề | Ghi chú |
|----|--------|---------|
| FL-4.2.1 | Equivalence Partitioning (Phân vùng tương đương) | Chia lớp, chọn đại diện mỗi lớp |
| FL-4.2.2 | Boundary Value Analysis (Giá trị biên) | 2-value / 3-value BVA, tính coverage % |
| FL-4.2.3 | Decision Table (Bảng quyết định) | Đếm rule = tích số điều kiện |
| FL-4.2.4 | State Transition (Chuyển đổi trạng thái) | Phủ state / transition / switch |
| FL-4.5.3 | ATDD | Suy ra test case từ acceptance criteria |
| FL-5.1.4 | Ước lượng công sức kiểm thử | Metrics-based / expert-based |
| FL-5.1.5 | Ưu tiên hóa test case | Risk / coverage / requirement-based |
| FL-5.5.1 | Viết báo cáo lỗi | Nội dung defect report (IEEE 1044) |

### 🟡 K1 (Ghi nhớ) — học thuộc là đủ
FL-1.1.1, 1.2.2, 1.5.2 · 2.1.2, 2.1.3 · 3.1.1, 3.2.1, 3.2.3, 3.2.5 · 5.1.2, 5.1.6, 5.2.1, 5.3.1 · 6.2.1

### 🟢 K2 (Hiểu) — chiếm đa số, cần hiểu bản chất để phân biệt/so sánh
Toàn bộ LO còn lại (~42 LO).

---

## 📍 Đối Chiếu Tiến Độ: Còn Thiếu So Với Q#1–26

**Đã cover tốt (qua Q#1–26):** phần lớn Ch.1, các LO chính Ch.2, Ch.3 (review), và một phần Ch.4 (BVA, statement coverage, state transition, error guessing).

**🔴 Chưa đụng tới / cần tập trung cho Q#27–40:**

| Vùng | LO cần học | Vì sao ưu tiên |
|------|-----------|----------------|
| **Ch.4 hộp đen** | 4.2.1 (EP), **4.2.3 (Decision Table)** | Decision Table chưa học — đang bắt đầu ở Q#27 |
| **Ch.4 hợp tác** | 4.5.1, 4.5.2 (acceptance criteria) | Chưa cover cách viết tiêu chí chấp nhận |
| **Ch.4 kinh nghiệm** | 4.4.2, 4.4.3 (exploratory, checklist) | Mới học error guessing |
| **Ch.5 — TOÀN BỘ** | 5.1 → 5.5 (16 LO) | **9 câu thi**, gần như chưa học gì |
| **Ch.6 — TOÀN BỘ** | 6.1, 6.2 (2 LO) | Nhỏ nhưng dễ ăn trọn 2 điểm |
| **Ch.2 bổ sung** | 2.1.4 (DevOps), 2.2.2 (loại KT), 2.3.1 (bảo trì) | Còn sót vài LO |

> **Chiến lược:** Q#27–40 nên dồn vào **Chương 5 (9 câu)** và hoàn thiện **Chương 4 (11 câu)** — đây là 20/40 điểm và cũng là phần đang hổng nhất.

---

## 🔗 Tài Liệu Liên Quan Trong Repo
- `ISTQB_CTFL_Complete_Progress.md` — tiến độ chi tiết Q#1–26.
- `ISTQB_Theory_Summary_Q1-Q26.md` — tổng hợp lý thuyết đã học.
- `ISTQB_De_Cuong_On_Tap_v4.0.md` — (file này) bản đồ syllabus đầy đủ.

---

*Trích xuất & biên soạn từ đề cương chính thức ISTQB CTFL v4.0.1 (bản tiếng Việt). Thuật ngữ tiếng Việt lấy nguyên văn theo Phụ lục A của đề cương.*
