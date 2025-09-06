# Customer-Segmentation-by-Demographics
Customer Segmentation by Demographics using Python

#Mục tiêu cần đạt
Xác định rõ các nhóm khách hàng dựa trên sở thích và đặc điểm hành vi
Đề xuất các loại hình du lịch phù hợp với từng phân khúc.
Xây dựng mô hình dự đoán nhóm khách hàng cho các trường hợp mới.

#Nguồn dữ liệu: được thu thập từ kaggle 
Mục tiêu: dùng để phân tích phân khúc khách hàng theo nhân khẩu học và sở thích du lịch.
Mô tả: 17 thuộc tính với 11760 dòng dữ liệu và 3 kiểu dữ liệu (int, float, object).

#Các thuộc tính bao gồm (đã bỏ bớt các cột không cần thiết):

UserID: mã định danh người dùng 
Yearly_avg_view_on_travel_page: Số lượng trung bình lượt xem trang du lịch của người dùng trong một năm.
preferred_device: Thiết bị người dùng truy cập ứng dụng
total_likes_on_outstation_checkin_give: Tổng số lượt thích mà người dùng đã dành cho các bài đăng check-in 
yearly_avg_Outstation_checkins: Số lần trung bình mỗi năm mà người dùng đi du lịch
member_in_family: Số thành viên trong gia đình của người dùng
preferred_location_type: Loại địa điểm du lịch mà người dùng yêu thích
week_since_last_outstation_checkin: Số tuần kể từ lần check-in gần nhất của người dùng.
working_flag: Cho biết người dùng có đang đi làm hay không.
Adult_flag: Cho biết người dùng có phải là người trưởng thành hay không
Daily_Avg_mins_spend_on_traveling_page: Số phút trung bình mỗi ngày mà người dùng dành để xem các trang du lịch.

#Tiền xử lý dữ liệu bao gồm: 

Giảm thuộc tính của dữ liệu: Loại bỏ các thuộc tính không cần thiết, giảm kích thước dữ liệu để cải thiện hiệu suất mà không làm mất thông tin quan trọng
Chuẩn hóa và chuyển đổi dữ liệu: Đưa dữ liệu về cùng một thang đo hoặc định dạng để đảm bảo tính chính xác khi áp dụng các mô hình
Xử lý dữ liệu thiếu: Giải quyết các giá trị bị thiếu để đảm bảo bộ dữ liệu hoàn chỉnh và sẵn sàng cho phân tích
Xử lý dữ liệu nhiễu: Loại bỏ các giá trị bất thường để tránh ảnh hưởng đến mô hình phân tích

#Khám phá dữ liệu bằng các biểu đồ để tìm ra mối liên hệ và thuộc tính có độ ảnh hưởng nhiều nhất

#Phân khúc khách hàng sử dụng K-Means

- Thanh niên năng động: Nhóm khách hàng này có xu hướng tìm kiếm và dành thời gian nhiều hơn cho các trang du lịch. Họ có thể rất quan tâm đến việc khám phá các địa điểm mới nhưng không đi du lịch quá thường xuyên, có thể là do ngân sách hoặc công việc. Thời gian dành cho trang du lịch cao. Số lần du lịch trung bình hàng năm trung bình thấp
- Khách hàng yêu thích du lịch: Nhóm này rất quan tâm và dành thời gian cho việc tìm kiếm thông tin du lịch, đồng thời đi du lịch khá thường xuyên trong năm. Đây là nhóm khách hàng sẵn sàng chi tiêu cho các chuyến đi. Thời gian trung bình dành cho trang du lịch trung bình đến cao. Số lần check-in trung bình hàng năm cao. 
- Trung niên ít thời gian: Nhóm khách hàng này có thể không dành nhiều thời gian vào việc lên kế hoạch du lịch, họ du lịch không quá thường xuyên nhưng vẫn có nhu cầu trải nghiệm các chuyến đi ngắn hạn. Thời gian dành cho trang du lịch trung bình. Số lần du lịch  hàng năm trung bình.
- Thanh niên ít quan tâm đến du lịch: Nhóm này ít tìm kiếm thông tin du lịch và không có thói quen du lịch thường xuyên. Có thể là do chưa có đủ thu nhập hoặc chưa nhận thức được các lợi ích của du lịch. Thời gian dành cho trang du lịch thấp. Số lần du lịch trung bình hàng năm thấp.

#Đề xuất chiến lược cho từng nhóm

- Thanh niên năng động:  các chuyến đi đa dạng về giá cả, từ du lịch tiết kiệm hoặc cắm trại, du lịch mạo hiểm, du lịch khám phá đến các trải nghiệm cao cấp, để phù hợp với nhiều mức thu nhập và nhu cầu. Cung cấp các gói ưu đãi, giảm giá hoặc các chương trình khuyến mãi để chuyển sự quan tâm thành hành động.
- Khách hàng yêu thích du lịch: Khách hàng có thể trải dài từ trẻ đến già. Các chuyến đi khám phá, du lịch trải nghiệm, các hoạt động mạo hiểm,... có thể hấp dẫn khách hàng độ tuổi trẻ bởi sự mới mẻ. Hoặc các gói du lịch cao cấp, nghỉ dưỡng sang trọng với nhóm khách hàng có độ tuổi cao hơn. Quan trọng là cung cấp các ưu đãi khi đi du lịch nhiều lần, như thẻ thành viên, khuyến mãi. Liên tục cập nhật việc quảng bá để giữ chân nhóm khách hàng này.
- Trung niên ít thời gian: Các gói du lịch nghỉ dưỡng, du lịch chữa bệnh, du lịch ẩm thực hay tham quan các địa danh văn hóa để phục vụ nhu cầu thư giãn của nhóm khách này. Cung cấp các dịch vụ hỗ trợ lên kế hoạch từ khâu mua vé đến việc hỗ trợ chọn địa điểm; các ưu đãi về giá, gói du lịch cao cấp và nên chú trọng vào sự chăm sóc khách hàng chu đáo, tận tâm.
- Thanh niên ít quan tâm đến du lịch: Tạo ra các gói du lịch với chi phí thấp và thời gian ngắn, chẳng hạn như các chuyến du lịch cuối tuần hoặc du lịch trong ngày. Sử dụng chiến dịch "du lịch cùng bạn bè" trên các nền tảng mạng xã hội phổ biến như Instagram, TikTok, Facebook để nhóm này dễ dàng tiếp cận và tham gia.



