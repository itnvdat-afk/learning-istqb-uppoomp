# ISTQB CTFL v4.0.1 — Ôn Tập Lý Thuyết Toàn Bộ Bài Học

**Nguồn:** Đề cương ISTQB® Certified Tester Foundation Level v4.0.1 (bản tiếng Việt).
**Phạm vi:** Toàn bộ nội dung 6 chương (không kèm bộ câu hỏi luyện tập). Tài liệu này dùng để đọc — ôn — hiểu bản chất từng khái niệm.

> **Cách dùng:** Đọc từ trên xuống theo chương. Mỗi mục là một learning objective. Các ô 🔑 là điểm dễ ra thi / dễ nhầm.

---

# 📘 CHƯƠNG 1 — Nền tảng Kiểm thử

## 1.1 Kiểm thử là gì?

- **Kiểm thử phần mềm** = một tập hợp **nhiều hoạt động** nhằm phát hiện lỗi và **đánh giá chất lượng** các sản phẩm công việc. Sản phẩm công việc khi được kiểm thử gọi là **đối tượng kiểm thử (test object)**.
- 🔑 **Hai hiểu lầm phổ biến:**
  1. Kiểm thử chỉ là **thực thi test case** → SAI. Còn nhiều hoạt động khác (lập kế hoạch, phân tích, thiết kế...).
  2. Kiểm thử chỉ là **xác minh (verification)** → SAI. Bao gồm cả **thẩm định (validation)**.
- **Verification (xác minh):** hệ thống có đáp ứng **yêu cầu đã mô tả** không? ("làm đúng thứ đã đặc tả")
- **Validation (thẩm định):** hệ thống có đáp ứng **nhu cầu người dùng & bên liên quan** trong môi trường vận hành không? ("làm đúng thứ người dùng cần")
- Kiểm thử **động** (cần thực thi phần mềm) vs kiểm thử **tĩnh** (không cần thực thi — rà soát & phân tích tĩnh).

### 1.1.1 Mục tiêu kiểm thử điển hình
- Đánh giá sản phẩm công việc (yêu cầu, user story, thiết kế, mã nguồn).
- Phát hiện sự cố và tìm lỗi.
- Đảm bảo độ bao phủ cần thiết của đối tượng kiểm thử.
- **Giảm mức rủi ro** về chất lượng phần mềm.
- Xác minh yêu cầu đã được đáp ứng; xác minh tuân thủ hợp đồng/pháp lý/quy định.
- Cung cấp thông tin cho bên liên quan **ra quyết định**.
- **Tăng niềm tin** vào chất lượng.
- Thẩm định đối tượng kiểm thử hoạt động như mong đợi.

> 🔑 Mục tiêu thay đổi tùy **ngữ cảnh** (sản phẩm, mức kiểm thử, rủi ro, SDLC, yếu tố doanh nghiệp).

### 1.1.2 Kiểm thử và Gỡ lỗi (Debugging)
- Là **hai hoạt động riêng biệt**.
- **Kiểm thử** phát hiện sự cố (động) hoặc lỗi trực tiếp (tĩnh).
- **Gỡ lỗi** (không phải hoạt động kiểm thử) = tìm nguyên nhân → phân tích → loại bỏ. Gồm: **tái hiện → chẩn đoán → sửa lỗi**.
- Sau sửa: **kiểm thử xác nhận** (lỗi đã hết chưa) rồi **kiểm thử hồi quy** (có sinh lỗi mới ở nơi khác không).

## 1.2 Tại sao cần kiểm thử?

### 1.2.1 Đóng góp của kiểm thử vào thành công
- Phương thức **hiệu quả chi phí** để phát hiện lỗi → (gỡ lỗi loại bỏ) → **gián tiếp nâng chất lượng**.
- Đánh giá **trực tiếp** chất lượng tại các giai đoạn SDLC → hỗ trợ quyết định phát hành.
- Là **đại diện gián tiếp cho người dùng** trong dự án.
- Đáp ứng yêu cầu hợp đồng/pháp lý/tiêu chuẩn.

### 1.2.2 Kiểm thử và Đảm bảo Chất lượng (QA)
| | **Kiểm thử (QC)** | **QA (Đảm bảo Chất lượng)** |
|---|---|---|
| Hướng | Hướng **sản phẩm** | Hướng **quy trình** |
| Tính chất | **Khắc phục** (corrective) | **Phòng ngừa** (preventive) |
| Tập trung | Đạt mức chất lượng phù hợp | Triển khai & cải tiến quy trình |
| Là gì | Một hình thức **kiểm soát chất lượng (QC)** | Nguyên tắc: quy trình tốt → sản phẩm tốt |

> 🔑 Kiểm thử là **QC**, KHÔNG phải QA. QA là trách nhiệm của **tất cả mọi người**.

### 1.2.3 Sai sót – Lỗi – Sự cố – Nguyên nhân gốc rễ
```
Nguyên nhân gốc rễ (root cause)
   → Con người mắc Sai sót (error/mistake)
      → tạo ra Lỗi (defect/fault/bug) — trong tài liệu, mã nguồn...
         → khi thực thi có thể gây Sự cố (failure)
```
- 🔑 Một lỗi **không phải lúc nào cũng** gây sự cố (có lỗi luôn gây, có lỗi chỉ gây trong điều kiện cụ thể, có lỗi không bao giờ gây).
- 🔑 Sự cố còn có thể do **môi trường** (bức xạ, từ trường...), không chỉ do lỗi.
- **RCA (root cause analysis):** phân tích để tìm & xử lý nguyên nhân gốc → ngăn ngừa lỗi tương tự tương lai.

## 1.3 Bảy Nguyên tắc Kiểm thử
1. **Kiểm thử cho thấy sự tồn tại của lỗi**, không chứng minh vắng mặt lỗi.
2. **Kiểm thử vét cạn là không thể** → dùng kỹ thuật, ưu tiên hóa, kiểm thử dựa vào rủi ro.
3. **Kiểm thử sớm** tiết kiệm thời gian & chi phí (shift-left).
4. **Lỗi tập trung** (Pareto 80/20) — vài thành phần chứa phần lớn lỗi.
5. **Test case giảm hiệu quả theo thời gian** (nghịch lý thuốc trừ sâu) → phải rà soát, sửa đổi, bổ sung test.
6. **Kiểm thử phụ thuộc ngữ cảnh** — không có cách tiếp cận chung cho mọi trường hợp.
7. **Ngộ nhận về việc không có lỗi** — verification kỹ + sửa hết lỗi vẫn có thể ra hệ thống không đáp ứng nhu cầu → cần cả **validation**.

