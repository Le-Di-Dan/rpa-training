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
| Selector | Bộ chọn | Mô tả giúp bot tìm đúng một phần tử, dựa vào cấu trúc và thuộc tính | 01-03 |
| Dynamic attribute | Thuộc tính động | Thuộc tính đổi giá trị mỗi lần chạy (vd id tự sinh) — không nên dùng trong selector | 01-03 |
| Microsoft UI Automation (UIA) | (giữ nguyên) | Framework trợ năng của Windows, trình bày app desktop thành cây phần tử cho bot đọc | 01-03 |
| MSAA (Microsoft Active Accessibility) | (giữ nguyên) | Công nghệ trợ năng cũ hơn UIA, cho app rất cũ | 01-03 |
| AutomationId / Name / ControlType | (giữ nguyên) | Thuộc tính UIA: mã định danh / tên hiển thị (bị dịch theo ngôn ngữ OS) / loại control | 01-03 |
| Accessibility | Trợ năng | Hỗ trợ người khuyết tật dùng máy tính; RPA tận dụng hạ tầng này | 01-03 |
| Image recognition | Nhận diện hình ảnh | Tìm phần tử bằng cách so khớp ảnh đã lưu với màn hình | 01-03 |
| Match threshold | Ngưỡng khớp | % giống tối thiểu để robot chấp nhận đã tìm thấy đối tượng | 01-03 |
| OCR (Optical Character Recognition) | Nhận dạng ký tự quang học | Chuyển ảnh có chữ thành chữ | 01-03 |
| Coordinates | Toạ độ | Vị trí (x, y) trên màn hình; click theo toạ độ là cách giòn nhất | 01-03 |
| Core action | Hành động chính | Hành động được record của một bước trong wizard Nintex (mặc định: click) | 01-03 |
| Detected object | Đối tượng được nhận diện | Phần tử đã click lúc record, robot phải tìm lại lúc chạy | 01-03 |
| Image and text / Text only | Ảnh và chữ / Chỉ chữ | Hai phương pháp nhận diện trong Nintex Detection Match Configuration | 01-03 |
| Inner text / Outer text | Chữ bên trong / Chữ xung quanh | Chữ trong / quanh đối tượng, đọc bằng OCR để xác nhận vị trí | 01-03 |
| Search area (Click / Stripe / Full) | Vùng tìm kiếm | Nơi robot Nintex tìm đối tượng: quanh điểm click / một dải / toàn màn hình | 01-03 |
| Unique / Static / Clean | Duy nhất / Tĩnh / Sạch | 3 tiêu chí Nintex cho một đối tượng dễ nhận diện | 01-03 |
| Offset | Độ lệch | Click lệch một khoảng cố định từ một đối tượng dễ nhận diện ở gần | 01-03 |
| HTML Object Selector | Bộ chọn đối tượng HTML | Công cụ chọn phần tử web của Nintex, dùng trong HTML commands | 01-03 |
| Nintex RPA Connector Extension | Tiện ích kết nối trình duyệt | Extension cần cài để Nintex điều khiển Chrome/Edge | 01-03 |
| Timeout | Thời gian chờ tối đa | Quá thời gian này mà chưa thấy phần tử thì báo lỗi | 01-03 |
| DPI scaling | Tỉ lệ hiển thị | Thiết lập phóng to giao diện Windows (100%, 125%...) — làm đổi kích thước ảnh trên màn hình | 01-03 |
