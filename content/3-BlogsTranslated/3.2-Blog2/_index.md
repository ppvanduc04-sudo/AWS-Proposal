---
title: "Blog 2"
date: "2025-01-15"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# 10 thông báo hàng đầu năm 2025 về hoạt động đám mây của AWS

của Nereida Woo, Calvin Weng và Raviteja Sunkavalli trên26 THÁNG 11 NĂM 2025 trong Thông báo , Đổi mới và Tái tạo , Công cụ Quản lý Liên kết cố định Chia sẻ

![blog8_image4.png](/images/blog8_image4.png)

Tại AWS re:Invent 2025, chúng tôi rất vui mừng được chia sẻ những cải tiến mới nhất được thiết kế để hỗ trợ các tổ chức phát triển mạnh mẽ trong kỷ nguyên AI đang chuyển đổi. Những thông báo hàng đầu về Vận hành Đám mây năm nay sẽ giải quyết những thách thức cấp bách nhất mà khách hàng của chúng tôi đang phải đối mặt hiện nay—từ việc có được khả năng hiển thị toàn diện về khối lượng công việc AI tạo sinh đến việc tăng tốc đáng kể việc giải quyết sự cố và quản lý hiệu quả sự gia tăng theo cấp số nhân của dữ liệu vận hành trong môi trường đám mây hiện đại.

### 1. Khả năng quan sát AI tạo sinh trong Amazon CloudWatch và AgentCore Observability

Amazon CloudWatch cung cấp khả năng quan sát toàn diện cho các ứng dụng và tác nhân AI tạo sinh, cung cấp thông tin chi tiết tích hợp về độ trễ, mức sử dụng mã thông báo và lỗi trên toàn bộ ngăn xếp AI của bạn. Tính năng mới này hoạt động liền mạch với Amazon Bedrock AgentCore và tương thích với các nền tảng tác nhân nguồn mở như LangChain, LangGraph và CrewAI. Bạn có thể giám sát các lệnh gọi mô hình, theo dõi quy trình làm việc của tác nhân từ đầu đến cuối và nhanh chóng xác định các điểm nghẽn hiệu suất — tất cả mà không cần viết mã đo lường tùy chỉnh. Để tìm hiểu thêm, hãy truy cập Khả năng quan sát AI tạo sinh trong Amazon CloudWatch .

![blog8_image7.png](/images/blog8_image7.png)

[Hình 1] Bảng thông tin AI tạo sinh của Amazon CloudWatch

![blog8_image3.png](/images/blog8_image3.png)

[Hình 2] Giao diện quản lý tác nhân

### 2. Bản đồ ứng dụng Amazon CloudWatch hiện hỗ trợ khám phá dịch vụ không có công cụ

Bản đồ ứng dụng Amazon CloudWatch Application Signals giờ đây tự động phát hiện và trực quan hóa cấu trúc ứng dụng của bạn mà không cần thiết bị đo lường, mang đến cho bạn khả năng hiển thị tức thì về các mối quan hệ và phụ thuộc dịch vụ. Cải tiến này được xây dựng dựa trên bản đồ ứng dụng đã ra mắt vào đầu tháng 9, bổ sung tính năng nhóm tự động thông minh, giúp sắp xếp các dịch vụ dựa trên mối quan hệ của chúng và cung cấp thông tin chi tiết về hoạt động theo ngữ cảnh ngay trong chế độ xem bản đồ.

![blog8_image8.png](/images/blog8_image8.png)

[Hình 3] Bản đồ ứng dụng CloudWatch

### 3. Điều tra Amazon CloudWatch hiện có tính năng tạo báo cáo sự cố và phân tích 5 câu hỏi “tại sao”