## 1.4 Hoạt động, Sản phẩm & Vai trò Kiểm thử

### 1.4.1 Hoạt động & nhiệm vụ kiểm thử (quy trình kiểm thử)
| Hoạt động | Trả lời / Nội dung |
|-----------|--------------------|
| **Lập kế hoạch** | Xác định mục tiêu + chọn cách tiếp cận (mục 5.1) |
| **Giám sát & kiểm soát** | Theo dõi tiến độ vs kế hoạch; hành động điều chỉnh (mục 5.3) |
| **Phân tích** | "**Kiểm thử cái gì?**" → xác định khía cạnh/điều kiện kiểm thử có thể đo lường |
| **Thiết kế** | "**Kiểm thử như thế nào?**" → test case, hạng mục bao phủ, dữ liệu, môi trường |
| **Triển khai** | Tạo/thu thập testware: test procedure, script, test suite, dữ liệu; thiết lập môi trường |
| **Thực thi** | Chạy test (test run); so sánh kết quả thực tế vs mong đợi; ghi nhận & phân tích bất thường |
| **Hoàn tất** | Tại các mốc; xử lý lỗi còn lại, lưu trữ testware, rút bài học, báo cáo hoàn tất |

> 🔑 Các hoạt động thường **lặp lại / song song**, không tuần tự tuyệt đối. Nhớ rõ: **Phân tích = cái gì**, **Thiết kế = như thế nào**.

### 1.4.2 Quy trình kiểm thử theo ngữ cảnh
Các yếu tố ngữ cảnh ảnh hưởng cách kiểm thử: **bên liên quan, thành viên nhóm, lĩnh vực nghiệp vụ, yếu tố kỹ thuật, ràng buộc dự án, yếu tố tổ chức, SDLC, công cụ**.

### 1.4.3 Sản phẩm kiểm thử (Testware) — đầu ra của mỗi hoạt động
- Lập kế hoạch → kế hoạch KT, lịch KT, danh sách rủi ro, tiêu chí bắt đầu/kết thúc.
- Giám sát & kiểm soát → báo cáo tiến độ, chỉ đạo kiểm soát.
- Phân tích → khía cạnh KT ưu tiên hóa, báo cáo lỗi cơ sở KT.
- Thiết kế → test case, test charter, hạng mục bao phủ, yêu cầu dữ liệu/môi trường.
- Triển khai → test procedure, test script (thủ công/tự động), test suite, dữ liệu, stub/driver/simulator.
- Thực thi → nhật ký kiểm thử, báo cáo lỗi.
- Hoàn tất → báo cáo hoàn tất, action items, bài học, yêu cầu thay đổi.

### 1.4.4 Khả năng truy vết (Traceability)
Truy vết giữa cơ sở KT ↔ testware ↔ kết quả ↔ lỗi. Lợi ích:
- Đánh giá **độ bao phủ** (tiêu chí bao phủ đo lường được, làm KPI).
- Phân tích **tác động thay đổi**, hỗ trợ đánh giá tuân thủ.
- Báo cáo dễ hiểu hơn cho bên liên quan.

### 1.4.5 Vai trò trong kiểm thử
| Vai trò | Trách nhiệm |
|---------|-------------|
| **Quản lý kiểm thử** (test management) | Tổng thể quy trình, đội ngũ, dẫn dắt. Tập trung: **lập kế hoạch, giám sát, kiểm soát, hoàn tất**. |
| **Thực hiện kiểm thử** (testing) | Khía cạnh **kỹ thuật**. Tập trung: **phân tích, thiết kế, triển khai, thực thi**. |

> 🔑 Một người có thể giữ cả hai vai trò. Trong Agile, một số nhiệm vụ quản lý KT do thành viên nhóm đảm nhận.

## 1.5 Kỹ năng Thiết yếu & Thực hành Tốt

### 1.5.1 Kỹ năng chung cần thiết
Kiến thức về kiểm thử · cẩn thận/tỉ mỉ/tò mò/chú ý chi tiết · **giao tiếp tốt, lắng nghe chủ động, làm việc nhóm** · tư duy phân tích/phản biện/sáng tạo · kiến thức kỹ thuật · **kiến thức nghiệp vụ (domain)**.
> 🔑 Tester thường truyền "tin xấu" → **giao tiếp** cực kỳ quan trọng (chú ý confirmation bias). Truyền đạt lỗi theo hướng **xây dựng**.

### 1.5.2 Cách tiếp cận Toàn Đội ngũ (Whole Team Approach)
- Xuất phát từ **Extreme Programming (XP)**.
- Mọi thành viên đủ kiến thức làm bất kỳ nhiệm vụ nào; **tất cả chịu trách nhiệm chất lượng**; cùng không gian làm việc → giao tiếp tốt.
- Tester hợp tác với nghiệp vụ (viết acceptance test) & lập trình viên (chiến lược KT, tự động hóa).
- 🔑 **Không phải lúc nào cũng phù hợp** — hệ thống an toàn cao có thể cần độc lập cao hơn.

### 1.5.3 Tính độc lập của kiểm thử
Các mức độ độc lập (tăng dần): **tự kiểm thử (không độc lập) → đồng nghiệp cùng nhóm (thấp) → tester ngoài nhóm cùng tổ chức (cao) → tester ngoài tổ chức (rất cao)**.
- **Lợi ích:** phát hiện loại lỗi khác (khác thiên kiến, góc nhìn); chất vấn/bác bỏ giả định.
- **Hạn chế:** cô lập khỏi nhóm dev, vấn đề giao tiếp/đối đầu; lập trình viên mất ý thức trách nhiệm chất lượng; bị xem là nút thắt cổ chai / đổ lỗi chậm trễ.
- 🔑 Độc lập **không thay thế sự am hiểu** — dev vẫn phát hiện nhiều lỗi trong code của mình.

---

# 📗 CHƯƠNG 2 — Kiểm thử Trong suốt Vòng đời PTPM

## 2.1 Kiểm thử theo Bối cảnh SDLC

