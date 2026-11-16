# Nintex RPA — Sự thật sản phẩm đã kiểm chứng

> Ngày nghiên cứu: 2026-11-16. Mọi thông tin dưới đây lấy từ trang chính hãng Nintex (nintex.com, help.nintex.com, community.nintex.com) đã đọc trực tiếp trong ngày này. Số thứ tự `[n]` trỏ tới mục **Nguồn** ở cuối file.
> Chỗ nào không đọc được trang gốc thì ghi rõ **chưa xác minh**.

## 0. Lưu ý quan trọng: Nintex có HAI sản phẩm RPA khác nhau

| | **Nintex RPA** (trước là Kryon RPA) | **Nintex Foxtrot RPA** (trước là Nintex RPA LE) |
|---|---|---|
| Nguồn gốc | Mua lại Kryon, công bố 15/02/2022 [17] | Release notes ghi "Nintex RPA LE is now Nintex Foxtrot RPA" [5] |
| Thành phần chính | RPA Server, Database, Studio, Attended/Unattended Robots, Admin Tool, Console Plus, System Manager [3][4] | Nintex RPA Central, Nintex Bot, Foxtrot RPA Unlocker, RPA Chrome Extension, Central SQL Configuration Tool [5] |
| Phiên bản mới nhất (theo release notes) | **26.6** (ghi "June 2026", được gắn nhãn "Latest release"); 25.11.2 (July 2026, chỉ sửa lỗi phía client) [4][6] | **Nintex RPA Central 4.0.0 + Nintex Bot 18.0.0** (26/05/2026) [5] |
| Docs | `help.nintex.com/en-US/kryonrpa/<version>/...` | `help.nintex.com/en-US/rpa/...` |
| Connector trong Nintex Automation Cloud | "Nintex RPA" connector [14] | "Nintex Foxtrot RPA" connector (riêng biệt) [14] |

**Hệ quả cho người học:** Trong tin tuyển dụng / công ty nói "Nintex RPA" thì gần như chắc là dòng **Kryon** (Studio + Robot + Console). Cần hỏi công ty đang dùng dòng nào, phiên bản nào (vd 24.4, 25.11, 26.6), vì UI và docs khác nhau giữa các phiên bản. Phần còn lại của tài liệu tập trung vào dòng Kryon, trừ khi ghi khác.

## 1. Kiến trúc & thành phần (Nintex RPA – dòng Kryon)

Trang System Architecture bản 25.11 liệt kê [3]:

- **RPA Server** và **Database**: thành phần on-premises (cài trên máy chủ của doanh nghiệp).
- **Studio** (Nintex Studio): công cụ để "create and manage automation content for Nintex Robots" [9]. Developer **ghi (record)** các **wizard** trong Studio; wizard là "an intelligent pre-developed script" được lưu trên RPA Server và robot chạy nó [9].
- **Unattended and Attended Robots**:
  - *Unattended robot*: chạy trên máy ảo (VM), làm việc lặp lại khối lượng lớn, không cần người [8].
  - *Attended robot*: chạy nền trên máy nhân viên, giúp khi được gọi hoặc khi một app/màn hình được theo dõi xuất hiện (qua **Sensors**) [8]. Hai chế độ chạy wizard: **Do It** (robot tự thao tác) và **Guide Me** (robot chỉ chỗ cho người bấm/gõ) [8].
- **Admin Tool**: quản trị (bản 25.11 thêm tìm kiếm user) [3][7].
- **Console Plus**: giao task cho robot; có thể thay bằng **Nintex Public API** [8]. Bản 25.11 thêm xoá nhiều task một lần [7].
- **System Manager**: công cụ cài đặt/nâng cấp/sửa/gỡ RPA Server (bản 2.0 ra cùng 25.11) [7].
- **Nintex Assistant** và **DAC (Dynamic Advanced Commands)**: được nhắc trong release notes [4]; bản 26.6 thêm "Auto run wizard at Assistant start" và "Seamless DAC install and sync from server to client" [6].
- **SEQ**: log server, nằm trong cấu hình server (xem mục 2) [2].

Mốc phiên bản gần đây (theo release notes) [4]:

