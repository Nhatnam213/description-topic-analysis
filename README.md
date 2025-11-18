<h1 align="center">🧠 YouTube Topic Modeling  
<br>(Phân tích chủ đề mô tả video YouTube bằng LDA – BERTopic – Top2Vec – CombinedTM)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/NLP-Vietnamese-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LDA-Topic%20Modeling-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/BERTopic-Transformer%20Embedding-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Top2Vec-Semantic%20Clustering-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/CombinedTM-LDA+BERTopic-blueviolet?style=for-the-badge" />
</p>

---

# 🌟 1. Introduction (Giới thiệu)

This project analyzes **Vietnamese YouTube video descriptions** to discover **latent semantic topics** using modern topic modeling algorithms:  
**LDA, BERTopic, Top2Vec, and a hybrid CombinedTM (LDA + BERTopic)**.  
*(Dự án phân tích mô tả video YouTube tiếng Việt bằng LDA, BERTopic, Top2Vec và mô hình lai CombinedTM.)*

Why this matters?  
- YouTube descriptions reflect content trends & user behavior  
- Topic modeling helps understand large-scale unstructured data  
- Vietnamese text is noisy → requires deep preprocessing  
- Useful for recommendation systems, content moderation, trend analysis

Dataset:  
- **7,653 cleaned Vietnamese video descriptions**  
- Collected via YouTube Data API v3  
- Includes title, tags, category_id, description, engagement metrics  

---

# 🧼 2. Preprocessing (Tiền xử lý)

Applied steps:

- Lowercase text  
- Remove emoji, URLs, emails, hashtags  
- Remove advertisement keywords (“đăng ký”, “like”, “share”)  
- Normalize Vietnamese characters  
- Tokenize using **Underthesea**  
- Remove stopwords  
- Filter out short descriptions (< 5 tokens)

Outputs:
- `clean_description`
- tokenized list for LDA  
- corpus + dictionary  

---

# 🧠 3. Topic Modeling Methods (Các mô hình được sử dụng)

## 🔹 **1. LDA (Latent Dirichlet Allocation)**  
*(Mô hình thống kê phân phối xác suất chủ đề)*  
- Input: Bag-of-Words  
- Optimized number of topics: **5**  
- Best Coherence: **0.549**

---

## 🔹 **2. BERTopic**  
*(Embedding + UMAP + HDBSCAN + cTF-IDF)*  
- Multilingual Transformer  
- Best Coherence: **0.714**  
- Best semantic quality across models  
- Produces clear topic boundaries

---

## 🔹 **3. Top2Vec**  
*(Joint embedding for documents–words–topics)*  
- Automatically finds number of topics  
- High Topic Diversity  
- Lowest Coherence among 3 main models

---

## 🔹 **4. CombinedTM (LDA + BERTopic)**  
*(Mô hình lai kết hợp phân bố chủ đề LDA + embedding BERTopic)*  

Results:
- Coherence **0.663** (highest overall)  
- Stable & interpretable  
- Strong semantic grouping  

---

# 📊 4. Results & Model Comparison (Kết quả và so sánh mô hình)

## ⭐ **Overall Best Model: CombinedTM (LDA + BERTopic)**  
High balance of:
✔ Coherence  
✔ Stability  
✔ Purity  
✔ Topic Diversity  

---

# 🏆 5. Comparison Table (Bảng so sánh thuật toán)

### 📌 **Table: Key Metrics Overview**

| Model | C_v | NPMI | NMI | ARI | Diversity | Nhận xét |
|-------|------|-------|------|------|-----------|---------|
| **LDA** | 0.549 | 0.039 | 0.193 | 0.092 | 0.800 | Dễ diễn giải, ranh giới yếu |
| **BERTopic** | 0.660 | 0.077 | **0.339** | **0.176** | 0.741 | Ngữ nghĩa mạnh nhất, phân tách rõ |
| **Top2Vec** | 0.421 | 0.000 | 0.148 | 0.043 | **0.800** | Đa dạng cao, ngữ nghĩa yếu |
| **CombinedTM** | **0.663** | 0.076 | 0.339 | 0.068 | 0.748 | Tốt nhất tổng thể, cân bằng |

---

# 🌀 6. Visualizations (Trực quan hóa)

Repository includes:

- WordCloud  
- Bubble Chart  
- Topic Cluster Maps  
- Coherence plots  
- Embedding visualizations (UMAP)

---

# 🧪 7. Key Findings (Kết luận quan trọng)

- BERTopic → strongest semantic model  
- LDA → interpretable but overlapping  
- Top2Vec → diverse but weak coherence  
- CombinedTM → **best hybrid model**, highest Coherence  
- Vietnamese descriptions require strong preprocessing  
- Short-text topic modeling is challenging but solvable with embeddings  

---

# 🚀 8. Applications (Ứng dụng thực tế)

- YouTube content trend analysis  
- Automatic content tagging  
- Detect emerging hot topics  
- Improving recommendation algorithms  
- Digital media research  

---

# 👨‍🏫 9. Team (Nhóm thực hiện)

- **Hà Thế Anh**  
- **Nguyễn Nhật Nam**  
- **Hoàng Quang Minh**  

**Supervisor:**  
- **Lê Nhật Tùng – HUTECH University**

