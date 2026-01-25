# Car Review Analysis – Data Scientist Assessment

## Overview
This project performs sentiment analysis and topic extraction on 1224 car reviews using:
- **Machine Learning**: Logistic Regression + LDA
- **Generative AI**: GPT-4o (or alternative) via prompt engineering

# Project overview
```
car-review-analysis/
│
├── data/
│   └── train.txt                 # Dữ liệu gốc (không chỉnh sửa)
│
├── notebooks/
│   └── car_review_analysis.ipynb # Notebook chính: chứa toàn bộ pipeline ML + LLM
│
├── src/
│   ├── __init__.py
│   ├── preprocessing.py          # Hàm clean text, tokenize, lemmatize
│   ├── ml_sentiment.py           # Huấn luyện & đánh giá Logistic Regression
│   ├── ml_topic.py               # LDA topic modeling
│   ├── llm_sentiment.py          # Gọi LLM cho sentiment (zero-shot/few-shot)
│   ├── llm_topic.py              # LLM topic extraction (direct hoặc clustering-based)
│   └── utils.py                  # Helper: load data, save results, plot, v.v.
│
├── outputs/
│   ├── ml_sentiment_results.csv
│   ├── ml_topics.txt             # Top words per topic từ LDA
│   ├── llm_sentiment_results.csv
│   ├── llm_topics_summary.txt    # Chủ đề từ LLM
│   └── figures/                  # Biểu đồ (confusion matrix, word cloud, v.v.)
│       ├── sentiment_cm.png
│       ├── lda_wordcloud.png
│       └── topic_distribution.png
│
├── reports/
│   └── Car_Review_Analysis_Report.pptx  # Báo cáo 4–5 slides theo yêu cầu
│
├── requirements.txt              # Danh sách thư viện cần cài
├── README.md                     # Hướng dẫn chạy project (1–2 phút)
└── .gitignore                    # (Tùy chọn) nếu bạn dùng Git
```

## How to Run
    ```bash
    conda create -n car_review_analysis python=3.11
    conda activate car_review_analysis
    pip install -r requirements.txt
    ```
1. `pip install -r requirements.txt`
2. Download spaCy model: `python -m spacy download en_core_web_sm`
3. Set your OpenAI API key in environment (or use free LLM alternative)
4. Open `notebooks/car_review_analysis.ipynb` and run all cells

## Output
Results are saved in `outputs/`. Slides in `reports/`.