| Phiên bản | Thời điểm | Ghi chú đáng chú ý |
|---|---|---|
| 26.6 | June 2026 | Hỗ trợ Azure SQL database, Windows Server 2025, dùng Node.js v24 [4][6] |
| 25.11.2 | July 2026 | Sửa lỗi phía client |
| 25.11 | November 2025 | Nâng lên .NET Core 8.0.21 + .NET Framework 4.8; System Manager 2.0 [4][7] |
| 24.4.4 | July 2025 | |
| 24.4 | April 2024 | |
| 23.11 | November 2023 | Tương thích .NET 6 |

Trang release notes: <https://help.nintex.com/en-US/platform/ReleaseNotes/NintexKryonRPA.htm>. Lưu ý: release notes ghi 25.11.2 (July 2026) muộn hơn 26.6 (June 2026) nhưng 26.6 vẫn là "Latest release" — đây là bản vá cho dòng 25.11.

## 2. Yêu cầu hệ thống

### 2.1 Máy client — Studio & Robot (bản 25.11) [1]

| | Unattended Robot | Attended Robot | **Nintex Studio** |
|---|---|---|---|
| Máy | physical hoặc virtual | physical hoặc virtual | physical hoặc virtual |
| CPU | Tối thiểu Intel Core Duo 2 GHz, ≥ 4 cores; khuyến nghị i3/i5/i7 ≥ 4 cores | Như bên trái (cần i3/i5/i7 nếu dùng sensor/push) | i3/i5/i7, ≥ 4 cores |
| RAM | 4 GB (khuyến nghị 8 GB) | 4 GB (8 GB nếu dùng sensor/push) | **8 GB (khuyến nghị 12 GB)** |
| Disk | 50 GB | 50 GB | 50 GB |
| OS | Windows 10 (64-bit), **Windows 11 (64-bit)**, hoặc Windows Server được hỗ trợ | như trên | như trên |

Ghi chú khác: độ phân giải tối thiểu 1024x768; tên máy (NETBIOS) tối đa 15 ký tự; best practice là OS của máy Studio giống OS máy robot nhất có thể [1].

### 2.2 Máy chủ — RPA Server (bản 25.11) [2]

- **OS: Windows Server 2012 R2 trở lên** (khuyến nghị 2019+). Bản 26.6 thêm hỗ trợ Windows Server 2025 [6]. Trang server **không** liệt kê Windows 10/11.
- **SQL Server: có cần.**
  - Môi trường **Test**: SQL Server 2016+ **Express** ("NO license required"); installer có thể tự cài SQL Server 2017 Express.
  - **Production**: SQL Server 2016+ **Standard** (cần license), cài trước khi cài RPA Server.
  - Bản 26.6 thêm khả năng kết nối Azure SQL database [6].
- **All-in-one (một máy)**: **có**, cho môi trường Test — "RPA Server, Database, Console, and SEQ" trên cùng một máy, **4 cores / 16 GB RAM / 250 GB disk**.
- Production tối thiểu một máy: 8 cores / 24 GB / 250 GB (installer cần ≥ 100 GB).
- Trước khi cài [10]: cần quyền local admin; cần user chạy dịch vụ Nintex; nếu dùng Kerberos (SSO) thì user phải thuộc domain Active Directory; cổng mạng mở được qua wizard; có thể kết nối database ở xa.

### 2.3 Foxtrot RPA (để tham khảo) [5][13]

- Central và Bot chỉ hỗ trợ OS 64-bit.
- **Bắt buộc máy thuộc network domain** (không phải workgroup), kể cả khi cài thử; nếu không, cài đặt thất bại.
- Có thể cài Central + Bot trên một máy cho trial; installer tự cài .NET Framework 4.7.2, SQL Server 2017 Express, PowerShell 3.0.
- Không hỗ trợ VDI non-persistent/shared session.

### 2.4 macOS

Tất cả trang yêu cầu hệ thống đã đọc chỉ liệt kê Windows (client: Windows 10/11/Server; server: Windows Server). **Không có hỗ trợ macOS** trong tài liệu đã đọc.

### 2.5 Đánh giá cho máy của người học (Windows 11, 32 GB RAM, ~20 GB trống)

