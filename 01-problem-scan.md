<<<<<<< HEAD
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
=======
## Phase 1: Problem Scan - Tìm kiếm và xác định vấn đề
### 📝 List bài toán của tôi (AI version):
| # | Subsidiary (Vinhomes) | Lens | Mô tả ngắn bài toán |
|---|----------------------------------|------|---------------------|
| 1 | Vinhomes | Stakeholder Pain | Phân loại và phản hồi yêu cầu cư dân từ hotline/Zalo/app còn thủ công: 8-12 phút/ticket, 200-400 ticket/ngày, tiêu hao khoảng 27-80 giờ lao động/ngày và dễ trễ SLA 15-25%. |
| 2 | Vinhomes | Repetitive | Điều phối ticket bảo trì/nội khu theo mức độ ưu tiên bằng Excel và chat nhóm: 30-40% ticket bị chuyển tay 1-2 lần, tốn 10-15 phút/ticket, thất thoát khoảng 80-150 giờ/tháng cho mỗi cụm lớn. |
| 3 | Vinhomes | Time-consuming | Soạn biên bản hiện trạng, checklist bàn giao và đối soát hồ sơ mua bán/thuê/nhận nhà thủ công: 12-20 phút/hồ sơ, khoảng 500 hồ sơ/tháng, mất 100-160 giờ/tháng và phát sinh sai sót 3-5%. |
| 4 | Vinhomes | AI-upgrade | Tổng hợp báo cáo vận hành ngày/tuần từ nhiều file Excel, email và chat: 3-5 giờ/báo cáo, 20-30 báo cáo/tháng, làm “chôn” khoảng 60-150 giờ/tháng của đội vận hành trong copy-paste và làm sạch dữ liệu. |
| 5 | Vinhomes | Stakeholder Pain | Lập lịch bảo vệ/vệ sinh/cây xanh theo kinh nghiệm, chưa dự báo tải theo khung giờ cao điểm: overstaff 5-8% hoặc thiếu ca 10-15%, tương đương lãng phí khoảng 40-120 triệu đồng/tháng mỗi đơn vị vận hành lớn. |

### 📝 List bài toán của tôi (human version):
| # | Subsidiary | Lens | Mô tả ngắn bài toán |
|---|----------------------------------|------|---------------------|
| 1 | Vinhomes | Stakeholder Pain | Thiết bị gọi điện cho chủ nhà ở sảnh các chung cư Saphere Vinhomes Ocean Park 1 thường xuyên gặp lỗi, dẫn đến việc cư dân thường xuyên phản ánh đến ban quản lí tòa nhà, giam trải nghiệm khách hàng tại chung cư. |
| 2 | Vinhomes | Repetitive | Đội bảo vệ Vinhomes thường xuyên phải theo dõi camera để tìm kiếm phương tiện đỗ sai quy định để đến khóa bánh, làm mất nhiều thời gian của đội ngũ bảo vệ |
| 3 | Vinhomes | Repetitive | Bộ phận ban quản lí tòa nhà vẫn sử dụng sổ tay để ghi chú các dánh sách lấy thẻ cư dân trong ngày |
| 4 | Vinhomes | Repetitive | Việc ghi phạt đỗ xe trái quy định được thực hiện một cách thủ công bởi đội bảo vệ, dẫn đến lúc nào cũng cần có 1 người trực, tốn nhân lực. |
| 5 | Vinhomes | Time consuming | Việc ra vào hầm gửi xe tòa nhà phải có 1 người túc trực để mở thanh chắn, chưa tự động hóa |

## Phase 2: Quick Assess - Đánh giá nhanh và chọn bài toán tiềm năng

Chọn **top 3 bài toán** từ danh sách trên và hoàn thiện **3 Quick Problem Cards** dưới đây (10 phút/card).

>>>>>>> origin/main

