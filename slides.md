---
marp: true
theme: gaia
size: 16:9
paginate: true
backgroundColor: #0b0d12
color: #e6e8ec
header: 'Claude Cowork Workshop · 22/05/2026'
footer: 'nguyễn bá nghĩa · the-agents-work'
style: |
  section {
    font-family: 'Inter', 'Segoe UI', system-ui, -apple-system, sans-serif;
    font-size: 25px;
    padding: 56px 68px;
  }
  section.lead {
    text-align: left;
    padding-top: 90px;
  }
  section.cover {
    background: linear-gradient(135deg, #0b0d12 0%, #1a1d27 100%);
  }
  h1 {
    color: #ffb86c;
    font-size: 54px;
    font-weight: 800;
    letter-spacing: -1px;
    line-height: 1.05;
  }
  h2 {
    color: #8be9fd;
    font-size: 36px;
    font-weight: 700;
    margin-bottom: 14px;
  }
  h3 {
    color: #ffb86c;
    font-size: 26px;
    margin-top: 18px;
  }
  strong { color: #f8f8f2; }
  em { color: #bd93f9; font-style: normal; }
  code {
    background: #1f2230;
    color: #50fa7b;
    padding: 2px 8px;
    border-radius: 4px;
    font-size: 0.9em;
  }
  pre {
    background: #0f1117;
    border: 1px solid #2a2d39;
    border-radius: 8px;
    padding: 14px 18px;
    font-size: 20px;
  }
  pre code {
    background: transparent;
    padding: 0;
    color: #d4d4d4;
  }
  blockquote {
    border-left: 4px solid #ffb86c;
    color: #f1f5f9;
    background: #161922;
    padding: 14px 22px;
    border-radius: 4px;
    margin: 12px 0;
  }
  table {
    font-size: 21px;
    width: 100%;
    border-collapse: collapse;
  }
  th { background: #1a1d27; color: #ffb86c; font-weight: 700; }
  td, th { border: 1px solid #2a2d39 !important; padding: 8px 12px; }
  ul, ol { line-height: 1.5; }
  li { margin: 4px 0; }
  section::after {
    color: #6b7280;
    font-size: 16px;
  }
  footer, header {
    color: #6b7280;
    font-size: 14px;
  }
  .big {
    font-size: 44px;
    font-weight: 800;
    color: #50fa7b;
    line-height: 1.15;
  }
  .muted { color: #9ca3af; }
  .pill {
    display: inline-block;
    background: #1f2230;
    color: #ffb86c;
    padding: 3px 12px;
    border-radius: 999px;
    font-size: 17px;
    margin: 0 4px 4px 0;
  }
  .pill-green { background: #14322a; color: #50fa7b; }
  .pill-cyan { background: #122b33; color: #8be9fd; }
  .pill-purple { background: #221a36; color: #bd93f9; }
  .tag {
    color: #8be9fd;
    font-size: 16px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 700;
  }
  section.compact {
    font-size: 22px;
    padding: 48px 64px;
  }
  section.compact h2 { font-size: 34px; }
  section.compact h3 { font-size: 23px; }
  section.compact table { font-size: 19px; }
  section.compact pre { font-size: 17px; }
  section.compact blockquote { font-size: 21px; }
---

<!-- _class: lead cover -->
<!-- _paginate: false -->

<span class="tag">Workshop · 22:00–00:00 EDT · 22/05/2026</span>

# Claude Cowork
## Giao việc cho AI — nhận deliverable hoàn chỉnh

<br>

**nguyễn bá nghĩa** · cộng đồng Claude & AI Automation VN

<span class="pill pill-cyan">163 attendees</span> <span class="pill pill-purple">Google Meet</span> <span class="pill pill-green">Live demo + Q&A</span>

---

## Mình là ai

- **Nguyễn Bá Nghĩa** — admin cộng đồng Claude & AI Automation Việt Nam *(~100k thành viên)*
- Ship side-project bằng **Claude Code + Cowork + MCP** hằng ngày
- Tin: AI agent phải **làm được việc trên máy mình** mới đáng tiền

<br>

> Workshop tối nay không phải để hỏi "Claude là gì". Mà để **xem nó làm việc thật**, hands-on, từ A → Z. Ai theo kịp mở máy làm cùng.

---

## Agenda (2 giờ)

| # | Phần | Thời lượng |
|---|---|---|
| 1 | **Vì sao Cowork?** vấn đề & timeline | 8 phút |
| 2 | **Kiến trúc** — Levels 1-3 + Advanced | 12 phút |
| 3 | **Workflow** — plan-first, mid-steering | 8 phút |
| 4 | **Setup** từ A → Z, project đầu tiên | 12 phút |
| 5 | **Demo Library** — 10+ use case live | 45 phút |
| 6 | **Prompt patterns** — bí kíp ra output xịn | 15 phút |
| 7 | **Tips · limits · Q&A** | còn lại |

---

<!-- _class: lead -->

<span class="tag">Part 1 of 7</span>

# Vì sao Cowork?
## Vấn đề bạn đang gặp & lời giải mới

---

## Vấn đề ngầm với Chat

Bạn dùng Claude/ChatGPT mỗi ngày, nhưng:

- 🔄 **Copy-paste qua lại** giữa app & chatbot
- 📎 **Upload từng file** — limit, hết quota, không nhớ
- 🧠 **Phải brief lại** mỗi conversation
- 📤 **Output trong chat** — phải save thủ công ra file
- ⏰ Không có gì **tự chạy** sau khi đóng máy

<br>

> Bạn không cần một **chatbot thông minh hơn**. Bạn cần một **đồng nghiệp biết tự làm việc**.

---

## Cowork = bước nhảy khái niệm

| Claude Chat | Claude Cowork |
|---|---|
| Bạn **dẫn** mọi bước<br>Output là **text trong chat**<br>"Smart conversation"<br>Phải copy-paste để dùng | Bạn **mô tả mục tiêu**<br>Output là **file hoàn chỉnh**<br>"Delegate, it delivers"<br>Save trực tiếp vào folder |

<br>

<span class="big">Chat trả lời · Cowork làm việc</span>

> *"Hand off a task, get a polished deliverable."* — claude.com/cowork

---

## Timeline ra mắt

| Mốc | Sự kiện | Ý nghĩa |
|---|---|---|
| **12/01/2026** | Research preview cho Max (macOS) | Beta hẹp |
| **16/01/2026** | Mở research preview cho Pro (macOS) | Cá nhân bắt đầu dùng được |
| **17/03/2026** | Mobile control / Dispatch preview | Ra lệnh từ điện thoại |
| **09/04/2026** | **GA chính thức** trên macOS + Windows | Desktop-ready + enterprise telemetry |

<br>

> Tại event 22/05/2026, Cowork **mới GA khoảng 6 tuần**. Đây là lúc học sớm còn lợi thế.

---

## 4 con số đáng nhớ

| Con số | Vì sao nhớ |
|---|---|
| <span style="color:#50fa7b">$20/tháng</span> | Claude Pro là mức tối thiểu; Cowork đi kèm paid plan, không tách SKU riêng. |
| <span style="color:#50fa7b">Plugin marketplace</span> | Marketplace còn trẻ, số lượng đổi nhanh theo tuần. Check lại trong app trước khi demo. |
| <span style="color:#50fa7b">8 tutorial chọn lọc</span> | Bộ link chính chủ dùng trong workshop: setup, first task, customize, Sales, Legal, Marketing Ops, SMB... |
| <span style="color:#50fa7b">Vẫn có hallucinate</span> | Output legal/finance/high-stakes phải review tay, dù có cite nguồn. |

---

<!-- _class: lead -->

<span class="tag">Part 2 of 7</span>

# Kiến trúc Cowork
## Levels 1-3 + Advanced — theo Anthropic

---

## Bức tranh tổng

```
                  ┌─────────────────────────────────┐
                  │  PLUGIN (Level 3 — bundle)      │
                  │  ┌───────────────────────────┐  │
                  │  │ SKILL (Level 2 — capture) │  │
                  │  │  ┌─────────────────────┐  │  │
                  │  │  │ CONNECTORS + INSTR  │  │  │
                  │  │  │ (Level 1 — context) │  │  │
                  │  │  └─────────────────────┘  │  │
                  │  └───────────────────────────┘  │
                  └─────────────────────────────────┘
                            ↑ ADVANCED ↑
                  /schedule · Live Artifacts · Dispatch
```

> Mỗi tầng **đóng gói tầng dưới**. Lên tầng nào tuỳ độ trưởng thành.

---

## Level 1: Context & Tools

### Connectors
Kết nối các hệ thống công việc — Slack, Salesforce, Microsoft 365, Jira, QuickBooks, HubSpot, Drive... Bật từ sidebar **Customize**.

> *Claude có thể đọc dữ liệu **và ghi lại**: cập nhật ticket, soạn email, đăng bài, lưu tệp.*

### Instructions (3 tầng)
- **Global** — áp mọi project *(Settings → Cowork → Global instructions)*
- **Project** — chỉ trong project đó *(bảng phải Project)*
- **Organization** — admin enterprise set cho cả công ty

---

## Level 2: Skills — đóng gói chuyên môn

**Skill = tệp hướng dẫn cho nhiệm vụ lặp lại.**

Dùng bằng cách:
- Gõ `/skill-name` *(vd: `/brief`, `/account-research`)*
- Hoặc mô tả tự nhiên — Claude tự tìm skill phù hợp

<br>

**Cách tạo skill:**
> *"Gói những gì chúng ta vừa làm thành một skill."*

Sau đó Claude đặt tên, lưu file, gắn vào project. Lần sau gọi tên là chạy được.

---

## Level 3: Plugins — bundle to share

**Plugin = Connectors + Skills gộp lại thành 1 package.**

Anthropic ship sẵn 4 plugin chính:

| Plugin | Workflow tiêu biểu |
|---|---|
| **Sales** | `/account-research` · `/call-summary` · CRM connector |
| **Legal** | `/brief` skill · document sources · citation auto |
| **Product / Marketing Ops** | weekly review prep · metrics dashboard |
| **Operations / SMB** | QB + PayPal + HubSpot · monthly close |

---

## Advanced: 3 superpower

| Feature | Làm gì | Khi dùng |
|---|---|---|
| **`/schedule`** | Chạy prompt theo lịch (hourly/daily/weekly) | Brief sáng, report Sunday, monthly close |
| **Live Artifacts** | Dashboard / tracker pin sidebar, auto-refresh | Theo dõi metrics real-time mở-lại-là-thấy |
| **Dispatch** | Trigger task từ điện thoại → desktop làm | Đang đi cafe, ra lệnh "soạn báo cáo Q" |

<br>

> 3 cái này là khác biệt **đáng tiền** so với Chat. Đừng bỏ qua.

---

<!-- _class: lead -->

<span class="tag">Part 3 of 7</span>

# Workflow
## Cowork làm việc thế nào (chính chủ)

---

## Quy trình 3 bước

| 1. Describe | 2. Execute | 3. Review |
|---|---|---|
| Mô tả output mong muốn + nguồn dữ liệu.<br>Desktop **hoặc** điện thoại (Dispatch). | Claude lên plan → hỏi clarifying → **làm song song nhiều nguồn** → xin duyệt bước quan trọng. | Approve, redirect, hoặc để **schedule** chạy định kỳ. |

<br>

> Watch realtime hoặc đóng máy đi pha cà phê. Quay lại check.

---

## Plan-first model

```
Bạn: "Dọn folder Downloads"

Claude:  Tôi sẽ:
  1. Scan 312 file trong Downloads
  2. Tạo: Documents/, Images/, Videos/, Archives/
  3. Sort theo extension + ngày tạo
  4. Đánh dấu 14 file duplicate để review

         Approve? [Yes / Edit / Cancel]
```

**3 nút quyền lực:**

<span class="pill pill-green">✅ Yes</span> Claude chạy phần còn lại
<span class="pill pill-cyan">✏️ Edit</span> Chỉnh plan trước khi chạy
<span class="pill">❌ Cancel</span> Dừng, không động vào file

---

## Mid-task steering

Đang chạy giữa chừng → bạn vẫn **chen ngang được**:

- *"Khoan, đừng xoá cái này."*
- *"File Hợp đồng cho hết vào Legal/."*
- *"Output đổi sang Markdown thay vì PDF."*
- *"Chỉ sort 100 file mới nhất, bỏ qua phần kia."*

<br>

> Đây là điểm khác biệt **lớn nhất** với automation truyền thống (Zapier, Make, n8n):
> **Bạn can thiệp bằng ngôn ngữ tự nhiên — giữa chừng.**

---

## "Put what matters in files"

Một câu của Anthropic, vàng:

> *"Cowork doesn't remember between sessions like Chat does."*

<br>

**Hệ quả:**
- Đừng dựa vào chat history — nó **không nhớ**
- Mọi rule lâu dài → viết vào **Project Instructions** hoặc file `CLAUDE.md`
- Tài liệu tham khảo → để trong **folder project**, đừng paste
- Output muốn dùng tiếp → bắt Claude **save ra file**

---

<!-- _class: lead -->

<span class="tag">Part 4 of 7</span>

# Setup
## Từ 0 → task đầu tiên trong 15 phút

---

## Prep checklist

- [ ] **Tài khoản Claude Pro** $20/tháng *(Max $100 nếu muốn unlimited)* — claude.com/pricing
- [ ] **Claude Desktop app** *(Cowork KHÔNG có trên browser)* — claude.com/download
- [ ] OS: macOS hoặc Windows
- [ ] Máy phải **awake** khi Cowork chạy task
- [ ] **Chrome extension** "Claude in Chrome" — bắt buộc nếu muốn browser automation
- [ ] Folder sandbox riêng — gợi ý `~/Cowork-Sandbox/`

---

## Bước 1: Tạo Project đầu tiên

**Một Project = một home cho công việc.**

```
File → New Project → "Q1 Marketing Review"
   ↓
Chọn folder: ~/Documents/q1-marketing/
   ↓
Claude có quyền: đọc, ghi, tạo file trong folder này
```

<br>

> Mọi file Claude đọc (PDF, sheet, doc) hoặc tạo ra đều ở **chính folder bạn chọn**. Không upload, không cloud lạ.

---

<!-- _class: compact -->

## Bước 2: Connect tools

Sidebar phải → **Customize** → **Connectors** → bấm Authorize:

| Communication | Files & Notes | Work |
|---|---|---|
| Gmail<br>Slack<br>Outlook<br>Zoom | Google Drive<br>Notion<br>OneDrive<br>Dropbox | Salesforce<br>HubSpot<br>Jira / Linear<br>QuickBooks<br>Stripe / PayPal |

<br>

> Sau khi connect: nói *"check Slack tuần này"* — Claude tự pull, không paste.

---

## Bước 3: Viết Project Instructions

Đây là **bộ não cố định** của project. Vd:

```
Tôi là PM team Product. Khi viết report:
  - Tone: chuyên nghiệp, ngắn gọn, có số
  - Format: Markdown, H2/H3, bullet
  - Nếu thấy số liệu — luôn cite file nguồn
  - Không tự suy diễn. Không chắc → hỏi tôi.
  - Tên team: Andie, Long, Phương, Vinh
  - Save mọi output vào ./reports/YYYY-MM-DD-*.md
```

<br>

> Instructions này áp **mọi task** trong project. Đỡ phải nhắc lại mỗi prompt.

---

## Bước 4: Cài plugin

Customize → **Plugins** → browse marketplace:

- **Sales** — `/account-research`, `/call-summary`, CRM connector
- **Legal** — `/brief`, citation engine, doc sources
- **Product** — sprint review, roadmap update
- **Operations** — bookkeeping, payroll, month-end close

<br>

Hoặc cài lẻ từ **plugin marketplace** *(community-built, số lượng đổi nhanh theo tuần)*.

> **Tip:** chưa biết bắt đầu đâu → cài đúng plugin cho **nghề của bạn**, học theo workflow Anthropic đề xuất.

---

<!-- _class: lead -->

<span class="tag">Part 5 of 7</span>

# Demo Library
## 10+ use case có thật — bám docs + workflow mẫu

---

## Demo Group A — File & Document

### A1. Dọn folder Downloads (lộn xộn)

```
Prompt: "Organize my Downloads folder: move PDFs to
Documents/, images to Images/, videos to Videos/,
archives to Archives/. Rename each file với prefix
ngày hôm nay. Đánh dấu file duplicate."
```

**Output:** Folder có cấu trúc, 14 file dup được flag review.

---

## A2. Batch rename theo pattern

```
Prompt: "Rename all 50 photos in Vacation folder
theo pattern Hanoi_2026_001.jpg → Hanoi_2026_050.jpg,
sort theo thời gian chụp trong EXIF."
```

**Output:** 50 file đổi tên đúng thứ tự thời gian.

---

## A3. Drive download + organize

```
Prompt: "Download tất cả file từ folder 'Work Projects'
trên Google Drive, organize locally theo tên project,
tạo file INDEX.md liệt kê từng project + 1 dòng tóm tắt."
```

**Output:** Cấu trúc folder + index document.

---

## Demo Group B — Document Creation

### B1. PowerPoint từ outline

```
Prompt: "Create 10-slide PPT về 'remote work best
practices' — intro, 7 content slide, summary, Q&A.
Theme blue, font Inter. Save: ./remote-work-tips.pptx"
```

**Output:** File `.pptx` hoàn chỉnh, mở Keynote/PPT dùng được.

---

## B2. Blog post 1000 từ

```
Prompt: "Write 1000-word blog post: 'AI assistants —
benefits cho dân văn phòng VN'. Cấu trúc intro,
4 main points, conclusion. Save `.docx`."
```

**Output:** Bài viết format đẹp, ready-to-publish.

### B3. Invoice template Excel

```
Prompt: "Create professional invoice template Excel.
Có: business info, bill-to, items table với formula
auto tính subtotal/tax/total. Bilingual VI/EN."
```

**Output:** `invoice-template.xlsx` ready in dùng.

---

## Demo Group C — Data Processing

### C1. Expense tracker với công thức

```
Prompt: "Create expense tracking spreadsheet:
categories (Food, Transport, Entertainment, Utilities,
Health). Formula auto-sum theo tháng + biểu đồ pie
breakdown. Currency VND."
```

**Output:** Sheet với formula `SUMIF`, chart sẵn.

---

## C2. Merge 5 CSV regions

```
Prompt: "Merge 5 file CSV sales từ 5 vùng. Chuẩn hoá
date về YYYY-MM-DD, xoá duplicate, sort theo date,
add column 'region' từ tên file gốc."
```

**Output:** `sales-merged.csv` clean, ready cho analysis.

### C3. Hoá đơn ảnh → Spreadsheet

```
Prompt: "Trích xuất 30 ảnh hoá đơn trong /receipts:
ngày, nhà cung cấp, mã, số tiền (VND), loại chi phí.
Gộp 1 sheet, xoá duplicate, sort theo ngày."
```

**Output:** `chi-phi-thang-5.xlsx` đầy đủ.

---

## Demo Group D — Research

### D1. Tổng hợp 5 PDF nghiên cứu

```
Prompt: "Read 5 PDF research papers in /research-Q1,
tạo summary identifying:
  - Common themes (3-5)
  - Conflicts / disagreements
  - Key statistics
Cite từng claim với (paper, page).
Save: ./Q1-research-synthesis.md"
```

**Output:** Doc tổng hợp có chú thích học thuật chuẩn.

---

## Demo Group E — Persona Workflows

### E1. SMB — Monday Morning Brief
*(theo tut "Cowork for your small business")*

```
/schedule daily 8:00 weekdays:
  - Cash position (QuickBooks)
  - Settlements hôm qua (PayPal)
  - Pipeline status (HubSpot)
  - Lịch hôm nay (Calendar)
Tổng hợp 1 trang, gửi Slack #morning-brief.
```

> Mở máy lên đã có brief sẵn. Quyết định trong 2 phút.

---

## E2. Sales — Account research trước call
*(plugin Sales, skill `/account-research`)*

```
Pre-call:
   /account-research Acme Corp

Output trong 90 giây:
  ✓ Spend trajectory 12 tháng (CRM)
  ✓ Stakeholder map (LinkedIn + email history)
  ✓ Product adoption %
  ✓ Open deals + risk signals

Post-call:
   /call-summary [transcript]

→ Action items + internal note + draft follow-up
```

---

## E3. Marketing Ops — Weekly review tự prep
*(tut chính chủ "marketing-ops-review")*

```
/schedule sunday 17:00:
  - Pull metrics từ GA4 + HubSpot + Linear
  - Drag email feedback tag "marketing"
  - Soạn draft 1 trang detailed metrics
  - + 1 slide leadership summary
  - Flag 3 chỗ chưa rõ để team review thứ Hai
```

> Sunday Claude làm. Monday 9:00 team review — không còn "ai pull metrics?".

---

## E4. Legal — `/brief` daily
*(plugin Legal, tut chính chủ)*

```
/schedule daily 7:30:
  /brief — quét tất cả vụ việc connected sources:
    ✓ Cái gì due hôm nay
    ✓ Cái gì NEW từ hôm qua
    ✓ Urgent matters (red flag)
  Mọi claim có CITATION → click ra source line gốc
```

> Trước khi sign-off: click citation, đọc tay nguồn gốc.

---

## E5. PM — Meeting prep auto

```
"Pull all files in /ClientX-folder, tạo briefing:
  - Project status hiện tại
  - Recent updates 7 ngày
  - Pending items + owner
  - 5 talking point nên đề cập
Save ./meetings/2026-05-22-clientx-prep.md"
```

### E6. Personal — Weekly Life Review

```
/schedule sunday 20:00:
  - Email cá nhân tuần: highlight bạn bè quan trọng
  - Lịch tuần sau: conflict?
  - File chi tiêu cá nhân tuần này
  - Tổng hợp 1 trang gửi Notion 'weekly-review'
```

---

<!-- _class: lead -->

<span class="tag">Part 6 of 7</span>

# Prompt Patterns
## 5 bí kíp để ra output xịn

---

## Pattern 1: Scope chính xác

❌ *"Dọn folder của tôi"*

✅ *"Dọn folder `~/Downloads/` (chỉ files trước 01/05/2026), move PDF vào Documents/, ảnh vào Images/. Không động đến file < 7 ngày tuổi."*

<br>

> **Càng rõ scope, càng ít hallucinate.** Quy tắc: nếu một fresher nhìn vào prompt phải hỏi lại → prompt chưa đủ.

---

## Pattern 2: Reference connected tools, không paste

❌ Copy-paste 20 email vào chat

✅ *"Check Gmail tuần này, lọc tag 'feedback', tóm tắt theo nhóm: bug · feature request · complaint."*

<br>

> Sau khi đã connect Gmail/Drive/Slack — **gọi tên là dùng được**, đừng paste. Cowork tự pull đúng phạm vi.

---

## Pattern 3: Yêu cầu cite nguồn

❌ *"Viết summary các meeting Q1"*

✅ *"Viết summary các meeting Q1. **Mỗi số liệu hoặc quote phải có format `(file.md, line X)` hoặc `(meeting-2026-03-15.md)`. Nếu không tìm được nguồn — ghi `[no-source]` thay vì đoán.**"*

<br>

> Cite cưỡng bức không xoá hallucination, nhưng biến lỗi thành thứ **dễ kiểm tra**.

---

## Pattern 4: Đưa template / ví dụ output

❌ *"Viết report Q1"*

✅ *"Viết report Q1, theo template `./templates/quarterly-report-template.md`. Style giống `./reports/q4-2025.md` *(file mẫu đính kèm)*. Giữ heading + section order giống y."*

<br>

> Cho Claude **1 file mẫu** = giảm 90% nguy cơ output lệch tone/format.

---

## Pattern 5: Sign-off workflow

❌ Auto-execute hết, đêm về kiểm tra

✅ *"Plan trước → tôi approve → execute. Nếu gặp file > 10MB hoặc file `.contract.*` — **dừng, hỏi tôi**. Output cuối: draft mode trong `_drafts/`, không ghi đè bản gốc."*

<br>

> Sign-off gate = nệm an toàn cho task quan trọng. Mất 5 giây bấm Yes, đỡ 5 giờ recovery.

---

<!-- _class: lead -->

<span class="tag">Part 7 of 7</span>

# Tips · Limits · Q&A

---

## Anti-hallucinate playbook

| Vấn đề | Cách chặn |
|---|---|
| Bịa số liệu | Bắt cite `(file, line)` từng số |
| Tự suy diễn | Thêm: *"Không chắc → hỏi, đừng đoán"* |
| Output rỗng tuếch | Cho template + sample file đính kèm |
| Sửa nhầm file gốc | Bật **"draft only mode"** — output vào `_drafts/` |
| Lệch tone công ty | Pin `brand-voice.md` vào project |
| Quên rule giữa session | Đưa hết vào **Project Instructions** |

<br>

> Community estimate vẫn ghi nhận hallucination trên số liệu/citation. **Legal/finance bắt buộc review tay.**

---

## Common errors + fixes

| Lỗi | Nguyên nhân | Fix |
|---|---|---|
| *"Claude can't access my files"* | Folder chưa grant permission | System Pref → Privacy → Files & Folders → bật Claude |
| First launch chậm | Tải sandbox runtime ~1.2GB | Đợi 3-5 phút lần đầu, sau nhanh |
| Connector ngắt | OAuth token hết hạn | Customize → Connectors → Re-authorize |
| Schedule không chạy | Máy sleep | Settings → Energy Saver → Prevent sleep khi cắm sạc |
| Output trống | Prompt scope mơ hồ | Áp dụng Pattern 1: scope chính xác |

---

## Limitations cần biết trước

- 🇺🇸 **Default host US** — EU data residency chỉ có **Enterprise**
- 💻 **Chỉ Desktop app** Mac/Win — không browser, không mobile (Dispatch beta)
- 🔋 **Máy phải awake** khi task chạy
- 🐢 Task phức tạp 5-30 phút — đừng kỳ vọng instant
- 💸 Pro $20 đủ cho cá nhân — schedule dày → cân nhắc Max $100
- 🔌 Connector gaps thay đổi nhanh — thiếu native thì dùng Chrome/MCP, nhưng test kỹ quyền ghi
- 🤖 **KHÔNG tự ký hợp đồng / chuyển tiền** — bắt buộc human approval

---

## Khi nào KHÔNG nên dùng Cowork

❌ Quyết định pháp lý / tài chính **cuối cùng** *(draft OK, ký KHÔNG)*

❌ Dữ liệu siêu nhạy cảm chưa qua DPA — chờ Enterprise + BAA

❌ Task **< 30 giây** — overhead plan/approve không đáng

❌ Bạn **không có thời gian review** output — sẽ tích nợ kỹ thuật rất nhanh

❌ Việc **một lần, mơ hồ** — vẫn nên dùng **Chat**

<br>

> Quy tắc vàng: **Cowork giỏi việc lặp, có structure. Việc 1 lần, mơ hồ — dùng Chat.**

---

<!-- _class: compact -->

## Lộ trình 30 ngày

| Day 1 | Week 1 | Month 1 |
|---|---|---|
| Cài Desktop<br>Tạo 1 Project<br>Chạy 1 task duy nhất *(vd: dọn Downloads)* | Connect 3 tool: Drive + Gmail + Slack<br>Viết Project Instructions<br>Setup 1 scheduled task | Cài plugin theo nghề<br>Tự build 2-3 skill<br>Dispatch từ điện thoại<br>Train team cùng dùng |

> Mục tiêu **Month 1**: tìm 1 workflow lặp lại tiết kiệm vài giờ/tuần. Đừng scale trước khi task đầu tiên chạy ổn.

---

<!-- _class: compact -->

## Resources — 8 tutorial chọn lọc

1. **Set up Cowork to work the way you do** — `claude.com/resources/tutorials/cowork-onboarding-guide`
2. **Delegating your first task** — `.../delegating-your-first-task-in-claude-cowork`
3. **Customize Claude Cowork** — `.../customize-claude-cowork`
4. **Choosing between Cowork or Chat** — `.../choosing-between-claude-cowork-or-chat`
5. **For Sales: account research** — `.../using-claude-cowork-for-sales-account-research`
6. **For Legal: question briefing** — `.../using-claude-cowork-for-legal-question-briefing`
7. **For Marketing Ops: weekly review** — `.../using-claude-cowork-for-marketing-ops-review`
8. **For Small Business** — `.../using-claude-for-your-small-business`

---

## Resources — community deep dives

- **claudecowork.im** — unofficial guide đầy đủ, 40+ FAQ, ~30 prompt mẫu
- **datacamp.com/tutorial/claude-cowork** *(Jan 2026)* — hands-on academic
- **jeffsu.org/learn-80-of-claude-cowork-in-...** — 80/20 productivity workflow
- **YouTube · AI Foundations** — "Full Cowork Tutorial for Beginners" (33 phút)

<br>

**Repo workshop này:**
- `github.com/the-agents-work/claude-cowork-workshop`
- *Slide + ghi chú demo + tất cả link bài đọc*

---

## Q&A — câu hay được hỏi trước

- *Cowork có an toàn cho file công ty?* → **Sandboxed shell + approval per step.** Folder bạn không grant — Claude không thấy.
- *Có thay được nhân viên?* → Thay **việc lặp lại**, không thay **judgment**. Vẫn cần người review output.
- *Bao lâu thì quen?* → 2-3 ngày dùng nghiêm túc theo lộ trình 30 ngày.
- *Tiếng Việt có ổn?* → OCR + sinh tiếng Việt ổn với tài liệu rõ nguồn. Vẫn review tên riêng/số liệu.
- *Cowork vs Claude Code?* → Code cho **dev** (git/build/refactor). Cowork cho **knowledge worker** (Office/email/file/browser).
- *Có dùng được trên Linux?* → Chưa. Chỉ Mac + Windows.

---

<!-- _class: lead cover -->
<!-- _paginate: false -->

# Cảm ơn cả nhà 🙌

<br>

**Slide + repo:**
github.com/the-agents-work/claude-cowork-workshop

**Live deck (Pages):**
the-agents-work.github.io/claude-cowork-workshop/

**Theo dõi mình:**
nguyễn bá nghĩa · community Claude & AI Automation VN ~100k

<br>

> *Tuần sau quay lại kể chuyện đầu tiên Cowork giúp bạn — chúng ta cùng học từ workflow thật.*
