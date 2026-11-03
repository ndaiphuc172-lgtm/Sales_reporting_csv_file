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

## Câu hỏi và kết quả

| Câu hỏi kinh doanh | Kết quả năm 2019 |
|---|---|
| Tháng có doanh thu cao nhất? | Tháng 12: **4.613.443,34 USD** |
| Thành phố có doanh thu cao nhất? | San Francisco (CA): **8.259.719,03 USD** |
| Giờ có nhiều đơn đặt hàng nhất? | **19:00**, kế đến **12:00** và **11:00** |
| Cặp sản phẩm thường mua cùng nhau nhất? | Lightning Charging Cable + iPhone: **1.010 đơn** |
| Sản phẩm bán nhiều nhất theo số lượng? | AAA Batteries (4-pack): **31.012 sản phẩm** |

Tổng doanh thu: **34.483.365,68 USD**; số đơn: **178.406**; số lượng bán: **209.038 sản phẩm**; số dòng sản phẩm trong năm: **185.916**.

## Phương pháp và chất lượng dữ liệu

- Đọc đủ 12 CSV; kiểm tra tên cột, dữ liệu thiếu, số lượng/giá, ngày giờ và địa chỉ.
- 186.850 dòng đầu vào gồm 545 dòng trống, 355 tiêu đề lặp và 185.950 dòng hợp lệ.
- Có 34 dòng thuộc năm 2020: giữ trong dữ liệu sạch, loại khỏi KPI năm 2019 theo ngày đặt hàng thực tế.
- Giữ và đánh dấu 264 dòng trùng hoàn toàn vì chưa có khóa dòng đơn để xác nhận đó là lỗi.
- Doanh thu = số lượng × đơn giá; tính tiền bằng **cent nguyên** để tránh sai số số thực. Các cột `_cents` trong bảng CSV cần chia 100 để đổi sang USD.
- Số đơn là số Order ID duy nhất, không phải số dòng. Một mã đơn có thể chứa nhiều sản phẩm.
- Thành phố đi kèm bang để tách Portland (OR) và Portland (ME).
- Mỗi cặp sản phẩm khác nhau tính tối đa một lần trong một đơn; bổ sung support, confidence và lift.
- Kiểm tra đối soát: doanh thu theo tháng, thành phố, giờ và sản phẩm đều bằng tổng năm; số đơn theo tháng và giờ bằng tổng số đơn.

## Công cụ và kỹ thuật

Xử lý nhiều CSV; kiểm tra chất lượng dữ liệu; `Decimal`, `datetime`, regex; `Counter`, `defaultdict`, `itertools.combinations`; tổng hợp chỉ tiêu; phân tích giỏ hàng; tạo báo cáo HTML/SVG và xuất JSON/CSV.

## Giới hạn và đề xuất

Dữ liệu không có giá vốn, thông tin khách hàng, quảng cáo, hoàn trả hoặc lượt truy cập. Vì vậy chưa thể tính lợi nhuận, retention hay ROI. Giờ đặt hàng giữ nguyên theo nguồn vì chưa có thông tin múi giờ. Các giờ cao điểm và cặp mua kèm là cơ sở đề xuất thử nghiệm quảng cáo/bundle, chưa chứng minh quan hệ nhân quả.

## Tham khảo

- Bộ dữ liệu và các câu hỏi kinh doanh được phát triển dựa trên project [Sales-Reporting](https://github.com/boringPpl/Sales-Reporting).