- **Mô hình SDLC** = biểu diễn trừu tượng của quy trình phát triển. Ba nhóm:
  - **Tuần tự (sequential):** Waterfall, V-model.
  - **Lặp (iterative):** Spiral, Prototyping.
  - **Gia tăng (incremental):** Unified Process.
- Thực hành Agile / phương pháp: ATDD, BDD, DDD, XP, FDD, Kanban, Lean IT, Scrum, TDD.

### 2.1.1 Ảnh hưởng của SDLC đến kiểm thử
Ảnh hưởng: phạm vi & thời điểm KT · mức độ chi tiết tài liệu · lựa chọn kỹ thuật/cách tiếp cận · mức độ tự động hóa · vai trò & trách nhiệm tester.
- **Tuần tự:** giai đoạn đầu tester rà soát yêu cầu, phân tích, thiết kế; KT động thường ở giai đoạn sau.
- **Lặp/gia tăng:** mỗi chu kỳ tạo phần gia tăng → KT tĩnh & động ở mọi mức; cần phản hồi nhanh & **hồi quy nhiều**.
- **Agile:** yêu cầu thay đổi liên tục; tài liệu gọn nhẹ; tự động hóa rộng rãi; KT thủ công dùng nhiều kỹ thuật **dựa trên kinh nghiệm**.

### 2.1.2 Thực hành kiểm thử tốt (mọi SDLC)
- Mỗi hoạt động phát triển có **một hoạt động kiểm thử tương ứng**.
- Mỗi **mức kiểm thử** có mục tiêu riêng biệt (tránh trùng lặp).
- Phân tích & thiết kế test **bắt đầu ngay** trong giai đoạn phát triển tương ứng (kiểm thử sớm).
- Tester **rà soát bản nháp sớm** (hỗ trợ shift left).

### 2.1.3 Kiểm thử dẫn dắt phát triển (test-first)
| Phương pháp | Đặc điểm |
|-------------|----------|
| **TDD** (Test-Driven Development) | Test case viết trước → viết code đáp ứng → tái cấu trúc. Định hướng lập trình bằng test. |
| **ATDD** (Acceptance TDD) | Test case dựa trên **tiêu chí chấp nhận**, viết trước khi phát triển (mục 4.5.3). |
| **BDD** (Behavior-Driven Development) | Mô tả hành vi mong muốn bằng ngôn ngữ tự nhiên **Given/When/Then** → tự động chuyển thành test. |

> 🔑 Cả ba đều áp dụng **kiểm thử sớm + shift left**, test viết **trước** code, hỗ trợ mô hình lặp.

### 2.1.4 DevOps và Kiểm thử
- Phối hợp **phát triển (gồm KT) + vận hành**, cần thay đổi văn hóa; dùng **CI (tích hợp liên tục)** & **CD (phân phối liên tục)**.
- **Lợi ích KT:** phản hồi nhanh về chất lượng code; CI thúc đẩy shift left; môi trường KT ổn định; tăng khả năng quan sát đặc tính phi chức năng; giảm KT thủ công lặp lại; giảm nguy cơ lỗi hồi quy.
- **Thách thức:** phải thiết lập quy trình phân phối; duy trì công cụ CI/CD; tự động hóa tốn nguồn lực, khó thiết lập/duy trì.
- 🔑 Dù tự động hóa cao, **KT thủ công (đặc biệt góc độ người dùng) vẫn cần thiết**.

### 2.1.5 Shift Left
- = Nguyên tắc **kiểm thử sớm** — hoạt động KT tiến hành **sớm hơn** trong SDLC.
- 🔑 Shift left **KHÔNG** có nghĩa xem nhẹ KT ở giai đoạn sau.
- Thực hành: rà soát đặc tả từ góc nhìn tester · viết test trước code · dùng CI/CD · phân tích tĩnh trước KT động · **KT phi chức năng ngay từ mức thành phần**.
- Có thể tốn thêm chi phí/đào tạo ban đầu nhưng tiết kiệm về sau; cần bên liên quan **hiểu & đồng thuận**.

### 2.1.6 Retrospective & Cải tiến Quy trình
- Họp rút kinh nghiệm cuối dự án/chu kỳ/mốc phát hành. Thảo luận: **Điều gì thành công? Điều gì cần cải thiện? Làm sao áp dụng cải tiến?**
- Kết quả thường nằm trong **báo cáo hoàn tất kiểm thử**.
- Lợi ích: nâng hiệu quả/hiệu suất KT · nâng chất lượng testware · gắn kết & học hỏi · cải thiện cơ sở KT · tăng hợp tác dev–test.

## 2.2 Các Mức & Loại Kiểm thử

### 2.2.1 Các mức kiểm thử (5 mức)
| Mức | Trọng tâm |
|-----|-----------|
| **Kiểm thử thành phần** (component/unit) | Thành phần độc lập; do lập trình viên; cần test harness. |
| **Kiểm thử tích hợp thành phần** | Điểm kết nối & tương tác giữa các thành phần; phụ thuộc chiến lược (bottom-up/top-down/big-bang). |
| **Kiểm thử hệ thống** | Hành vi tổng thể end-to-end; chức năng + phi chức năng; đội độc lập. |
| **Kiểm thử tích hợp hệ thống** | Kết nối với hệ thống/dịch vụ ngoài; môi trường gần thực tế. |
| **Kiểm thử chấp nhận** | Validation & mức độ sẵn sàng triển khai; do người dùng mục tiêu. Gồm: **UAT, chấp nhận vận hành, hợp đồng, quy định, alpha, beta**. |

> Phân biệt các mức dựa trên: đối tượng KT, mục tiêu KT, cơ sở KT, lỗi & sự cố, cách tiếp cận & trách nhiệm.

### 2.2.2 Các loại kiểm thử (4 loại)
| Loại | Đánh giá |
|------|----------|
| **Chức năng** (functional) | "hệ thống **làm gì**" — tính đầy đủ, đúng đắn, phù hợp của chức năng. |
| **Phi chức năng** (non-functional) | "hệ thống hoạt động **tốt như thế nào**" — theo ISO/IEC 25010. |
| **Hộp đen** (black-box) | Dựa trên **đặc tả**; kiểm tra hành vi vs đặc tả. |
| **Hộp trắng** (white-box) | Dựa trên **cấu trúc**; đảm bảo bao phủ cấu trúc bên trong. |

