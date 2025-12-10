---
title: "Blog 3"
date: "2025-01-15"
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Tích hợp S&P Global Data mở rộng khả năng Nghiên cứu nhanh của Amazon

của Jon Einkauf , Brandon Pominville và Prasanth Ponnoth trên08 THÁNG 12 NĂM 2025 trong Amazon Quick Suite , Thông báo , Trí tuệ nhân tạo Liên kết cố định Bình luận Chia sẻ

Hôm nay, chúng tôi vui mừng thông báo về sự tích hợp mới giữa Amazon Quick Research và S&P Global. Sự tích hợp này mang đến cho khách hàng của Quick Research cả tin tức, nghiên cứu và thông tin chuyên sâu về S&P Global Energy lẫn dữ liệu S&P Global Market Intelligence trong một công cụ nghiên cứu chuyên sâu.

Tích hợp S&P Global mở rộng khả năng của Quick Research, cho phép các chuyên gia kinh doanh phân tích nhiều nguồn dữ liệu—bao gồm tin tức năng lượng toàn cầu và thông tin tài chính chuyên sâu—trong một không gian làm việc, loại bỏ nhu cầu chuyển đổi giữa các nền tảng và biến nhiều tuần nghiên cứu thành vài phút tạo ra thông tin chuyên sâu. Quick Suite kết nối thông tin trên các kho lưu trữ nội bộ, các ứng dụng phổ biến, dịch vụ AWS và thông qua tích hợp Giao thức Bối cảnh Mô hình (MCP) với hơn 1.000 ứng dụng. Ứng dụng AI đại diện này đang định hình lại cách thức hoàn thành công việc bằng cách chuyển đổi cách các nhóm tìm kiếm thông tin chuyên sâu, thực hiện nghiên cứu chuyên sâu, tự động hóa tác vụ, trực quan hóa dữ liệu và thực hiện hành động trên các ứng dụng.

Trong bài đăng này, chúng tôi sẽ khám phá các tập dữ liệu của S&P Global và kiến ​​trúc giải pháp tích hợp với Quick Research.

## Tổng quan về giải pháp

S&P Global  là đơn vị tiên phong triển khai hai máy chủ MCP trên AWS để các tổ chức có thể dễ dàng tích hợp các dịch vụ tài chính và nội dung năng lượng đáng tin cậy vào quy trình làm việc được hỗ trợ bởi AI, đồng thời vẫn duy trì chất lượng, bảo mật và độ tin cậy mà các nhà lãnh đạo doanh nghiệp yêu cầu.

Sự hợp tác của chúng tôi với AWS mở rộng cách S&P Global cung cấp thông tin tình báo đáng tin cậy thông qua thế hệ trải nghiệm AI đại diện tiếp theo. Bằng cách hợp tác với các công ty AI hàng đầu, mục tiêu của chúng tôi là đảm bảo khách hàng có thể truy cập dữ liệu và thông tin chi tiết đáng tin cậy của chúng tôi bất kể quy trình làm việc của họ diễn ra ở đâu.

– Bhavesh Dayalji, Giám đốc AI của S&P Global và Giám đốc điều hành của Kensho.

### S&P Global Energy: Thông tin tình báo toàn diện về hàng hóa và năng lượng

Tích hợp S&P Global Energy, hiện có sẵn trong Amazon Quick Research, sử dụng máy chủ MCP AI Ready Data để cung cấp quyền truy cập toàn diện vào thông tin thị trường hàng hóa và năng lượng, bao gồm các lĩnh vực Dầu khí, Điện, Kim loại, Năng lượng Sạch, Nông nghiệp và Vận tải biển trên toàn cầu. Được xây dựng dựa trên uy tín của S&P Global là một cơ quan thị trường đáng tin cậy, máy chủ MCP sử dụng hàng trăm nghìn tài liệu do chuyên gia tạo ra, bao gồm các bài phân tích, bình luận và bài báo phản ánh nhiều thập kỷ kinh nghiệm trong ngành.

Giải pháp cung cấp góc nhìn đa chiều độc đáo, cung cấp thông tin từ cập nhật thị trường hàng ngày đến triển vọng một năm và mở rộng đến phân tích kịch bản 20 năm trở lên. Với dữ liệu được làm mới mỗi 30 phút, các nhà lãnh đạo doanh nghiệp có thể truy cập gần như theo thời gian thực vào thông tin về hàng hóa và năng lượng, giúp tăng tốc đáng kể tốc độ ra quyết định khi tìm hiểu các thách thức về quy định, cơ hội đầu tư hoặc tác động môi trường.

### S&P Global Market Intelligence: Thông tin tình báo tài chính đáng tin cậy

