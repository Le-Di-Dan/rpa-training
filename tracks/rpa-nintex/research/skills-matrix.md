# Ma trận kỹ năng thị trường — RPA Developer (trọng tâm Nintex RPA, ứng dụng App Operations)

> Thị trường: Việt Nam (17 tin) + Quốc tế (29 tin) · Level: junior/middle (+ intern/unknown) · Ngày thu thập: 2026-11-16 · Làm mới tiếp theo: 2027-02-16
> Dữ liệu gốc: `postings.jsonl` (mở URL từng tin để tự kiểm chứng) · Bảng số liệu sinh bởi `.claude/scripts/skill-stats.py` · Sự thật sản phẩm Nintex: `nintex-product-facts.md`

## Kết luận nhanh

Mục tiêu của người học là **nội bộ** (qua thử việc App Ops tại công ty dùng Nintex RPA), nên tool chính được chọn theo **nhu cầu công ty**, còn dữ liệu thị trường dùng để chọn **kỹ năng nền tảng chuyển đổi được** và định hướng giai đoạn 2.

- **Cốt lõi (L4)**
  - Nhóm *RPA platform* (97.6% tin): tool phổ biến nhất thị trường là UiPath (68.3%), Power Automate (36.6%). **Tool chọn học sâu: Nintex RPA (Kryon)** — vì công ty đang dùng (ngoại lệ có chủ đích, xem bên dưới). Các khái niệm RPA chung (recorder, selector/object detection, biến, flow, error handling, attended/unattended, server/queue) được dạy theo cách chuyển đổi được sang UiPath/Power Automate.
- **Quan trọng (L3)**
  - *Programming language* (58.5%): **Python** (39%) — Nintex Run Script hỗ trợ Python; người học đã biết JavaScript (JScript / "Run JavaScript on Page" cũng dùng được).
  - *API & data formats* (48.8%): **REST API + JSON** — Nintex có Call REST API Method, Query JSON.
  - *SQL/Database* (43.9%): **SQL** cơ bản — Nintex có Database commands.
  - *Process analysis* (36.6%): phân tích quy trình, chọn quy trình đáng tự động hoá, đo ROI — rất quan trọng để "bán" ý tưởng cho leader.
  - *Version control* (36.6%): **Git** — người học đã dùng (frontend 4 năm), có thể miễn.
  - *Low-code / Power Platform* (31.7%): để giai đoạn 2 (không phục vụ mục tiêu 2 tháng).
- **Nên biết (L2)**
  - *Documentation PDD/SDD/runbook* (22%), *RPA orchestration* (22% — Orchestrator/Control Room ≈ Nintex Console Plus + queue), *Office/Excel/email automation* (22%), *Testing/UAT* (19.5%), *OCR/IDP* (22%), *Generative AI / LLM* (24.4% — xu hướng 2026), *Agile* (24.4%), *Workflow automation non-RPA* (22%).
- **Nền tảng bổ sung** (ít ghi trong tin nhưng bắt buộc cho bối cảnh App Ops):
  - **Quản lý truy cập & phân quyền (IAM/RBAC, quy trình request–approve–provision–audit)** — vì bài toán đầu tiên là bot phân quyền user.
  - **Vận hành ứng dụng cơ bản (ITIL: incident/request/change, ticket, SLA, runbook)** — người học mới vào App Ops, chưa có nền tảng này.
  - **Exception handling, logging, giám sát bot** — chỉ 12% tin ghi rõ, nhưng bot vận hành production mà không có thì sẽ hỏng âm thầm.
  - **Bảo mật cho bot**: credential vault, không hard-code mật khẩu, nguyên tắc least privilege — bot phân quyền là bot có quyền cao.
- **Chứng chỉ đạt ngưỡng (≥ 15%)**: chỉ **UiPath certification (bất kỳ)** — 28.3% (không lọc level). Không tin nào yêu cầu chứng chỉ Nintex RPA.
  - **Nintex RPA Developer Certification** (Nintex University) đưa vào lộ trình theo yêu cầu người học + là chuẩn de-facto của tool công ty dùng; theo community Nintex (11/2024) là miễn phí — **chưa xác minh** format thi.
  - UiPath certification → để giai đoạn 2.

## Cách lựa chọn tool trong mỗi nhóm