Các chức năng vận hành hỗ trợ bởi AI (AIOps) giúp bạn giải quyết sự cố nhanh hơn, giảm bớt công sức thủ công và trao quyền cho người vận hành ở mọi cấp độ kinh nghiệm để khắc phục sự cố cho các hệ thống phân tán phức tạp.   Tính năng điều tra CloudWatch , đã được triển khai rộng rãi vào tháng 6, đánh dấu một bước tiến đáng kể trong lĩnh vực trí tuệ vận hành. Chức năng này tận dụng AI tạo sinh để tự động hóa việc phân tích nguyên nhân gốc rễ phức tạp và cung cấp trải nghiệm khắc phục sự cố có hướng dẫn cho các nhóm DevOps đang gặp phải các sự cố nghiêm trọng. Dựa trên nền tảng này, bản phát hành tháng 10 của chúng tôi đã giới thiệu các chức năng tạo báo cáo sự cố tương tác, thay đổi căn bản cách các tổ chức tiếp cận các thách thức vận hành—cho phép các nhóm chuyển từ phản ứng khẩn cấp thụ động sang giải quyết vấn đề có hệ thống, dựa trên kiến ​​thức và cải tiến liên tục.

Chúng tôi cũng đã giới thiệu quy trình phân tích '5 Whys' tích hợp hỗ trợ AI, triển khai phương pháp luận hệ thống chính xác mà các nhóm AWS sử dụng nội bộ để tìm ra nguyên nhân gốc rễ. Dựa trên hai thập kỷ kỷ luật vận hành của AWS thông qua phương pháp Sửa lỗi (COE) của chúng tôi - cùng một khuôn khổ mà chúng tôi đã tinh chỉnh nội bộ để ghi lại sự cố, xác định các vấn đề hệ thống và ngăn ngừa tái diễn - khả năng báo cáo sự cố của CloudWatch hiện gói gọn kiến ​​thức tổ chức này trong một dịch vụ dễ tiếp cận. Chỉ cần một cú nhấp chuột, bộ sưu tập dữ liệu toàn diện trên các số liệu đo từ xa, sự kiện triển khai, thay đổi cấu hình và hoạt động điều tra sẽ được kích hoạt để tạo tài liệu sự cố chi tiết, theo ngữ cảnh. Không giống như các mẫu chung chung, mỗi báo cáo được xây dựng động từ dữ liệu vận hành cụ thể, lịch sử thay đổi và bối cảnh kiến ​​trúc của bạn - cung cấp cho các bên liên quan chính xác những thông tin chi tiết hữu ích cần thiết để tăng cường khả năng phục hồi trong môi trường độc đáo của bạn.

![blog8_image2.png](/images/blog8_image2.png)

[Hình 4] Báo cáo sự cố điều tra của Amazon CloudWatch

![blog8_image9.png](/images/blog8_image9.png)

[Hình 5] Phân tích 5 lý do trong Báo cáo sự cố điều tra CloudWatch

### 4. Máy chủ MCP của Amazon CloudWatch và Application Signals

Máy chủ Giao thức Bối cảnh Mô hình (MCP) dành cho Amazon CloudWatch và CloudWatch Application Signals giúp kết nối các trợ lý AI và tác nhân để tương tác tự nhiên với dữ liệu quan sát của bạn. Các máy chủ MCP này cung cấp quyền truy cập chuẩn hóa vào các số liệu, nhật ký, cảnh báo, dấu vết và dữ liệu tình trạng dịch vụ, cho phép bạn xây dựng quy trình vận hành tự động và tích hợp CloudWatch với các công cụ phát triển hỗ trợ AI. Tìm hiểu thêm về cách nâng cao AIOps của bạn .

### 5. Amazon CloudWatch Application Signals bổ sung các cải tiến cho GitHub Action và máy chủ MCP

CloudWatch Application Signals hiện được tích hợp trực tiếp vào quy trình làm việc của nhà phát triển với GitHub Action mới, cung cấp thông tin chi tiết về khả năng quan sát trong các yêu cầu kéo và quy trình CI/CD. Kết hợp với khả năng nâng cao của máy chủ MCP, nhà phát triển có thể xác định các sự cố suy giảm hiệu suất, theo dõi tình trạng dịch vụ và khắc phục sự cố mà không cần rời khỏi môi trường phát triển.

