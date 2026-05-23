# Claude Cowork Workshop · Slide tutorial (VN)

Bộ slide tiếng Việt **chuyên sâu** về **Claude Cowork** — agent của Anthropic tự thực thi knowledge-work trên máy người dùng (research preview 01/2026 · GA 09/04/2026).

Soạn cho live event **"Claude & Automation với Cowork"** — 22:00 EDT, 22/05/2026, Google Meet, ~163 attendees. Tổ chức: [Nguyễn Bá Nghĩa](https://github.com/nghiahsgs), admin cộng đồng Claude & AI Automation VN (~100k).

## Xem nhanh

- **HTML deck (live):** https://the-agents-work.github.io/claude-cowork-workshop/
- **HTML deck (local):** `docs/index.html`
- **PDF deck:** [`docs/claude-cowork-workshop.pdf`](./docs/claude-cowork-workshop.pdf)
- **Source:** [`slides.md`](./slides.md) (Markdown Marp)

## 7 phần · 55 slide

1. **Vì sao Cowork?** — vấn đề ngầm với Chat, timeline GA, 4 con số đáng nhớ
2. **Kiến trúc** — Levels 1-3 theo Anthropic *(Context & Tools → Skills → Plugins)* + Advanced *(`/schedule`, Live Artifacts, Dispatch)*
3. **Workflow** — Describe → Execute → Review, plan-first, mid-task steering, *"put what matters in files"*
4. **Setup** — checklist Pro/Max, tạo Project, connect tools, viết Instructions, cài Plugin
5. **Demo Library** — 6 group, 15+ ví dụ cụ thể chia theo persona (SMB · Sales · Marketing Ops · Legal · PM · Personal)
6. **Prompt patterns** — 5 bí kíp: scope chính xác, reference connected tools, cite nguồn, template, sign-off
7. **Tips · Limits · Q&A** — anti-hallucinate playbook, common errors, lộ trình 30 ngày

## Demo highlights

| Group | Ví dụ |
|---|---|
| File & Document | dọn Downloads, batch rename EXIF, Drive download + index |
| Document Creation | PPT 10-slide, blog 1000 từ, invoice template bilingual |
| Data Processing | expense tracker pie chart, merge 5 CSV regions, hoá đơn ảnh → XLSX |
| Research | 5 PDF papers → cited synthesis |
| Persona Workflows | SMB Monday Brief, Sales `/account-research`, Marketing `/schedule` Sunday, Legal `/brief` daily, PM meeting prep, Personal Weekly Life Review |

## Build local

```bash
npm install
npm run build       # PDF + HTML vào docs/
npm run watch       # live reload khi sửa slides.md
npm run build:pptx  # export sang PowerPoint nếu cần
```

Marp tự convert Markdown → HTML/PDF/PPTX. Sửa `slides.md` là xong, không cần biết HTML/CSS *(style đã sẵn trong frontmatter)*.

## Nguồn (đã verify)

**Chính chủ Anthropic** *(8 tutorial chọn lọc cho workshop)*:
- [Set up Cowork to work the way you do](https://claude.com/resources/tutorials/cowork-onboarding-guide)
- [Delegating your first task](https://claude.com/resources/tutorials/delegating-your-first-task-in-claude-cowork)
- [Customize Claude Cowork](https://claude.com/resources/tutorials/customize-claude-cowork)
- [Choosing between Cowork or Chat](https://claude.com/resources/tutorials/choosing-between-claude-cowork-or-chat)
- [For Sales: account research](https://claude.com/resources/tutorials/using-claude-cowork-for-sales-account-research)
- [For Legal: question briefing](https://claude.com/resources/tutorials/using-claude-cowork-for-legal-question-briefing)
- [For Marketing Ops: weekly review](https://claude.com/resources/tutorials/using-claude-cowork-for-marketing-ops-review)
- [For Small Business](https://claude.com/resources/tutorials/using-claude-for-your-small-business)

**Product pages:**
- [claude.com/cowork](https://www.claude.com/cowork) · [claude.com/product/cowork](https://claude.com/product/cowork) · [claude.com/download](https://claude.com/download)

**Community deep dives:**
- [claudecowork.im](https://claudecowork.im) — unofficial complete guide, 30+ prompt mẫu
- [techsy.io / Cowork Guide 2026](https://techsy.io/en/blog/claude-cowork-guide) — community view về pricing, limitations, marketplace maturity
- [pasqualepillitteri.it / triple announcement](https://pasqualepillitteri.it/en/news/755/anthropic-managed-agents-cowork-ga-april-9-2026) — GA enterprise features
- Jeff Su · DataCamp · YouTube AI Foundations *(33 phút)*

## License

MIT — fork, edit, dùng cho workshop nội bộ, content marketing. Credit về repo này khi public lại.