| Nhóm | Thị trường | Chọn | Lý do |
|---|---|---|---|
| RPA platform | UiPath 68% · Power Automate 37% · AA 22% · Nintex RPA 15%* | **Nintex RPA** (giai đoạn 1), UiPath hoặc Power Automate (giai đoạn 2) | Công ty (Vingroup) dùng Nintex RPA; mục tiêu là qua thử việc. *Con số 15% bị thổi phồng vì có một nhóm tìm kiếm cố ý săn tin Nintex — thực tế còn thấp hơn. |
| Ngôn ngữ | Python 39% · C# 27% · VB.NET 17% | **Python** + tận dụng JavaScript | Nintex Run Script hỗ trợ Python/JScript; Python phổ biến nhất; JS người học đã giỏi. |
| API | REST 46% | **REST + JSON** | Nintex có lệnh REST/JSON; người học đã quen fetch/axios. |
| Orchestration | UiPath Orchestrator / AA Control Room | **Nintex Console Plus + RPA Server queue** | Tương đương khái niệm; chuyển đổi được. |

## Tin có nhắc Nintex / Kryon (7/46)

| Công ty | Tin | Level | Vai trò của Nintex |
|---|---|---|---|
| CGI (Montreal) | RPA Automation Expert with Power Automate Desktop | middle | Một trong các tool chấp nhận |
| SouthState Bank (US) | Nintex RPA Team Lead | lead | Nintex RPA LE / Foxtrot (dòng khác Kryon) |
| Extraco Banks (US) | Process Improvement Specialist | middle | Nintex RPA + Nintex Workflow Cloud |
| Encora (Kuala Lumpur) | Platform Automation Engineer (RPA + Testing) | unknown | Kryon, thiên vận hành nền tảng |
| Lavu Tech Solutions (Kuala Lumpur) | Automation Test Engineer (Kryon) | middle | Kryon |
| SouthState Bank (US) | RPA Developer II | middle | "UiPath and Nintex preferred" |
| ITRadiant (Hyderabad) | Nintex Developer | middle | Nintex RPA là điểm cộng |

Không tin Việt Nam nào nhắc Nintex RPA (chỉ thấy "Nintex Workflows" trong tin SharePoint — không phải RPA).

<!-- Output của skill-stats.py (lọc level: intern, junior, middle, unknown) -->

## Mẫu dữ liệu

- Số tin tuyển dụng phân tích: **41** (lọc level: intern, junior, middle, unknown)
- Theo nguồn: himalayas: 8, greenhouse: 6, jobgether: 4, joboko: 4, itviec: 3, monster: 2, leadingtalent.ca: 1, ziprecruiter: 1, wellfound: 1, grabjobs: 1, trabajo.org: 1, diversityjobs: 1, itradiant.com: 1, lever: 1, hpt.vn: 1, vietnamworks: 1, aniday: 1, vieclam.itc.edu.vn: 1, careerviet: 1, topcv: 1
- Theo level: middle: 26, unknown: 7, junior: 7, intern: 1
- Bằng chứng: page: 31, snippet: 10 (page = đã đọc trang gốc, snippet = chỉ thấy qua kết quả tìm kiếm)

## Theo nhóm kỹ năng

