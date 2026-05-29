**Tên nhóm: VinUni**

**Thành viên:**

**Phùng Bá Quân - 2A202600866**

**Nguyễn Hoàng Long - 2A202600785**

# 🏗️ Phase 3 — DEEP-DIVE (Nhóm, 85 min)

## 3.1. Current-State Workflow Mapping (25 min)
**Vẽ quy trình hiện tại lên bảng/giấy A3.** Sử dụng các ký hiệu:
* 🔴 **Bottleneck:** Bước gây tắc nghẽn, tốn thời gian, hoặc sai sót nhiều nhất.
* 🔄 **Handoff:** Điểm chuyển giao thông tin giữa người và hệ thống, hoặc giữa các bộ phận.
* Ghi rõ thời gian vận hành trung bình: **Tổng cộng = ____ phút/lượt**.

## 3.2. Problem Statement (6-field) & Metrics (15 min)
Điền đầy đủ 6 trường thông tin của bài toán:

| Field | Nội dung chi tiết |
|---|---|
| **1. Actor / Operator** | Nhân viên CSKH, admin cơ sở, và Giáo viên chủ nhiệm (GVCN) — những người tiếp nhận và xử lý ticket phụ huynh hằng ngày. |
| **2. Current Workflow** | 1) Phụ huynh gửi yêu cầu qua app/Zalo/email/hotline. 2) Nhân viên mở ticket, đọc nội dung và phân loại tay (policy/schedule/fee/bus/event/complaint). 3) Tra cứu tài liệu nội bộ (Google Drive, file PDF) để lấy câu trả lời. 4) Soạn phản hồi thủ công hoặc chuyển lên bộ phận chuyên trách. 5) Ghi log vào CRM. Tổng thời gian trung bình: 5–8 phút/ticket. |
| **3. Bottleneck** | Phân loại thủ công và tra cứu trong KB (step 2–3): tốn thời gian, dễ sai, nhiều câu hỏi lặp lại dẫn đến backlog. |
| **4. Business Impact** | Với 50k học sinh và 1–2 tương tác/tháng → 50k–100k ticket/tháng. Nếu 1 ticket mất 5 phút thì 4.167–8.333 giờ/tháng; gây tốn nhân lực, trễ SLA, giảm trải nghiệm phụ huynh. Tiết kiệm 30% ticket lặp nghĩa là trả lại hàng nghìn giờ công mỗi tháng. |
| **5. Success Metric** | - First Response Time (FRT) trung bình cho ticket in-scope < 2 phút.  - First Contact Resolution (FCR) ≥ 70% cho ticket thuộc KB.  - Giảm ticket lặp lại (repeat rate) ≥ 30% trong 3 tháng pilot. |
| **6. Operational Boundary** | AI chỉ được tự động trả lời các câu hỏi nằm trong KB xác nhận; mọi câu trả lời có confidence thấp hoặc liên quan quyết định học vụ phải đưa về dạng draft cho nhân viên duyệt (HITL). Cấm AI sửa đổi dữ liệu học sinh, đưa ra quyết định kỷ luật/điểm số, hoặc tự động xóa/đóng ticket mà không có con người kiểm tra. |

## 3.3. Future-State Flow & AI Fit (25 min)
* **Xác định mức AI Fit (AI-Fit Matrix):** Giải pháp thuộc nhóm nào? [ ] Rule / State-Machine [ ] LLM Feature [ ] Agentic Loop.
* **Vẽ Future-State Flow:** Đánh dấu rõ:
  * 🔵 **AI Step:** Tác vụ LLM xử lý.
  * 🟢 **Human Step (HITL):** Bước con người phê duyệt/review (Human-in-the-loop).
  * ↩️ **Fallback:** Kế hoạch dự phòng khi LLM trả về kết quả lỗi hoặc không tự tin.

**AI Fit:** Chọn **LLM Feature** (không cần Agent tự trị vì quy trình có cấu trúc cố định; rủi ro khi AI trả lời sai có thể được kiểm soát bằng Human-in-the-loop và rule-based routing).

