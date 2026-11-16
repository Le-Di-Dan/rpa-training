# Nintex RPA — Giá & cách có license để học

> Ngày nghiên cứu: 2026-11-16. Giá phần mềm doanh nghiệp thay đổi theo hợp đồng — **kiểm tra lại với Nintex trước khi chi tiền**.

## 1. Nintex có công bố giá không?

**Không.** Trang giá chính thức <https://www.nintex.com/pricing/> không có con số nào, chỉ có "Talk with our sales team", "Request a demo" và link "Free trials". Trang sản phẩm RPA <https://www.nintex.com/platforms/cloud-automation/rpa/> cũng không có giá, chỉ có "Book a personalized demo" và "Get a free trial".

## 2. Con số từ bên thứ ba (KHÔNG chính thức, mâu thuẫn nhau)

| Nguồn | Con số | Độ tin cậy |
|---|---|---|
| SaaSWorthy (qua kết quả tìm kiếm; trang gốc chặn 403) | "Nintex RPA Standard" $90/user/tháng, **tối thiểu 5 user**, kèm attended bot; Enterprise $140/workflow-botflow/tháng, tối thiểu 10 | Thấp — không rõ ngày, không rõ là dòng Kryon hay Foxtrot |
| TrustRadius (qua kết quả tìm kiếm; trang gốc chặn 403) | Standard $85/tháng, Enterprise $135/tháng | Thấp |
| Capterra / Software Advice (ghi "provided by vendor", trang ~2022) | Standard "starting under $850/month" cho unlimited users + 10 botflows; Enterprise "under $1250/month"; tính theo năm | Trung bình nhưng **cũ (2022)**, "botflow" là khái niệm của dòng Foxtrot / Nintex Automation Cloud, có thể không áp dụng cho Nintex RPA (Kryon) |
| Vendr (qua kết quả tìm kiếm; trang gốc chặn 403) | License tách riêng cho phát triển bot và chạy bot; unattended bot thường đắt gấp 2–3 lần attended | Thấp |

Quy đổi thô theo các con số trên: **tối thiểu khoảng 450–850 USD/tháng, thanh toán theo năm (≈ 5.000–10.000 USD/năm)**. Đây là ước lượng từ nguồn không chính thức, chưa xác minh.

## 3. Cá nhân có mua được không?

- **Không tìm thấy** gói cá nhân, gói developer/học tập, hay Community edition trên trang chính hãng (xem thêm `nintex-product-facts.md` mục 3).
- Mọi kênh mua đều qua **sales / partner**, hợp đồng doanh nghiệp, tính theo năm.
- Nintex RPA (dòng Kryon) còn cần **RPA Server tự cài**: Windows Server + SQL Server; môi trường test all-in-one cần **4 cores / 16 GB RAM / 250 GB disk** (help.nintex.com, bản 25.11). Kể cả có license, máy của người học (còn ~20 GB trống) cũng chưa đủ ổ cứng.
- Không tìm thấy Nintex RPA trên Azure Marketplace / AWS Marketplace (listing AWS có tên Nintex là K2, sản phẩm khác).
- Đã thử đọc tài liệu chính hãng "Nintex Product Definitions" (PDF, nintex.com/wp-content/uploads/2024/10/) — không trích xuất được văn bản. Kết quả tìm kiếm trích: "each Nintex RPA Standard Bot is assigned to one Nintex RPA User and one Machine" — **chưa đọc trực tiếp**.

## 4. Kết luận & khuyến nghị

Với ngân sách "vài chục USD", **mua license Nintex RPA cá nhân là không khả thi**: giá ước tính hàng nghìn USD/năm, bán theo hợp đồng doanh nghiệp, và phải tự dựng server.

Các đường thay thế, xếp theo khả năng thành công:
1. **Xin công ty**: công ty đã có license + RPA Server. Đề xuất với leader: cấp tài khoản Studio trên môi trường **dev/test** (không phải production), hoặc một máy học tập được phép dùng ngoài giờ, hoặc tài khoản Nintex University theo license công ty (khoá học + chứng chỉ thường gắn với tài khoản customer/partner).
2. **Trial 30 ngày chính thức** (miễn phí): <https://www.nintex.com/trial/free-trial-rpa/> — nên đăng ký bằng email công ty; hỏi rõ trial có gồm Studio + Robot + server (hay cloud VM) không. Lưu ý mâu thuẫn: năm 2024 nhân viên Nintex nói "we don't have a trial version anymore".
3. **Hỏi partner Nintex của công ty** (đơn vị triển khai) về môi trường demo/sandbox cho nhân viên khách hàng.

## Nguồn (truy cập 2026-11-16)
- [Nintex Pricing (chính hãng)](https://www.nintex.com/pricing/)
- [Nintex RPA product page (chính hãng)](https://www.nintex.com/platforms/cloud-automation/rpa/)
- [Nintex RPA free trial (chính hãng)](https://www.nintex.com/trial/free-trial-rpa/)
- [Nintex Product Definitions PDF (chính hãng, chưa đọc được nội dung)](https://nintex.com/wp-content/uploads/2024/10/Nintex-Product-Definitions.pdf)
- [Community: Nintex RPA Developer Learning Path](https://community.nintex.com/rpa-8/nintex-rpa-developer-learning-path-61045)
- [SaaSWorthy — Nintex RPA pricing](https://www.saasworthy.com/product/nintex-rpa/pricing) (403, chỉ thấy qua tìm kiếm)
- [Capterra — Nintex RPA](https://www.capterra.com/p/212080/Nintex-RPA/) (403, chỉ thấy qua tìm kiếm)
- [Software Advice — Nintex RPA](https://www.softwareadvice.com/bpm/nintex-rpa-profile/) (chỉ thấy qua tìm kiếm)
- [TrustRadius — Nintex pricing](https://www.trustradius.com/products/nintex-process-platform/pricing) (403, chỉ thấy qua tìm kiếm)
- [Vendr — Nintex](https://www.vendr.com/marketplace/nintex) (403, chỉ thấy qua tìm kiếm)
- [Rework — Power Automate vs Nintex](https://resources.rework.com/tools/business-process/power-automate-vs-nintex) (chỉ thấy qua tìm kiếm)
