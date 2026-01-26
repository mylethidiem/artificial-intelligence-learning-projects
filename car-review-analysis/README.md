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
│
├── reports/
│   └── Car_Review_Analysis_Report.pptx  # Báo cáo 4–5 slides theo yêu cầu
│	└── Report.docx  # Báo cáo words
│
├── requirements.txt              # Danh sách thư viện cần cài
├── README.md                     # Hướng dẫn chạy project (1–2 phút)
└── .gitignore                    # (Tùy chọn) nếu bạn dùng Git
```

## How to Run
1. Create environment and install packages
	```bash
    conda create -n car_review_analysis python=3.11
    conda activate car_review_analysis
	pip install -r requirements.txt
    ```
2. Download spaCy model: `python -m spacy download en_core_web_sm`
3. Get and set your OpenAI API key/Gemini key in environment (or use free LLM alternative or Local LLM instead)
4. Open `notebooks/car_review_analysis.ipynb` and run all cells

## Output
Slides and summary in `reports/`.