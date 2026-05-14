# 🚀 Hiretify - Nền tảng tuyển dụng kết nối sinh viên và doanh nghiệp 

Hiretify là một nền tảng tuyển dụng hiện đại, được tối ưu hóa bằng Trí tuệ nhân tạo (AI), giúp kết nối sinh viên và các doanh nghiệp một cách nhanh chóng và chuyên nghiệp. Dự án không chỉ là một trang web tuyển dụng thông thường mà còn tích hợp các công nghệ tiên tiến nhất hiện nay.

---

## ✨ Tính năng nổi bật

### 🎓 Dành cho Ứng viên (Sinh viên)
- **AI Chatbot:** Trợ lý ảo thông minh giúp tìm kiếm việc làm và giải đáp quy trình qua ngôn ngữ tự nhiên.
- **Online CV Builder:** Trình tạo CV kéo thả chuyên nghiệp, cho phép xuất file PDF chất lượng cao.
- **Tìm kiếm thông minh:** Lọc công việc theo lĩnh vực, hình thức và từ khóa.
- **Quản lý ứng tuyển:** Nộp đơn nhanh, đính kèm Cover Letter và theo dõi trạng thái đơn hàng thời gian thực.
- **Chat thời gian thực:** Nhắn tin trực tiếp với nhà tuyển dụng qua Socket.io.

### 🏢 Dành cho Nhà tuyển dụng (Doanh nghiệp)
- **Đăng tin bằng AI:** Hỗ trợ đăng tin tuyển dụng nhanh chóng thông qua việc trò chuyện với Trợ lý ảo.
- **Quản lý ứng viên:** Xem hồ sơ, duyệt CV và cập nhật trạng thái ứng tuyển (Duyệt/Từ chối).
- **Hệ thống thông báo:** Nhận email thông báo tự động qua **Brevo API** khi có ứng viên mới.

### 🛡️ Dành cho Quản trị viên (Admin)
- **Dashboard:** Thống kê tổng quan về người dùng, công việc và các hoạt động trên hệ thống.
- **Quản lý báo cáo:** Xử lý các khiếu nại về tin tuyển dụng vi phạm từ người dùng.

---

## 🛠 Tech Stack

### 💻 Frontend
- **Framework:** React.js 19 (Vite)
- **State Management:** Zustand
- **Styling:** Tailwind CSS, Shadcn UI
- **Navigation:** React Router 7
- **Real-time:** Socket.io-client
- **Utilities:** Axios, Lucide Icons, html2canvas, jsPDF

### ⚙️ Backend
- **Framework:** Node.js, Express 5
- **Database:** MongoDB (Mongoose 9)
- **Real-time:** Socket.io
- **Authentication:** JWT (JsonWebToken), Bcryptjs
- **Media Storage:** Cloudinary, Multer
- **Email Service:** Brevo API (via Nodemailer)

### 🤖 AI Integration
- **Model:** Google Gemini AI
- **Features:** Natural Language Processing, Function Calling (Automated Job Posting)

---

## 🚀 Hướng dẫn cài đặt

### 1. Clone dự án
```bash
git clone https://github.com/thuongcjn/recruitment_plaform.git
cd recruitment_plaform
```

### 2. Cấu hình Backend
Di chuyển vào thư mục `server`, cài đặt thư viện và tạo file `.env`:
```bash
cd server
npm install
```
Cấu hình file `.env`:
```env
# Server Configuration
PORT=5000
NODE_ENV=development
MONGO_URI=your_mongodb_atlas_uri
CLIENT_URL=http://localhost:5173

# Authentication
JWT_SECRET=your_access_token_secret
JWT_REFRESH_SECRET=your_refresh_token_secret
JWT_EXPIRE=15m
JWT_REFRESH_EXPIRE=7d

# Google Gemini AI
GEMINI_API_KEY=your_google_ai_key

# Brevo Email API (SMTP)
BREVO_API_KEY=your_brevo_api_key
EMAIL_FROM=your_sender_email

# Cloudinary Storage
CLOUDINARY_CLOUD_NAME=your_name
CLOUDINARY_API_KEY=your_key
CLOUDINARY_API_SECRET=your_secret
```

### 3. Cấu hình Frontend
Di chuyển vào thư mục `client`, cài đặt và tạo file `.env`:
```bash
cd ../client
npm install
```
Cấu hình file `.env`:
```env
VITE_API_URL=http://localhost:5000
```

### 4. Khởi chạy
Chạy cả 2 terminal cho Server và Client bằng lệnh:
```bash
npm run dev
```

---

## 📂 Cấu trúc thư mục chính
```text
hiretify/
├── client/                 # Frontend React ứng dụng
│   ├── src/
│   │   ├── api/            # Dịch vụ gọi API
│   │   ├── components/     # UI, Layout, CV Builder, AI Components
│   │   ├── pages/          # Các trang chính (Dashboard, Chat, Profile...)
│   │   └── store/          # Quản lý trạng thái Zustand
├── server/                 # Backend Node.js ứng dụng
│   ├── config/             # Kết nối Database
│   ├── controllers/        # Logic nghiệp vụ (Auth, Job, AI, Chat...)
│   ├── models/             # Schema MongoDB
│   ├── routes/             # API Endpoints
│   └── utils/              # Socket.io & Email Services
```

---

## 📈 Star History

<a href="https://star-history.com/#thuongcjn/recruitment_plaform&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=thuongcjn/recruitment_plaform&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=thuongcjn/recruitment_plaform&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=thuongcjn/recruitment_plaform&type=Date" />
 </picture>
</a>

---

## 🤝 Đóng góp
Tôi luôn hoan nghênh các đóng góp để cải thiện dự án!
1. Fork dự án.
2. Tạo nhánh tính năng (`git checkout -b feature/AmazingFeature`).
3. Commit thay đổi (`git commit -m 'Add some AmazingFeature'`).
4. Push lên nhánh (`git push origin feature/AmazingFeature`).
5. Mở Pull Request.

---

## 📄 Giấy phép
Dự án được cấp phép theo MIT License.

⭐ **Nếu bạn thấy dự án này hữu ích, hãy tặng cho tôi một ngôi sao nhé!**

