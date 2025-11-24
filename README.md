AI Communication Scoring Tool — Nirmaan Intern Case Study
This project implements an AI-based scoring system for evaluating students’ spoken communication skills using a transcript of their self-introduction.
The system combines rule-based checks, NLP semantic similarity, and rubric-based weighting to generate a final score (0–100) with per-criterion feedback.
This submission is created as part of the Nirmaan AI Intern Case Study.

**🚀 Features**

Accepts any transcript text input
Computes:
Overall communication score (0–100)
Word count
Per-criterion scoring (semantic + rule-based)
Semantic similarity using Sentence Transformers
Keyword score (if available in rubric)
Length evaluation (min/max words)
Generates JSON-formatted detailed feedback
Simple Gradio UI for demo and testing
Clean, modular scoring pipeline

**🧠 Scoring Approach**

The scoring aligns with the case study requirements:
1️⃣ Rule-Based Scoring
Keyword matches (if the rubric provides keywords)
Word count checks (max/min word limits)

2️⃣ NLP-Based Semantic Scoring
Uses Sentence Transformers (all-MiniLM-L6-v2) to compute similarity between:
The transcript (student input)
Each rubric criterion description
Semantic similarity ∈ [0,1] is scaled into a score ∈ [0,100].

3️⃣ Rubric-Driven Weighting
Each rubric criterion has a weight, and the final score is:
Final Score = Weighted average of all criterion scores (scaled to 0–100)

4️⃣ Output Format
Overall score
Total word count
**Per-criterion:**
Semantic score
Keyword score
Length score
Final weighted combined score
Feedback summary

**🌐 Live Demo (Gradio App)**

You can test the communication scoring tool directly here:

👉 https://63acccb08c73ed00de.gradio.live/

**📊 Sample Input & Output**
📝 Input Transcript
Hello, My name is Chandan Shetty, Good morning to everyone!
📌 Output
Metric	Value
Overall Score	57.85
Word Count	10
