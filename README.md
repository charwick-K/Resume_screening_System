# 🧠 Automated Resume Screening System (ARSS)

A smart web application designed to assist employers and HR professionals by automatically analyzing resumes and surfacing the most relevant candidates for a given job description. This system leverages natural language processing and recommendation engine techniques to match resumes with job requirements, streamlining the recruitment process and saving valuable time.

---

## 📌 Project Overview

This project was developed by me, **Kondru Charwick Hamesh**, as a practical solution to the growing challenge of resume overload in hiring pipelines. By combining content-based and collaborative filtering techniques, the system performs fuzzy matching between job descriptions and resumes to rank candidates based on relevance.

🔍 Key Features:
- Extracts and processes resume content from PDF and DOCX files
- Matches resumes to job descriptions using NLP and vector similarity
- Ranks candidates based on relevance score
- Simple and intuitive web interface for uploading and reviewing results
- Docker support for easy deployment

---

## 🧰 Technologies & Libraries Used

The system is built using Python and Flask, with several NLP and machine learning libraries:

| Category        | Tools & Libraries                                                                 |
|----------------|------------------------------------------------------------------------------------|
| Web Framework   | Flask                                                                             |
| NLP & ML        | Gensim, Scikit-learn, NLTK, Autocorrect, Inflect, Contractions, TextSearch        |
| File Handling   | Textract, PyPDF2, pdfminer.six                                                    |
| Utilities       | NumPy, Requests                                                                   |
| Language        | Python 3.6 (Anaconda 4.3.0, 64-bit)                                               |

---

## 📂 Dataset

The dataset includes a collection of resumes and job descriptions used for training and testing the system. You can download it from the following sources:

- 🔗 [Primary Link (S3)](https://s3.ap-south-1.amazonaws.com/codebyte-bucket/Resume%26Job_Descriptions.zip)
- 🔗 [Mirror Link (Google Drive)](https://drive.google.com/open?id=17M9oDPip5JFFFNJhDCBQKy8BMqoyxajU)

---

## 🚀 Getting Started

### 🔧 Prerequisites

Make sure you have Python 3.6 installed. Then install the required dependencies:

```bash
pip install -r requirements.txt
```

### 📦 Required Python Packages

```text
textract==1.6.3
requests==2.22.0
Flask==1.1.1
gensim==3.8.0
sklearn==0.0
PyPDF2==1.26.0
autocorrect==0.4.4
nltk==3.4.5
contractions==0.0.21
textsearch==0.0.17
inflect==2.1.0
numpy==1.17.2
pdfminer.six==20181108
```

---

## 🖥️ Running the Application Locally

To launch the web app on your local machine:

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Start the Flask server:
   ```bash
   python app.py
   ```

3. Open your browser and go to: `http://localhost:5000`

4. Login credentials:
   - **Username**: `admin`
   - **Password**: `whitetigers2018`

---

## 🐳 Running with Docker

To containerize and run the application using Docker:

1. Build the Docker image:
   ```bash
   docker build -t arss .
   ```

2. Run the container:
   ```bash
   docker run -it -p 5000:5000 arss
   ```

Then navigate to `http://localhost:5000` in your browser.

---

## 🧠 How It Works

The system follows these core steps:

1. **Resume Parsing**: Extracts raw text from uploaded resumes using `textract`, `PyPDF2`, or `pdfminer.six`.
2. **Text Preprocessing**: Cleans and normalizes text using NLP techniques (tokenization, stemming, stopword removal).
3. **Vectorization**: Converts job descriptions and resumes into vector representations using TF-IDF or Word2Vec.
4. **Similarity Scoring**: Computes cosine similarity between job descriptions and resumes.
5. **Ranking**: Displays resumes sorted by relevance score, allowing recruiters to quickly identify top candidates.

---

## 📈 Future Enhancements

- Integrate advanced models like BERT for contextual embeddings
- Add support for DOCX and image-based resumes using OCR
- Enable multi-role job matching and filtering by skills or experience
- Build an admin dashboard for analytics and candidate tracking

---

## 👨‍💻 Author

Developed by **Kondru Charwick Hamesh**  
📧 Email: [charwick14@gmail.com](mailto:charwick14@gmail.com)

---

## 📄 License

This project is open-source and available under the MIT License. See the `LICENSE` file for more details.
