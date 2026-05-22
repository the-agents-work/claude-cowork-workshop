# Claude Cowork Workshop

Slide tutorial bản tiếng Việt giới thiệu **Claude Cowork** — agent của Anthropic tự thực thi task trên máy người dùng (ra mắt research preview 01/2026, GA 09/04/2026).

Soạn cho live event **"Claude & Automation với Cowork"** — 22:00 EDT, 22/05/2026, Google Meet, ~163 attendees. Tổ chức bởi [Nguyễn Bá Nghĩa](https://github.com/nghiahsgs).

## Xem nhanh

- **HTML deck:** `dist/index.html` (mở bằng browser)
- **PDF deck:** `dist/claude-cowork-workshop.pdf`
- **Source:** [`slides.md`](./slides.md)
- **GitHub Pages:** sẽ enable sau khi push

## Nội dung 7 phần

1. **Cowork là gì** — khác Chat & Claude Code thế nào
2. **Workflow** — plan-first, mid-task steering
3. **Live demo** — 4 use case: report quý, dọn folder, hoá đơn → spreadsheet, tổng hợp đa nguồn
4. **MCP** — Gmail, Drive, Slack, Zoom, Notion
5. **Scheduled tasks** — chạy auto mỗi ngày/tuần
6. **Tips & limitations** — anti-hallucinate, khi không nên dùng
7. **Getting started** — prep checklist, pricing tier

## Build local

```bash
npm install
npm run build         # PDF + HTML
npm run watch         # live reload khi sửa slides.md
npm run serve         # serve qua marp local server
```

## Edit slides

Sửa file `slides.md` (Markdown chuẩn Marp). Style + theme nằm trong frontmatter `style:` ở đầu file — đổi màu, font, size tại chỗ.

## Nguồn tham khảo

- [claude.com/cowork](https://www.claude.com/cowork) — product page chính chủ
- [claude.com/product/cowork](https://claude.com/product/cowork) — overview & tagline
- [docs.claude.com](https://docs.claude.com) — Anthropic documentation
- [Anthropic news 9/4/2026](https://www.anthropic.com/news) — Cowork GA + Managed Agents launch
- [techsy.io / Claude Cowork Guide 2026](https://techsy.io/en/blog/claude-cowork-guide) — pricing, limitations, anti-hallucinate
- [pasqualepillitteri.it / triple announcement](https://pasqualepillitteri.it/en/news/755/anthropic-managed-agents-cowork-ga-april-9-2026) — chi tiết enterprise features

## License

MIT — dùng thoải mái cho workshop, content marketing, internal training. Ghi credit về repo này nếu fork.