![blog8_image10.png](/images/blog8_image10.png)

[Hình 6] Phân tích nguyên nhân gốc rễ tự động trong các vấn đề GitHub

![blog8_image11.png](/images/blog8_image11.png)

[Hình 7] Yêu cầu kéo GitHub tự động để khắc phục sự cố

Chúng tôi đã giới thiệu một bộ tính năng toàn diện được thiết kế đặc biệt để giải quyết những thách thức này một cách trực diện. Bằng cách tái cấu trúc cách thức thu thập, tập trung hóa, phân tích và trực quan hóa dữ liệu vận hành, những cải tiến này mang lại khả năng tổng hợp thông minh giúp giảm đáng kể độ phức tạp, khả năng phân tích mạnh mẽ giúp đưa ra những thông tin chi tiết hữu ích và khả năng hiển thị tập trung giúp loại bỏ các bộ phận giám sát rời rạc.

### 6. Dịch vụ Amazon OpenSearch nâng cao khả năng phân tích nhật ký với trải nghiệm PPL mới

Dịch vụ Amazon OpenSearch giới thiệu những cải tiến đáng kể cho Ngôn ngữ Xử lý Đường ống (PPL), giúp phân tích nhật ký nhanh hơn và trực quan hơn. Những cải tiến này bao gồm khả năng truy vấn nâng cao, hiệu suất tốt hơn cho các truy vấn phân tích phức tạp và tích hợp liền mạch với CloudWatch Logs để phân tích nhật ký thống nhất trên toàn bộ môi trường AWS của bạn.

### 7. Amazon CloudWatch giám sát người dùng thực (RUM) bổ sung hỗ trợ cho các ứng dụng iOS và Android

Amazon CloudWatch hiện đã mở rộng tính năng Giám sát Người dùng Thực (RUM) sang các ứng dụng di động, cung cấp khả năng hiển thị trải nghiệm người dùng thực tế trên các thiết bị iOS và Android. Giám sát các chỉ số hiệu suất, theo dõi hành trình người dùng, xác định lỗi phía máy khách và hiểu rõ hiệu suất của ứng dụng di động trên các thiết bị, mạng và khu vực địa lý khác nhau - tất cả đều từ bảng điều khiển CloudWatch.

### 8. AWS CloudTrail bổ sung tính năng tổng hợp sự kiện dữ liệu để đơn giản hóa việc giám sát bảo mật

AWS CloudTrail hiện cung cấp tính năng tổng hợp sự kiện và thông tin chi tiết về các sự kiện dữ liệu, hợp nhất hoạt động API khối lượng lớn thành các bản tóm tắt 5 phút, đồng thời tự động phát hiện các mẫu bất thường. Khả năng kép này giúp giảm khối lượng và chi phí dữ liệu, đồng thời tăng cường giám sát bảo mật—giúp bạn xác định các bất thường như mẫu truy cập S3 bất ngờ hoặc điều tiết DynamoDB mà không cần phân tích thủ công. Để tìm hiểu thêm, hãy truy cập  mục Tổng hợp sự kiện và Thông tin chi tiết về sự kiện dữ liệu của AWS CloudTrail .

### 9. Amazon CloudWatch ra mắt tính năng Tập trung nhật ký liên tài khoản và liên vùng

CloudWatch Logs Centralization hợp nhất dữ liệu nhật ký từ nhiều tài khoản và vùng AWS thành một tài khoản đích duy nhất—loại bỏ các quy trình tổng hợp tùy chỉnh và cung cấp chế độ xem thống nhất cho tất cả dữ liệu vận hành. Được tích hợp với AWS Organizations, bạn có thể xác định phạm vi và mở rộng các quy tắc tập trung trên toàn bộ tổ chức, các đơn vị tổ chức cụ thể hoặc các tài khoản được chọn. Sự kiện nhật ký được tự động làm giàu với các trường @aws.account và @aws.region để duy trì ngữ cảnh nguồn và nguồn gốc dữ liệu.