**8 đặc tính chất lượng phi chức năng (ISO 25010):** hiệu năng, tương thích, khả dụng, độ tin cậy, bảo trì, tính di động, an toàn (bảo mật)... *(danh sách phi chức năng chính)*.
> 🔑 Cả 4 loại đều áp dụng được ở **mọi mức kiểm thử**.

### 2.2.3 Kiểm thử Xác nhận & Hồi quy
- **Xác nhận (confirmation):** lỗi đã sửa **thành công** chưa. (chạy lại test đã fail / bổ sung test / lặp bước tái hiện).
- **Hồi quy (regression):** thay đổi **không gây tác động tiêu cực** ở chỗ khác. Nên **phân tích ảnh hưởng** trước để xác định phạm vi.
- 🔑 Bộ test hồi quy tăng dần theo thời gian → **rất phù hợp tự động hóa** (tích hợp vào CI/CD).

## 2.3 Kiểm thử Bảo trì
- **Loại bảo trì:** sửa lỗi · cập nhật theo môi trường · cải thiện hiệu năng/khả năng bảo trì. Có bản phát hành **theo kế hoạch** & **khẩn cấp (bản vá)**.
- **Phạm vi** phụ thuộc: mức rủi ro thay đổi · kích thước hệ thống · quy mô thay đổi.
- **Yếu tố kích hoạt (triggers):**
  - **Thay đổi phần mềm** (cải tiến, sửa lỗi, vá khẩn).
  - **Nâng cấp/chuyển đổi môi trường** (đổi nền tảng, chuyển đổi dữ liệu).
  - **Ngừng sử dụng** (retirement) — kiểm thử lưu trữ & khôi phục dữ liệu.

---

# 📙 CHƯƠNG 3 — Kiểm thử tĩnh

## 3.1 Cơ bản về Kiểm thử tĩnh
- Phần mềm **không cần thực thi**. Hai hình thức: **rà soát** (thủ công) & **phân tích tĩnh** (công cụ).
- Mục tiêu: cải thiện chất lượng, phát hiện lỗi, đánh giá đặc tính (dễ đọc, đầy đủ, đúng đắn, khả năng KT, nhất quán). Áp dụng cho **cả verification & validation**.
- **Phân tích tĩnh:** phát hiện vấn đề trước KT động, ít công sức (không cần test case), thường bằng công cụ, tích hợp trong CI; đánh giá cả khả năng bảo trì & bảo mật.

### 3.1.1 Sản phẩm công việc có thể kiểm thử tĩnh
- **Rà soát:** hầu như **bất kỳ** sản phẩm nào đọc-hiểu được (yêu cầu, code, kế hoạch KT, test case, backlog, hợp đồng, mô hình...).
- **Phân tích tĩnh:** cần sản phẩm **có cấu trúc** (mô hình, mã nguồn, JSON...).
- Không phù hợp: tài liệu khó diễn giải cho người & không nên phân tích bằng công cụ (vd code chạy được của bên thứ ba vì lý do pháp lý).

### 3.1.2 Giá trị của kiểm thử tĩnh
- Phát hiện lỗi **sớm nhất** (nguyên tắc kiểm thử sớm).
- Phát hiện lỗi mà KT động **không thể** (code không bao giờ chạy, sai design pattern, lỗi trong tài liệu).
- Đánh giá chất lượng & tạo niềm tin; giúp bên liên quan **thống nhất cách hiểu**, cải thiện giao tiếp.
- 🔑 Rà soát **tốn kém**, nhưng **tổng chi phí dự án thấp hơn** vì sửa lỗi sớm rẻ hơn.

### 3.1.3 Kiểm thử tĩnh vs Kiểm thử động
| | Kiểm thử tĩnh | Kiểm thử động |
|---|---|---|
| Thực thi | Không | Có |
| Phát hiện | **Lỗi trực tiếp** | **Sự cố** (→ phân tích tìm lỗi) |
| Áp dụng | Cả sản phẩm không thực thi (tài liệu) | Chỉ sản phẩm có mã thực thi |
| Đặc tính | Không phụ thuộc thực thi (vd bảo trì) | Phụ thuộc thực thi (vd hiệu năng) |

**Lỗi dễ/rẻ phát hiện bằng KT tĩnh:** lỗi yêu cầu (mơ hồ, mâu thuẫn, thiếu sót...) · lỗi thiết kế · một số lỗi lập trình (biến chưa khởi tạo, code chết) · sai lệch tiêu chuẩn · đặc tả giao diện sai · một số lỗ hổng bảo mật (buffer overflow) · thiếu bao phủ yêu cầu.

## 3.2 Phản hồi & Quy trình Rà soát

### 3.2.1 Lợi ích phản hồi sớm & thường xuyên
Truyền đạt sớm vấn đề chất lượng; tránh làm lại tốn kém; ngăn hiểu sai yêu cầu; tập trung vào tính năng giá trị cao.

### 3.2.2 Hoạt động trong quy trình rà soát (ISO/IEC 20246)
1. **Lập kế hoạch** — xác định phạm vi, mục đích, tiêu chí kết thúc, nguồn lực.
2. **Khởi tạo rà soát** — đảm bảo mọi người & tài liệu sẵn sàng, hiểu vai trò.
3. **Rà soát cá nhân** — mỗi người rà soát độc lập, ghi lại bất thường/khuyến nghị/câu hỏi.
4. **Trao đổi & phân tích** — thảo luận bất thường (không phải mọi bất thường là lỗi), quyết định trạng thái & hành động.
5. **Khắc phục & báo cáo** — tạo báo cáo lỗi, đạt tiêu chí kết thúc → chấp nhận.

### 3.2.3 Vai trò trong rà soát
| Vai trò | Trách nhiệm |
|---------|-------------|
| **Quản lý** | Quyết định nội dung rà soát, cung cấp nguồn lực. |
| **Tác giả** (author) | Tạo & sửa sản phẩm được rà soát. |
| **Điều phối viên** (facilitator/moderator) | Tổ chức họp hiệu quả, môi trường an toàn. |
| **Thư ký** (scribe) | Ghi lại bất thường & quyết định. |
| **Người rà soát** (reviewer) | Thực hiện rà soát. |
| **Trưởng nhóm rà soát** (review leader) | Chịu trách nhiệm tổng thể, quyết định người tham gia, thời gian/địa điểm. |