| Nhóm | % tin nhắc tới | % bắt buộc | Tầng | Cấp độ đích | Tool phổ biến nhất trong nhóm |
|---|---|---|---|---|---|
| RPA platform | 97.6% | 92.7% | Cốt lõi | L4 | UiPath (68.3%), Power Automate (36.6%), RPA (chung, không ghi tool) (29.3%) |
| Programming language | 58.5% | 41.5% | Quan trọng | L3 | Python (39.0%), C# (26.8%), VB.NET (17.1%) |
| API & data formats | 48.8% | 41.5% | Quan trọng | L3 | REST API (46.3%), JSON (12.2%), System integration (9.8%) |
| SQL/Database | 43.9% | 39.0% | Quan trọng | L3 | SQL (43.9%) |
| Process analysis | 36.6% | 29.3% | Quan trọng | L3 | Process analysis (29.3%), Process mining (9.8%) |
| Version control | 36.6% | 19.5% | Quan trọng | L3 | Git (36.6%) |
| Low-code / Power Platform | 31.7% | 17.1% | Quan trọng | L3 | Power BI (14.6%), Power Apps (12.2%), Power Platform (9.8%) |
| Agile | 24.4% | 17.1% | Nên biết | L2 | Agile (24.4%), Jira (4.9%) |
| Generative AI / LLM | 24.4% | 19.5% | Nên biết | L2 | Generative AI / LLM (24.4%) |
| Office/Excel/email automation | 22.0% | 19.5% | Nên biết | L2 | Excel (12.2%), Microsoft Office/365 (9.8%), Email automation (2.4%) |
| Workflow automation (non-RPA) | 22.0% | 22.0% | Nên biết | L2 | Workflow automation (14.6%), n8n (4.9%), Zapier (2.4%) |
| RPA orchestration | 22.0% | 22.0% | Nên biết | L2 | Orchestrator / Control Room (22.0%), REFramework (17.1%) |
| OCR/IDP | 22.0% | 4.9% | Nên biết | L2 | OCR/IDP (22.0%) |
| Documentation (PDD/SDD/runbook) | 22.0% | 19.5% | Nên biết | L2 | PDD/SDD & documentation (22.0%) |
| Testing/UAT | 19.5% | 19.5% | Nên biết | L2 | Testing/UAT (19.5%) |
| CI/CD | 14.6% | 4.9% | Bỏ qua | - | CI/CD (14.6%) |
| Cloud | 12.2% | 4.9% | Bỏ qua | - | AWS (12.2%), Azure (9.8%), GCP (4.9%) |
| Exception handling & debugging | 12.2% | 12.2% | Bỏ qua | - | Exception handling (9.8%), Debugging/Troubleshooting (7.3%) |
| RPA operations & monitoring | 9.8% | 9.8% | Bỏ qua | - | RPA operations & monitoring (7.3%), Incident management (2.4%), ServiceNow (2.4%) |

## Theo từng kỹ năng / tool

