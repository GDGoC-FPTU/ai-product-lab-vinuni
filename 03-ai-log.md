# 03. AI Log

## Log quá trình trao đổi và chọn ý tưởng

Ban đầu, tôi đề xuất problem statement xoay quanh việc tự động hóa quá trình thu phí và quản lý ra vào ở bãi đỗ xe Vinhomes. Ý tưởng này xuất phát từ quan sát rằng khu vực bãi xe thường có nhiều thao tác vận hành lặp lại, và tôi kỳ vọng AI có thể hỗ trợ giảm tải cho đội bảo vệ cũng như tối ưu tốc độ ra vào.

Sau khi thảo luận với đồng đội, nhóm đã phản biện rằng vai trò của bảo vệ tại khu vực bãi xe không chỉ là thu phí hay mở thanh chắn, mà chủ yếu là đảm bảo an ninh và phòng tránh gian lận. Hệ thống hiện tại đã có mức độ tự động hóa nhất định, nên nếu chỉ thay việc mở thủ công bằng mở tự động thì không tạo ra cải thiện đáng kể về tốc độ ra vào. Ngược lại, thay đổi đó có thể làm giảm mức độ kiểm soát an ninh và không tạo ra giá trị đủ lớn để ưu tiên làm bài toán.

Từ phản hồi đó, nhóm quyết định đổi hướng sang một bài toán có pain point rõ hơn và phù hợp hơn với tiêu chí scoping của lab: khắc phục việc thu thập và ghi chép thông tin thủ công ở Vinschool, đặc biệt là khi giáo viên phải xử lý các thông báo hoặc tin nhắn từ phụ huynh. Đây là workflow có nhiều bước lặp lại, dễ sai sót khi nhập tay, và có tiềm năng rõ ràng cho AI hỗ trợ trong khâu phân loại, tóm tắt, ghi nhận và chuẩn hóa thông tin.

Quyết định đổi ý tưởng giúp nhóm tập trung vào một bài toán có giá trị vận hành rõ hơn, ít tranh cãi hơn về mặt an toàn, và phù hợp hơn với hướng ứng dụng AI để giảm thời gian xử lý thủ công thực sự.

## Log quá trình sử dụng AI trong việc hỗ trợ ra ý tưởng

Khi dùng AI để hỗ trợ brainstorm, tôi nhận thấy AI hallucination khá nhiều: các gợi ý thường nghe hợp lý ở bề mặt nhưng không thật sự bám vào pain point cụ thể mà các PnL của Vingroup đang gặp phải. Thay vì hiểu đúng bối cảnh vận hành, AI thường suy diễn theo những mẫu quen thuộc và đưa ra các bài toán khá chung chung.

Một vấn đề khác là AI hay bịa hoặc phóng đại metric theo kiểu “cho có số”, ví dụ nêu ra thời gian tiết kiệm, tỷ lệ giảm lỗi, hay mức tăng hiệu suất nhưng không có căn cứ rõ ràng từ workflow thực tế. Điều đó khiến tôi phải kiểm tra lại từng ý tưởng bằng cách đối chiếu với logic vận hành, người đang làm, và mức độ đau thật sự của bài toán.

Từ trải nghiệm này, tôi rút ra rằng AI phù hợp hơn như một công cụ gợi ý ban đầu, còn phần quyết định problem statement vẫn cần người dùng hiểu domain kiểm tra và chỉnh lại. Nếu không, rất dễ chọn nhầm bài toán chỉ vì metric đẹp nhưng không có giá trị vận hành thật.
