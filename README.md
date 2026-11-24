# du-bao-doanh-thu
Dự báo doanh thu bán lẻ theo tháng bằng Holt-Winters.
# Dự báo doanh thu bán lẻ theo tháng (Superstore)

## Mục tiêu
Dự báo doanh thu 12 tháng của năm 2019 để hỗ trợ kế hoạch nhập hàng và khuyến mãi.

## Dữ liệu
Superstore Sales Dataset (Kaggle, tác giả Rohit Sahoo), gồm 4 năm đơn hàng 2015-2018.
Doanh thu được gom theo tháng, tổng cộng 48 tháng.

## Phương pháp
1. Làm sạch dữ liệu, gom doanh thu theo tháng
2. Phân tích xu hướng và mùa vụ
3. Baseline: dự đoán bằng cùng tháng của năm trước
4. Mô hình Holt-Winters, thử 4 cấu hình
5. Huấn luyện lại bằng toàn bộ dữ liệu, dự báo 2019

## Kết quả
| Mô hình | MAE | MAPE |
|---|---|---|
| Baseline | 15.444 | 24,9% |
| Holt-Winters (xu hướng + mùa cộng) | 10.545 | 19,8% |

Dự báo 2019: tổng khoảng 899.044, tăng khoảng 24,5% so với 2018.
Cao điểm: tháng 12, 11, 9. Thấp điểm: tháng 2, 1, 4.

## Khuyến nghị
- Nhập hàng và chuẩn bị nhân sự trước tháng 9 và mùa cuối năm
- Chạy khuyến mãi vào tháng 1, 2 và 4
- Giữ tồn kho dự phòng vì sai số mỗi tháng khoảng 20%

## Hạn chế
Chỉ có 4 năm dữ liệu, bài kiểm tra chỉ có 12 tháng, mô hình chưa tính yếu tố bên ngoài.

## Công cụ
Python, pandas, statsmodels, matplotlib (Google Colab)