| Kỹ năng | Nhóm | % tin nhắc tới | % bắt buộc | % ưu tiên | Tầng (nếu xét riêng) |
|---|---|---|---|---|---|
| UiPath | RPA platform | 68.3% | 56.1% | 12.2% | Cốt lõi |
| REST API | API & data formats | 46.3% | 41.5% | 4.9% | Quan trọng |
| SQL | SQL/Database | 43.9% | 39.0% | 4.9% | Quan trọng |
| Python | Programming language | 39.0% | 26.8% | 12.2% | Quan trọng |
| Git | Version control | 36.6% | 19.5% | 17.1% | Quan trọng |
| Power Automate | RPA platform | 36.6% | 24.4% | 12.2% | Quan trọng |
| Process analysis | Process analysis | 29.3% | 29.3% | 0.0% | Nên biết |
| RPA (chung, không ghi tool) | RPA platform | 29.3% | 24.4% | 4.9% | Nên biết |
| C# | Programming language | 26.8% | 22.0% | 4.9% | Nên biết |
| Agile | Agile | 24.4% | 17.1% | 7.3% | Nên biết |
| Generative AI / LLM | Generative AI / LLM | 24.4% | 19.5% | 4.9% | Nên biết |
| Automation Anywhere | RPA platform | 22.0% | 14.6% | 7.3% | Nên biết |
| OCR/IDP | OCR/IDP | 22.0% | 4.9% | 17.1% | Nên biết |
| Orchestrator / Control Room | RPA orchestration | 22.0% | 22.0% | 0.0% | Nên biết |
| PDD/SDD & documentation | Documentation (PDD/SDD/runbook) | 22.0% | 19.5% | 2.4% | Nên biết |
| Blue Prism | RPA platform | 19.5% | 9.8% | 9.8% | Nên biết |
| Testing/UAT | Testing/UAT | 19.5% | 19.5% | 0.0% | Nên biết |
| REFramework | RPA orchestration | 17.1% | 17.1% | 0.0% | Nên biết |
| VB.NET | Programming language | 17.1% | 17.1% | 0.0% | Nên biết |
| .NET | Programming language | 14.6% | 12.2% | 2.4% | Bỏ qua |
| CI/CD | CI/CD | 14.6% | 4.9% | 9.8% | Bỏ qua |
| Nintex RPA | RPA platform | 14.6% | 9.8% | 4.9% | Bỏ qua |
| Power BI | Low-code / Power Platform | 14.6% | 4.9% | 9.8% | Bỏ qua |
| Workflow automation | Workflow automation (non-RPA) | 14.6% | 14.6% | 0.0% | Bỏ qua |
| AWS | Cloud | 12.2% | 4.9% | 7.3% | Bỏ qua |
| Excel | Office/Excel/email automation | 12.2% | 12.2% | 0.0% | Bỏ qua |
| JSON | API & data formats | 12.2% | 12.2% | 0.0% | Bỏ qua |
| JavaScript | Programming language | 12.2% | 9.8% | 2.4% | Bỏ qua |
| Power Apps | Low-code / Power Platform | 12.2% | 4.9% | 7.3% | Bỏ qua |
| Azure | Cloud | 9.8% | 2.4% | 7.3% | Bỏ qua |
| Exception handling | Exception handling & debugging | 9.8% | 9.8% | 0.0% | Bỏ qua |
| Java | Programming language | 9.8% | 7.3% | 2.4% | Bỏ qua |
| Microsoft Office/365 | Office/Excel/email automation | 9.8% | 7.3% | 2.4% | Bỏ qua |
| Power Platform | Low-code / Power Platform | 9.8% | 7.3% | 2.4% | Bỏ qua |
| Process mining | Process analysis | 9.8% | 0.0% | 9.8% | Bỏ qua |
| System integration | API & data formats | 9.8% | 7.3% | 2.4% | Bỏ qua |
| Debugging/Troubleshooting | Exception handling & debugging | 7.3% | 7.3% | 0.0% | Bỏ qua |
| RPA operations & monitoring | RPA operations & monitoring | 7.3% | 7.3% | 0.0% | Bỏ qua |
| Chatbot | — | 4.9% | 0.0% | 4.9% | Bỏ qua |
| Dataverse | Low-code / Power Platform | 4.9% | 2.4% | 2.4% | Bỏ qua |
| Docker | — | 4.9% | 0.0% | 4.9% | Bỏ qua |
| ERP | — | 4.9% | 4.9% | 0.0% | Bỏ qua |
| GCP | Cloud | 4.9% | 0.0% | 4.9% | Bỏ qua |
| Jira | Agile | 4.9% | 2.4% | 2.4% | Bỏ qua |
| Low-code | Low-code / Power Platform | 4.9% | 4.9% | 0.0% | Bỏ qua |
| Postman | API & data formats | 4.9% | 2.4% | 2.4% | Bỏ qua |
| Power Platform ALM | — | 4.9% | 2.4% | 2.4% | Bỏ qua |
| PowerShell | Programming language | 4.9% | 2.4% | 2.4% | Bỏ qua |
| SAP | — | 4.9% | 4.9% | 0.0% | Bỏ qua |
| SDLC | — | 4.9% | 4.9% | 0.0% | Bỏ qua |
| Salesforce | — | 4.9% | 4.9% | 0.0% | Bỏ qua |
| Scripting | — | 4.9% | 4.9% | 0.0% | Bỏ qua |
| SharePoint Online | — | 4.9% | 4.9% | 0.0% | Bỏ qua |
| Test automation | — | 4.9% | 2.4% | 2.4% | Bỏ qua |
| n8n | Workflow automation (non-RPA) | 4.9% | 2.4% | 2.4% | Bỏ qua |
| AWS Lambda | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Amazon S3 | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Apps Script | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Automation CoE governance | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Automation design | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Automation scripting | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Azure AI | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Azure Data Factory | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Azure Functions | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Business process management | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| CSS | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Change management | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Citrix | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Cloud | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Cognigy | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Confluence | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Continuous Improvement | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Custom connectors | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| DAX | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Data analysis | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Druid | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Email automation | Office/Excel/email automation | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Enterprise Workflow (EWF) | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Fiserv Premier | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Google Workspace | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| HTML | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Incident management | RPA operations & monitoring | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Korean | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Lean | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Linux | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Logistics domain | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Machine Learning | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Make | Workflow automation (non-RPA) | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Microsoft Copilot | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Microsoft Dataverse | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Microsoft Fabric | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Microsoft Teams | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Nintex Automation Cloud | Workflow automation (non-RPA) | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Nintex Forms | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Nintex Workflow | Workflow automation (non-RPA) | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Nintex Workflow Cloud | Workflow automation (non-RPA) | 2.4% | 2.4% | 0.0% | Bỏ qua |
| NumPy | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| OutSystems | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| PDF automation | Office/Excel/email automation | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Pega Robotics (OpenSpan) | RPA platform | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Playwright | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Power Fx | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Power Query | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| PowerPoint | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| PySpark | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| RPA best practices | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| RPA governance | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Robocorp | RPA platform | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Selenium | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| ServiceNow | RPA operations & monitoring | 2.4% | 2.4% | 0.0% | Bỏ qua |
| SharePoint | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| SharePoint On-Prem | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Synapse | — | 2.4% | 0.0% | 2.4% | Bỏ qua |
| Teslar | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Test Driven Development | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Waterfall | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Web automation | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Windows | — | 2.4% | 2.4% | 0.0% | Bỏ qua |
| XML | API & data formats | 2.4% | 2.4% | 0.0% | Bỏ qua |
| Zapier | Workflow automation (non-RPA) | 2.4% | 0.0% | 2.4% | Bỏ qua |
| pandas | — | 2.4% | 2.4% | 0.0% | Bỏ qua |

