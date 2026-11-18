# Thuật ngữ Anh – Việt — rpa-nintex

| Tiếng Anh | Tiếng Việt | Giải thích | Gặp ở bài |
|---|---|---|---|
| RPA (Robotic Process Automation) | Tự động hoá quy trình bằng robot phần mềm | Phần mềm "bắt chước" người dùng thao tác trên giao diện app/web (click, gõ, đọc màn hình) | onboarding |
| App Operations (App Ops) | Vận hành ứng dụng | Đội đảm bảo ứng dụng chạy ổn định, xử lý sự cố và yêu cầu của người dùng | onboarding |
| Attended robot | Robot có người đi kèm | Chạy trên máy nhân viên, được người kích hoạt khi cần | onboarding |
| Unattended robot | Robot tự chạy | Chạy trên máy/VM riêng, không cần người, theo lịch hoặc hàng đợi | onboarding |
| Wizard (Nintex) | Kịch bản tự động | Tên gọi một "bot script" trong Nintex RPA, được record trong Studio | onboarding |
| PDD (Process Definition Document) | Tài liệu mô tả quy trình | Mô tả quy trình hiện tại và quy trình sau tự động hoá, dùng để thống nhất với nghiệp vụ | onboarding |
| SDD (Solution Design Document) | Tài liệu thiết kế giải pháp | Mô tả kỹ thuật bot sẽ được xây như thế nào | onboarding |
| RBAC (Role-Based Access Control) | Phân quyền theo vai trò | Gán quyền cho role, gán role cho user | onboarding |
| Software robot / bot | Robot phần mềm | Chương trình thao tác máy tính thay người | 01-01 |
| UI automation | Tự động hoá qua giao diện | Điều khiển app bằng click/gõ trên giao diện (cách RPA làm) | 01-01 |
| API integration | Tích hợp qua API | Hệ thống trao đổi dữ liệu trực tiếp qua API, không qua giao diện | 01-01 |
| Rule-based | Dựa trên quy tắc | Việc mô tả được bằng "nếu… thì…", không cần phán đoán | 01-01 |
| Legacy application | Ứng dụng cũ (kế thừa) | Phần mềm cũ, thường không có API hiện đại | 01-01 |
| Fragile | Giòn, dễ vỡ | Dễ hỏng khi môi trường thay đổi nhỏ (vd giao diện đổi) | 01-01 |
| ROI (Return on Investment) | Lợi tức đầu tư | Lợi ích thu được so với công sức/chi phí bỏ ra | 01-01 |
| Do It / Guide Me | Làm hộ / Hướng dẫn | Hai chế độ chạy wizard của attended robot Nintex | 01-01 |
| Nintex Studio | (giữ nguyên) | Công cụ record và chỉnh sửa wizard | 01-01 |
| Nintex Console Plus | (giữ nguyên) | Nơi giao task cho unattended robot | 01-01 |
| Platform | Nền tảng | Tập hợp thành phần phối hợp để xây, chạy, quản lý bot | 01-02 |
| Orchestration / Orchestrator | Điều phối / Bộ điều phối | Giao việc cho robot, xếp ưu tiên, lên lịch, theo dõi | 01-02 |
| RPA Server | Máy chủ RPA | Trung tâm của Nintex RPA (on-premises): lưu wizard, điều phối task | 01-02 |
| On-premises | Tại chỗ | Cài trên máy chủ của công ty, không phải cloud của nhà cung cấp | 01-02 |
| Task | Nhiệm vụ | Một lần chạy một wizard cụ thể | 01-02 |
| Queue | Hàng đợi | Danh sách task chờ robot lấy về chạy | 01-02 |
| Trigger (time-based / event-based) | Bộ kích hoạt (theo thời gian / theo sự kiện) | Cơ chế tự tạo task: theo lịch, hoặc khi có file/folder/email/database thay đổi | 01-02 |
| Priority | Độ ưu tiên | Task ưu tiên cao chạy trước (Nintex 21.4: 10 cao nhất → 1 thấp nhất) | 01-02 |
| Pull model | Mô hình kéo | Robot tự hỏi queue và lấy task, không bị đẩy task tới | 01-02 |
| Sensor | Cảm biến | Attended robot tự kích hoạt khi nhân viên mở một app/màn hình cụ thể | 01-02 |
| Wizard catalog | Danh mục wizard | Danh sách wizard nhân viên chọn để chạy trên attended robot | 01-02 |
| Idle / Running / Stopped / Disconnected | Rảnh / Đang chạy / Đã dừng / Mất kết nối | Trạng thái robot trong Console Plus | 01-02 |
| Virtual machine (VM) | Máy ảo | Máy tính chạy bằng phần mềm trên máy thật; nơi thường đặt unattended robot | 01-02 |
| Robot account | Tài khoản robot | Tài khoản riêng cho robot đăng nhập hệ thống | 01-02 |
| Admin Tool | Công cụ quản trị | Quản lý license, Credentials Vault, user của Nintex RPA | 01-02 |
| SEQ | (giữ nguyên) | Log server đi kèm Nintex RPA | 01-02 |
| Nintex Public API | API công khai của Nintex | Cho hệ thống khác tạo task cho robot | 01-02 |
| UiPath Orchestrator | (giữ nguyên) | Bộ điều phối web của UiPath, tương đương Console Plus | 01-02 |
| Desktop flow / Cloud flow | Luồng desktop / Luồng cloud | Power Automate: bot RPA chạy trên máy / workflow chạy trên cloud | 01-02 |
| Work queue | Hàng đợi công việc | Tên gọi queue trong Power Automate | 01-02 |