Tích hợp S&P Global Market Intelligence, hiện đã có trong Amazon Quick Research, sử dụng máy chủ API MCP hỗ trợ Kensho LLM do Kensho, trung tâm đổi mới AI của S&P Global, phát triển. Máy chủ MCP này cho phép truy cập dữ liệu tài chính đáng tin cậy thông qua các truy vấn ngôn ngữ tự nhiên, tích hợp liền mạch với Amazon Quick Research. Các chuyên gia tài chính có thể truy cập S&P Capital IQ Financials, bản ghi cuộc gọi thu nhập, thông tin công ty, giao dịch và nhiều hơn nữa, chỉ bằng cách đặt câu hỏi.

Giải pháp Kensho giải quyết một thách thức quan trọng trong dịch vụ tài chính: giúp các kho dữ liệu tài chính khổng lồ có thể truy cập ngay lập tức mà không cần ngôn ngữ truy vấn phức tạp hay chuyên môn kỹ thuật. Các nhóm kỹ thuật, sản phẩm và kinh doanh có thể tiết kiệm đáng kể thời gian và tài nguyên bằng cách chuyển đổi những gì trước đây đòi hỏi hàng giờ trích xuất dữ liệu thành các truy vấn đàm thoại, trả về thông tin chính xác, đáng tin cậy chỉ trong vài giây.

## Kiến trúc giải pháp

Kiến trúc máy chủ MCP của S&P Global được thể hiện trong sơ đồ sau. Khi sử dụng một trong các tích hợp S&P, lưu lượng sẽ chuyển từ Quick Research qua Amazon API Gateway đến AWS Application Load Balancer với các dịch vụ MCP được lưu trữ trên Amazon Elastic Kubernetes Service (Amazon EKS). Máy chủ MCP sử dụng dữ liệu được lưu trữ trên Amazon S3 và AWS Relational Database Service for PostgreSQL cho dữ liệu có cấu trúc, và Amazon OpenSearch Service cho lưu trữ vector. Kiến trúc này cung cấp các máy chủ MCP sẵn sàng cho doanh nghiệp với khả năng bảo mật chuyên sâu, tự động mở rộng quy mô và khả năng quan sát toàn diện.

![blog9_image3.png](/images/blog9_image3.png)

MCP là một tiêu chuẩn mở hỗ trợ giao tiếp liền mạch giữa các tác nhân AI và các nguồn dữ liệu, công cụ và dịch vụ bên ngoài. MCP hoạt động trên kiến ​​trúc máy khách-máy chủ, trong đó máy chủ MCP xử lý các lệnh gọi công cụ, thường bao gồm nhiều lệnh gọi API và hiển thị các triển khai logic nghiệp vụ dưới dạng các hàm có thể gọi. Điều này cho phép các tác nhân AI khám phá các khả năng một cách linh hoạt, thương lượng các tính năng và chia sẻ ngữ cảnh một cách an toàn với tất cả các yêu cầu quan trọng cho các ứng dụng cấp doanh nghiệp.

Giải pháp của S&P Global có những thành phần chính sau:

Đường ống dữ liệu tự động với Amazon Bedrock: Trọng tâm của giải pháp là đường ống thu thập dữ liệu Retrieval Augmented Generation (RAG) sử dụng Amazon Bedrock . Đường ống này chuyển đổi dữ liệu thị trường thô thành Dữ liệu Sẵn sàng cho AI . Các tài liệu từ kho lưu trữ độc quyền của S&P Global trải qua quá trình tiền xử lý, phân đoạn và làm giàu trước khi được chuyển đổi thành các vector nhúng bằng mô hình Cohere Embed do Bedrock lưu trữ. Đường ống thu thập chạy theo lịch trình, làm mới kho vector OpenSearch sau mỗi 30 phút để truy cập dữ liệu năng lượng gần như theo thời gian thực.

Tìm kiếm vectơ và ngữ nghĩa: Amazon OpenSearch đóng vai trò là cơ sở dữ liệu vectơ, lưu trữ các dữ liệu nhúng được tạo bởi Bedrock và cho phép tìm kiếm ngữ nghĩa trên toàn bộ dữ liệu năng lượng của S&P Global. Kho dữ liệu vectơ OpenSearch được tối ưu hóa cho các phép toán vectơ đa chiều, hỗ trợ tìm kiếm tương đồng nhanh chóng, giúp máy chủ MCP có khả năng truy xuất thông tin liên quan theo ngữ cảnh để đáp ứng các truy vấn ngôn ngữ tự nhiên.

Khả năng phục hồi và khả năng mở rộng: Giải pháp này sử dụng Amazon EKS để lưu trữ tất cả các giải pháp máy chủ MCP với hai cụm sản xuất, cho phép phân tách lưu lượng và khả năng chuyển đổi dự phòng. Phương pháp cụm kép này đảm bảo tính khả dụng liên tục ngay cả khi xảy ra sự cố bất ngờ. Cả Cluster Autoscaler và Horizontal Pod Autoscaler đều cho phép mở rộng linh hoạt dựa trên nhu cầu. Các máy chủ MCP được xây dựng với nền tảng FastMCP, cung cấp các điểm cuối HTTP hiệu suất cao, tuân thủ thông số kỹ thuật Streamable HTTP Transport theo yêu cầu của giao thức MCP.

