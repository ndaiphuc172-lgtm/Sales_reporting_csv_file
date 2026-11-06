# Sales Reporting 2019 — Python Mini Project

Phân tích 12 file dữ liệu bán hàng năm 2019 nhằm đánh giá doanh thu, thời điểm đặt hàng và xu hướng mua sản phẩm cùng nhau.

## Cấu trúc repo

| Đường dẫn | Nội dung |
|---|---|
| `data/sales2019_1.csv` đến `data/sales2019_12.csv` | 12 CSV dữ liệu gốc |
| `report.ipynb` | Notebook độc lập, chứa đầy đủ mã xử lý, phân tích và biểu đồ đã chạy |
| `README.md` | Hướng dẫn, kết quả và quy tắc tính |

## Cách chạy

1. Tải hoặc clone toàn bộ repo.
2. Mở thư mục repo bằng VS Code, cài extension Python và Jupyter nếu chưa có.
3. Mở `report.ipynb`, chọn Python 3.10 trở lên và nhấn **Run All**. Thư mục làm việc cần là thư mục gốc repo, nơi có `data/`.
4. Sau khi chạy, mở `outputs/report.html` để xem báo cáo đầy đủ. Bảng tổng hợp nằm tại `outputs/tables/`, dữ liệu sạch tại `outputs/data/`.

Notebook dùng thư viện chuẩn Python để xử lý dữ liệu và tạo biểu đồ SVG. Kết quả và biểu đồ đã được lưu trong notebook để có thể xem trực tiếp trên GitHub.

