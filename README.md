# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date: 24\5\2026
# Register no: 212224040286
# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.


# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."
Procedure:
1. Define the core requirements of a personal productivity assistant.
2. Identify and construct appropriate prompts for each task using an LLM (e.g., ChatGPT).
3. Simulate natural user interaction through a simple interface or command-line system.
4. Collect feedback or inputs from users and adapt responses accordingly.
5. (Optional) Integrate basic memory to simulate preference adaptation.
EXPECTED OUTPUT: - (attached the drive link)
Output (Example Response by LLM):
Personal Productivity Assistant Features:
1. Daily Task Manager:
o Accept tasks via natural language (e.g., "Remind me to call mom at 6 PM").
o Organize tasks by priority and deadline.
o Provide daily summaries and pending items.
2. Smart Scheduler:
o Schedule events and set reminders using contextual understanding.
o Notify user of overlapping appointments or free time slots.
3. Wellness Tips Generator:
o Suggest daily wellness advice (hydration, exercise, screen-time breaks).
o Adapt suggestions based on past user preferences and responses.


# Objectives

* Understand prompt engineering concepts
* Build a prompt-based productivity application
* Compare outputs from different prompt styles
* Improve task organization using AI
* Demonstrate practical usage of LLMs



# Tools Required

| Tool                                                                           | Purpose                 |
| ------------------------------------------------------------------------------ | ----------------------- |
| Python                                                                         | Application Development |
| [OpenAI API](https://platform.openai.com/docs/overview?utm_source=chatgpt.com) | AI Response Generation  |
| VS Code                                                                        | Code Editor             |
| Streamlit (Optional)                                                           | Web Interface           |



# System Architecture

```text
User Input
     ↓
Prompt Engineering Layer
     ↓
Large Language Model
     ↓
Task Analysis & Scheduling
     ↓
Organized Output
```


# Types of Prompt Designs

## 1. Simple Prompt

### Prompt

```text
Organize my tasks for today:
- Finish assignment
- Attend meeting at 2 PM
- Buy groceries
- Exercise
```

### Output

```text
1. Finish assignment
2. Attend meeting at 2 PM
3. Buy groceries
4. Exercise
```

### Observation

* Basic ordering only
* No prioritization
* No time optimization


## 2. Structured Prompt

### Prompt

```text
You are a productivity assistant.
Organize the following tasks based on priority and time:

Tasks:
- Finish assignment (deadline tomorrow)
- Attend meeting at 2 PM
- Buy groceries
- Exercise for 30 minutes

Generate:
1. Priority order
2. Suggested timeline
3. Important reminders
```

### Output

```text
Priority Tasks:
1. Finish assignment
2. Attend meeting
3. Buy groceries
4. Exercise

Suggested Timeline:
9 AM – 12 PM : Assignment
2 PM – 3 PM : Meeting
5 PM – 6 PM : Groceries
7 PM – 7:30 PM : Exercise

Reminder:
Complete the assignment before evening.
```

### Observation

* Better organization
* Includes scheduling
* More useful response

## 3. Advanced Prompt

### Prompt

```text
Act as an intelligent personal productivity coach.

User Profile:
- College student
- Easily distracted
- Available from 9 AM to 9 PM
- Prefers breaks after long work sessions

Tasks:
- Finish assignment (high priority)
- Attend project meeting at 2 PM
- Buy groceries
- Exercise
- Prepare presentation slides

Requirements:
1. Create an optimized schedule
2. Include short breaks
3. Suggest productivity techniques
4. Motivate the user
5. Highlight high-priority tasks
```

### Output

```
Optimized Schedule:

9:00 AM – 11:00 AM
Complete assignment

11:00 AM – 11:15 AM
Short break

11:15 AM – 1:00 PM
Prepare presentation slides

2:00 PM – 3:00 PM
Project meeting

3:00 PM – 3:15 PM
Refreshment break

5:00 PM – 6:00 PM
Buy groceries

7:00 PM – 7:30 PM
Exercise

Productivity Tips:
- Use Pomodoro Technique
- Avoid social media during study hours
- Keep phone on silent mode

Motivation:
You are progressing steadily. Focus on one task at a time.
```

### Observation

* Personalized output
* Context-aware scheduling
* Human-like assistance
* Better productivity guidance



# Python Implementation

```
import openai

openai.api_key = "YOUR_API_KEY"

prompt = """
Act as a smart productivity assistant.

Organize these tasks:
- Finish assignment
- Attend meeting at 2 PM
- Buy groceries
- Exercise

Create:
1. Priority order
2. Timeline
3. Productivity tips
"""

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "user", "content": prompt}
    ]
)

print(response['choices'][0]['message']['content'])
```

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/7eb44e7e-b550-4d96-b01f-151d2db4eeeb" />

# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