Bảo mật : Bảo mật được tích hợp sẵn trong mọi lớp của giải pháp. API Gateway đóng vai trò là điểm cuối cho quyền truy cập máy chủ MCP. Nhà cung cấp danh tính doanh nghiệp của S&P Global được sử dụng cho xác thực OAuth . API Gateway được bảo mật hơn nữa với Tường lửa Ứng dụng Web (WAF) của AWS với khả năng phát hiện mối đe dọa tiên tiến. Các vai trò và chính sách AWS IAM áp dụng nguyên tắc đặc quyền tối thiểu, do đó mỗi thành phần chỉ có các quyền mà nó yêu cầu. AWS Secrets Manager lưu trữ thông tin xác thực để truy cập tài nguyên và dịch vụ AWS một cách an toàn. AWS Security Groups và cấu hình VPC cung cấp khả năng cô lập mạng, trong khi TLS 1.2+ với AWS Certificate Manager xác thực tất cả dữ liệu đang truyền tải vẫn được mã hóa. Bảo mật nhiều lớp này bao gồm các biện pháp kiểm soát bảo mật chuyên sâu.

Khả năng quan sát: Amazon CloudWatch cung cấp tính năng ghi nhật ký tập trung, thu thập số liệu và giám sát theo thời gian thực toàn bộ quy trình từ khâu thu thập dữ liệu đến phản hồi của máy chủ MCP. AWS CloudTrail ghi lại nhật ký hoạt động API chi tiết và theo dõi kiểm tra, rất cần thiết cho việc tuân thủ trong các ngành được quản lý chặt chẽ.

## Phần kết luận

Cùng nhau, các máy chủ MCP này được xây dựng trên AWS và tích hợp vào Amazon Quick Research thể hiện tầm nhìn của S&P Global về tương lai của dịch vụ tài chính và trí tuệ năng lượng: duy trì sự tin cậy, độ chính xác và chiều sâu mà các nhà lãnh đạo doanh nghiệp yêu cầu trong khi nắm bắt tiềm năng chuyển đổi của AI để làm cho trí tuệ đó ​​dễ tiếp cận hơn, có thể hành động hơn và được tích hợp vào quy trình làm việc hiện đại.

Bạn đã sẵn sàng bắt đầu chưa? Vui lòng tham khảo mục Nghiên cứu nhanh dữ liệu của bên thứ ba để biết thêm chi tiết.

### Về các tác giả

Jon Einkauf là Trưởng nhóm Sản phẩm tại AWS, có trụ sở tại Seattle, nơi ông tập trung vào việc xây dựng các công cụ hỗ trợ AI, giúp doanh nghiệp tổng hợp thông tin và đẩy nhanh tiến độ nghiên cứu. Với hơn một thập kỷ kinh nghiệm tại Amazon trong các lĩnh vực y tế kỹ thuật số, điện toán đám mây và sản phẩm AI, ông đã lãnh đạo các nhóm đa chức năng về quản lý sản phẩm, kỹ thuật và thiết kế để cung cấp các giải pháp sáng tạo cho khách hàng trên toàn thế giới.

![blog9_image1.jpg](/images/blog9_image1.jpg)

Prasanth Ponnoth là kiến ​​trúc sư giải pháp AWS, chuyên hỗ trợ các dịch vụ tài chính toàn cầu với hơn 20 năm kinh nghiệm trong ngành và công nghệ, bao gồm di chuyển, hiện đại hóa đám mây và xây dựng các hệ thống phân tán quy mô lớn. Lĩnh vực quan tâm của ông là học máy, container/Kubernetes và các công nghệ nguồn mở. Tại AWS, ông là thành viên của cộng đồng kỹ thuật học máy và tập trung vào các dịch vụ Amazon Bedrock, Amazon SageMaker AI và Amazon Bedrock AgentCore.

![blog9_image4.jpg](/images/blog9_image4.jpg)

Brandon Pominville là Kiến trúc sư Giải pháp Cấp cao tại AWS, có trụ sở tại New York, nơi anh làm việc với các khách hàng dịch vụ tài chính toàn cầu để xây dựng nền tảng dữ liệu và AI an toàn, có khả năng mở rộng trên đám mây. Với hơn 20 năm kinh nghiệm trong lĩnh vực dịch vụ tài chính, nền tảng dữ liệu doanh nghiệp và điện toán đám mây, anh chuyên chuyển đổi các yêu cầu kinh doanh thành các giải pháp kỹ thuật. Ngoài giờ làm việc, Brandon thích dành thời gian cho gia đình ở ngoài trời hoặc trên du thuyền, và chơi bóng chuyền.

![blog9_image2.png](/images/blog9_image2.png)
