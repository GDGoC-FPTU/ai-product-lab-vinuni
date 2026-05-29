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


```
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #3                                       │
│                                                             │
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