```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #3                                       │
│                                                             │
<<<<<<< HEAD
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
=======
│ Bài toán (1 câu): Việc ra vào hầm gửi xe tòa nhà phải có    │
│ 1 người túc trực để mở/đóng thanh chắn, chưa tự động hóa,   │
│ gây tốn nhân lực, chậm lưu thông và tăng chi phí vận hành.  │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [x] Vinhomes  │
│                     [ ] Vinmec   [ ] Khác (Ghi rõ)________  │
│                                                             │
│ Ai đang đau (Actor)? Đội bảo vệ, Nhân viên bãi xe, Cư dân   │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Xe đến hầm, tài xế bấm chuông/ gọi để yêu cầu mở       │
│   2. Nhân viên trực kiểm tra (thẻ, danh sách, xác thực)     │
│   3. Nhân viên mở thanh chắn bằng tay/điều khiển từ xa      │
│   4. Ghi nhận thủ công (biển số, thời gian) nếu cần         │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bước 1-3 (⏱ cần người túc  │
│ trực 24/7; thời gian chờ trung bình 30-90s/xe, có thể tăng   │
│ mạnh giờ cao điểm; yêu cầu nhân lực ~720 giờ/tháng/ cửa   │
│ vào)                                                        │
│ AI có thể nhảy vào hỗ trợ ở bước nào?                      │
│   - ANPR/CV nhận diện biển số cho cư dân đã đăng ký, tự mở   │
│     thanh chắn cho xe hợp lệ                                 │
│   - Ứng dụng/web cho cư dân/khách gửi mã QR/OTP để vào ra    │
│   - Hệ thống tích hợp với bộ điều khiển cửa để tự động mở    │
│   - Agent cho phép giám sát tập trung, xử lý ngoại lệ và     │
│     tương tác bằng chat/voice khi cần                        │
│                                                             │
│ Đo thành công bằng gì (Metric có số)?                       │
│   - Giảm giờ trực nhân lực từ ~720 giờ/tháng -> ~40-120 giờ/ │
│     tháng (chỉ cần can thiệp ngoại lệ)                      │
│   - Giảm thời gian chờ trung bình từ 30-90s -> <5s cho xe    │
│     đã đăng ký                                                │
│   - Giảm chi phí vận hành (OPEX) ~50-80% cho nghiệp vụ trực │
│   │                                                           │
│   - Giảm rủi ro an ninh và tăng lưu lượng thông xe vào giờ   │
│     cao điểm                                                 │
│                                                             │
│ Quick Architecture: [ ] No AI  [x] Rule  [ ] LLM  [x] Agent  │
└─────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #1                                       │
│                                                             │
│ Bài toán (1 câu): Đội bảo vệ Vinhomes phải theo dõi camera  │
│ thủ công để phát hiện xe đỗ sai quy định và khóa bánh, gây  │
│ tốn nhiều thời gian và nhân lực.                            │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [x] Vinhomes  │
│                     [ ] Vinmec   [ ] Khác (Ghi rõ)________  │
│                                                             │
│ Ai đang đau (Actor)? Bộ phận bảo vệ / Vận hành tòa nhà      │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Bảo vệ xem camera lần lượt các khu vực trong Vinhomes  │
│   2. Phát hiện xe đỗ sai/quy định và xác minh vi phạm       │
│   3. Theo dõi thời gian đỗ sai để xác nhận (ghi log/ảnh)    │
│   4. Di chuyển đến vị trí và khóa bánh                      │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bước 1 và 2 (⏱ chiếm phần │
│ lớn thời gian giám sát; tổng cộng có thể lên đến nhiều giờ │
│ mỗi ngày tùy quy mô)                                       │
│ AI có thể nhảy vào hỗ trợ ở bước nào?                      │
│   - Sử dụng Computer Vision để phát hiện phương tiện, phân   │
│     loại vi phạm, theo dõi thời gian đỗ và gửi cảnh báo tự  │
│     động kèm ảnh/chụp màn hình cho bảo vệ                   │
│   - Kết hợp OCR/ANPR để nhận diện biển số và tra cứu lịch sử │
│   - Agent điều phối thông báo, hướng dẫn vị trí, và tạo ticket│
│                                                             │
│ Đo thành công bằng gì (Metric có số)?                       │
│   - Giảm thời gian bảo vệ phải theo dõi từ "24h/ngày" ->   │
│     "vài phút/ngày" (chỉ xem xét các cảnh báo AI)          │
│   - Giảm nhân lực trực giám sát trực tiếp (giảm OPEX)       │
│                                                             │
│ Quick Architecture: [ ] No AI  [x] Rule  [ ] LLM  [x] Agent  │
└─────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #2                                       │
│                                                             │
│ Bài toán (1 câu): Việc ghi phạt đỗ xe trái quy định được     │
│ thực hiện thủ công bởi đội bảo vệ, luôn cần trực 1 người,    │
│ tốn nhân lực và gây chậm trễ trong xử lý vi phạm.           │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [x] Vinhomes  │
│                     [ ] Vinmec   [ ] Khác (Ghi rõ)________  │
│                                                             │
│ Ai đang đau (Actor)? Đội bảo vệ, Ban quản lý tòa nhà, cư dân │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Phát hiện xe vi phạm bằng quan sát/camera thủ công      │
│   2. Ghi chép thông tin (biển số, thời gian, ảnh) bằng sổ/│
│      form thủ công                                          │
│   3. Thông báo cư dân bằng cuộc gọi/ghi giấy                │
│   4. Thu/phạt trực tiếp hoặc yêu cầu đóng phạt sau           │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bước 1 và 2 (⏱ cần người   │
│ trực liên tục; quy trình ghi chép và xác minh mất 10-20 phút│
│ mỗi sự kiện, gây tốn kém nhân lực)                        │
│ AI có thể nhảy vào hỗ trợ ở bước nào?                      │
│   - CV/ANPR nhận diện biển số và ghi nhận ảnh/video vi phạm  │
│   - Hệ thống web/app tự động tạo biên bản điện tử, gửi thông │
│     báo + link đóng phạt cho cư dân                          │
│   - Tự động xác thực/ghi nhận thanh toán qua gateway, cập   │
│     nhật trạng thái vi phạm và lịch sử vi phạm              │
│   - Agent kết nối giữa camera, DB cư dân và hệ thống thu phí │
│                                                             │
│ Đo thành công bằng gì (Metric có số)?                       │
│   - Giảm nhu cầu trực 24/7 của nhân lực xuống còn N/A (chỉ  │
│     xử lý cảnh báo)                                         │
│   - Thời gian ghi phạt trung bình từ 15-20 phút -> <2 phút  │
│     (tạo biên bản + gửi link thanh toán tự động)            │
│   - Tăng tỷ lệ thu phạt đúng hạn lên +30-50% nhờ link thanh │
│     toán trực tiếp                                           │
│                                                             │
│ Quick Architecture: [ ] No AI  [x] Rule  [ ] LLM  [x] Agent  │
└─────────────────────────────────────────────────────────────┘
```
>>>>>>> origin/main
