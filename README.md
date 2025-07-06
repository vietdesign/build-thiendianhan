# Thiên Địa Nhân - Ứng dụng Phong Thủy & Tử Vi

🌐 **Domain**: [thiendianhan.app](https://thiendianhan.app)

Ứng dụng phong thủy, tử vi và thiên văn học toàn diện với hệ thống thành viên cao cấp và quản lý nội dung chuyên nghiệp.

## ✨ Tính năng chính

### 🌟 Hệ Mặt Trời (Solar System)
- Mô phỏng hệ mặt trời 3D tương tác
- Thông tin chi tiết về 8 hành tinh
- Hiệu ứng visual đẹp mắt với WebGL
- **Route**: `/solar`

### 📰 Tin Tức (Trang chủ)
- Hệ thống tin tức phong thủy và tử vi
- Hot news và bài viết theo chuyên đề
- Slider tin nổi bật với skeleton loading
- **Route**: `/` (trang chủ)

### 📅 Xem Ngày (Calendar)
- Tìm ngày tốt cho các hoạt động
- Tính toán theo âm lịch và dương lịch
- **Trừ sao tự động** sau 1 phút sử dụng
- **Route**: `/calendar`

### 🗓️ Lịch Việt
- **Tab Lịch Âm**: Xem ngày âm lịch, pha mặt trăng
- **Tab Lịch Tiết Khí**: Tính toán 24 tiết khí
- **Miễn phí** cho tất cả người dùng
- **Route**: `/lich-viet`

### 🎯 Bát Tự (Tử Vi)
- Tính toán bát tự cá nhân chi tiết
- Phân tích ngũ hành sinh khắc
- Tư vấn hướng đi và nghề nghiệp phù hợp
- **Trừ sao tự động** sau 1 phút sử dụng
- **Route**: `/battu`

### 🧭 La Kinh (Phong Thủy)
- Tính hướng phong thủy chính xác
- Sử dụng la bàn điện tử GPS
- Tính toán cát hung theo địa lý
- **Trừ sao tự động** sau 1 phút sử dụng
- **Route**: `/lakinh`

### 🌊 Lục Hào (Thủy Triều)
- Dự đoán thủy triều theo khu vực
- Thông tin về pha mặt trăng chi tiết
- Lịch thuỷ triều hàng ngày
- **Trừ sao tự động** sau 1 phút sử dụng
- **Route**: `/luchao`

## 🔐 Hệ thống Xác thực & Membership

### Đăng ký tài khoản
- Đăng ký bằng email và mật khẩu
- Xác thực email tự động
- **Tự động tạo gói Basic** với 20 sao
- Lưu trữ thông tin user an toàn

### Đăng nhập
- **Admin**: Tài khoản admin mặc định (admin/22121985)  
- **Firebase**: Đăng nhập bằng tài khoản đã đăng ký
- Phiên đăng nhập có hiệu lực **3 ngày**

### Bảo mật
- Xác thực email bắt buộc
- Mã hóa mật khẩu
- Tự động đăng xuất sau 3 ngày

## ⭐ Hệ thống Membership & Stars

### Các hạng thành viên
- **Basic** (20 sao/tháng): Mặc định khi đăng ký
- **Standard** (200 sao/tháng): VIP 1 tháng
- **Premium** (3000 sao/năm): VIP 1 năm
- **Master** (200 sao/ngày): VIP 1 năm

### Tính năng Stars System
- **Trừ sao tự động** khi sử dụng trang quá 1 phút
- **Countdown notification** 60 giây trước khi trừ sao
- **Cooldown 10 phút** giữa các lần trừ sao
- **Reset tự động** theo chu kỳ gói
- **Admin quản lý** sao của users

### Quyền truy cập
- **Tất cả users** có **full permissions** cho tất cả tính năng
- **Phân biệt** qua số sao và thời hạn membership
- **Không hạn chế** quyền truy cập dựa trên gói

## 📊 Thống kê truy cập
- Đếm lượt truy cập từng trang
- Lưu trữ thống kê trên Firebase
- Hiển thị realtime counter
- Performance optimization với caching

## 🛠️ Admin Panel

### Quản lý Users
- Danh sách tất cả thành viên
- Chi tiết thông tin user
- **Cộng sao** cho users (1-1000 sao)
- **Nâng cấp membership** tiers
- Quản lý permissions (symbolic)

### Quản lý News
- Tạo/Sửa articles
- Quản lý categories
- Preview trước khi publish
- Bulk operations

### Dashboard & Analytics
- Thống kê users theo membership tiers
- Page views và visit counters
- Registration analytics
- Expiring memberships alerts

## 🚀 Deployment & Production

### 🌐 Live Website
- **Production**: [thiendianhan.app](https://thiendianhan.app)
- **Staging**: [lunar-calendar.vercel.app](https://lunar-calendar.vercel.app)

### 📋 Domain Setup
- Xem chi tiết: [DOMAIN_SETUP_GUIDE.md](DOMAIN_SETUP_GUIDE.md)
- DNS Configuration cho thiendianhan.app
- SSL Certificate tự động từ Vercel

### 🚀 Local Development

#### Yêu cầu
- Node.js >= 16
- npm hoặc yarn
- Firebase project

#### Cài đặt dependencies
```bash
npm install
```

#### Cấu hình Firebase
1. Tạo file `.env` từ template
2. Điền thông tin Firebase config
3. Chi tiết xem [FIREBASE_AUTH_SETUP.md](FIREBASE_AUTH_SETUP.md)

#### Chạy ứng dụng
```bash
npm start
```

Mở [http://localhost:3000](http://localhost:3000) để xem trong browser.

#### Build cho production
```bash
npm run build
```

## 📁 Cấu trúc project

```
src/
├── components/          # React components
├── pages/              # Các trang chính
├── contexts/           # React contexts (Auth)
├── hooks/              # Custom hooks (usePageTimeTracker, usePermissions)
├── utils/              # Utility functions
├── data/               # Dữ liệu tĩnh
├── assets/             # Hình ảnh, icons
├── admin/              # Admin panel components & pages
└── firebase/           # Firebase configuration
```

## 🔧 Performance & Optimizations

### 📊 Visit Tracking Optimization
- **97.8% reduction** trong Firebase writes
- **Batch processing** với 30s intervals
- **Local queuing** và fallback mechanisms
- **Session-based** visit counting

### 🎯 Page Points System
- **Smart countdown** với pause/resume
- **Page Visibility API** integration
- **Toast notifications** với skip functionality
- **Cooldown management** với localStorage

### ⚡ General Optimizations
- **Cached categories** (5 phút expiry)
- **Parallel data loading** với Promise.all
- **Reduced Firebase calls** qua batching
- **Session storage** cho page stats
- **Conditional setup** chỉ khi cần thiết

### 🛡️ Fallback Mechanisms
- **Composite index fallback** cho Firestore queries
- **Client-side filtering** khi server query thất bại
- **Graceful error handling** cho tất cả operations

## 💡 Demo Mode

Nếu chưa cấu hình Firebase:
- Vẫn có thể đăng nhập bằng admin
- Page counter sẽ hiển thị "--"
- Stars system hiển thị demo data
- Tính năng đăng ký/đăng nhập Firebase sẽ báo lỗi

## 📖 Tài liệu chi tiết

### 🔧 Setup & Configuration
- [Domain Setup Guide](DOMAIN_SETUP_GUIDE.md) - Cấu hình thiendianhan.app
- [Firebase Setup](FIREBASE_SETUP.md) - Cài đặt Firebase
- [Firebase Authentication](FIREBASE_AUTH_SETUP.md) - Hệ thống đăng nhập
- [Firestore Indexes](FIRESTORE_INDEX_SETUP.md) - Database indexes

### 💎 Features & Systems
- [Membership System](MEMBERSHIP_SYSTEM_GUIDE.md) - Hệ thống thành viên
- [Permissions Guide](PERMISSIONS_GUIDE.md) - Quản lý quyền
- [News System](NEWS_SETUP_GUIDE.md) - Hệ thống tin tức
- [Page Points Deduction](PAGE_POINTS_DEDUCTION_GUIDE.md) - Trừ sao tự động

### 🚀 Performance & Optimization
- [Visit Tracking Optimization](VISIT_TRACKING_OPTIMIZATION.md) - Tối ưu tracking
- [Page Visibility Fix](PAGE_VISIBILITY_FIX.md) - Fix countdown pause/resume
- [Toast Visibility Fix](TOAST_VISIBILITY_FIX.md) - Fix toast disappearing
- [Dashboard Page Names Update](DASHBOARD_PAGE_NAMES_UPDATE.md) - Cập nhật tên trang

## 🛠️ Tech Stack

### Frontend
- **React** - UI framework
- **Tailwind CSS** - Styling
- **React Router** - Navigation
- **Heroicons** - Icon system

### Backend & Database
- **Firebase Auth** - Authentication
- **Firestore** - Database
- **Firebase Storage** - File storage

### Performance
- **Service Worker** - Caching
- **Lazy Loading** - Component optimization
- **Code Splitting** - Bundle optimization

### 3D Graphics
- **Three.js** - Solar System visualization

## 🐛 Troubleshooting

### Lỗi thường gặp
1. **Missing projectId**: Chưa cấu hình `.env` file
2. **Email verification**: Kiểm tra spam folder
3. **Firebase permissions**: Kiểm tra Firestore rules
4. **Stars không update**: Kiểm tra real-time listener
5. **Composite index**: Tạo indexes cho Firestore queries

### Debug Pages
- `/debug` - Firestore data debug
- `/permission-test` - Test permissions system

### Liên hệ hỗ trợ
- Tạo issue trên GitHub
- Kiểm tra documentation trong project
- 📧 Email: admin@lunarapp.com
- 📱 Hotline: 0123-456-789

## 🌐 Production Deployment

### Current Deployment
- **Platform**: Vercel
- **Domain**: [thiendianhan.app](https://thiendianhan.app)
- **Auto-deploy**: Connected to GitHub main branch

### Vercel Configuration
```json
{
  "buildCommand": "npm run build",
  "outputDirectory": "build",
  "framework": "create-react-app",
  "routes": [
    {
      "src": "/[^.]+",
      "dest": "/",
      "status": 200
    }
  ]
}
```

### Environment Variables (Production)
```env
REACT_APP_FIREBASE_API_KEY=production_api_key
REACT_APP_FIREBASE_AUTH_DOMAIN=thiendianhan.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=thiendianhan
REACT_APP_FIREBASE_STORAGE_BUCKET=thiendianhan.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=sender_id
REACT_APP_FIREBASE_APP_ID=app_id
REACT_APP_FIREBASE_MEASUREMENT_ID=measurement_id
```

## 🔮 Future Roadmap

### Planned Features
- [ ] Real-time chat system
- [ ] Mobile app (React Native)
- [ ] AI-powered fortune telling
- [ ] Social features & sharing
- [ ] Premium content subscription
- [ ] Multi-language support

### Performance Improvements
- [ ] PWA implementation
- [ ] Image optimization
- [ ] Full-text search
- [ ] Push notifications
- [ ] Offline support

## 📊 Analytics & Monitoring

### Built-in Analytics
- Page visit tracking
- User registration analytics
- Membership conversion rates
- Stars usage patterns

### Firebase Analytics
- User engagement metrics
- Performance monitoring
- Crash reporting
- Custom events tracking

## 🤝 Contributing

1. Fork the project
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Lunar calendar algorithms
- Vietnamese astronomical data
- Firebase team for excellent platform
- React community for awesome ecosystem
