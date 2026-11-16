# Module 01 — Nền tảng RPA

- **Tầng**: Cốt lõi (khái niệm) · **Cấp độ đích**: L3
- **Giờ ước tính**: 12 · **Điều kiện tiên quyết**: không
- **Liên quan chứng chỉ**: không
- **Tài liệu chính hãng gốc**: https://help.nintex.com/en-US/kryonrpa/current/ (đối chiếu docs UiPath/Power Automate cho khái niệm chung)

## Sau module này bạn sẽ làm được
1. Giải thích RPA là gì, khi nào nên/không nên dùng, khác gì tích hợp API và workflow
2. Mô tả kiến trúc một nền tảng RPA (Studio, Robot attended/unattended, Server/Orchestrator, queue) và ánh xạ sang Nintex
3. Đánh giá, chấm điểm và chọn quy trình đáng tự động hoá, tính ROI
4. Viết PDD (Process Definition Document) cho một quy trình thật

## Danh sách bài học
| # | Bài | Mục tiêu (1 dòng) | Giờ | Trạng thái file |
|---|---|---|---|---|
| 01 | RPA là gì và khi nào nên dùng | Phân biệt RPA với API integration, workflow, script; nhận ra quy trình hợp với RPA | 1.5 | chưa viết |
| 02 | Kiến trúc nền tảng RPA | Studio, Robot attended/unattended, Server/Orchestrator, queue — ánh xạ Nintex/UiPath/Power Automate | 1.5 | chưa viết |
| 03 | Bot nhìn ứng dụng như thế nào | Selector/DOM, UI Automation, nhận diện hình ảnh, OCR — vì sao bot hay 'click hụt' | 1.5 | chưa viết |
| 04 | Vòng đời dự án RPA | Discovery → đánh giá → PDD → SDD → phát triển → UAT → triển khai → hypercare | 1.5 | chưa viết |
| 05 | Chọn quy trình & tính ROI | Ma trận tiêu chí, ước tính giờ tiết kiệm/FTE, rủi ro | 1.5 | chưa viết |
| 06 | Thiết kế bot bền vững | Business vs system exception, retry, logging, idempotency, bảo mật credential | 1.5 | chưa viết |

## Bài tập
| Mã | Tên | Loại (lab/debug/tư duy/project) | Bắt buộc | Cấp độ chứng minh |
|---|---|---|---|---|
| ex01 | Đánh giá 5 quy trình ứng viên tự động hoá | tư duy | ✅ | L2 |
| ex02 | PDD cho quy trình phân quyền user | tư duy/project | ✅ | L3 |

## Definition of Done
- [ ] Tất cả bài tập bắt buộc đạt ≥ 80/100 + vấn đáp
- [ ] Quiz module ≥ 80% (`/on-tap module 01`)
- [ ] Chấm điểm ≥ 5 quy trình theo ma trận tiêu chí, chọn 1 quy trình có tính ROI
- [ ] PDD có As-Is, To-Be, ≥ 5 ngoại lệ, số liệu ước tính
