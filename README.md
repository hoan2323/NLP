
## 📌 Overview

"**Topic and Sentiment Classification for a Short Text**" là một cuộc thi hấp dẫn về **xử lý ngôn ngữ tự nhiên (NLP)**, nơi các thí sinh được thử thách xây dựng mô hình để:

- **Phân loại chủ đề** của văn bản ngắn (ví dụ: Kinh tế, Xã hội, Thể thao...)
- **Phân tích cảm xúc** (Tích cực / Trung tính / Tiêu cực)

Cuộc thi nhằm thúc đẩy ứng dụng các mô hình tiên tiến như **PhoBERT** và các kỹ thuật học máy trong việc hiểu nội dung ngôn ngữ tiếng Việt.

## 🧑‍💻 Model Used

Dự án này sử dụng **`vinai/phobert-base`** – một mô hình pre-trained transformer cho tiếng Việt được phát triển bởi [VinaAI](https://github.com/VinAIResearch/PhoBERT).

### 📦 Các thư viện chính

- `transformers`
- `underthesea`
- `torch`, `torch.nn`, `torch.utils.data`
- `scikit-learn`
- `pandas`, `numpy`

## 📁 Dataset

Bộ dữ liệu gồm các văn bản ngắn tiếng Việt, mỗi văn bản có:

- `id`: định danh duy nhất
- `content`: văn bản đầu vào
- `sentiment`: cảm xúc (`Tích cực`, `Trung tính`, `Tiêu cực`)
- `topic`: danh sách chủ đề cách nhau bởi dấu `;`

## 📊 Evaluation

### 🔹 Sentiment Score (25%)
- Tính trung bình số điểm các dự đoán cảm xúc **chính xác** so với nhãn thực tế.

### 🔹 Topic Score (75%)
- Tính số lượng chủ đề dự đoán đúng.
- Trừ đi độ lệch về số lượng topic.
- Tính tỉ lệ so với tổng số topic thực tế.