### 3.2.4 Các loại rà soát (formal tăng dần)
| Loại | Đặc điểm chính |
|------|----------------|
| **Rà soát không chính thức** (informal) | Không quy trình cố định, không ghi nhận chính thức. Mục tiêu: phát hiện bất thường. |
| **Walkthrough** (rà soát có hướng dẫn) | **Do TÁC GIẢ chủ trì**. Đa mục tiêu: đánh giá chất lượng, đào tạo, đồng thuận, ý tưởng mới. Rà soát cá nhân trước không bắt buộc. |
| **Rà soát kỹ thuật** (technical review) | Người rà soát có **trình độ kỹ thuật**, do **điều phối viên** dẫn. Mục tiêu: đồng thuận & quyết định kỹ thuật. |
| **Đánh giá chuyên sâu** (inspection) | **Chính thức nhất**, theo đủ quy trình. Mục tiêu: **tối đa hóa phát hiện bất thường**; thu thập chỉ số cải tiến. **Tác giả KHÔNG được làm trưởng nhóm/thư ký**. |

### 3.2.5 Yếu tố thành công của rà soát
- Mục tiêu & tiêu chí kết thúc **rõ ràng, đo lường được** — 🔑 **KHÔNG lấy việc đánh giá con người làm mục tiêu rà soát**.
- Chọn loại rà soát phù hợp; rà soát từng phần nhỏ; phản hồi cho tác giả; đủ thời gian chuẩn bị; **hỗ trợ từ quản lý**; biến rà soát thành **văn hóa**; đào tạo đầy đủ; điều phối họp hiệu quả.

---

# 📕 CHƯƠNG 4 — Phân tích và Thiết kế Test case

## 4.1 Tổng quan Kỹ thuật Kiểm thử
| Nhóm | Dựa trên | Đặc điểm |
|------|----------|----------|
| **Hộp đen** (đặc tả) | Hành vi được mô tả | Test độc lập với cách lập trình; đổi code (giữ hành vi) → test vẫn dùng được. |
| **Hộp trắng** (cấu trúc) | Cấu trúc bên trong / code | Test chỉ tạo được **sau khi có** thiết kế/code. |
| **Dựa trên kinh nghiệm** | Kiến thức & kinh nghiệm tester | **Bổ trợ**; phát hiện lỗi mà hộp đen/trắng bỏ sót. |

## 4.2 Kỹ thuật Hộp đen

### 4.2.1 Phân vùng Tương đương (EP) — **K3**
- Chia dữ liệu thành **vùng tương đương**: mọi giá trị trong vùng được xử lý **giống nhau** → chỉ cần **1 test case/vùng**.
- Vùng **hợp lệ** & **không hợp lệ**. Vùng **không chồng lấn**, **không rỗng**.
- **Bao phủ 100%:** mọi vùng (kể cả không hợp lệ) được test ≥1 lần. Coverage = số vùng đã test / tổng vùng × 100%.
- Nhiều tập phân vùng → **Each Choice**: mỗi vùng trong từng tập được phủ ≥1 lần (không xét tổ hợp).

### 4.2.2 Phân tích Giá trị Biên (BVA) — **K3**
- Kiểm tra giá trị tại **biên (ranh giới)** của vùng tương đương → chỉ áp dụng cho vùng **có thứ tự**.
- Lỗi hay xảy ra khi biên đặt **sai vị trí** hoặc **bỏ sót**.
- **BVA 2 giá trị:** mỗi biên có 2 hạng mục = giá trị biên + giá trị liền kề (của vùng kề).
- **BVA 3 giá trị:** mỗi biên có 3 hạng mục = giá trị biên + 2 giá trị lân cận. **Chặt chẽ hơn** 2 giá trị.
- 🔑 Ví dụ: `if (x ≤ 10)` bị code sai thành `if (x = 10)` → BVA 2 giá trị (10, 11) **không bắt được**, nhưng x=9 (BVA 3 giá trị) **bắt được**.

### 4.2.3 Kiểm thử Bảng Quyết định — **K3**
- Dùng khi tổ hợp **điều kiện** khác nhau → **hành động** khác nhau (biểu diễn logic nghiệp vụ phức tạp).
- Hàng = điều kiện (condition) + hành động (action). Cột = một **quy tắc** (tổ hợp điều kiện duy nhất).
- **Ký hiệu điều kiện:** `T` (thỏa), `F` (không thỏa), `–` (không ảnh hưởng), `N/A` (không áp dụng). **Hành động:** `X` (xảy ra), trống (không xảy ra).
- **Limited-entry:** giá trị Boolean. **Extended-entry:** nhiều loại giá trị (khoảng, vùng, rời rạc).
- Bảng đầy đủ = mọi tổ hợp. Có thể **tối giản** (bỏ cột không khả thi, gộp cột).
- **Bao phủ 100%:** test mọi cột khả thi. 🔑 Số tổ hợp tăng **cấp số nhân** theo số điều kiện.

### 4.2.4 Kiểm thử Chuyển đổi Trạng thái — **K3**
- **Sơ đồ trạng thái:** states + transitions + events + (guard condition) + actions. Nhãn: `event [guard] / action`.
- **Bảng trạng thái:** hàng = trạng thái, cột = sự kiện; ô trống = **chuyển đổi không hợp lệ** (bảng thể hiện rõ, sơ đồ thì không).
- **Ba tiêu chí bao phủ:**
  | Tiêu chí | Hạng mục | Ghi chú |
  |----------|----------|---------|
  | **Bao phủ mọi trạng thái** | Các trạng thái | Yếu nhất — có thể đạt mà không đi hết transition. |
  | **Bao phủ chuyển đổi hợp lệ (0-switch)** | Transition hợp lệ | **Phổ biến nhất**. 100% ⇒ phủ hết trạng thái. |
  | **Bao phủ mọi chuyển đổi** | Cả hợp lệ + **không hợp lệ** | Mạnh nhất; mỗi test chỉ 1 transition không hợp lệ (tránh che lỗi). Tối thiểu cho phần mềm an toàn cao. |

## 4.3 Kỹ thuật Hộp trắng

### 4.3.1 Kiểm thử Câu lệnh & Bao phủ Câu lệnh — K2
- Hạng mục bao phủ = **câu lệnh thực thi được**. Coverage = câu lệnh đã chạy / tổng câu lệnh × 100%.
- 🔑 100% statement = mọi câu lệnh **được thực thi ≥1 lần** → nếu câu lệnh có lỗi được chạy, lỗi **có thể** lộ ra.
- 🔑 100% statement **KHÔNG** đảm bảo bắt hết lỗi (lỗi phụ thuộc dữ liệu, vd chia 0), và **KHÔNG** đảm bảo phủ hết nhánh.

