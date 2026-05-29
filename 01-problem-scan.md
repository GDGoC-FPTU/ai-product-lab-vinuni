# 🔍 Phase 1 — SCAN (Cá nhân, 20 min)

Hãy sử dụng **4 Lenses** dưới đây để quét qua hoạt động vận hành của các công ty thành viên Vingroup. Ghi lại **ít nhất 5 bài toán/bottleneck** thực tế.

### 4 Lenses tìm bài toán AI cho Vingroup:
1. **Lặp lại (Repetitive):** Tác vụ lặp đi lặp lại nhiều lần hằng ngày. (Ví dụ: So khớp hóa đơn sạc điện tại VinFast, route lại chuyến taxi tại Xanh SM).
2. **Tốn thời gian (Time-consuming):** Tác vụ ngốn thời gian xử lý thủ công của nhân viên. (Ví dụ: Soạn thảo phản hồi đánh giá 1-star của cư dân Vinhomes).
3. **AI có thể tốt hơn (AI-upgrade):** Dịch vụ khách hàng hiện tại còn chậm hoặc phản hồi rập khuôn. (Ví dụ: Chatbot CSKH Vinpearl hỗ trợ đặt vé vui chơi).
4. **Pain từ người khác (Stakeholder Pain):** Bottleneck khiến khách hàng hoặc nhân viên thực địa phàn nàn. (Ví dụ: Tài xế Xanh SM phàn nàn về việc hệ thống gợi ý điểm đón khách không chính xác).

> [!TIP]
> **🤖 AI Prompts — Partner brainstorm:**
> Hãy sử dụng prompt sau để brainstorm các bài toán thực tế nếu bạn chưa có ý tưởng:
> *"Tôi là AI Engineer tại Vin Smart Future (Vingroup). Tôi đang tìm kiếm các pain point vận hành cụ thể có thể tối ưu bằng AI cho mảng [Chọn một: VinFast / Xanh SM / Vinhomes / Vinmec]. Hãy gợi ý cho tôi 5 quy trình nghiệp vụ thủ công, tốn nhiều thời gian và gây rò rỉ hiệu suất kèm con số thống kê ước tính về tổn thất."*

### 📝 List bài toán của tôi:
| # | Subsidiary (VinFast/Xanh SM...) | Lens | Mô tả ngắn bài toán |
|---|----------------------------------|------|---------------------|
| 1 | Khác (Vinschool) | AI-upgrade + Time-consuming | Tuyển sinh: xử lý lead phụ huynh, tư vấn chương trình học, đặt tour tham quan, nhắc hồ sơ và theo dõi khả năng nhập học đang làm thủ công qua điện thoại, Excel, Zalo và CRM. |
| 2 | Khác (Vinschool) | Time-consuming | Chấm bài, viết nhận xét, tạo feedback theo rubric và tổng hợp đánh giá định kỳ cho học sinh tốn nhiều giờ mỗi tuần của giáo viên. |
| 3 | Khác (Vinschool) | Stakeholder Pain + Repetitive | Theo dõi chuyên cần, đi muộn, nghỉ học và cảnh báo sớm học sinh có nguy cơ cần can thiệp cho GVCN/cố vấn/phụ huynh. |
| 4 | Khác (Vinschool) | Repetitive + AI-upgrade | Giao tiếp phụ huynh: trả lời câu hỏi lặp lại, xử lý ticket dịch vụ, tóm tắt lịch sử trao đổi và route đúng bộ phận. |
| 5 | Khác (Vinschool) | Time-consuming + Stakeholder Pain | Xếp thời khóa biểu, phân bổ giáo viên/phòng học/xe bus và xử lý các thay đổi đột xuất gây conflict dây chuyền. |

---

# 🃏 Phase 2 — QUICK-ASSESS (Cá nhân, 30 min)

Chọn **top 3 bài toán** từ danh sách trên và hoàn thiện **3 Quick Problem Cards** dưới đây (10 phút/card).

```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #___                                     │
│                                                             │
│ Bài toán (1 câu): AI admissions copilot tự động xử lý lead  │
│ và nhắc hồ sơ để tăng tốc tuyển sinh Vinschool.             │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [ ] Vinhomes  │
│                     [ ] Vinmec   [x] Khác (Ghi rõ) Vinschool│
│                                                             │
│ Ai đang đau (Actor)? Nhân viên tuyển sinh / tư vấn phụ      │
│ huynh / admissions consultant.                              │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Nhận inquiry từ form/điện thoại/Zalo                    │
│   2. Ghi lead vào CRM và kiểm tra độ tuổi/chương trình      │
│   3. Gọi tư vấn, gửi học phí, đặt tour tham quan             │
│   4. Nhắc hồ sơ còn thiếu và follow-up trước khi nhập học    │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bước 3-4 (⏱ 15-30 phút/lượt)│
│ AI có thể nhảy vào hỗ trợ ở bước nào? Chấm điểm lead, trả   │
│ lời 24/7, gợi ý next-best-action, nhắc hồ sơ thiếu.          │
│                                                             │
│ Đo thành công bằng gì (Metric có số)? Giảm lead response     │
│ time từ >30 phút xuống <5 phút; tăng tour booking rate >=10%.│
│                                                             │
│ Quick Architecture: [ ] No AI  [ ] Rule  [x] LLM  [ ] Agent │
└─────────────────────────────────────────────────────────────┘
```

