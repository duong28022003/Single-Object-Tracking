# Single-Object-Tracking (SOT)

SOT (Single Object Tracking) là một nhánh của bài toán Object Tracking, tập trung vào việc theo dõi vị trí và trạng thái của **một đối tượng duy nhất** trong video theo thời gian.

---

## Hướng tiếp cận

### 1. Histogram + MeanShift Tracker

<p align="center">
<img src="https://i.imgur.com/9sPueeC.png" alt="Histogram + MeanShift Tracker" width="600"/>
</p>

### 2. DeepSORT + YOLO

<p align="center">
<img src="https://i.imgur.com/Vh6ObWm.png" alt="DeepSORT + YOLO" width="600"/>
</p>
> 📄 **Chi tiết các phương pháp** xem trong file `Report.pdf`.

---

## Dataset

**LaSOT (Large-scale Single Object Tracking)** là một bộ dữ liệu chuyên dụng cho bài toán theo dõi đối tượng đơn, cung cấp các video với chú thích chi tiết khung hình theo thời gian.

🔗 Tham khảo tại: [http://vision.cs.stonybrook.edu/~lasot/](http://vision.cs.stonybrook.edu/~lasot/)

---

## Đánh giá 

- Thực hiện đánh giá trên 29 sub-dataset khác nhau (bao gồm 20 tập của lớp mouse và 9 tập của lớp person)
- Mỗi frame được tính là tracking thành công nếu chỉ số IoU (Intersection of Union) đạt trên ngưỡng 0.5.
- Đối với mỗi video (hay 1 chuỗi frames), tiến hành đo tỉ lệ thành công trên toàn bộ chuỗi.

<p align="center">
<img src="https://i.imgur.com/zqcUZ93.png" alt="metrics" width="600"/>
</p>

## Kết quả

- Nhìn chung, phương pháp sử dụng YOLO kết hợp deepSORT cho kết quả tốt hơn so với Histogram kết hợp MeanShift, với tỉ lệ thành công trung bình đạt **23.93%**
- Một phần kết quả được thể hiện trong bảng dưới

<p align="center">
<img src="https://i.imgur.com/CTpac6r.png" alt="evaluation" width="600"/>
</p>

🎥 Video minh họa kết quả:

![Tracking Result](tracking_result.gif)