### 4.3.2 Kiểm thử Nhánh & Bao phủ Nhánh — K2
- **Nhánh** = chuyển luồng điều khiển giữa 2 nút (vô điều kiện hoặc có điều kiện: if/then, switch/case, vòng lặp).
- Coverage = nhánh đã chạy / tổng nhánh × 100%.
- 🔑 **100% Branch ⇒ 100% Statement** (chiều ngược lại KHÔNG chắc). Branch mạnh hơn Statement.

### 4.3.3 Giá trị của Kiểm thử Hộp trắng
- **Điểm mạnh:** toàn bộ chương trình được xem xét → phát hiện lỗi ngay cả khi đặc tả mơ hồ/thiếu; cung cấp **thước đo bao phủ khách quan**.
- **Điểm yếu:** nếu code **thiếu** một yêu cầu, hộp trắng **không phát hiện** lỗi thiếu sót đó (đó là việc của hộp đen).
- Có thể dùng trong KT tĩnh (dry run, rà soát pseudocode).

## 4.4 Kỹ thuật Dựa trên Kinh nghiệm

### 4.4.1 Đoán lỗi (Error Guessing)
- Dự đoán sai sót/lỗi/sự cố dựa vào kiến thức & kinh nghiệm về: cách hệ thống **đã hoạt động trong quá khứ** · lỗi lập trình viên hay mắc · sự cố ở hệ thống tương tự.
- **Fault attacks:** triển khai thực tế — lập danh sách lỗi có thể xảy ra → thiết kế test bắt chúng.

### 4.4.2 Kiểm thử Khám phá (Exploratory Testing)
- **Thiết kế + thực thi + đánh giá đồng thời**, vừa làm vừa tìm hiểu đối tượng KT.
- **Session-based:** giới hạn thời gian (vd 45 phút), dùng **test charter**, kết thúc bằng buổi tổng kết (debrief).
- Hữu ích khi **ít/không có tài liệu** hoặc **áp lực thời gian**; bổ trợ kỹ thuật chính quy; hiệu quả hơn nếu tester **giàu kinh nghiệm**.

### 4.4.3 Kiểm thử Dựa trên Checklist
- Thiết kế & thực thi test theo **checklist** (xây từ kinh nghiệm/điều quan trọng với người dùng/cách phần mềm hỏng).
- Checklist cần **cập nhật thường xuyên** (mục cũ giảm hiệu quả); tránh quá dài.
- Độ bao phủ cao hơn nhưng **tính lặp lại thấp hơn** (vì ở mức khái quát).

## 4.5 Cách Tiếp cận Dựa trên Cộng tác
> Khác các kỹ thuật trên (phát hiện lỗi), nhóm này tập trung **phòng tránh lỗi** qua hợp tác & giao tiếp.

### 4.5.1 Viết User Story theo Cộng tác
- **3 C's:** **Card** (thẻ mô tả) · **Conversation** (thảo luận cách dùng) · **Confirmation** (tiêu chí chấp nhận).
- Định dạng: *"Là [vai trò], tôi muốn [mục tiêu], để [giá trị nghiệp vụ]"* + tiêu chí chấp nhận.
- Nhìn từ 3 góc: **nghiệp vụ – phát triển – kiểm thử**.
- **INVEST:** Independent, Negotiable, Valuable, Estimable, Small, Testable.

### 4.5.2 Tiêu chí Chấp nhận (Acceptance Criteria)
- Điều kiện phần mềm phải đáp ứng để được chấp nhận → xem như **khía cạnh kiểm thử**.
- Dùng để: xác định phạm vi story · đồng thuận · mô tả kịch bản hợp lệ & không hợp lệ · cơ sở KT chấp nhận · hỗ trợ lập kế hoạch/ước lượng.
- **Hai dạng phổ biến:** **hướng kịch bản** (Given/When/Then) · **hướng quy tắc** (gạch đầu dòng / bảng input–output).

### 4.5.3 ATDD — **K3**
- Phương pháp **test-first**: test case tạo **trước** khi lập trình user story, bởi nhiều góc nhìn (khách hàng, dev, tester).
- **Quy trình:** (1) buổi làm việc nhóm về đặc tả (phân tích user story & tiêu chí chấp nhận, xử lý thiếu sót/mơ hồ) → (2) tạo test case dựa trên tiêu chí chấp nhận.
- Thứ tự test: **hợp lệ (positive)** trước → **không hợp lệ (negative)** → **phi chức năng**.
- Test gồm precondition, dữ liệu đầu vào, postcondition; phủ mọi khía cạnh story, không vượt phạm vi, không trùng lặp.

---

# 📓 CHƯƠNG 5 — Quản lý các Hoạt động Kiểm thử

## 5.1 Lập Kế hoạch Kiểm thử

### 5.1.1 Mục đích & nội dung kế hoạch kiểm thử
- Mô tả mục tiêu, nguồn lực, quy trình; ghi lại cách & lịch đạt mục tiêu; là phương tiện **giao tiếp**; chứng minh tuân thủ chính sách/chiến lược KT.
- **Nội dung điển hình:** bối cảnh KT · giả định & ràng buộc · bên liên quan · truyền thông · danh sách rủi ro · **phương pháp tiếp cận KT** (mức, loại, kỹ thuật, tiêu chí bắt đầu/kết thúc, độ độc lập, chỉ số, dữ liệu, môi trường) · ngân sách & lịch.

### 5.1.2 Đóng góp của tester trong lập kế hoạch Iteration & Release
- **Release planning:** hướng đến bản phát hành; tester viết user story & tiêu chí chấp nhận, phân tích rủi ro, ước lượng, xác định cách tiếp cận KT.
- **Iteration planning:** hướng đến từng vòng lặp; tester phân tích rủi ro chi tiết, phân tách nhiệm vụ KT, ước lượng công sức.

