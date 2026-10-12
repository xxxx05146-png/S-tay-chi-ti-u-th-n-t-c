# Sổ Tay Chi Tiêu Cá Nhân (Single Page Application - PWA)

Ứng dụng web sổ tay chi tiêu cá nhân tối ưu hóa cho màn hình điện thoại (Mobile-First, PWA-Ready), được đóng gói trọn vẹn trong **1 file `index.html` duy nhất** (kết hợp đầy đủ HTML5, CSS3 hiện đại và JavaScript thuần).

---

## 🌟 Tính Năng Nổi Bật

### 1. Bàn Phím Số Tích Hợp (Custom In-App Keypad)
- **Tự động nhận diện nghìn đồng:** Không cần gõ ba số 0!
  - Bấm `5` $\rightarrow$ Màn hình hiển thị `5.000 đ`
  - Bấm `30` $\rightarrow$ Màn hình hiển thị `30.000 đ`
  - Bấm `120` $\rightarrow$ Màn hình hiển thị `120.000 đ`
  - Bấm `1500` $\rightarrow$ Màn hình hiển thị `1.500.000 đ`
- **Âm thanh gõ cơ học (Mechanical Audio Feedback):** Tích hợp Web Audio API phát xung âm thanh sắc nét tần số cao **~1200Hz, độ dài 5ms** kết hợp rung haptic (`navigator.vibrate`) mô phỏng tiếng bấm nút cơ học thật mỗi khi chạm phím.
- **Luồng ghi chép 1 chạm siêu tốc:** Bấm số tiền $\rightarrow$ Chạm thẳng vào biểu tượng Danh mục $\rightarrow$ Giao dịch được lưu ngay lập tức, cập nhật số dư khả dụng, đưa bàn phím về 0 (không cần nút OK/Lưu rườm rà).

### 2. Danh Mục Phân Biệt Màu Sắc (Color-Coded)
Mỗi danh mục có biểu tượng emoji sinh động, nền pastel nhẹ và viền nổi bật:
* **Tiền ra (Chi tiêu):**
  - 🍛 Ăn uống (`#F97316` - Cam)
  - ☕ Đồ uống/Cà phê (`#F59E0B` - Hổ phách)
  - 🏠 Trọ / KTX (`#2563EB` - Xanh dương)
  - 📚 Học tập/Giáo trình (`#6366F1` - Indigo)
  - 🤖 Dịch vụ AI (`#8B5CF6` - Tím)
  - 👕 Quần áo (`#EC4899` - Hồng)
  - 💊 Sức khỏe/Thuốc (`#EF4444` - Đỏ)
  - 🛵 Đi lại/Xăng xe (`#06B6D4` - Cyan)
  - 🛒 Nhu yếu phẩm (`#10B981` - Xanh ngọc)
  - 📦 Khác (`#64748B` - Xám Slate)
* **Tiền vào (Thu nhập):**
  - 💼 Dạy thêm/Lương (`#16A34A` - Xanh lục)
  - 👨‍👩‍👧 Trợ cấp gia đình (`#0D9488` - Xanh ngọc)
  - 🎁 Khác (`#CA8A04` - Vàng đồng)

### 3. Giao Diện & Trải Nghiệm (UI/UX)
- **Top Bar:** Hiển thị thời gian thực tiếng Việt (`Thứ X, ngày DD/MM`) và icon bánh răng `⚙️` mở bảng cài đặt.
- **Card Số dư thông minh:**
  - Hiển thị nổi bật số dư khả dụng (kèm nút `👁️` ẩn/hiện số dư để bảo mật).
  - Tích hợp thanh tiến độ Hạn mức chi tiêu mỗi ngày: Tự động đổi màu cảnh báo đỏ rực nếu tiêu vượt hạn mức.
  - Tổng số tiền thực tế đã chi trong ngày hôm nay.
- **Cử chỉ vuốt tay (Swipe Gestures):**
  - Vuốt sang phải $\rightarrow$ Chuyển nhanh sang tab **Tiền vào**.
  - Vuốt sang trái $\rightarrow$ Chuyển nhanh sang tab **Tiền ra**.
  - Hoặc chạm 2 tab chuyển đổi cố định ở trên.
- **Lịch sử 5 giao dịch gần nhất:** Nằm ở đáy màn hình, nút `[✕]` xóa giao dịch sẽ **tự động hoàn lại số dư tương ứng** tức thì.

### 4. Lưu Trữ Offline & Đồng Bộ Google Sheets
- **Offline-First:** Lưu trữ 100% trên thiết bị qua `localStorage` (mở tức thì không cần mạng, không sợ mất dữ liệu).
- **Google Sheets Webhook Sync:** Gửi request POST ngầm (mode `no-cors`) đồng bộ lên Google Spreadsheet mỗi khi phát sinh giao dịch.

### 5. Cài Đặt (Settings Modal)
- Chuyển đổi giao diện Sáng / Tối (Light / Dark mode).
- Điều chỉnh thủ công số dư ví hiện tại.
- Bật/Tắt hạn mức ngày & cài đặt định mức chi tiêu.
- Cấu hình link Google Apps Script Webhook URL & nút test kết nối.
- Xuất file sao lưu dự phòng JSON và Đặt lại dữ liệu.

---

## 🚀 Hướng Dẫn Sử Dụng Nhanh