Với thời gian thiết lập tối thiểu, các nhóm sẽ nâng cao hiệu quả hoạt động, tăng cường khả năng bảo mật và giải quyết sự cố nhanh hơn. Bản sao đầu tiên của nhật ký tập trung không phát sinh thêm chi phí thu thập, giúp đây trở thành giải pháp tiết kiệm chi phí cho việc quản lý nhật ký đa tài khoản. Đọc thêm về cách đơn giản hóa việc quản lý nhật ký.

### 10. Amazon CloudWatch Database Insights bổ sung tính năng giám sát liên tài khoản, liên khu vực

CloudWatch Database Insights hiện hỗ trợ giám sát liên tài khoản và liên vùng, cho phép giám sát tập trung hiệu suất cơ sở dữ liệu trên toàn bộ tổ chức AWS của bạn. Giám sát các số liệu Amazon RDS, Amazon Aurora và Amazon DynamoDB từ một tài khoản giám sát duy nhất, đối chiếu hiệu suất cơ sở dữ liệu với tình trạng ứng dụng và khắc phục sự cố nhanh hơn với khả năng giám sát thống nhất.

### Phần kết luận

Những thông báo này đánh dấu một bước tiến vượt bậc về năng lực vận hành đám mây. Chúng tôi đã xây dựng các giải pháp mang tính đột phá, trực tiếp giải quyết những thách thức đặc thù của hoạt động trong kỷ nguyên AI. Từ khả năng quan sát AI toàn diện , mang lại khả năng hiển thị chưa từng có vào các ứng dụng AI, đến giải pháp xử lý sự cố được hỗ trợ bởi AI giúp tăng tốc đáng kể việc khắc phục sự cố, cho đến quản lý dữ liệu thông minh giúp loại bỏ sự phức tạp — những cải tiến của AWS giúp bạn vận hành nhanh hơn, thông minh hơn và hiệu quả hơn.

Đừng bỏ lỡ cơ hội trải nghiệm trực tiếp những khả năng đột phá này. Hãy tham dự buổi Tọa đàm Đổi mới và các phiên thảo luận tại re:Invent để được trình diễn trực tiếp và ghé thăm gian hàng Vận hành Đám mây để khám phá cách những đổi mới này có thể chuyển đổi hoạt động của bạn. Tương lai của vận hành đám mây đã ở đây—mạnh mẽ, thông minh và hiệu quả hơn bao giờ hết.

![blog8_image1.jpg](/images/blog8_image1.jpg)

### Nereida Woo

Nereida là Kiến trúc sư Giải pháp Chuyên gia WW về Vận hành Đám mây, tập trung vào Quản lý Vận hành Tập trung và Vận hành Ứng dụng trên AWS. Khi không làm việc, cô ấy thích đi du lịch để tham dự các buổi hòa nhạc.

![blog8_image6.jpg](/images/blog8_image6.jpg)

### Calvin Weng

Calvin Weng là Giám đốc Tiếp thị Sản phẩm của AWS Cloud Operations, tập trung vào khả năng quan sát và dịch vụ giám sát. Ngoài giờ làm việc, Calvin thích đi du lịch, làm gốm, chơi bóng bàn chuyên nghiệp và khám phá vùng Tây Bắc Thái Bình Dương cùng chú chó Kai của mình.

![blog8_image5.jpg](/images/blog8_image5.jpg)

### Raviteja Sunkavalli

Raviteja Sunkavalli là Kiến trúc sư Giải pháp Chuyên gia Cấp cao Toàn cầu tại Amazon Web Services, chuyên về khả năng quan sát AIOps và GenAI. Anh hỗ trợ khách hàng toàn cầu triển khai các giải pháp quản lý sự cố và khả năng quan sát trên các môi trường đám mây phức tạp và phân tán. Ngoài giờ làm việc, anh thích chơi cricket và khám phá các công thức nấu ăn
