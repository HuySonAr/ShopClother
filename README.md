# ShopClother

Đây là dự án Monorepo chứa cả **Frontend** (Next.js) và **Backend** (NestJS), sử dụng `pnpm` làm trình quản lý gói.

## 🚀 Hướng dẫn Cài đặt Môi trường (Cho cả Team)

### 1. Yêu cầu hệ thống
- **Node.js**: Phiên bản 18 trở lên.
- **pnpm**: Bắt buộc sử dụng `pnpm` thay vì `npm` hay `yarn` để tránh xung đột thư viện.
  - Cài đặt pnpm (nếu chưa có): `npm install -g pnpm`

### 2. Cài đặt toàn bộ dự án
Vì đây là cấu trúc Workspace, bạn chỉ cần đứng ở **thư mục gốc (root)** của dự án và chạy:
```bash
pnpm install
```
Lệnh này sẽ tự động cài đặt tất cả thư viện cho cả thư mục `frontend` và `backend`.

---

## 💻 Hướng dẫn chạy Frontend (Next.js)

1. Mở terminal và di chuyển vào thư mục frontend:
   ```bash
   cd frontend
   ```
2. Khởi động server môi trường dev:
   ```bash
   pnpm dev
   ```
3. Mở [http://localhost:3000](http://localhost:3000) trên trình duyệt để xem.

4. Quy chuẩn Code (Coding Standards)
### Format Code tự động
Dự án đã được cấu hình **Prettier** kết hợp với plugin `prettier-plugin-tailwindcss` để tự động sắp xếp (sort) các class của Tailwind theo đúng chuẩn.

**Yêu cầu với team:**
- Đảm bảo bạn đã cài đặt extension **[Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)** trong VS Code.
- Bật tính năng **Format On Save** trong VS Code:
  1. Mở Cài đặt (`Ctrl + ,` hoặc `Cmd + ,`)
  2. Tìm kiếm `Format On Save`
  3. Tích chọn ô `Editor: Format On Save`
  4. Đảm bảo `Default Formatter` được set là Prettier.
- Khi lưu file, các class Tailwind dài sẽ được tự động sắp xếp gọn gàng.

---

## ⚙️ Hướng dẫn chạy Backend (NestJS)

1. Mở một terminal khác (song song với frontend) và di chuyển vào thư mục backend:
   ```bash
   cd backend
   ```
2. Khởi động server môi trường dev (có chế độ tự động reload khi sửa code):
   ```bash
   pnpm start:dev
   ```
3. Server API mặc định thường sẽ chạy ở port **8080**.

*(Các lệnh hữu ích khác cho Backend: `pnpm build`, `pnpm test`, `pnpm format`)*

---

## 📌 Tóm tắt Workflow hằng ngày cho team
Mỗi khi bắt đầu ngày làm việc hoặc pull code mới về, bạn nên làm theo thứ tự sau:
1. Mở terminal ở **thư mục gốc**: `pnpm install` (để cập nhật gói mới nếu có).
2. Mở terminal 1 ở `frontend`: `pnpm dev`.
3. Mở terminal 2 ở `backend`: `pnpm start:dev`.
4. Bắt đầu code!
