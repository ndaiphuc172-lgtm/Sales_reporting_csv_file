# Sales Reporting 2019 - Python Mini Project

Ph�n t�ch 12 file d? li?u b�n h�ng nam 2019 nh?m d�nh gi� doanh thu, th?i di?m d?t h�ng v� xu hu?ng mua s?n ph?m c�ng nhau.

## C?u tr�c repo

| Du?ng d?n | N?i dung |
|---|---|
| `data/sales2019_1.csv` d?n `data/sales2019_12.csv` | 12 CSV d? li?u g?c |
| `report.ipynb` | Notebook d?c l?p, ch?a d?y d? ma x? ly, ph�n t�ch v� bi?u d? da ch?y |
| `README.md` | Hu?ng d?n, k?t qu? v� quy t?c t�nh |

## C�ch ch?y

1. T?i ho?c clone to�n b? repo.
2. M? thu m?c repo b?ng VS Code, c�i extension Python v� Jupyter n?u chua c�.
3. M? `report.ipynb`, ch?n Python 3.10 tr? l�n v� nh?n **Run All**. Thu m?c l�m vi?c c?n l� thu m?c g?c repo, noi c� `data/`.
4. Sau khi ch?y, m? `outputs/report.html` d? xem b�o c�o d?y d?. B?ng t?ng h?p n?m t?i `outputs/tables/`, d? li?u s?ch t?i `outputs/data/`.

Notebook d�ng thu vi?n chu?n Python d? x? ly d? li?u v� t?o bi?u d? SVG. K?t qu? v� bi?u d? da du?c luu trong notebook d? c� th? xem tr?c ti?p tr�n GitHub.

## C�u h?i v� k?t qu?

| C�u h?i kinh doanh | K?t qu? nam 2019 |
|---|---|
| Th�ng c� doanh thu cao nh?t? | Th�ng 12: **4.613.443,34 USD** |
| Th�nh ph? c� doanh thu cao nh?t? | San Francisco (CA): **8.259.719,03 USD** |
| Gi? c� nhi?u don d?t h�ng nh?t? | **19:00**, k? d?n **12:00** v� **11:00** |
| C?p s?n ph?m thu?ng mua c�ng nhau nh?t? | Lightning Charging Cable + iPhone: **1.010 don** |
| S?n ph?m b�n nhi?u nh?t theo s? lu?ng? | AAA Batteries (4-pack): **31.012 s?n ph?m** |

T?ng doanh thu: **34.483.365,68 USD**; s? don: **178.406**; s? lu?ng b�n: **209.038 s?n ph?m**; s? d�ng s?n ph?m trong nam: **185.916**.

## Phuong ph�p v� ch?t lu?ng d? li?u

- D?c d? 12 CSV; ki?m tra t�n c?t, d? li?u thi?u, s? lu?ng/gi�, ng�y gi? v� d?a ch?.
- 186.850 d�ng d?u v�o g?m 545 d�ng tr?ng, 355 ti�u d? l?p v� 185.950 d�ng h?p l?.
- C� 34 d�ng thu?c nam 2020: gi? trong d? li?u s?ch, lo?i kh?i KPI nam 2019 theo ng�y d?t h�ng th?c t?.
- Gi? v� d�nh d?u 264 d�ng tr�ng ho�n to�n v� chua c� kh�a d�ng don d? x�c nh?n d� l� l?i.
- Doanh thu = s? lu?ng x don gi�; t�nh ti?n b?ng **cent nguy�n** d? tr�nh sai s? s? th?c. C�c c?t `_cents` trong b?ng CSV c?n chia 100 d? d?i sang USD.
- S? don l� s? Order ID duy nh?t, kh�ng ph?i s? d�ng. M?t ma don c� th? ch?a nhi?u s?n ph?m.
- Th�nh ph? di k�m bang d? t�ch Portland (OR) v� Portland (ME).
- M?i c?p s?n ph?m kh�c nhau t�nh t?i da m?t l?n trong m?t don; b? sung support, confidence v� lift.
- Ki?m tra d?i so�t: doanh thu theo th�ng, th�nh ph?, gi? v� s?n ph?m d?u b?ng t?ng nam; s? don theo th�ng v� gi? b?ng t?ng s? don.

## C�ng c? v� k? thu?t

X? ly nhi?u CSV; ki?m tra ch?t lu?ng d? li?u; `Decimal`, `datetime`, regex; `Counter`, `defaultdict`, `itertools.combinations`; t?ng h?p ch? ti�u; ph�n t�ch gi? h�ng; t?o b�o c�o HTML/SVG v� xu?t JSON/CSV.

## Gi?i h?n v� d? xu?t

D? li?u kh�ng c� gi� v?n, th�ng tin kh�ch h�ng, qu?ng c�o, ho�n tr? ho?c lu?t truy c?p. V� v?y chua th? t�nh l?i nhu?n, retention hay ROI. Gi? d?t h�ng gi? nguy�n theo ngu?n v� chua c� th�ng tin m�i gi?. C�c gi? cao di?m v� c?p mua k�m l� co s? d? xu?t th? nghi?m qu?ng c�o/bundle, chua ch?ng minh quan h? nh�n qu?.

## Tham kh?o

- B? d? li?u v� c�c c�u h?i kinh doanh du?c ph�t tri?n d?a tr�n project [Sales-Reporting](https://github.com/boringPpl/Sales-Reporting).

