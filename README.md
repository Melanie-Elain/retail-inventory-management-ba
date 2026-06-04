Retail Inventory Management System
1. Giới thiệu dự án
  Retail Inventory Management System là hệ thống quản lý cửa hàng bán lẻ được phát triển nhằm hỗ trợ toàn bộ quy trình kinh doanh từ quản lý sản phẩm, tồn kho, nhập hàng, bán hàng đến theo dõi đơn hàng và báo cáo thống kê.

  Hệ thống được xây dựng theo kiến trúc phân lớp (Layered Architecture) kết hợp Repository Pattern và Service Layer nhằm đảm bảo khả năng mở rộng, bảo trì và tái sử dụng mã nguồn.

  Dự án được thực hiện với mục tiêu mô phỏng quy trình vận hành thực tế của một cửa hàng bán lẻ quy mô vừa và nhỏ.

2. Mục tiêu dự án
    Quản lý sản phẩm và danh mục sản phẩm.
    Quản lý kho hàng và tồn kho.
    Quản lý nhà cung cấp.
    Quản lý nhập hàng.
    Quản lý đơn hàng bán.
    Quản lý chương trình khuyến mãi.
    Quản lý khách hàng.
    Theo dõi doanh thu và báo cáo thống kê.
    Áp dụng nguyên tắc FIFO trong quản lý xuất kho.
    Ghi nhận Audit Log cho các thao tác quan trọng.

3. Phạm vi hệ thống
  Front Office (Customer)
    Đăng ký tài khoản
    Đăng nhập
    Xem sản phẩm
    Tìm kiếm sản phẩm
    Quản lý giỏ hàng
    Đặt hàng
    Xem hóa đơn
    Theo dõi lịch sử đơn hàng
  Back Office (Staff)
    Sales Staff
      Quản lý đơn hàng
      Quản lý khuyến mãi
      Xem thống kê bán hàng
      Tra cứu sản phẩm
    Warehouse Staff
      Quản lý nhập hàng
      Quản lý tồn kho
      Quản lý kho hàng
      Quản lý nhà cung cấp
    Administrator
      Quản lý toàn bộ dữ liệu hệ thống
      Quản lý nhân viên
      Quản lý khách hàng
      Quản lý sản phẩm
      Quản lý đơn hàng
      Quản lý kho
      Quản lý báo cáo

4. Công nghệ sử dụng
  Backend
    ASP.NET Core Web API
    Entity Framework Core
    MySQL
    Swagger/OpenAPI
  Frontend
    Blazor Interactive Server
    Blazorise
    Tailwind CSS
  Kiến trúc
    Repository Pattern
    Service Layer Pattern
    Dependency Injection
    RESTful API

5. Kiến trúc hệ thống
Client (Blazor UI)
       │
       ▼
REST API Controllers
       │
       ▼
Business Services
       │
       ▼
Generic Repository
       │
       ▼
     MySQL

6. Cơ sở dữ liệu
  Hệ thống được thiết kế theo mô hình quan hệ với các nhóm bảng chính:
  Người dùng & Hệ thống
    users
    customers
    audit_logs
  Sản phẩm & Kho hàng
    products
    categories
    warehouses
    inventory
    suppliers
  Nhập hàng
    purchase_orders
    purchase_items
  Bán hàng
    carts
    cart_items
    orders
    order_items
    payments
  Khuyến mãi
    promotions
    promotion_products

7. Nghiệp vụ chính
  Quy trình đặt hàng
    Khách hàng thêm sản phẩm vào giỏ hàng.
    Khách hàng thực hiện checkout.
    Hệ thống tạo đơn hàng.
    Kiểm tra tồn kho.
    Trừ tồn kho theo FIFO.
    Tạo hóa đơn.
    Nhân viên xử lý đơn hàng.
    Hoàn tất giao hàng.
  Quy trình nhập hàng
    Nhân viên kho tạo phiếu nhập.
    Chọn nhà cung cấp.
    Nhập sản phẩm và số lượng.
    Hệ thống cập nhật tồn kho.
    Ghi nhận lịch sử nhập hàng.

8. Các chức năng nổi bật
  Quản lý tồn kho FIFO
  Hệ thống áp dụng nguyên tắc First In First Out (FIFO) để đảm bảo hàng nhập trước được xuất trước.
  Audit Logging
    Ghi nhận:
    Đăng nhập
    Tạo dữ liệu
    Cập nhật dữ liệu
    Xóa dữ liệu
  Quản lý khuyến mãi
    Hỗ trợ:
    Voucher giảm theo phần trăm
    Voucher giảm theo số tiền cố định
    Giới hạn thời gian sử dụng
  Dashboard thống kê
    Theo dõi:
    Doanh thu
    Đơn hàng
    Sản phẩm
    Khách hàng

9. API Documentation
Swagger được tích hợp để kiểm thử và tài liệu hóa API.
https://localhost:xxxx/

10. Cấu trúc dự án
retail-inventory-management-ba
│
├── backend
│
├── frontend
│
├── docs
│   ├── business-requirements
│   ├── stakeholder-analysis
│   ├── process-flow
│   ├── use-cases
│   ├── user-stories
│   ├── urs
│   ├── wireframes
│   ├── api-analysis
│   ├── test-cases
│   └── screenshots
│
└── README.md

11. Tài liệu Business Analysis
| Tài liệu | Nội dung |
| :--- | :--- |
| **BRD** | Business Requirements Document |
| **Stakeholder Analysis** | Phân tích các bên liên quan |
| **Use Case List** | Danh sách chức năng hệ thống |
| **Use Case Diagram** | Sơ đồ Use Case |
| **Product Backlog** | Danh sách User Story |
| **URS** | User Requirement Specification |
| **Process Flow** | Quy trình nghiệp vụ |
| **API Documentation** | Phân tích API |
| **Test Cases** | Kiểm thử chức năng |
| **Wireframes** | Thiết kế giao diện |
| **Screenshots** | Hình ảnh hệ thống |


12. Hướng phát triển
  Tích hợp cổng thanh toán trực tuyến.
  Tích hợp Email Notification.
  Hỗ trợ đa kho hàng.
  Triển khai phân quyền chi tiết hơn.
  Tối ưu hiệu năng truy vấn.
  Triển khai Docker và CI/CD.
  Nâng cấp cơ sở dữ liệu lên SQL Server hoặc PostgreSQL.
  Bổ sung báo cáo BI trực quan.

13. Tác giả
  Trần Bảo Hân
  Business Analyst Intern / System Analyst Fresher
  Project: Retail Inventory Management System