### 5.1.3 Tiêu chí Bắt đầu & Kết thúc
- **Tiêu chí bắt đầu (entry):** điều kiện tiên quyết để bắt đầu hoạt động (nguồn lực, testware, chất lượng ban đầu — vd smoke test đạt).
- **Tiêu chí kết thúc (exit):** điều phải đạt để tuyên bố hoàn thành (thước đo bao phủ, số lỗi còn lại, tiêu chí "có/không").
- 🔑 **Hết thời gian/ngân sách** cũng là tiêu chí kết thúc hợp lệ (nếu bên liên quan chấp nhận rủi ro).
- Agile: **Definition of Done (DoD)** = tiêu chí kết thúc · **Definition of Ready (DoR)** = tiêu chí bắt đầu.

### 5.1.4 Kỹ thuật Ước lượng — **K3**
| Kỹ thuật | Nhóm | Cách làm |
|----------|------|----------|
| **Dựa trên tỷ lệ** (ratio-based) | Số liệu | Tỷ lệ chuẩn từ dự án cũ (vd dev:test = 3:2 → dev 600 ngày → test 400 ngày). |
| **Ngoại suy** (extrapolation) | Số liệu | Đo sớm trong dự án, ngoại suy phần còn lại (vd TB 3 chu kỳ gần nhất). Hợp mô hình lặp. |
| **Wideband Delphi** | Chuyên gia | Chuyên gia ước lượng độc lập → thảo luận → lặp đến đồng thuận. **Planning Poker** là biến thể (Agile). |
| **Ước lượng ba điểm** (three-point) | Chuyên gia | E = (a + 4m + b)/6; sai số SD = (b − a)/6. Vd a=6,m=9,b=18 → E=10 ± 2 giờ. |

### 5.1.5 Ưu tiên hóa Test Case — **K3**
| Chiến lược | Test nào chạy trước |
|------------|---------------------|
| **Dựa vào rủi ro** | Test phủ rủi ro cao nhất. |
| **Dựa vào độ bao phủ** | Test đạt bao phủ cao nhất (biến thể: bao phủ **bổ sung** cao nhất). |
| **Dựa vào yêu cầu** | Test liên kết yêu cầu ưu tiên cao nhất. |
> 🔑 Nếu test ưu tiên cao **phụ thuộc** test ưu tiên thấp → test thấp vẫn phải chạy trước. Xét cả tính sẵn có của nguồn lực.

### 5.1.6 Tháp Kiểm thử (Test Pyramid)
- Mô hình phân bổ test theo mức chi tiết & tự động hóa.
- **Tầng đáy:** test nhỏ, độc lập, nhanh, số lượng **nhiều** (unit/component).
- **Tầng đỉnh:** test phức tạp, end-to-end, chậm, số lượng **ít**.
- Mô hình gốc (Cohn 2009): unit / service / UI tests.

### 5.1.7 Góc phần tư Kiểm thử (Testing Quadrants) — Marick
Hai trục: **nghiệp vụ ↔ công nghệ** và **hỗ trợ nhóm ↔ đánh giá sản phẩm**.
| Quadrant | Hướng | Nội dung |
|----------|-------|----------|
| **Q1** | Công nghệ · hỗ trợ nhóm | KT thành phần & tích hợp thành phần; tự động hóa, tích hợp CI. |
| **Q2** | Nghiệp vụ · hỗ trợ nhóm | KT chức năng, examples, user story, prototype, API; kiểm tra tiêu chí chấp nhận. |
| **Q3** | Nghiệp vụ · đánh giá sản phẩm | KT khám phá, khả dụng, UAT; hướng người dùng, thủ công. |
| **Q4** | Công nghệ · đánh giá sản phẩm | Smoke test, KT phi chức năng (trừ khả dụng); tự động hóa/công cụ. |

## 5.2 Quản lý Rủi ro
- **Hai hoạt động chính:** **Phân tích rủi ro** (nhận diện + đánh giá) & **Kiểm soát rủi ro** (giảm thiểu + giám sát).
- **Kiểm thử dựa vào rủi ro (risk-based testing):** chọn/ưu tiên/quản lý KT dựa trên phân tích & kiểm soát rủi ro.

### 5.2.1 Định nghĩa & thuộc tính rủi ro
- **Rủi ro** = sự kiện/mối nguy tiềm ẩn gây tác động bất lợi. Xác định bởi 2 yếu tố:
  - **Khả năng xảy ra** (likelihood): xác suất (0 < p < 1).
  - **Mức độ ảnh hưởng** (impact): hậu quả khi xảy ra.
- 🔑 **Mức rủi ro = Khả năng xảy ra × Mức độ ảnh hưởng.** Mức càng cao càng quan trọng.

### 5.2.2 Rủi ro Dự án vs Rủi ro Sản phẩm
| | **Rủi ro dự án** | **Rủi ro sản phẩm** |
|---|---|---|
| Liên quan | Quản lý & kiểm soát dự án | Đặc tính chất lượng sản phẩm (ISO 25010) |
| Ví dụ | Chậm bàn giao, thiếu kỹ năng, mâu thuẫn, vấn đề nhà cung cấp | Thiếu/sai chức năng, tính toán sai, lỗ hổng bảo mật, hiệu năng kém |
| Hậu quả | Ảnh hưởng tiến độ/ngân sách/phạm vi | Người dùng không hài lòng, mất doanh thu/danh tiếng, phạt pháp lý, thương tích |

### 5.2.3 Phân tích Rủi ro Sản phẩm
- Mục tiêu: nâng nhận thức rủi ro & tập trung nguồn lực KT để **giảm rủi ro còn lại**. Nên bắt đầu **sớm**.
- Gồm: **nhận diện rủi ro** (liệt kê — brainstorming, phỏng vấn, sơ đồ nhân-quả) & **đánh giá rủi ro** (phân loại, xác định khả năng/ảnh hưởng/mức, ưu tiên hóa).
- Cách tiếp cận: **định lượng** (nhân khả năng × ảnh hưởng) · **định tính** (ma trận rủi ro) · kết hợp.
- Ảnh hưởng: phạm vi KT, mức & loại KT, kỹ thuật & độ bao phủ, ước lượng nguồn lực, ưu tiên phát hiện lỗi nghiêm trọng sớm.

### 5.2.4 Kiểm soát Rủi ro Sản phẩm
- = **Giảm thiểu** (mitigation) + **Giám sát** (monitoring) rủi ro.
- **Lựa chọn ứng phó:** giảm thiểu bằng kiểm thử · **chấp nhận** · **chuyển giao** · **lập kế hoạch dự phòng**.
- Hành động giảm thiểu qua KT: chọn tester phù hợp · mức độ độc lập phù hợp · rà soát & phân tích tĩnh · kỹ thuật & bao phủ phù hợp · loại KT phù hợp · KT động (gồm hồi quy).