### Cách 1: Mở Trực Tiếp Trên Máy Tính
Chỉ cần nhấp đúp vào file `index.html` để mở trong trình duyệt Chrome, Edge, Safari hoặc Firefox.
> **Mẹo trên máy tính:** Bạn có thể bấm các phím số `0-9`, phím `Backspace`, phím `C` (hoặc `Esc`) và mũi tên trái/phải `←` `→` để điều khiển ứng dụng cực nhanh!

---

### Cách 2: Triển Khai Miễn Phí Lên GitHub Pages
1. Tạo một Repository mới trên GitHub (ví dụ: `so-tay-chi-tieu`).
2. Tải file `index.html` lên thư mục gốc (root) của Repository.
3. Vào **Settings** của Repo $\rightarrow$ chọn mục **Pages** (cột bên trái).
4. Tại mục **Build and deployment** $\rightarrow$ **Branch**: chọn `main` (hoặc `master`), thư mục `/(root)` $\rightarrow$ Nhấn **Save**.
5. Sau 1 phút, bạn sẽ nhận được đường link dạng:
   ```text
   https://<username>.github.io/so-tay-chi-tieu/
   ```

---

### Cách 3: Ghim Ra Màn Hình Chính Điện Thoại (Cài PWA)
- **Trên iPhone (Safari):**
  1. Mở link GitHub Pages trên trình duyệt **Safari**.
  2. Bấm nút **Chia sẻ** (biểu tượng hình vuông có mũi tên hướng lên).
  3. Cuộn xuống và chọn **Thêm vào MH chính** (Add to Home Screen).
  4. Ứng dụng sẽ xuất hiện trên màn hình điện thoại như một app native độc lập không có thanh địa chỉ duyệt web!
- **Trên Android (Chrome):**
  1. Mở link trên trình duyệt **Chrome**.
  2. Bấm vào biểu tượng menu **3 chấm** góc trên bên phải.
  3. Chọn **Cài đặt ứng dụng** (Install App) hoặc **Thêm vào màn hình chính**.

---

## 📊 Hướng Dẫn Kết Nối Google Sheets Tự Động

Ứng dụng hỗ trợ tự động ghi nhận mỗi khoản thu chi vào Google Sheet của bạn qua Google Apps Script Webhook:

### Bước 1: Tạo Google Sheet
1. Mở [Google Sheets](https://sheets.new) và tạo 1 bảng tính mới.
2. Tạo các tiêu đề cột tại dòng 1:
   - Cột A: `Thời gian ghi`
   - Cột B: `Thời gian giao dịch`
   - Cột C: `Loại (Tiền ra/vào)`
   - Cột D: `Danh mục`
   - Cột E: `Số tiền (VNĐ)`
   - Cột F: `Số dư sau GD`

### Bước 2: Tạo Apps Script
1. Trên menu Google Sheet, chọn **Tiện ích mở rộng (Extensions)** $\rightarrow$ **Apps Script**.
2. Xóa hết mã cũ và dán đoạn mã sau:

```javascript
function doPost(e) {
  try {
    var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
    var data = JSON.parse(e.postData.contents);
    
    // Ghi dòng dữ liệu mới
    sheet.appendRow([
      new Date(),
      data.formattedDate,
      data.type,
      data.category,
      data.amount,
      data.balanceAfter
    ]);
    
    return ContentService.createTextOutput(JSON.stringify({
      status: "success",
      message: "Recorded successfully"
    })).setMimeType(ContentService.MimeType.JSON);
  } catch (error) {
    return ContentService.createTextOutput(JSON.stringify({
      status: "error",
      message: error.toString()
    })).setMimeType(ContentService.MimeType.JSON);
  }
}
```

### Bước 3: Triển Khai (Deploy) Lấy Link Webhook
1. Nhấn nút **Triển khai (Deploy)** ở góc trên bên phải $\rightarrow$ chọn **Triển khai mới (New deployment)**.
2. Chọn loại: **Ứng dụng web (Web app)** (icon bánh răng).
3. Thiết lập:
   - **Mô tả:** `Webhook Sổ Tay Chi Tiêu`
   - **Thực thi dưới dạng (Execute as):** `Tôi (email của bạn)`
   - **Ai có quyền truy cập (Who has access):** Chọn **Bất kỳ ai (Anyone)**.
4. Nhấn **Triển khai (Deploy)** $\rightarrow$ Cấp quyền truy cập nếu được yêu cầu.
5. Sao chép đường link **URL ứng dụng web** (có dạng `https://script.google.com/macros/s/.../exec`).

### Bước 4: Đã Tích Hợp Sẵn Vào App!
> [!NOTE]
> Đường link Webhook Google Apps Script của bạn:
> `https://script.google.com/macros/s/AKfycbyrW2usnveDLDDNH83v-ygl6vlsjX_QrmXhkAEJq3iC07z9rZMZgilKouoU4Cvf130h3g/exec`
> đã được **tích hợp sẵn làm mặc định** vào ứng dụng.
> - Mỗi khi bạn ghi một khoản tiền chi hay thu trong app, dữ liệu sẽ tự động được gửi ngầm tới Google Sheet của bạn.
> - Bạn có thể bấm nút bánh răng `⚙️` $\rightarrow$ bấm **🧪 Test gửi thử** để kiểm tra đồng bộ bất kỳ lúc nào.

