# 🎮 Memory Game - Trò Chơi Trí Nhớ

Một trò chơi trí nhớ đẹp mắt và thú vị được xây dựng với React, Vite và Tailwind CSS. Test khả năng ghi nhớ của bạn bằng cách tìm các cặp thẻ giống nhau!

## 📋 Mục Lục

- [Giới thiệu](#giới-thiệu)
- [Cách Chơi](#cách-chơi)
- [Hướng Dẫn Settings](#hướng-dẫn-settings)
- [Tính Năng Đặc Biệt](#tính-năng-đặc-biệt)
- [Cách Cài Đặt](#cách-cài-đặt)
- [Cách Build](#cách-build)

---

## 🎯 Giới thiệu

Memory Game là trò chơi trí nhớ cổ điển với giao diện hiện đại và đẹp mắt. Người chơi cần tìm các cặp thẻ giống nhau trong thời gian giới hạn. Game có nhiều tùy chọn cấu hình để phù hợp với mọi trình độ chơi.

### ✨ Tính năng chính

- 🎨 Giao diện đẹp mắt với animations mượt mà
- ⚙️ Tùy chỉnh độ khó với nhiều tỉ lệ lưới khác nhau
- ⏱️ Hệ thống đếm thời gian với cảnh báo âm thanh
- 🖼️ Tùy chỉnh hình ảnh thẻ bài
- 🔊 Hiệu ứng âm thanh sống động
- 💾 Tự động lưu settings vào localStorage
- 🌙 Chế độ Standby khi không sử dụng

---

## 🎮 Cách Chơi

### Bước 1: Khởi động Game

1. Mở game, bạn sẽ thấy màn hình chính với 2 nút:
   - **START**: Bắt đầu chơi game
   - **SETTINGS**: Vào màn hình cài đặt

### Bước 2: Hiểu luật chơi

1. **Giai đoạn Preview**:
   - Khi bắt đầu, tất cả các thẻ sẽ tự động mở ra trong vài giây
   - Đây là cơ hội để bạn ghi nhớ vị trí của các cặp thẻ
   - Thời gian preview có thể tùy chỉnh trong Settings (mặc định: 3 giây)

2. **Giai đoạn Chơi**:
   - Sau khi preview, tất cả thẻ sẽ úp xuống
   - Click vào 2 thẻ để lật chúng lên
   - Nếu 2 thẻ giống nhau:
     - ✅ Thẻ sẽ hiển thị nền xanh lá trong 2 giây
     - ✅ Phát âm thanh "ting" (thành công)
     - ✅ Thẻ sẽ giữ nguyên mở và không thể click lại
   - Nếu 2 thẻ khác nhau:
     - ❌ Thẻ sẽ hiển thị nền đỏ trong 2 giây
     - ❌ Phát âm thanh "error" (thất bại)
     - ❌ Thẻ sẽ tự động úp xuống sau 2 giây

3. **Mục tiêu**:
   - Tìm tất cả các cặp thẻ giống nhau trước khi hết thời gian
   - Hoàn thành game để xem pháo hoa chúc mừng! 🎆

### Bước 3: Hoàn thành Game

- **Thắng**: Nếu bạn tìm được tất cả các cặp trước khi hết thời gian
  - Hiển thị popup chúc mừng với pháo hoa
  - Phát âm thanh "win_game"
  - Có 2 lựa chọn: **Chơi lại** hoặc **Về trang chủ**

- **Thua**: Nếu hết thời gian trước khi tìm được tất cả các cặp
  - Hiển thị popup thất bại
  - Phát âm thanh "lose_game"
  - Có 2 lựa chọn: **Chơi lại** hoặc **Về trang chủ**

### 💡 Mẹo chơi

- 🧠 Tập trung trong giai đoạn preview để ghi nhớ vị trí
- ⏰ Quản lý thời gian - đồng hồ sẽ chuyển màu đỏ và phát tiếng tick trong 5 giây cuối
- 🎯 Lập chiến lược - bắt đầu từ các góc và cạnh
- 🔄 Có thể click liên tục nhiều thẻ khác nhau để tìm cặp

---

## ⚙️ Hướng Dẫn Settings

Vào **SETTINGS** để tùy chỉnh game theo ý thích của bạn. Tất cả settings sẽ được tự động lưu và giữ nguyên khi bạn refresh trang.

### 1. Grid Ratio (Tỉ lệ Lưới)

Chọn số hàng và cột của lưới thẻ bài:

- **4x6** (Mặc định): 4 hàng × 6 cột = 24 thẻ (12 cặp) - **Dễ**
- **4x8**: 4 hàng × 8 cột = 32 thẻ (16 cặp) - **Trung bình**
- **6x6**: 6 hàng × 6 cột = 36 thẻ (18 cặp) - **Khó**
- **6x8**: 6 hàng × 8 cột = 48 thẻ (24 cặp) - **Rất khó**

**Gợi ý**: 
- Người mới chơi nên bắt đầu với **4x6**
- Người chơi có kinh nghiệm có thể thử **6x6** hoặc **6x8**

### 2. Play Time (Thời gian Chơi)

Thiết lập thời gian giới hạn cho mỗi lượt chơi:

- **Mặc định**: 60 giây
- **Tăng/Giảm**: Click nút **+** hoặc **−** để thay đổi
- **Bước nhảy**: Mỗi lần click tăng/giảm 15 giây
- **Giới hạn tối thiểu**: 60 giây (không thể giảm xuống dưới 60s)

**Cảnh báo thời gian**:
- Khi còn 5 giây cuối, đồng hồ sẽ:
  - Chuyển sang màu đỏ
  - Phát âm thanh "tick" mỗi giây để cảnh báo

**Gợi ý**:
- Người mới: 90-120 giây
- Người chơi trung bình: 60-90 giây
- Người chơi chuyên nghiệp: 60 giây hoặc ít hơn

### 3. Preview Time (Thời gian Xem Trước)

Thiết lập thời gian để xem tất cả thẻ trước khi bắt đầu chơi:

- **Mặc định**: 3 giây
- **Tăng/Giảm**: Click nút **+** hoặc **−** để thay đổi
- **Bước nhảy**: Mỗi lần click tăng/giảm 1 giây
- **Giới hạn tối thiểu**: 3 giây (không thể giảm xuống dưới 3s)

**Gợi ý**:
- Người mới: 5-7 giây để có thời gian ghi nhớ
- Người chơi trung bình: 3-5 giây
- Người chơi chuyên nghiệp: 3 giây (thử thách tối đa)

### 4. Card Images (Hình ảnh Thẻ Bài)

Tùy chỉnh hình ảnh hiển thị trên các thẻ bài:

- **Số lượng**: Game hỗ trợ tối thiểu 4 hình ảnh (mặc định có 8 hình)
- **Thay đổi**: 
  1. Hover chuột vào hình ảnh bạn muốn thay
  2. Click nút **"Change"** xuất hiện
  3. Chọn file hình ảnh từ máy tính của bạn
  4. Hình ảnh sẽ được tự động cập nhật

**Lưu ý**:
- Hình ảnh sẽ được lưu dưới dạng base64 trong localStorage
- Mỗi hình ảnh sẽ được sử dụng cho 2 thẻ (tạo thành 1 cặp)
- Nếu bạn có 8 hình ảnh, sẽ có 16 thẻ (8 cặp) trong game

**Gợi ý**:
- Sử dụng hình ảnh có độ phân giải vừa phải để game chạy mượt
- Chọn hình ảnh có màu sắc và hình dạng khác biệt để dễ phân biệt
- Có thể sử dụng hình ảnh cá nhân, logo, hoặc hình ảnh yêu thích

### 5. Reset to Defaults (Đặt lại Mặc định)

Click nút **"RESET TO DEFAULTS"** để:
- Khôi phục tất cả settings về giá trị mặc định
- Xóa tất cả hình ảnh tùy chỉnh và quay về hình ảnh mặc định
- Xóa dữ liệu đã lưu trong localStorage

**Lưu ý**: Hành động này không thể hoàn tác!

---

## 🌟 Tính Năng Đặc Biệt

### 🔊 Hiệu Ứng Âm Thanh

Game có các âm thanh để tăng trải nghiệm:

- **ting**: Khi tìm đúng cặp thẻ
- **error**: Khi chọn sai cặp thẻ
- **tick**: Tiếng đồng hồ trong 5 giây cuối (phát mỗi giây)
- **win_game**: Khi hoàn thành game thành công
- **lose_game**: Khi hết thời gian thua game

### 🌙 Chế Độ Standby

- Nếu không có tương tác trong **1 phút**, game sẽ tự động chuyển sang chế độ standby
- Hiển thị video clip standby để tiết kiệm tài nguyên
- Click bất kỳ đâu để quay lại màn hình trước đó
- **Lưu ý**: Standby sẽ **KHÔNG** kích hoạt khi đang trong game (frame Game)

### 💾 Tự Động Lưu Settings

- Tất cả settings được tự động lưu vào **localStorage** của trình duyệt
- Settings sẽ được giữ nguyên khi bạn:
  - Refresh trang
  - Đóng và mở lại trình duyệt
  - Chuyển sang tab khác

## 📝 Lưu Ý

- Game sử dụng **localStorage** để lưu settings, đảm bảo trình duyệt của bạn hỗ trợ và cho phép sử dụng localStorage
- Hình ảnh tùy chỉnh được lưu dưới dạng base64, có thể làm tăng kích thước localStorage
- Game hoạt động tốt nhất trên các trình duyệt hiện đại (Chrome, Firefox, Edge, Safari)


**Made with ❤️ using React + Vite + Tailwind CSS by DinoDev**
