# Tổng Hợp Giải Pháp Dự Án CampusPay

## 1. Phân Tích Rủi Ro & Nguyên Nhân
* **Business Plan (Mất trắng):** Phụ thuộc hoàn toàn vào 1 thiết bị đơn lẻ (Single Point of Failure - Laptop trưởng nhóm).
* **Mã nguồn (Rủi ro cao):** Lưu qua USB dễ hỏng/thất lạc, thiếu công cụ quản lý phiên bản tập trung (Git).
* **Hiện tượng "23 phiên bản file" (Version Fragmentation):** Do chia sẻ file thủ công, gây xung đột mã nguồn và rủi ro dùng nhầm bản lỗi khi pitching.

---

## 2. Quy Trình Hybrid Workflow Chuẩn
```text
[ 1. Local SSD ] (Thao tác cực nhanh, làm việc offline)
       │ (Ctrl + S)
       ▼
[ 2. Auto Sync Agent ] (Tiến trình đồng bộ ngầm)
       │
       ▼
[ 3. Cloud Storage ] (Đồng bộ đa thiết bị, lưu vết lịch sử)