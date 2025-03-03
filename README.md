# 🛠️ Golang RESTful API Invoices Project By Phạm Lê Kha

API này được xây dựng bằng Golang, sử dụng MySQL/MongoDB cho CRUD và các tính năng quản lý công việc.

---

## 🚀 **Cài Đặt**

1. **Clone project:**  
```bash
git clone https://github.com/SviverVew/invoice_master.git
```

2. **Cài dependencies:**  
```bash
go mod tidy
```

3. **Cấu hình `.env`:**  
```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=yourdatabase

MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-email-password
```

4. **Chạy server:**  
```bash
go run main.go
```
Server mặc định tại: `http://localhost:8080`.

---

## 📋 **API Endpoints**

### **User Management**
- **GET** `/users` - Lấy danh sách user
- **POST** `/users` - Tạo user mới
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "123456"
}
```
- **PUT** `/users/{id}` - Cập nhật user
- **DELETE** `/users/{id}` - Xóa user

### **Job Management**
- **GET** `/jobs` - Lấy danh sách công việc
- **POST** `/jobs` - Tạo công việc mới
```json
{
  "jobTitle": "Backend Developer",
  "workingLocation": "Ho Chi Minh City",
  "jobCategory": "IT"
}
```
- **POST** `/jobs/apply` - Ứng tuyển công việc
```json
{
  "id": "userID"
}
```

### **Password Reset**
- **POST** `/auth/reset-password` - Gửi email đặt lại mật khẩu
```json
{
  "email": "john@example.com"
}
```
- **POST** `/auth/update-password` - Cập nhật mật khẩu mới
```json
{
  "userID": "12345",
  "newPassword": "newpassword123"
}
```

---

## 🧪 **Test API**
Sử dụng **Postman** để kiểm tra các endpoint và các trường hợp đặc biệt.