## Chứng chỉ

- Tin có nhắc tới ít nhất 1 chứng chỉ: **39.0%** (16/41)

| Chứng chỉ | % tin nhắc tới | % bắt buộc | Đạt ngưỡng 15%? |
|---|---|---|---|
| UiPath certification (bất kỳ) | 26.8% | 9.8% | ✅ |
| Microsoft Power Platform cert (PL-xxx) | 4.9% | 2.4% | — |
| AWS Cloud Practitioner | 2.4% | 0.0% | — |
| Automation Anywhere certification | 2.4% | 0.0% | — |
| Blue Prism Developer Certification | 2.4% | 0.0% | — |
| CBAP | 2.4% | 0.0% | — |
| Lean Six Sigma | 2.4% | 0.0% | — |
| Microsoft Azure Fundamentals (AZ-900) | 2.4% | 0.0% | — |
| Nintex Certified Advanced Workflow Professional | 2.4% | 0.0% | — |
| PMI-PBA | 2.4% | 0.0% | — |
| Scrum Foundations | 2.4% | 0.0% | — |
| Security Plus certification | 2.4% | 0.0% | — |
| UiPath, Blue Prism, Microsoft Power Automate, or comparable RPA certification | 2.4% | 0.0% | — |


> Chạy không lọc level (46 tin): xu hướng tương tự — RPA platform 87%, Programming 58.7%, API 52.2%, SQL 45.7%, Process analysis 37%, Git 34.8%. UiPath certification 28.3% (đạt ngưỡng).

## Đối chiếu nguồn khác

- **Tài liệu chính hãng Nintex** (`nintex-product-facts.md`): khả năng của Nintex Studio khớp với nhóm kỹ năng thị trường cần — REST API, JSON, SQL/Database, Excel, Email, HTML/web, Run Script (Python/JScript), Credentials Vault, error handling, queue. → Học Nintex sâu vẫn rèn được đúng các kỹ năng chuyển đổi.
- **Xu hướng 2026** trong tin quốc tế: RPA kết hợp GenAI/LLM/agent (24%), Git + CI/CD cho bot. Ghi nhận cho giai đoạn 2.
- Chưa đối chiếu được roadmap.sh (không có lộ trình RPA chính thức) và khảo sát ngành (Gartner/Forrester sau paywall) — **chưa xác minh**.

## Hạn chế của dữ liệu

- Cỡ mẫu thực tế: 46 tin (41 sau lọc level) — dưới mục tiêu 50, tỷ lệ % chỉ mang tính tham khảo.
- 12/46 tin chỉ có snippet (không đọc được trang gốc).
- Việt Nam: tin RPA ít và nhiều tin đã hết hạn; LinkedIn, TopCV (403), VietnamWorks (JS) gần như không đọc được → 10/17 tin VN lấy từ nguồn ngoài danh sách (joboko, monster...). Chỉ 3/17 tin VN có ngày đăng.
- Quốc tế: LinkedIn/Indeed/Glassdoor bị chặn; nguồn chính là himalayas, greenhouse, jobgether — thiên về công ty công nghệ/remote.
- Tin có Nintex được **cố ý săn tìm** (kể cả tin cũ tới ~12 tháng) → % Nintex bị thổi phồng so với thực tế.
- 7/17 tin VN là role lân cận (Power Platform, BA có RPA) — đẩy nhóm Low-code/Power Platform lên cao.
