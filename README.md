# Single-Object-Tracking (SOT)

SOT (Single Object Tracking) là một nhánh của bài toán Object Tracking, tập trung vào việc theo dõi vị trí và trạng thái của **một đối tượng duy nhất** trong video theo thời gian.

---

## Hướng tiếp cận

### 1. Histogram + MeanShift Tracker

<img src="https://i.imgur.com/9sPueeC.png" alt="Histogram + MeanShift Tracker" width="600"/>

### 2. DeepSORT + YOLO

<img src="https://i.imgur.com/Vh6ObWm.png" alt="DeepSORT + YOLO" width="600"/>

> 📄 **Chi tiết các phương pháp** xem trong file `Report.pdf`.

---

## Dataset

**LaSOT (Large-scale Single Object Tracking)** là một bộ dữ liệu chuyên dụng cho bài toán theo dõi đối tượng đơn, cung cấp các video với chú thích chi tiết khung hình theo thời gian.

🔗 Tham khảo tại: [http://vision.cs.stonybrook.edu/~lasot/](http://vision.cs.stonybrook.edu/~lasot/)

---

## Kết quả

- Thực hiện đánh giá trên 29 sub-dataset khác nhau (bao gồm 20 tập của lớp mouse và 9 tập của lớp person)

- Nhìn chung, phương pháp sử dụng YOLO kết hợp deepSORT cho kết quả tốt hơn so với Histogram kết hợp MeanShift, với tỉ lệ thành công trung bình đạt **23.93%** 

🎥 Video minh họa kết quả:

![Tracking Result](tracking_result.gif)
