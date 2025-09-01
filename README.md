# INTRODUCTION
Đây là dự án cuối khóa của nhóm **10-xGANs** thuộc khóa học **Python & ML 2025**. Nhóm gồm các thành viên:
1. Võ Huy Khánh
2. Nguyễn Đức Quân
3. Nguyễn Đình Nguyên
4. Nguyễn Vinh Phúc
5. Nguyễn Trọng Nhân
Dự án của nhóm được chia thành 2 phần chính, đó là sử dụng mô hình **GAN (Generative Adversarial Network)** để sinh thêm ảnh làm giàu cho dataset, và áp dụng mô hình **CNN (Convolutional Neural Network)** để chuẩn đoán bệnh viêm phổi (pneumonia) thông qua ảnh x-ray ngực của bệnh nhân. Dataset được lấy trên kaggle theo đường dẫn sau: [Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia?select=chest_xray).
# GAN
GAN (Generative Adversarial Network) là một mô hình học sâu có thể sinh ra dữ liệu mới, thường dùng để tạo ảnh. Mô hình GAN gồm hai phần: Generator, đóng vai trò như một nhà máy, nhiệm vụ của nó là sinh ảnh một cách chân thật nhất có thể, và Discriminator, có nhiệm vụ là phân biệt xem ảnh được đưa vào là ảnh thật hay là ảnh của Generator. Một ảnh của generator tạo ra được xem là lí tưởng khi discriminator không thể phân biệt được ảnh của generator là thật hay giả. Khi đó nhiệm vụ của mô hình GAN là hoàn tất.
# CNN
CNN (Convolutional Neural Network) là một mô hình học sâu được dùng để phân loại dữ liệu, thường dùng để phân loại ảnh. Kiến trúc của mô hình này căn bản là sự kết hợp giữa các block, trong mỗi block sẽ bao gồm nhiều lớp (layer). Những lớp này sẽ chiết xuất những đặc điểm của ảnh và xử lí từ từ, từ đó học được những đặc điểm của từng nhóm.
