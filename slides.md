---
marp: true
theme: gaia
size: 16:9
paginate: true
backgroundColor: #0b0d12
color: #e6e8ec
header: 'Claude Cowork Workshop · 22/05/2026'
footer: 'nguyễn bá nghĩa · the-agents-work · ~163 attendees'
style: |
  section {
    font-family: 'Inter', 'Segoe UI', system-ui, -apple-system, sans-serif;
    font-size: 26px;
    padding: 60px 70px;
  }
  section.lead {
    text-align: left;
  }
  h1 {
    color: #ffb86c;
    font-size: 56px;
    font-weight: 800;
    letter-spacing: -1px;
  }
  h2 {
    color: #8be9fd;
    font-size: 38px;
    font-weight: 700;
  }
  h3 {
    color: #ffb86c;
    font-size: 28px;
  }
  strong { color: #f8f8f2; }
  em { color: #bd93f9; font-style: normal; }
  code {
    background: #1f2230;
    color: #50fa7b;
    padding: 2px 8px;
    border-radius: 4px;
  }
  pre {
    background: #0f1117;
    border: 1px solid #2a2d39;
    border-radius: 8px;
  }
  blockquote {
    border-left: 4px solid #ffb86c;
    color: #f1f5f9;
    background: #161922;
    padding: 16px 24px;
    border-radius: 4px;
  }
  table {
    font-size: 22px;
    width: 100%;
  }
  th { background: #1a1d27; color: #ffb86c; }
  td, th { border-color: #2a2d39 !important; }
  ul { line-height: 1.55; }
  section::after {
    color: #6b7280;
    font-size: 16px;
  }
  footer, header {
    color: #6b7280;
    font-size: 14px;
  }
  .big {
    font-size: 48px;
    font-weight: 800;
    color: #50fa7b;
  }
  .muted { color: #9ca3af; }
  .pill {
    display: inline-block;
    background: #1f2230;
    color: #ffb86c;
    padding: 4px 14px;
    border-radius: 999px;
    font-size: 18px;
    margin-right: 6px;
  }
---

<!-- _class: lead -->
<!-- _paginate: false -->

# Claude Cowork
## Giao việc cho AI, nhận deliverable hoàn chỉnh

<br>

**Live workshop · 22:00–00:00 EDT · 22/05/2026**
nguyễn bá nghĩa · cộng đồng Claude & Automation VN

<span class="pill">~163 attendees</span> <span class="pill">Google Meet</span> <span class="pill">Live demo</span>

---

## Mình là ai

- **Nguyễn Bá Nghĩa** — admin cộng đồng Claude & AI Automation Việt Nam (~100k)
- Hằng ngày ship side-project bằng Claude (Code, Cowork, MCP)
- Tin: AI agent phải làm được việc *trên máy mình* mới đáng tiền — không phải để hỏi câu hỏi

<br>

> Workshop tối nay: **demo từ A → Z**, không lý thuyết suông. Ai theo kịp mở máy làm cùng.

---

## Agenda 2 tiếng

1. Cowork là gì — khác Chat thế nào? *(10 phút)*
2. Workflow 3 bước · plan-first · mid-steering *(10 phút)*
3. **Live demo** — 4 use case thật *(45 phút)*
4. MCP: nối Gmail / Drive / Slack / Zoom *(20 phút)*
5. Scheduled task — chạy auto mỗi ngày/tuần *(15 phút)*
6. Tips chống hallucinate · limitations *(10 phút)*
7. Q&A thoải mái *(còn lại)*

---

<!-- _class: lead -->

# Part 1
## Cowork là gì & vì sao đáng quan tâm

---

## Cowork là gì?

> *"Delegate to Claude, delight in the result. Hand off a task — get a polished deliverable."*
> — claude.com/cowork

<br>

- Không phải chatbot trả lời câu hỏi
- Là **agent tự làm việc** trên máy của bạn
- Bạn mô tả **outcome** → Claude lên plan → mở app, sửa file, gọi API, làm ra **kết quả gửi lại**

<span class="big">Mô tả → Claude làm → Bạn duyệt</span>

---

## Timeline ra mắt

| Mốc | Sự kiện |
|---|---|
| **01/2026** | Research preview — invite-only |
| **04/2026** | **GA cho mọi user Pro** *(9/4/2026)* |
| **04/2026** | 6 enterprise feature: RBAC, spend limits, OpenTelemetry, Zoom MCP, audit |
| **05/2026** | Mobile-trigger beta: ra lệnh từ điện thoại, máy bàn làm |

<br>

> Đây là lý do tối nay đáng tới: Cowork **mới GA 1 tháng**, đa số người còn chưa biết.

---

## Chat vs Cowork — khác gì?

| | **Claude Chat** | **Claude Cowork** |
|---|---|---|
| Mục đích | Trả lời, brainstorm | **Hoàn thành task** |
| Phạm vi | Conversation | **File hệ thống + apps** |
| Output | Text trong chat | **File, report, spreadsheet** |
| Thời gian | Tức thì | Phút → giờ → ngày |
| Lặp lại | Hỏi lại mỗi lần | **Schedule chạy auto** |
| Yêu cầu | Free / Pro | **Pro $20+ · Desktop app** |

---

## Cowork vs Claude Code — chọn cái nào?

<div style="display:grid;grid-template-columns:1fr 1fr;gap:24px;">

<div>

### Claude Code
- Dành cho **developer**
- Chạy trong terminal
- Git, build, test, refactor
- Output: **code commit**

</div>

<div>

### Claude Cowork
- Dành cho **knowledge worker**
- Desktop app GUI
- Office, email, browser, file
- Output: **report, sheet, doc**

</div>

</div>

<br>

> Slogan chính chủ: **"Cowork = Claude Code power for knowledge work"**

---

<!-- _class: lead -->

# Part 2
## Workflow — Cowork làm việc thế nào

---

## Quy trình 3 bước

<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:20px;text-align:center;">

<div>

### 1. Describe
Mô tả task bằng tiếng Việt từ desktop *hoặc điện thoại*

</div>

<div>

### 2. Execute
Claude lên plan, làm việc, *xin duyệt trước các bước quan trọng*

</div>

<div>

### 3. Review
Bạn approve, sửa hướng, hoặc để chạy schedule định kỳ

</div>

</div>

<br>

> Bạn có thể đứng nhìn realtime hoặc đi pha cà phê — quay lại check sau.

---

## Plan-first model

```
Bạn: "Dọn folder Downloads"
   ↓
Claude: "Tôi sẽ làm:
  1. Scan 312 file trong Downloads
  2. Tạo thư mục: Documents/, Images/, Videos/, Archives/
  3. Sắp xếp theo extension + ngày tạo
  4. Đánh dấu 14 file trùng để bạn duyệt xóa
  Approve? [Yes / Edit / Cancel]"
```

<br>

**3 nút quyền lực:**
- ✅ **Yes** — Claude chạy phần còn lại
- ✏️ **Edit** — chỉnh plan trước khi chạy
- ❌ **Cancel** — dừng, không động vào file

---

## Mid-task steering

Đang chạy giữa chừng → bạn vẫn **chen ngang được**:

- *"Khoan, đừng xóa cái này"*
- *"Chuyển hết file Hợp đồng vào folder Legal nhé"*
- *"Output đổi sang format markdown thay vì PDF"*

<br>

> Đây là điểm khác biệt lớn nhất với automation truyền thống (Zapier, Make):
> **Bạn có thể can thiệp bằng ngôn ngữ tự nhiên giữa chừng.**

---

<!-- _class: lead -->

# Part 3
## Live Demo — 4 use case có thật

---

## Demo 1 — Giao task phức tạp

**Prompt:**
```
Mở folder /Documents/01_23-Product-Meeting.
Đọc hết notes Q1 + project doc, viết Q1 Product Update Report:
  - Executive Summary
  - Launch Milestones
  - Key Decisions
  - What's Next
Format brand company, lưu cùng folder.
```

**Cowork sẽ:**
1. Liệt kê 23 file phát hiện được → hỏi xem có cần loại bỏ file nào không
2. Đọc tuần tự, trích quote + ngày + người ra quyết định
3. Soạn report ~6 trang theo template, save `.docx`
4. Báo lại: "Done. Có 3 chỗ tôi không chắc, đã highlight để bạn review."

---

## Demo 2 — Dọn folder Downloads lộn xộn

**Trước:** 312 file random, từ `Screenshot 2025-11-17.png` → `chuong-trinh_v3_final_FINAL.pdf`

**Sau (Cowork tự đề xuất):**
```
Downloads/
├── Documents/       (PDF, DOCX, contracts)
├── Spreadsheets/    (XLSX, CSV)
├── Images/          (PNG, JPG, screenshots)
├── Audio-Video/     (MP4, MP3)
├── Archives/        (ZIP, RAR)
└── _to-review/      (14 file trùng/không rõ)
```

> Tip: lần đầu, đừng cho auto-execute. **Approve từng nhóm** để học cách nó suy luận.

---

## Demo 3 — Hóa đơn → Spreadsheet

Bạn quẳng vào folder 30 ảnh hoá đơn (cả tiếng Việt) + nói:

```
"Trích xuất: ngày, nhà cung cấp, mã hoá đơn, số tiền (VND),
loại chi phí. Gộp thành 1 sheet. Loại bỏ duplicate."
```

<br>

**Output:** `chi-phi-thang-5.xlsx`

| Ngày | Nhà cung cấp | Mã | VND | Loại |
|---|---|---|---|---|
| 2026-05-03 | Grab | INV-882 | 184,000 | Đi lại |
| 2026-05-04 | Co.opmart | 4192 | 562,300 | Văn phòng phẩm |
| … | … | … | … | … |

---

## Demo 4 — Tổng hợp đa nguồn

**Prompt:**
```
Gộp dữ liệu báo cáo tuần này:
  - Metrics từ Google Analytics dashboard
  - Số đơn từ Stripe
  - Feedback khách trong inbox Gmail (tag "feedback")
  - Update task từ Linear

Viết bản tin 1 trang gửi team, kèm 3 insight nổi bật.
```

<br>

> Đây là chỗ Cowork **vượt xa** Chat: nó **mở 4 nguồn cùng lúc**, đối chiếu, viết report — thay vì bạn copy-paste từng cái.

---

<!-- _class: lead -->

# Part 4
## MCP — chìa khoá kết nối mọi thứ

---

## MCP là gì (siêu rút gọn)

**MCP = Model Context Protocol** — chuẩn mở do Anthropic ra, cho phép Claude kết nối tới **bất kỳ tool nào** có MCP server.

<br>

Hình dung như:
> *USB-C cho AI* — một chuẩn cắm chung, app nào hỗ trợ thì Claude xài được.

<br>

Bạn **không cần code**. Cowork có sẵn marketplace để click cài.

---

## Connector phổ biến nhất

<div style="display:grid;grid-template-columns:1fr 1fr;gap:30px;">

<div>

### Communication
- Gmail
- Slack
- Zoom *(GA 4/2026)*
- Outlook

### Files & Notes
- Google Drive
- Notion
- OneDrive
- Dropbox

</div>

<div>

### Work tools
- Linear
- Asana
- Jira
- HubSpot
- Stripe
- QuickBooks

### Browser
- Chrome (Computer Use)
- Tự động click, scroll, fill form

</div>

</div>

<br>

> Marketplace còn ~200 plugin community-built, đang tăng nhanh.

---

## Demo MCP — connect Gmail

**Bước 1.** Cowork → Settings → Connectors → Gmail → Authorize

**Bước 2.** Trong chat:
```
"Tổng hợp email tuần này theo 3 nhóm:
   - Khách quan trọng (VIP)
   - Cần phản hồi gấp
   - Spam/Newsletter (đề xuất xoá)
Trả về danh sách + draft reply cho nhóm 2."
```

**Bước 3.** Claude show plan → bạn approve → output:
- 47 email phân loại sẵn
- 8 draft reply trong folder `_drafts`
- 1 file `summary.md`

---

<!-- _class: lead -->

# Part 5
## Scheduled Task — Cowork thành nhân viên 24/7

---

## Scheduled task workflow

**Setup 1 lần, chạy mãi mãi:**

```
Task: "Daily email digest"
Cadence: 08:00 mỗi ngày
Steps:
  1. Đọc inbox Gmail từ 17h hôm qua → 08h hôm nay
  2. Lọc bỏ newsletter + promo
  3. Phân loại: VIP / cần reply / FYI / spam
  4. Gửi summary vào Slack #personal-brief
  5. Đánh sao 5 email cần xử lý nhất
```

Mỗi sáng mở máy → đã có brief sẵn.

---

## Ý tưởng schedule cho dân văn phòng

- **8:00 hằng ngày** — Brief email + lịch hôm nay
- **Thứ Hai 9:00** — Pull metrics tuần trước, điền template báo cáo
- **Thứ Sáu 17:00** — Slack digest tuần + ghi vào weekly review
- **Ngày 1 hàng tháng** — Bookkeeping: gộp hoá đơn → spreadsheet → gửi kế toán
- **Mỗi giờ** — Theo dõi inbox khách VIP, ping Slack nếu có email từ họ
- **Ngày 25 hàng tháng** — Chuẩn bị slide báo cáo monthly review

> Mỗi task chạy được = ~1 giờ/ngày tiết kiệm → trả lại $20 Pro trong 1 tuần.

---

<!-- _class: lead -->

# Part 6
## Tips & Pitfalls — Để không bị "AI lừa"

---

## 5 nguyên tắc ra output chất

1. **Đặt scope rõ ràng** — nói rõ folder nào, file nào, deadline nào
2. **Cho ví dụ output mong muốn** — gắn 1 sample report cũ → Claude bắt chước style
3. **Approve từng phần** lần đầu — đừng auto cả pipeline ngày 1
4. **Dùng `CLAUDE.md`** trong folder — viết rule cố định cho Cowork đọc
5. **Yêu cầu cite nguồn** — bắt nó ghi rõ data lấy từ file/email nào

---

## Anti-hallucinate playbook

| Vấn đề | Cách chặn |
|---|---|
| Claude bịa số liệu | Bắt **trích nguồn từng số**: "(file X, dòng Y)" |
| Claude tự suy diễn | Thêm: *"Nếu không chắc, hỏi tôi, đừng đoán"* |
| Output rỗng tuếch | Cho **template + ví dụ** đính kèm |
| Sửa nhầm file quan trọng | Bật **"draft only mode"** — không ghi đè bản gốc |
| Lệch tone công ty | Đính `brand-voice.md` vào folder làm việc |

<br>

> Theo techsy.io 2026: **~1% câu trả lời** vẫn có hallucinate.
> → Output legal/finance **bắt buộc** review tay.

---

## Limitations cần biết trước

- 🇺🇸 **Default host US** — EU data residency chỉ có Enterprise
- 🔌 **Marketplace MCP** còn non — chưa có native Salesforce/Shopify/NetSuite
- 🐢 **Không phải lúc nào cũng nhanh** — task phức tạp 5–30 phút
- 💸 **Pro $20** là tối thiểu, hết quota nhanh nếu schedule dày
- 🔒 **Sandboxed shell** — không phải toàn quyền máy, có scope folder rõ
- 🤖 **Không tự ký hợp đồng / chuyển tiền** — bắt buộc human approval ở các bước nhạy cảm

---

## Khi nào *KHÔNG* nên dùng Cowork

- ❌ Quyết định pháp lý / tài chính cuối cùng (drafting OK, ra quyết định không)
- ❌ Dữ liệu siêu nhạy cảm chưa qua DPA — chờ Enterprise + BAA
- ❌ Task < 30 giây — overhead plan/approve không đáng
- ❌ Bạn không có thời gian review output — sẽ tích nợ kỹ thuật rất nhanh

<br>

> Quy tắc: **Cowork giỏi việc lặp, có structure. Việc 1 lần, mơ hồ → vẫn nên dùng Chat.**

---

<!-- _class: lead -->

# Part 7
## Getting Started — Chiều nay làm gì

---

## Prep checklist

- [ ] **Tài khoản Claude Pro** — $20/tháng → claude.com/pricing
- [ ] **Claude Desktop app** — Mac hoặc Windows → claude.com/download
- [ ] Mở app → tab **Cowork** (cạnh Chat & Code)
- [ ] Cấp quyền **folder làm việc** (gợi ý: `~/Cowork-Sandbox/` riêng)
- [ ] Connect 1 MCP đầu tiên — gợi ý: Google Drive
- [ ] Setup `CLAUDE.md` ghi tên + role + tone bạn muốn
- [ ] Chạy task thử: *"Tóm tắt 3 file PDF mới nhất trong folder này"*

---

## Pricing tham khảo (verify lại trên claude.com/pricing)

| Plan | Giá | Phù hợp |
|---|---|---|
| **Pro** | $20/tháng | Cá nhân, freelancer, founder solo |
| **Team** | $25/seat *(min 5)* | Team 5-50 người, có SSO + shared workspace |
| **Enterprise** | Custom | Cần EU residency, BAA/HIPAA, audit log, Managed Agents API |

<br>

> Một số bundle theo ngành: **Marketing Ops, Small Business, Legal** — bật trong settings.

---

## Resources

**Chính chủ:**
- claude.com/cowork — product page
- claude.com/download — Desktop app
- docs.claude.com — Documentation
- anthropic.com/news — Announcement

**Repo workshop này:**
- github.com/the-agents-work/claude-cowork-workshop
- *Slide + ghi chú demo + link bài đọc thêm*

**Cộng đồng VN:**
- *(điền link Facebook group / Zalo / Discord của anh)*

---

<!-- _class: lead -->

# Q&A
## Mở mic, ask anything

<br>

**Một số câu hay được hỏi trước:**

- *Cowork có an toàn cho file công ty không?* → Sandbox + approval per step.
- *Có thay được nhân viên không?* → Thay **việc lặp lại**, không thay **judgement**.
- *Bao lâu thì quen?* → 2-3 ngày dùng nghiêm túc.
- *Tiếng Việt có ổn không?* → OCR + sinh tiếng Việt rất tốt từ Opus 4.7.

---

<!-- _class: lead -->
<!-- _paginate: false -->

# Cảm ơn cả nhà 🙌

<br>

**Slide + repo:**
github.com/the-agents-work/claude-cowork-workshop

**Theo dõi mình:**
nguyễn bá nghĩa · cộng đồng Claude & AI Automation VN

<br>

> *Bắt tay vào dùng. Tuần sau quay lại kể chuyện đầu tiên Cowork giúp bạn.*
