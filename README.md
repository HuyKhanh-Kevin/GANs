# INTRODUCTION
Đây là dự án cuối khóa của nhóm **10-xGANs** thuộc khóa học **Python & ML 2025**. Nhóm gồm các thành viên:
1. Võ Huy Khánh
2. Nguyễn Đức Quân
3. Nguyễn Đình Nguyên
4. Nguyễn Vinh Phúc
5. Nguyễn Trọng Nhân

Dự án này nhằm mục đích sử dụng mạng đối kháng sinh **(GAN - Generative Adversarial Network)** để tạo ra ảnh y tế giả (fake medical images) và sau đó sử dụng mạng nơ-ron tích chập **(CNN - Convolutional Neural Network)** để phân loại và phân biệt ảnh thật và ảnh giả.
Ứng dụng của phương pháp này có thể giúp cải thiện hiệu suất và độ chính xác trong việc phát hiện gian lận trong dữ liệu y tế, tăng cường dữ liệu cho các mô hình học sâu, hoặc đánh giá độ tin cậy của mô hình trong các bài toán nhận dạng hình ảnh y học. Dataset được nhóm tham khảo trên kaggle theo đường dẫn sau: [Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia?select=chest_xray).
# GAN
Generative Adversarial Network (GAN) là một kiến trúc mạng học sâu, được thiết kế để tạo ra dữ liệu giả có tính chân thực cao. Mô hình GAN bao gồm hai mạng con chính là Generator (mạng sinh) và Discriminator (mạng phân biệt), hoạt động đối kháng với nhau trong quá trình huấn luyện. Generator cố gắng tạo ra các mẫu dữ liệu giả sao cho giống dữ liệu thật nhất có thể, trong khi Discriminator có nhiệm vụ phân biệt giữa dữ liệu thật và dữ liệu giả do Generator tạo ra. Cả hai mạng được huấn luyện đồng thời theo cơ chế cạnh tranh: khi Discriminator càng phân biệt tốt thì Generator phải càng tinh vi hơn để đánh lừa được nó. Qua nhiều vòng huấn luyện, Generator sẽ học được cách tạo ra dữ liệu giả với chất lượng ngày càng cao, đến mức khó có thể phân biệt được với dữ liệu thật.

Trong lĩnh vực y tế, GAN được ứng dụng để tạo ra ảnh tổng hợp nhằm mục đích mở rộng tập dữ liệu huấn luyện, hỗ trợ đào tạo các mô hình học máy trong điều kiện thiếu dữ liệu. Ngoài ra, mô hình GAN còn giúp kiểm thử các hệ thống phát hiện hình ảnh bất thường hoặc tăng cường độ đa dạng trong dữ liệu đầu vào. Trong dự án này, nhóm sử dụng GAN để sinh ra các ảnh y tế giả dựa trên tập ảnh gốc, tạo nền tảng để mô hình phân loại học cách phân biệt giữa ảnh thật và ảnh được sinh ra.

# CNN

Convolutional Neural Network (CNN) là một kiến trúc mạng nơ-ron sâu được thiết kế đặc biệt cho các bài toán xử lý ảnh và nhận dạng mẫu trong dữ liệu dạng lưới hai chiều. CNN hoạt động dựa trên nguyên lý sử dụng các lớp tích chập (convolutional layers) để tự động trích xuất các đặc trưng từ hình ảnh đầu vào, sau đó kết hợp với các lớp pooling và fully connected để thực hiện quá trình phân loại. Khác với các mạng nơ-ron truyền thống, CNN có khả năng nhận diện các đặc trưng không gian trong ảnh như đường viền, hình dạng, hoặc kết cấu mà không cần thiết kế thủ công, giúp giảm thiểu số lượng tham số và tăng hiệu quả huấn luyện mô hình.
Trong phạm vi dự án này, CNN được sử dụng như một bộ phân loại để phân biệt giữa ảnh y tế thật và ảnh giả do GAN tạo ra. Mô hình CNN sẽ học cách nhận diện các đặc điểm đặc trưng mà ảnh giả không thể tái tạo hoàn hảo như ảnh thật, từ đó đưa ra dự đoán chính xác. Việc kết hợp CNN với GAN tạo thành một quy trình khép kín, trong đó GAN cung cấp dữ liệu tổng hợp để kiểm thử độ nhạy và khả năng phát hiện của CNN. Qua đó, nhóm có thể đánh giá hiệu quả của mô hình GAN trong việc sinh ảnh và đồng thời kiểm chứng năng lực phân loại của CNN trong các ứng dụng y tế, nơi mà tính chính xác và độ tin cậy là vô cùng quan trọng.



