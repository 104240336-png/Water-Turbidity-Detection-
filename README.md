# Water-Turbidity-Detection-
# ESP32 Water Turbidity Monitor with OLED 💧

Dự án giám sát độ đục của nước theo thời gian thực sử dụng vi điều khiển ESP32, cảm biến độ đục (Turbidity Sensor) và màn hình OLED 0.96 inch.

## 🚀 Tính năng nổi bật (Features)
* **Hiển thị trực quan:** Sử dụng màn hình OLED (I2C) sắc nét để hiển thị % độ đục và cảnh báo trạng thái nước (TRONG VEO, HƠI ĐỤC, RẤT BẨN).
* **Lọc nhiễu thuật toán:** Tích hợp bộ lọc lấy trung bình cộng (Average Filtering) từ 20 lần đo liên tiếp giúp số liệu cực kỳ ổn định, tránh hiện tượng nhảy số ảo.
* **Tối ưu cho ESP32:** Cấu hình chuẩn xác dải điện áp ADC của ESP32 và định nghĩa rõ ràng các chân giao tiếp I2C.

## 🛠️ Yêu cầu phần cứng (Hardware Requirements)
* 1x Mạch vi điều khiển **ESP32** (NodeMCU / DevKit).
* 1x **Cảm biến độ đục** (kèm bo mạch chuyển đổi tín hiệu, gạt công tắc sang chế độ 'A' - Analog).
* 1x **Màn hình OLED 0.96"** (Giao tiếp I2C, địa chỉ `0x3C`).
* Dây cắm Jumper và nguồn cấp 5V.

## 🔌 Sơ đồ nối dây (Wiring Diagram)

**1. Màn hình OLED (I2C) <-> ESP32**
* `VCC`  --> `VIN` (hoặc 5V)
* `GND`  --> `GND`
* `SDA`  --> `GPIO 21`
* `SCL`  --> `GPIO 22`

**2. Cảm biến độ đục <-> ESP32**
* `VCC` (Dây đỏ)   --> `VIN` (hoặc 5V) 
* `GND` (Dây đen)  --> `GND`
* `OUT` (Dây xanh) --> `GPIO 34` (Chân ADC lấy tín hiệu)