- Studio/Robot: Windows 11 64-bit **được hỗ trợ**, RAM 32 GB đủ; nhưng tài liệu ghi disk **50 GB** → máy chỉ còn ~20 GB trống là **chưa đạt** con số chính thức.
- RPA Server: cần **Windows Server** + SQL Server + 250 GB disk cho môi trường test → **không cài được trực tiếp** trên Windows 11 cá nhân theo tài liệu chính thức. Studio cài một mình cũng không đủ: một partner cài Studio 23.11 xong gặp lỗi "Cannot access Nintex Servers", nhân viên Nintex trả lời phải có "access to a licensed server" [11].
- Kết luận thực tế: cách khả thi nhất là **dùng server/license của công ty** (Studio trên máy cá nhân hoặc máy công ty kết nối RPA Server công ty), hoặc xin Nintex cấp trial (xem mục 3).

## 3. Quyền sử dụng để học (license / trial)

- **Trang trial chính thức**: <https://www.nintex.com/trial/free-trial-rpa/> ghi "Try Nintex RPA free for 30 days" và có nút "Start my free trial" + "Schedule a time to speak with our automation experts" [12]. Trang **không** nói trial gồm gì, giao dưới dạng gì (cloud VM hay bản tải về), có cần email công ty hay không — form không tải được khi đọc (chỉ thấy "Couldn't load the form", hướng dẫn liên hệ info@nintex.com) → **chưa xác minh** các điều kiện.
- **Mâu thuẫn**: tháng 02/2024 nhân viên Nintex trả lời trên community: "You will need access to a licensed server. Unfortunately we don't have a trial version anymore." [11]. Trang trial vẫn còn tồn tại; không rõ hiện nay trial có thực sự cấp server/license RPA cho cá nhân hay chỉ dẫn tới cuộc gọi sales.
- **Foxtrot RPA**: có thể "Request a trial license key online" qua email hoặc Account Manager [13] — đây là dòng Foxtrot, không phải Kryon.
- **Nintex Automation Cloud trial** (trên trang <https://www.nintex.com/trial/> là "Workflow and Apps Trial", 30 ngày; trang workflow trial ghi "no credit card, no fees"): **không nhắc tới RPA** trong nội dung trial [15][16]. Không có bằng chứng trial NAC bao gồm RPA.
- **Community edition / sandbox miễn phí**: **không tìm thấy** trong các trang chính hãng đã đọc.

**Khuyến nghị:** (1) hỏi công ty cấp quyền dùng Studio + một Robot trên RPA Server dev/test của công ty — đây là đường chắc chắn nhất; (2) song song, điền form trial 30 ngày (nên dùng email công ty) và hỏi rõ trial có gồm Studio + Robot không.

## 4. Đào tạo & chứng chỉ chính thức

### 4.1 Nintex University (learn.nintex.com)

- Trang sản phẩm RPA trên community liệt kê các learning path trên Nintex University [18]:
  - **"For IT Administrators"** (platform, architecture, installation, user management)
  - **"For RPA Developers"** (becoming a certified developer, RPA Studio and commands)
  - **"Additional Training"** (webinars, best practices)
- Khoá đã được công bố: "Install Nintex RPA" (cập nhật 04/2024 để dùng System Manager), "Upgrade Nintex RPA" [18].
- Nintex University chuyển sang LMS mới: khoá truy cập từ 17/09/2025 đến 02/10/2025 (không tạo user mới, không ghi danh mới trong thời gian này) [20].
- Mọi trang khoá học/chứng chỉ trên learn.nintex.com **yêu cầu đăng nhập** (redirect sang myauth.nintex.com) → **chưa xác minh** danh sách khoá chi tiết, thời lượng, ai được đăng ký (customer/partner/cá nhân).

### 4.2 Chứng chỉ Nintex RPA

Trang community RPA liệt kê 3 chứng chỉ (link exam trên learn.nintex.com) [18]:

1. **RPA Developer Certification**
2. **AA RPA Developer Certification** (cho attended automation developer; trong thread community gọi là "Nintex RPA Attended Automation Developer" certification [11])
3. **RPA Manager Certification**

- Phí: nhân viên Nintex trả lời trên community (05/11/2024): **"All certifications are free!"** [19]. Chưa xác minh lại trên trang chính thức hiện tại.
- Format thi (số câu, thời gian, điểm đạt), thời hạn hiệu lực: **chưa xác minh** (trang cần đăng nhập).
- Năm 2024 Nintex nói đang cập nhật toàn bộ đào tạo RPA, các learning path mới sẽ "include exams at the end of each path" [11].

### 4.3 Chứng chỉ Nintex liên quan khác

- **Automation Specialist I** và **Automation Specialist II Certification for Nintex Automation Cloud** (công bố 06/2024, thay cho Practitioner/Expert cũ) — không bao gồm RPA [21].
- K2 có chứng chỉ riêng (có thread community về "K2 Five certification exam") — **chưa xác minh** chi tiết.

## 5. Khả năng chính của Nintex Studio

### 5.1 Recorder & wizard

- Developer **record** wizard trong Studio; mỗi step có một **core action** (mặc định là click). Các core action dùng detected object: **Click, Hover, Detect object, Read from screen** [9][22].
- Các đối tượng được nhận diện: core action object, window visual object, object block, anchor object [22].

### 5.2 Cách bot nhận diện phần tử

- **Visual/object detection** (theo hình ảnh trên màn hình): có ngưỡng khớp (match threshold), tuỳ chọn "Match image color", vùng tìm kiếm **Click / Stripe / Full** [23]. Chi tiết thuật toán: **chưa xác minh** (trang Object Detection Criteria chưa đọc).
- **Web (HTML commands)**: dùng **"HTML Object Selector"** của Nintex để chọn phần tử; hỗ trợ **Google Chrome** và **Microsoft Chromium Edge**; cần cài **Nintex RPA Connector Extension** [24]. Tài liệu không nhắc CSS selector/XPath.
- Có thêm nhóm **UI Automation Commands**, **.NET Automation Commands**, **Java Automation Commands**, **SAP Commands** cho app desktop/doanh nghiệp [25][26].

### 5.3 Advanced Commands (bản 24.4) [25]

Advanced command được định nghĩa trong **Advanced Commands Editor** hoặc gọi từ vị trí cụ thể trong wizard; dùng để lấy dữ liệu ngoài, đọc/ghi app khác, "execute scripts, direct wizard flow using loops and conditions"; nhiều command xoay quanh **variable** [27].

14 nhóm: .NET Automation · AI-Powered Document and Text Analysis (OCR qua Microsoft Azure, cần license Microsoft) · Block · **Credentials Vault** · **Database** (chạy SQL query) · Date and Time · Digital PDF Analysis · **Flow** (điều kiện, vòng lặp, pause) · Global Variable · Mouse and Keyboard · Robotic Process Automation (thêm task vào queue, trigger từ file/folder/email/database) · Scripting · Window · **Wizard** (gồm error handling).

### 5.4 Dynamic Advanced Commands (DAC) [26]

Cập nhật được mà không cần cài lại server. Nhóm: **Email** · **Excel** · External Data · External Program · File · Folder · **HTML** · Java Automation · SAP · UI Automation · Variable.

Chi tiết đã xác minh:
- **Excel** [28]: Convert Excel to CSV, Copy from Excel, Create new Excel file, Delete from Excel, Excel column/row/worksheet actions, Paste to Excel, Query from Excel, Run macro. Hỗ trợ .xlsx/.xlsm/.xlsb/.xls/.csv/.tsv. Phần lớn **không cần cài Excel**, trừ Run macro và chọn range trong Copy/Paste.
- **HTML** [24]: Click on HTML Object, Does HTML Object Exist, Extract from HTML Table/List, Get HTML Object, Get HTML Object Text/Value, Get HTML Table, Scroll to HTML Object, Set HTML Object Value.
- **External Data** [29]: **Call REST API Method**, Query JSON, Query XML, Clipboard, Registry, Environment Variable, Windows Event Log...
- **External Program** [30]: Call Web Service Method, Get Web Page HTML, Open URL Link, Run .NET Plugin Method, Run curl Command, **Run JavaScript on Page**, Run Program, **Run Script**.
- **Run Script** hỗ trợ: **VBScript, JScript, Perl, PScript, Python** [31].
- **Email**: có nhóm Email Commands trong DAC [26]; danh sách lệnh cụ thể ở bản hiện hành **chưa xác minh**.

### 5.5 Tích hợp Nintex Automation Cloud (NAC)

- Action **"Nintex RPA - Start a Nintex RPA automation"** trong workflow NAC: cần Nintex RPA **22.9.1+**, cần **Nintex Gateway**, một **Nintex RPA connection**, wizard ở trạng thái **published**; chọn connection, automation path, **queue** bot; map input/output variable (tên biến đặt giữa hai dấu `$`, chữ thường) [14].
- Chiều ngược lại (bot gọi workflow, action "Run Workflow") được mô tả trong docs của dòng Foxtrot (`help.nintex.com/en-US/rpa/Actions/Run_Workflow.htm`) — chỉ thấy qua kết quả tìm kiếm, **chưa đọc trực tiếp**.

## 6. Vị thế thị trường

- Nintex công bố mua **Kryon** ngày **15/02/2022**, mô tả Kryon có process discovery tự động và "AI-driven attended and unattended RPA bots", nhằm mở rộng năng lực IPA của **Nintex Process Platform** [17].
- Trang sản phẩm RPA hiện nằm dưới mục **Cloud Automation** trên nintex.com; mô tả attended ("activate bots on-demand") và unattended ("bots operate independently"); RPA tích hợp native với nền tảng **CE** (Nintex Automation Cloud) và **K2**, để bot làm từng task trong workflow lớn hơn [12b].
- Release mới vẫn ra đều (25.11 tháng 11/2025, 26.6 năm 2026) [4][6][7] → sản phẩm còn được phát triển.

## Chưa xác minh được

- Nội dung trial 30 ngày Nintex RPA: giao dạng gì (cloud VM / tải về), có Studio + Robot không, có yêu cầu email công ty không, cá nhân có được cấp không. Form trên trang không tải được.
- Trial hiện còn thực sự hoạt động không (mâu thuẫn với câu trả lời "we don't have a trial version anymore" năm 2024).
- Danh sách khoá học, thời lượng, miễn phí hay trả phí, điều kiện đăng ký Nintex University hiện nay (trang cần đăng nhập).
- Format thi, số câu, thời gian, điểm đạt, thời hạn hiệu lực, phí chính thức của các chứng chỉ RPA (chỉ có câu trả lời community 11/2024 "All certifications are free!").
- RPA Server dòng Kryon có bắt buộc máy thuộc domain không (trang server 25.11 không nhắc; chỉ Kerberos cần AD).
- Tài liệu system requirements riêng cho bản 26.6.
- Danh sách lệnh Email DAC ở bản hiện hành; thuật toán chi tiết của object detection.
- Chi tiết chứng chỉ K2.
- Chưa tìm thấy Community edition / sandbox miễn phí nào cho Nintex RPA.

## Nguồn

Tất cả truy cập ngày **2026-11-16**.

1. System Requirements – Clients (25.11): <https://help.nintex.com/en-US/kryonrpa/25.11/Content/SystemArchitecture/System_Requirements_Clients.htm> (đối chiếu bản 24.4: <https://help.nintex.com/en-US/kryonrpa/24.4/Content/SystemArchitecture/System_Requirements_Clients.htm>)
2. System Requirements – Server (25.11): <https://help.nintex.com/en-US/kryonrpa/25.11/Content/SystemArchitecture/System_Requirements_old_Server.htm> (đối chiếu 24.4: <https://help.nintex.com/en-US/kryonrpa/24.4/Content/SystemArchitecture/System_Requirements_old_Server.htm>)
3. System Architecture (25.11): <https://help.nintex.com/en-US/kryonrpa/25.11/Content/SystemArchitecture/System_Architecture.htm>
4. Nintex RPA (Kryon) release notes: <https://help.nintex.com/en-US/platform/ReleaseNotes/NintexKryonRPA.htm>
5. Nintex Foxtrot RPA release notes: <https://help.nintex.com/en-US/platform/ReleaseNotes/NintexRPA.htm>
6. "Nintex RPA 26.6 has arrived!" (community, 13/07/2026): <https://community.nintex.com/rpa-8/nintex-rpa-26-6-has-arrived-74117>
7. "The RPA 2025 release has arrived" (community, 19/11/2025): <https://community.nintex.com/news-18/the-rpa-2025-release-has-arrived-73605>
8. RPA Platform (22.03): <https://help.nintex.com/en-us/kryonrpa/22.03/Content/SystemArchitecture/RPA_Platform.htm>
9. Introduction to Nintex Studio (23.11): <https://help.nintex.com/en-US/kryonrpa/23.11/Content/Studio/WindowDetectionandOptions/Introduction_to_Kryon_Studio.htm>
10. Preinstallation / Upgrade: Before you start (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/InstallationUpgrade/BeforeYouStart/Before_you_start.htm>
11. Community thread "Nintex RPA Developer Learning Path" (02/2024): <https://community.nintex.com/rpa-8/nintex-rpa-developer-learning-path-61045>
12. Trang trial RPA 30 ngày: <https://www.nintex.com/trial/free-trial-rpa/>
    12b. Trang sản phẩm RPA: <https://www.nintex.com/platforms/cloud-automation/rpa/>
13. Foxtrot – Install Nintex RPA Central and activate license key: <https://help.nintex.com/en-US/rpa/Central/Installation.htm>; Pre-installation checklist: <https://help.nintex.com/en-US/rpa/Central/Preinstallationchecklist.htm>
14. NAC action "Nintex RPA - Start a Nintex RPA automation": <https://help.nintex.com/en-us/nwc/Content/Designer/Actions/NintexRPA-StartANintexRPAAutomation.htm>
15. Trang tổng hợp trial: <https://www.nintex.com/trial/>
16. Workflow trial: <https://www.nintex.com/trial/free-trial-workflow/>
17. Press release Nintex mua Kryon (15/02/2022): <https://www.nintex.com/news/nintex-acquires-process-discovery-innovator-and-rpa-leader-kryon/>
18. Community – trang sản phẩm Nintex RPA (learning paths, certifications): <https://community.nintex.com/p/rpa>
19. Community "Nintex Certification" (05/11/2024): <https://community.nintex.com/nintex-university-117/nintex-certification-72578>
20. Community "A new era of learning is coming to Nintex University" (02/09/2025): <https://community.nintex.com/nintex-university-117/a-new-era-of-learning-is-coming-to-nintex-university-73389>
21. Community "Introducing the new Nintex Automation Cloud certifications" (18/06/2024): <https://community.nintex.com/content-corner-82/introducing-the-new-nintex-automation-cloud-certifications-62266>
22. Detected Object Types (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/Studio/ObjectDetection/Detected_Object_Types.htm>
23. Detection Match Configuration (24.4) — chỉ đọc qua đoạn trích kết quả tìm kiếm: <https://help.nintex.com/en-US/kryonrpa/24.4/Content/Studio/CoreActions/Detection_Match_Configuration.htm>
24. HTML Commands (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/AdvancedCommands/HTMLCommands/HTML_Commands.htm>
25. Advanced Commands (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/AdvancedCommands/Advanced_Commands.htm>
26. Dynamic Commands (24.4 và current): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/DynamicCommands/Dynamic_Commands.htm>, <https://help.nintex.com/en-US/kryonrpa/current/Content/DynamicCommands/Dynamic_Commands.htm>
27. Advanced Commands: Introduction (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/Studio/Bubbles/Advanced_Commands_Introduction.htm>
28. Excel commands (current): <https://help.nintex.com/en-US/kryonrpa/current/Content/AdvancedCommands/ExcelCommands/Excel_Commands.htm>
29. External Data Commands (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/AdvancedCommands/ExternalDataCommands/External_Data_Commands.htm>
30. External Program Commands (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/AdvancedCommands/ExternalProgramCommands/External_Program_Commands.htm>
31. Run Script (24.4): <https://help.nintex.com/en-US/kryonrpa/24.4/Content/AdvancedCommands/ExternalProgramCommands/Run_Script.htm>
