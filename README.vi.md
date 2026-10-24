# Post · ảnh chia sẻ trông như thật và bán được hàng

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | Tiếng Việt | [हिन्दी](README.hi.md)

<p align="center"><img src="docs/share.png" alt="Post: a day of notes into a native-looking carousel" width="100%"></p>
<p align="center"><sub>Thuộc bộ <a href="https://github.com/jack-reson8/copy-that"><b>Copy That</b></a> · cài cả bộ bằng một lệnh</sub></p>
<p align="center"><a href="https://jack-reson8.github.io/skill-skill/check/"><img src="https://img.shields.io/badge/skill%20health-100%2F100-brightgreen" alt="skill health 100/100"></a></p>

**Đưa cho Claude những sự thật của hôm nay. Nhận lại bộ ảnh cho Xiaohongshu (Tiểu Hồng Thư) / X trông như màn hình app thật, đọc như một người có duyên kể chuyện, và vừa quảng bá sản phẩm vừa xây series của bạn.**

<table><tr>
<td><img src="docs/frame-1.jpg" width="170"></td>
<td><img src="docs/frame-2.jpg" width="170"></td>
<td><img src="docs/frame-3.jpg" width="170"></td>
<td><img src="docs/frame-4.jpg" width="170"></td>
<td><img src="docs/frame-5.jpg" width="170"></td>
</tr></table>
<sub>Ngày 1 của series building-in-public ("bắt Claude tự kiếm lại 200 USD tiền thuê bao"), làm bằng skill này.</sub>

Phần lớn ảnh bài đăng do AI làm đều hỏng theo cùng một kiểu: thẻ nền gradient, danh sách emoji, một cảnh được "thiết kế" mà nhìn là biết template. Skill này ra đời sau 7 vòng bị chê thật ("xấu", "nhìn là biết AI làm", "không giống Claude", "quá nghiêm túc") cho đến khi bộ ảnh được chấp nhận. Phương pháp đã sửa được vấn đề đó chính là thứ được mã hóa ở đây:

| Bước | Claude làm gì |
|---|---|
| 1 · Brief | `brief.md`: vai trò GTM của bài đăng, nhận diện series, và danh sách sự thật có nguồn — ngoài danh sách này không được xuất hiện gì trong ảnh |
| 2 · Tham khảo | Xếp lưới các ảnh bìa nhiều like nhất của nền tảng, nghiên cứu bộ ảnh App Store của những app có gu, viết ra 3 điều rút ra (cổng kiểm) |
| 3 · Storyboard | Mỗi khung một dòng: tiêu đề, bằng chứng, thẻ nổi, câu đùa, vai trò GTM. Bắt buộc có: ảnh bìa kèm logo series, khung sản phẩm với kết quả thật và giá, trang số liệu tràn khung, lời mời theo dõi |
| 4 · Copy | Viết giản dị trước, rồi thêm 1–3 câu đùa từ thư viện mẫu (tiêu đề dạng câu hỏi tu từ, nhịp một dòng, đùa mặt lạnh, nhắc lại, kết bằng tương phản) |
| 5 · Dựng | Ảnh chụp màn hình điện thoại thật, mock UI chuẩn từng pixel (X, Claude, màn hình khóa iOS, Google, Stripe), hình minh họa không phải bảng, template poster App Store |
| 6 · Rà soát | Contact sheet ở kích thước thumbnail, đối chiếu với checklist |
| 7 · Bàn giao | Contact sheet + 2–3 phương án tiêu đề. Việc đăng bài luôn do bạn quyết |

## Cài đặt

**Dưới dạng plugin Claude Code (khuyến nghị)**

```bash
claude plugin marketplace add jack-reson8/post-skill
claude plugin install post@post-skill
```

**Dưới dạng skill thông thường**

```bash
git clone https://github.com/jack-reson8/post-skill
cp -R post-skill/plugins/post/skills/post ~/.claude/skills/
```
Cần Google Chrome (render headless) và Python 3 có Pillow để tạo contact sheet.

**Codex (CLI hoặc app ChatGPT trên máy tính):**

```bash
codex plugin marketplace add jack-reson8/post-skill
codex plugin add post@post-skill
```

Hoặc sao chép `plugins/post/skills/post` vào `~/.codex/skills/`. Skill tuân theo chuẩn mở [Agent Skills](https://agentskills.io), nên chạy được trên Claude Code, Codex và mọi agent đọc được SKILL.md.

**Các agent khác (Cursor, Gemini CLI, GitHub Copilot và các agent khác được skills CLI hỗ trợ):**

```bash
npx skills add jack-reson8/post-skill
```

## Quy tắc trung thực tích hợp sẵn
Chỉ dùng sự thật; mock hội thoại là bản dựng lại từ cuộc trò chuyện thật; không bao giờ làm giả tin nhắn, giao dịch, lượt thích hay lượt xem của người khác.

## Giấy phép
MIT. Các mock UI mô phỏng app của bên thứ ba cho các bài đăng mang tính bình luận; tên và nhãn hiệu thuộc về chủ sở hữu tương ứng.

Tác giả [@jack-reson8](https://github.com/jack-reson8) · skill cùng nhà: [pro-motion](https://github.com/jack-reson8/pro-motion), [skill-skill](https://github.com/jack-reson8/skill-skill)
