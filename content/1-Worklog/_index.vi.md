---
title: "Tổng quan Worklog"
date: "2025-09-01"
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Phần này trình bày **tổng quan về toàn bộ worklog** trong suốt quá trình thực tập.
Toàn bộ chương trình được hoàn thành trong **12 tuần**, theo một kế hoạch làm việc có cấu trúc rõ ràng với mục tiêu, nhiệm vụ và kết quả cụ thể cho từng tuần.

Trong suốt thời gian này, tôi đã từng bước xây dựng **Nền tảng Huấn luyện Thể hình AI (Fitness AI Training Platform)**, bao gồm frontend, backend, phân tích chuyển động bằng AI, giao tiếp thời gian thực, quản lý cơ sở dữ liệu và triển khai hệ thống trên nền tảng đám mây.  
Mỗi tuần tập trung vào một phần cụ thể của hệ thống, từ phân tích yêu cầu ban đầu cho đến kiểm thử end-to-end hoàn chỉnh.

Dưới đây là danh sách các tuần và tiến độ công việc:

---

### 🗂 **Tổng hợp Worklog theo từng tuần**

**Tuần 1:** [Khởi tạo dự án & phân tích yêu cầu hệ thống Fitness AI](1.1-week1/)  
→ Tìm hiểu yêu cầu nghiệp vụ, kiến trúc hệ thống, xác định entity và workflow.

**Tuần 2:** [Thiết lập Frontend & xây dựng UI cơ bản](1.2-week2/)  
→ Khởi tạo dự án React, tạo layout, xây dựng trang Training Plan Detail.

**Tuần 3:** [Tích hợp WebSocket cho phân tích chuyển động thời gian thực](1.3-week3/)  
→ Xây dựng WebSocket client, kiểm tra streaming dữ liệu, kết nối backend.

**Tuần 4:** [Tích hợp MediaPipe & phân tích góc cơ thể](1.4-week4/)  
→ Triển khai AI pose detection, xử lý landmark, tính toán góc tay/góc thân.

**Tuần 5:** [Phát triển Backend API & thiết lập MySQL Docker](1.5-week5/)  
→ Xây dựng entities, services, repositories với Spring Boot; cấu hình MySQL trong Docker.

**Tuần 6:** [Thiết kế API cho Challenge, Training Plan, Personalized Workout](1.6-week6/)  
→ Xây dựng CRUD, viết API endpoint, kiểm tra và validate dữ liệu.

**Tuần 7:** [Phát triển hệ thống tính reps, phân tích chuyển động & chấm điểm](1.7-week7/)  
→ Xây dựng logic tính điểm, custom reps, thuật toán tăng/giảm reps.

**Tuần 8:** [Cải thiện UX/UI: upload video, preview & tracking UI](1.8-week8/)  
→ Tối ưu giao diện TrainingPlanDetail và ChallengeDetailModal.

**Tuần 9:** [Tối ưu backend: lưu thông tin cơ thể & cá nhân hóa bài tập](1.9-week9/)  
→ Thu thập dữ liệu cơ thể người dùng, tích hợp vào logic phân tích.

**Tuần 10:** [Triển khai AWS RDS, thiết kế VPC, Subnet & Security Group](1.10-week10/)  
→ Migrate cơ sở dữ liệu từ Docker MySQL lên AWS RDS.

**Tuần 11:** [Triển khai Backend lên AWS Lambda + API Gateway](1.11-week11/)  
→ Đóng gói Spring Boot, build artifact, cấu hình Lambda & Layers.

**Tuần 12:** [Hoàn thiện hệ thống & kiểm thử end-to-end](1.12-week12/)  
→ Kiểm thử toàn bộ luồng hoạt động: Web → WebSocket → AI → Backend → Database.

---

Nhấn vào từng tuần để xem chi tiết công việc.