## 5.3 Giám sát, Kiểm soát & Kết thúc Kiểm thử
- **Giám sát (monitoring):** thu thập thông tin về hoạt động KT → đánh giá tiến độ & tiêu chí kết thúc.
- **Kiểm soát (control):** dùng thông tin giám sát → ra **chỉ đạo điều chỉnh** (đổi ưu tiên test, đánh giá lại tiêu chí, điều chỉnh lịch, bổ sung nguồn lực).
- **Kết thúc (completion):** thu thập dữ liệu, tổng hợp kinh nghiệm & testware tại các mốc.

### 5.3.1 Chỉ số Kiểm thử (Test Metrics)
Tiến độ dự án · tiến độ KT (test đã chạy/đạt/không đạt) · chất lượng sản phẩm · **lỗi** (số lượng, mật độ, tỷ lệ phát hiện) · rủi ro (mức còn lại) · **độ bao phủ** · chi phí.

### 5.3.2 Báo cáo Kiểm thử
| | **Báo cáo tiến độ** (progress) | **Báo cáo kết thúc** (completion) |
|---|---|---|
| Khi nào | **Định kỳ** trong quá trình (hàng ngày/tuần) | Khi hoàn tất (một lần) |
| Mục đích | Hỗ trợ **kiểm soát** liên tục | Tổng hợp một hoạt động KT |
| Tính chất | Thường xuyên, **ít trang trọng** | Theo biểu mẫu, **trang trọng** |

Nội dung tùy **đối tượng nhận** (bên liên quan khác nhau cần thông tin khác nhau).

### 5.3.3 Truyền đạt Trạng thái Kiểm thử
Cách: giao tiếp bằng lời · **bảng điều khiển** (dashboard, burn-down) · kênh điện tử (email/chat) · tài liệu trực tuyến · báo cáo chính thức. Nhóm **phân tán** → hình thức trang trọng hơn.

## 5.4 Quản lý Cấu hình (Configuration Management)
- Cung cấp cách **xác định – kiểm soát – theo dõi** testware như các **hạng mục cấu hình**.
- Hạng mục được duyệt → **phiên bản chuẩn (baseline)**, chỉ đổi qua **kiểm soát thay đổi chính thức**.
- Đảm bảo: định danh duy nhất, kiểm soát phiên bản, theo dõi thay đổi, **truy vết** → hỗ trợ tái hiện kết quả KT. Trong DevOps thường **tự động hóa**.

## 5.5 Quản lý Lỗi (Defect Management) — báo cáo lỗi **K3**
- Bất thường (anomaly) có thể là lỗi thật, **dương tính giả (false positive)**, hoặc yêu cầu cải tiến.
- **Luồng xử lý:** ghi nhận → phân tích & phân loại → quyết định (sửa/giữ) → **đóng**. Lỗi từ KT tĩnh cũng xử lý tương tự.
- **Mục tiêu báo cáo lỗi:** cung cấp thông tin để sửa · theo dõi chất lượng · ý tưởng cải tiến quy trình.
- **Nội dung báo cáo lỗi (KT động):** Bug ID · tiêu đề tóm tắt · ngày/người/vai trò báo cáo · đối tượng & môi trường KT · **bối cảnh** · **mô tả tái hiện** (các bước, log, ảnh chụp) · **kết quả mong đợi vs thực tế** · **mức độ nghiêm trọng** · **mức độ ưu tiên** · **trạng thái** (open/deferred/duplicate/closed/rejected...) · tham chiếu.
> 🔑 Phân biệt: **Severity** (mức nghiêm trọng — ảnh hưởng) vs **Priority** (mức ưu tiên sửa).

---

# 📔 CHƯƠNG 6 — Công cụ Kiểm thử

## 6.1 Công cụ Hỗ trợ Kiểm thử
Các loại công cụ: **quản lý kiểm thử** (SDLC, yêu cầu, test case, lỗi, cấu hình) · **kiểm thử tĩnh** (rà soát, phân tích tĩnh) · **thiết kế & triển khai** · **thực thi & đo bao phủ** · **phi chức năng** · **DevOps** (build, CI/CD) · **cộng tác** · công cụ ảo hóa/container · công cụ khác (kể cả bảng tính).

## 6.2 Lợi ích & Rủi ro của Tự động hóa Kiểm thử
> 🔑 Chỉ **mua/triển khai công cụ không đảm bảo thành công** — cần nỗ lực triển khai, bảo trì, đào tạo.

**Lợi ích:**
- Tiết kiệm thời gian (giảm việc thủ công lặp lại — hồi quy, nhập liệu, so sánh kết quả).
- Giảm lỗi con người nhờ **nhất quán & lặp lại**.
- Đánh giá **khách quan** hơn (độ bao phủ, số liệu khó lấy thủ công).
- Dễ truy cập thông tin cho quản lý & báo cáo.
- Rút ngắn thời gian thực thi → phát hiện lỗi sớm, time-to-market nhanh.
- Giải phóng thời gian tester cho test chuyên sâu hơn.

**Rủi ro:**
- **Kỳ vọng không thực tế** về công cụ.
- **Ước lượng sai** thời gian/chi phí/công sức triển khai & bảo trì.
- Dùng công cụ nơi **KT thủ công phù hợp hơn**.
- **Phụ thuộc quá mức** vào công cụ (bỏ qua tư duy phản biện con người).
- **Phụ thuộc nhà cung cấp** (ngừng hỗ trợ, phá sản) hoặc mã nguồn mở ngừng phát triển.
- Không tương thích nền tảng; chọn công cụ không đáp ứng quy định/tiêu chuẩn an toàn.

---

## 🔗 Tài liệu liên quan trong repo
- `ISTQB_De_Cuong_On_Tap_v4.0.md` — bản đồ syllabus (mã LO + K-level + trọng số thi).
- `ISTQB_Theory_Summary_Q1-Q26.md` — tổng hợp lý thuyết theo bộ câu hỏi.
- `ISTQB_On_Tap_Ly_Thuyet_Full.md` — (file này) toàn bộ nội dung bài học 6 chương.
- `ontap.html` — công cụ ôn tập tương tác.

*Biên soạn bám sát nội dung & thuật ngữ tiếng Việt của đề cương chính thức ISTQB® CTFL v4.0.1.*