**Quy trình tương lai (Future-State):**

```text
┌──────────────┐     ┌──────────────┐      ┌──────────────┐     ┌──────────────┐
│ Bước 1       │     │ Bước 2       │      │ Bước 3       │     │ Bước 4       │
│ Nhận message │     │ 🔵 Auto-class │     │ 🔵 AI draft │     │ 🟢 Staff/CSKH│
│ (app/Zalo/   │ ──→ │ i_fy + retrieve│ ──→ │ (templated)  │ ──→ │ click review │
│ email/hotline)│    │ KB results   │       │ & suggestion │     │ & send / edit│
└──────────────┘     └──────────────┘       └──────────────┘     └──────────────┘
                          │
                          ▼
                       ↩️ Fallback:
                       Nếu AI draft không phù hợp,
                       nhân viên sửa/viết lại rồi gửi.
```

---

Ghi chú ngắn:
- 🔵 AI Steps: tự động phân loại intent, trích xuất thông tin (tên học sinh, cơ sở, lớp), tìm câu trả lời chính thức trong KB, sinh draft trả lời theo template.
- 🟢 Human Steps: review draft, chỉnh sửa khi cần, và bấm `Send` — đảm bảo HITL cho mọi trường hợp nhạy cảm hoặc confidence thấp.
- Fallbacks: nếu không tìm được câu trả lời chính xác hoặc phát hiện PII/when-to-escalate → route về nhân viên (No auto-send).


---


# 🏁 Phase 5 — EVALUATE (Nhóm, 20 min)

### AI Readiness Checklist:
- [x] Data: Có sẵn lịch sử ticket để làm dataset mẫu (export CSV từ CRM) hoặc có thể thu thập nhanh tại 2 cơ sở pilot.
- [x] Scope: Có thể giới hạn scope pilot (FAQs: học phí, lịch, đồng phục, xe bus, sự kiện) để giảm rủi ro.
- [x] HITL: Nhân lực để review draft và xử lý escalation có sẵn tại cơ sở pilot.
- [ ] Privacy/Legal: Cần kiểm tra kỹ các yêu cầu bảo mật dữ liệu học sinh (PII), chuẩn bị hợp đồng xử lý dữ liệu.
- [x] Metrics: FRT, FCR, repeat rate và staff time saved có thể đo và dashboard được.

### Quyết định đề xuất của nhóm: **GO (Pilot có điều kiện)**

**Lý do (ngắn gọn, dễ hiểu):**
- Volume ticket lớn và nhiều câu hỏi lặp — AI có thể tự động hóa phần lớn các câu trả lời chuẩn, giảm thời gian chờ và tiết kiệm nhân lực.
- Kỹ thuật khả thi với mô hình NLU + retrieval + template; rủi ro thấp khi đặt điểm kiểm soát HITL và rule-based fallback.
- KPI đo được rõ: FRT, FCR, repeat rate.

**Điều kiện để bắt đầu (pre-req):**
- Chuẩn hoá KB canonical cho scope pilot; xuất 3–6 tháng ticket mẫu và label intents; xác nhận team review (HITL) và giao diện duyệt.
- Hoàn tất review privacy/legal về PII.

**Ước lượng nguồn lực & timeline (pilot):**
- Team: 2 engineers (1 ML, 1 backend), 1 product manager, 0.5 CS lead.
- Thời gian: 8–10 tuần để có prototype ổn định và dashboard metrics.

**Success criteria để mở rộng:**
- FRT trung bình < 2 phút cho in-scope tickets.
- FCR ≥ 70% cho in-scope tickets.
- Giảm repeat rate ≥ 30% sau 8 tuần.
- Nhân viên xác nhận giảm thời gian xử lý và không tăng khiếu nại từ phụ huynh.

**Fallback plan nếu pilot không đạt:**
- Giữ chế độ `Draft only` lâu hơn, tăng thang duyệt human (tất cả reply phải qua nhân viên) và điều chỉnh KB/rules; hoặc thu hẹp scope tiếp tục.

---
