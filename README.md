# Hệ thống bãi giữ xe thông minh tích hợp AI

## Tên dự án

**HỆ THỐNG QUẢN LÝ BÃI ĐỖ XE THÔNG MINH TÍCH HỢP AI HỖ TRỢ KIỂM SOÁT SỐ LƯỢNG XE**

## Thông tin môn học

- Môn học: Xây dựng hệ thống nhúng.
- Giảng viên hướng dẫn: Phạm Hoàng Việt.

## Nội dung

Dự án xây dựng mô hình bãi giữ xe thông minh sử dụng ESP32 làm bộ điều khiển trung tâm. Hệ thống có các chức năng chính:

- Kết nối WiFi và gửi dữ liệu giám sát lên ThingsBoard thông qua MQTT.
- Đo nồng độ khí bằng cảm biến MQ2 và kích hoạt còi cảnh báo khi vượt ngưỡng.
- Đếm số lượng ô tô và xe máy trong bãi.
- Điều khiển cổng vào và cổng ra bằng cảm biến siêu âm kết hợp servo.
- Nhận kết quả phân loại phương tiện qua UART, ví dụ `OTO` hoặc `XEMAY`.
- Hiển thị thời gian thực, số lượng xe máy và số lượng ô tô trên LCD I2C 20x4.
- Sử dụng module RTC DS3231 để duy trì thời gian thực.

## Linh kiện sử dụng

- ESP32 DevKit V1.
- Cảm biến khí MQ2.
- Còi buzzer cảnh báo.
- 2 cảm biến siêu âm HC-SR04 hoặc tương đương.
- 2 động cơ servo cho cổng vào và cổng ra.
- Module RTC DS3231.
- Màn hình LCD I2C 20x4.
- Module hoặc mạch phụ gửi dữ liệu phân loại xe qua UART.
- Breadboard, dây nối và nguồn cấp phù hợp.

## Công nghệ và thư viện

- PlatformIO.
- Arduino framework cho ESP32.
- ThingsBoard MQTT.
- `PubSubClient`.
- `ArduinoJson`.
- `RTClib`.
- `LiquidCrystal_I2C`.
- `ESP32Servo`.
- `MQUnifiedsensor`.

## Thành viên thực hiện

| STT | Họ và tên        | MSV        |
| --- | ---------------- | ---------- |
| 1   | Đào Ngọc Đức     | B22DCCN221 |
| 2   | Hà Mạnh Dũng     | B22DCCN125 |
| 3   | Tống Công Thành  | B22DCCN797 |
| 4   | Trần Trọng Vinh  | B22DCCN905 |
| 5   | Trần Trọng Dương | B22DCCN173 |

## Ghi chú

Trước khi nạp chương trình, cần kiểm tra lại thông tin WiFi, token ThingsBoard, chân kết nối phần cứng và nguồn cấp cho servo/cảm biến để phù hợp với mô hình thực tế.
