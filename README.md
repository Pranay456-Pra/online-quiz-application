# online-quiz-application
from flask import Flask, render_template, request

app = Flask(__name__)

# Quiz questions
quiz = [
    {
        "question": "What is the capital of Australia?",
        "options": ["Sydney", "Melbourne", "Canberra", "Perth"],
        "answer": "Canberra"
    },
    {
        "question": "Who developed Python?",
        "options": ["Guido van Rossum", "Elon Musk", "Bill Gates", "Mark Zuckerberg"],
        "answer": "Guido van Rossum"
    },
    {
        "question": "Which language is used for web apps?",
        "options": ["Python", "HTML", "JavaScript", "All of these"],
        "answer": "All of these"
    }
]

@app.route("/", methods=["GET", "POST"])
def index():
    if request.method == "POST":
        score = 0
        for i, q in enumerate(quiz):
            selected = request.form.get(f"q{i}")
            if selected == q["a]()
