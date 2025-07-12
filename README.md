# 🧠 Medical Insurance AI Agent

An intelligent AI Agent built using OpenAI GPT-4o and Python that allows users to ask **natural language questions** about a medical insurance dataset and receive **intelligent, human-like answers**.

---

## 🎯 Objective

The goal of this project is to build an **AI-powered assistant** that can:
1. Understand the structure and context of the `medical_insurance` dataset.
2. Accept natural language queries from users.
3. Use OpenAI's GPT-4o to generate step-by-step explanations and insights.
4. Provide real-time, interactive responses in the terminal or as a web app.

---

## 📊 Dataset: `medical_insurance.csv`

The dataset contains information about individuals and their health-related insurance costs.

### ✅ Columns Description:

| Column     | Description                                                  |
|------------|--------------------------------------------------------------|
| `age`      | Age of the individual in years                               |
| `sex`      | Gender (`male` or `female`)                                  |
| `bmi`      | Body Mass Index — indicator of body fat                      |
| `children` | Number of children/dependents covered by insurance           |
| `smoker`   | Smoking status (`yes` or `no`)                               |
| `region`   | Residential area (`northeast`, `southeast`, etc.)           |
| `charges`  | Final medical insurance cost charged                         |

---

## ⚙️ Tools & Technologies Used

| Tool          | Purpose                                                                 |
|---------------|-------------------------------------------------------------------------|
| `Python`      | Core language used for scripting and logic                              |
| `pandas`      | Loading, exploring, and summarizing the dataset                         |
| `OpenAI GPT-4o` | Generating human-like responses to data questions                    |
| `chat loop`   | Enables continuous Q&A via terminal                                     |
| `.env / os`   | Secure API key management                                               |
| `prompt engineering` | Combines dataset summary with user question to guide GPT        |

---

## 🔁 Project Workflow

```plaintext
1. Load the medical_insurance dataset using pandas
2. User types a natural language question
3. The AI agent function:
   - Summarizes the dataset
   - Builds a combined prompt (context + question)
   - Sends it to GPT-4o via OpenAI API
4. GPT-4o returns a smart, human-like answer
5. The system prints the answer in the terminal
6. Loop continues until the user types "exit"

---

User Types Question ─▶ ai_agent() ─▶ Summarize Dataset
                            │
                            ▼
                Build Combined Prompt (context + question)
                            │
                            ▼
                Send to OpenAI GPT-4o API (chat.completions)
                            │
                            ▼
            GPT analyzes + generates intelligent answer
                            │
                            ▼
               Return natural-language response to user
                            │
                            ▼
           Loop again or exit if user types "exit"


