# Sales Reporting 2019 — Python Mini Project

Phân tích 12 file CSV bán hàng để xem doanh thu theo tháng và thành phố, số đơn theo giờ, sản phẩm bán nhiều và các cặp sản phẩm thường được mua cùng.

| Đường dẫn | Nội dung |
|---|---|
| `data/sales2019_1.csv` đến `data/sales2019_12.csv` | Dữ liệu gốc của 12 tháng |
| `report.ipynb` | Mã Python, kết quả in trực tiếp và năm biểu đồ Matplotlib |
| `requirements.txt` | Thư viện để chạy notebook |

## Cách chạy

1. Tải hoặc clone repo và mở thư mục gốc bằng VS Code.
2. Dùng Python 3.10 trở lên và cài các thư viện:

   ```bash
   python -m pip install -r requirements.txt
   ```

3. Mở `report.ipynb`, chọn kernel Python đã cài thư viện, rồi bấm **Run All**. Thư mục làm việc cần chứa `data/`.
4. Xem kết quả và biểu đồ ngay dưới từng ô trong notebook. Bản đã chạy cũng xem được trên GitHub.