**Lý do chọn:** bài toán có volume rõ, metric đo được ngay, ranh giới an toàn tương đối dễ kiểm soát vì AI chỉ tư vấn và nhắc việc, chưa ra quyết định tuyển sinh cuối cùng.

```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #2                                       │
│                                                             │
│ Bài toán (1 câu): AI parent service copilot phân loại và    │
│ trả lời ticket phụ huynh cho các câu hỏi lặp lại.           │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [ ] Vinhomes  │
│                     [ ] Vinmec   [x] Khác (Ghi rõ) Vinschool│
│                                                             │
│ Ai đang đau (Actor)? Nhân viên CSKH / admin cơ sở / GVCN.   │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Nhận email, hotline, Zalo hoặc app message             │
│   2. Đọc nội dung và phân loại câu hỏi                       │
│   3. Tìm chính sách / lịch học / học phí / xe bus            │
│   4. Soạn phản hồi và chuyển tiếp nếu vượt thẩm quyền        │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bước 2-3 (⏱ 5-8 phút/ticket)│
│ AI có thể nhảy vào hỗ trợ ở bước nào? Phân loại ticket,     │
│ trả lời câu hỏi chuẩn, tóm tắt lịch sử phụ huynh, route đúng │
│ bộ phận và cảnh báo sentiment xấu.                          │
│                                                             │
│ Đo thành công bằng gì (Metric có số)? Giảm 30% ticket lặp   │
│ lại, first-response time < 2 phút, first-contact resolution  │
│ >= 70% với câu hỏi chuẩn hóa.                               │
│                                                             │
│ Quick Architecture: [ ] No AI  [ ] Rule  [x] LLM  [ ] Agent │
└─────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #3                                       │
│                                                             │
│ Bài toán (1 câu): AI grading assistant tạo nháp nhận xét và  │
│ feedback cá nhân hóa theo rubric cho giáo viên.             │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [ ] Vinhomes  │
│                     [ ] Vinmec   [x] Khác (Ghi rõ) Vinschool│
│                                                             │
│ Ai đang đau (Actor)? Giáo viên bộ môn / giáo viên chủ nhiệm. │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Thu bài và đọc từng bài làm                              │
│   2. Chấm theo rubric, dò lỗi thường gặp                     │
│   3. Viết nhận xét cá nhân hóa cho từng học sinh             │
│   4. Tổng hợp nhận xét học kỳ và gửi phụ huynh               │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bước 2-3 (⏱ 8-12 phút/bài) │
│ AI có thể nhảy vào hỗ trợ ở bước nào? Tạo nháp feedback,    │
│ phát hiện lỗi phổ biến, gợi ý bài tập bổ trợ và tổng hợp     │
│ nhận xét để giáo viên duyệt lần cuối.                        │
│                                                             │
│ Đo thành công bằng gì (Metric có số)? Giảm thời gian feedback│
│ từ 10 phút xuống <2 phút/bài; tiết kiệm ít nhất 2 giờ/giáo   │
│ viên/tuần; 100% output được giáo viên duyệt trước khi gửi.   │
│                                                             │
│ Quick Architecture: [ ] No AI  [ ] Rule  [x] LLM  [ ] Agent │
└─────────────────────────────────────────────────────────────┘
```

**Lý do chọn 3 card này:** chúng đại diện cho 3 dạng value khác nhau: tăng doanh thu tuyển sinh, giảm tải vận hành dịch vụ phụ huynh, và tiết kiệm thời gian giáo viên. Cả 3 đều có metric rõ và có thể pilot nhỏ.

> [!TIP]
> **🤖 AI Prompts — Stress-Test thẻ bài toán:**
> Hãy dán nội dung thẻ bài toán của bạn vào LLM để nhận phản biện:
> *"Đây là một thẻ bài toán vận hành tôi đề xuất cho Vin Smart Future: [Dán nội dung]. Hãy đóng vai trò là một CFO và Trưởng phòng Vận hành cực kỳ khắt khe, chỉ ra cho tôi 3 điểm yếu về logic, metric, và giải thích vì sao rule-based code thông thường có thể giải quyết bài toán này tốt hơn là dùng AI."*

---
