# 📧 AI Email Subject Generator

A simple yet powerful **AI-powered Email Subject Generator** built in Jupyter Notebook that analyzes the content of an email and creates a formal, professional subject line using OpenAI's GPT model.

🔗 GitHub Repository:
[https://github.com/vinay845/email_subject_generator](https://github.com/vinay845/email_subject_generator)

---

## 🚀 Project Overview

This notebook-based tool reads the full body of an email and intelligently suggests a suitable subject line that matches its tone and intent. It is ideal for automating email workflows or improving professional communication.

---

## ✨ Key Features

* 🔍 Analyzes the complete email content
* 🧠 Generates a formal and relevant subject line
* 🔐 Secure API key handling using `.env`
* ⚡ Fast and lightweight using `gpt-4.1-nano`
* ✅ Automatically validates OpenAI API key

---

## 🛠️ Technologies Used

* Python
* Jupyter Notebook (.ipynb)
* OpenAI API
* python-dotenv
* IPython Display

---

## 📁 Project Structure

```
email_subject_generator/
│
├── email_subject_generator.ipynb
├── .env
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/vinay845/email_subject_generator.git
cd email_subject_generator
```

### 2️⃣ Install dependencies

```bash
pip install openai python-dotenv ipython
```

---

## 🔑 Environment Configuration

Create a `.env` file in the root folder and add your OpenAI API key:

```env
OPENAI_API_KEY=sk-proj-your-api-key-here
```

✔ Ensure:

* No extra spaces
* Key starts with `sk-proj-`

The notebook checks and confirms the validity automatically.

---

## ▶️ How to Use

Open the notebook and define your email content:

```python
email = """Your email body here"""
subject_generator(email)
```

### ✅ Sample Output:

```
Subject: Staying Connected and Sharing Recent Updates
```

---

## 🧠 How It Works

1. The email content is passed to the model via structured prompts.
2. OpenAI analyzes tone and intent.
3. A concise formal subject line is returned.

Core function:

```python
def subject_generator(email):
    response = openai.chat.completions.create(
        model="gpt-4.1-nano", 
        messages=messages(email)
    )
    return "Subject: " + response.choices[0].message.content
```

---

## 📌 Ideal For

* Professionals writing formal emails
* Email automation systems
* CRM platforms
* Productivity enhancement tools

---

## 🔮 Future Improvements

* Multiple subject suggestions
* Tone selector (formal, friendly, urgent)
* Email summarization
* Web interface using Streamlit
* Browser extension integration

---

## 🤝 Contributing

Feel free to fork this repository and submit pull requests to improve functionality or add new features.

---

## 👤 Author

**Vinay Kahar**
GitHub: [https://github.com/vinay845](https://github.com/vinay845)

---

## 📄 License

This project is licensed under the MIT License.
Free to use, modify, and distribute.


