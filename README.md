# Weather App
*Đây là web mình làm theo trên youtube:https://www.youtube.com/watch?v=MIYQR-Ybrn4&list=PLjwm_8O3suyOgDS_Z8AWbbq3zpCmR-WE9, mình đã cải tiến thêm backend proxy với nodejs để bảo mật apiKey"
Ứng dụng thời tiết với bảo mật API key.*

## Cài đặt

1. Clone repository:
```bash
git clone <your-repo-url>
cd weather-app
```

2. Cài đặt dependencies:
```bash
npm install
```

3. Tạo file `.env` và thêm API key:
```bash
# Tạo file .env
echo "WEATHER_API_KEY=your_actual_api_key_here" > .env
```

4. Chạy ứng dụng:
```bash
npm start
```

Ứng dụng sẽ chạy tại `http://localhost:3000`

## Bảo mật API Key

### ✅ Cách đã triển khai:
- API key được lưu trong file `.env` (không được commit lên Git)
- Backend proxy để ẩn API key khỏi frontend
- File `.gitignore` để loại trừ các file nhạy cảm

### ⚠️ Lưu ý quan trọng:
1. **KHÔNG BAO GIỜ** commit API key lên Git
2. File `.env` đã được thêm vào `.gitignore`
3. Sử dụng backend proxy thay vì gọi API trực tiếp từ frontend

### 🔧 Cấu hình cho production:
- Sử dụng environment variables trên server
- Cấu hình CORS cho domain cụ thể
- Thêm rate limiting và validation

## Cấu trúc dự án

```
weather-app/
├── index.html          # Frontend
├── style.css           # CSS styles
├── server.js           # Backend proxy
├── package.json        # Dependencies
├── .env               # API key (không commit)
├── .gitignore         # Git ignore rules
└── images/            # Weather icons
```

## API Endpoints

- `GET /api/weather?city=<city_name>` - Lấy thông tin thời tiết

## Troubleshooting

Nếu gặp lỗi "API key not configured":
1. Kiểm tra file `.env` có tồn tại không
2. Đảm bảo API key đã được thêm vào file `.env`
3. Restart server sau khi thay đổi file `.env`


