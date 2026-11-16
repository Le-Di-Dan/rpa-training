# Module 03 — Python, dữ liệu, REST API, SQL cho automation

- **Tầng**: Quan trọng · **Cấp độ đích**: L3
- **Giờ ước tính**: 24 · **Điều kiện tiên quyết**: 01, 02
- **Liên quan chứng chỉ**: không
- **Tài liệu chính hãng gốc**: https://docs.python.org/3/tutorial/ · https://requests.readthedocs.io/ · https://openpyxl.readthedocs.io/ · https://playwright.dev/python/

## Sau module này bạn sẽ làm được
1. Viết script Python đọc/ghi CSV, Excel
2. Gọi REST API, xử lý JSON, xác thực bằng token
3. Truy vấn SQL cơ bản
4. Viết script có logging, xử lý lỗi, retry, chạy lại an toàn (idempotent)
5. Hiểu selector & wait khi tự động hoá giao diện web

## Danh sách bài học
| # | Bài | Mục tiêu (1 dòng) | Giờ | Trạng thái file |
|---|---|---|---|---|
| 01 | Python cho người đã biết JavaScript | Cài đặt, venv, cú pháp đối chiếu JS | 2 | chưa viết |
| 02 | Làm việc với file CSV & Excel | csv, openpyxl, đường dẫn file | 2 | chưa viết |
| 03 | REST API & JSON với requests | GET/POST/PUT, status code, token — đối chiếu axios | 2 | chưa viết |
| 04 | SQL cơ bản với SQLite | SELECT, WHERE, JOIN, INSERT, UPDATE | 2 | chưa viết |
| 05 | Regex & làm sạch dữ liệu | Kiểm tra email, mã nhân viên, chuẩn hoá chuỗi | 1.5 | chưa viết |
| 06 | Logging, exception, retry | logging, try/except, retry có giới hạn, idempotency | 1.5 | chưa viết |
| 07 | Tự động hoá giao diện web bằng code | Selector bền vững, auto-wait, vì sao bot click hụt (Playwright Python) | 2 | chưa viết |

## Bài tập
| Mã | Tên | Loại (lab/debug/tư duy/project) | Bắt buộc | Cấp độ chứng minh |
|---|---|---|---|---|
| ex01 | Excel → REST API → báo cáo (lc-admin) | lab | ✅ | L2 |
| ex02 | Debug script tự động hoá lỗi | debug | ✅ | L3 |
| ex03 | Tự động hoá giao diện web lc-admin | project | ✅ | L3 |

## Definition of Done
- [ ] Tất cả bài tập bắt buộc đạt ≥ 80/100 + vấn đáp
- [ ] Quiz module ≥ 80% (`/on-tap module 03`)
- [ ] Script xử lý 20 request (có dòng lỗi), 0 cấp sai, có báo cáo + log, chạy lại không cấp trùng
- [ ] Sửa ≥ 4/5 lỗi trong bài debug
