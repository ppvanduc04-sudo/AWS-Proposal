---
title: "Worklog Tuần 4"
date: "2025-09-29"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Cài đặt, cấu hình và triển khai VPN site-to-site trên Linux 2023.  
* Chuyển từ Openswan sang Libreswan do Openswan không tương thích với Linux 2023.  
* Hiểu cơ chế IPsec, IKE, DPD và cách kiểm tra trạng thái kết nối VPN.  

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                       |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------ |
| 2   | - Kiểm tra trạng thái Openswan trên Linux 2023 <br> - Dùng lệnh: `ipsec verify`, `ipsec whack --status` <br> - Xác định lỗi kết nối và dịch vụ không khởi động được          | 01/10/2025   | 01/10/2025      | Linux man pages, Openswan docs       |
| 3   | - Kiểm tra log Pluto & systemd: `journalctl -xeu ipsec.service` <br> - Phát hiện lỗi Pluto không chạy và file `/run/pluto/pluto.ctl` không tồn tại                        | 02/10/2025   | 02/10/2025      | Linux systemd docs                   |
| 4   | - Quyết định chuyển sang Libreswan 4.12 <br> - Backup cấu hình cũ `/etc/ipsec.conf` & `/etc/ipsec.d/`                                                                     | 03/10/2025   | 03/10/2025      | Libreswan official docs              |
| 5   | - Cài đặt Libreswan trên Linux 2023 <br> - Tạo file `/etc/ipsec.conf` và `/etc/ipsec.secrets` mới <br> - Cấu hình connection Tunnel2 với IP local & remote chính xác      | 04/10/2025   | 04/10/2025      | Libreswan official docs              |
| 6   | - Kiểm tra cấu hình: `ipsec validate`, `ipsec auto --check` <br> - Khởi động dịch vụ VPN: `systemctl restart ipsec` <br> - Kiểm tra trạng thái VPN `ipsec whack --status` | 05/10/2025   | 05/10/2025      | Libreswan docs, Linux man pages      |
| 7   | - Cấu hình hệ thống hỗ trợ VPN: <br> &emsp; + Bật IP forwarding <br> &emsp; + Firewall: mở UDP 500 & 4500 <br> - Test kết nối site-to-site VPN                           | 06/10/2025   | 07/10/2025      | Linux networking docs, AWS docs      |

### Kết quả đạt được tuần 4:

* Libreswan 4.12 đã được cài đặt và hoạt động ổn định trên Linux 2023.  
* Cấu hình VPN site-to-site với Tunnel2 được load và Pluto chạy ổn định.  
* Openswan 2.6.x đã được thay thế hoàn toàn do không tương thích với Linux 2023.  
* Kiến thức về IPsec, IKE, DPD, các thuật toán phase1 & phase2 (AES, SHA1, MODP1024) được củng cố.  
* Có khả năng kiểm tra và quản lý trạng thái VPN bằng lệnh:  
  * `ipsec whack --status`  
  * `ipsec validate`  
  * `journalctl -xeu ipsec.service`  
* Hệ thống được cấu hình sẵn sàng cho kết nối VPN, hỗ trợ forwarding và firewall UDP cho IPsec.  
* Chuẩn bị sẵn sàng để test kết nối thực tế với bên đối tác.
