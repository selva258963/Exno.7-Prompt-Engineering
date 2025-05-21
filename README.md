# Exno.7 – Prompt-Based Application Using ChatGPT

### Date: ``21-05-2025``

### Register No: ``212222040163``

## Aim:
To develop a prompt-based application using ChatGPT to organize daily tasks, demonstrating the progression from simple to more advanced prompt designs and their corresponding outputs.

---

## Algorithm:

1. **Define the Scenario and Use Case**
   - **Scenario**: A user wants to organize their daily tasks efficiently using AI prompts.
   - **Use Case**: The prompt-based application powered by ChatGPT helps the user generate structured, prioritized task lists based on various styles of input.

2. **Design Prompt Levels**
   - Simple: Basic task listing
   - Intermediate: Include priorities, durations, deadlines
   - Advanced: Role-based prompting, time scheduling, and context-based decision-making

3. **Generate Prompt-Response Examples**
   - Test different prompts and document ChatGPT's responses
   - Evolve prompt quality and complexity progressively

4. **Optional Implementation**
   - Use a Python CLI or notebook to simulate prompt inputs and display responses using ChatGPT API

---

## Simple Prompt Examples

### Prompt 1:
> Help me organize these tasks: grocery shopping, finish homework, clean my room.

**Output:**
1. Finish homework  
2. Grocery shopping  
3. Clean my room

---

### Prompt 2:
> List my tasks in bullet points:
- Laundry
- Buy milk
- Call mom

**Output:**
- Laundry  
- Buy milk  
- Call mom

---

## Intermediate Prompt Examples

### Prompt:
> Organize these tasks with priority and estimated duration:
- Finish report (2 hrs)  
- Walk the dog (30 mins)  
- Attend meeting (1 hr)

**Output:**
1. Attend meeting (1 hr) – High Priority  
2. Finish report (2 hrs) – Medium Priority  
3. Walk the dog (30 mins) – Low Priority

---

### Prompt:
> Categorize the following tasks under Work and Personal:
- Pay electricity bill  
- Submit project proposal  
- Call sister  
- Attend team meeting

**Output:**

**Work:**
- Submit project proposal  
- Attend team meeting

**Personal:**
- Pay electricity bill  
- Call sister

---

## Advanced Prompt Examples

### Role-based Prompt:
> You are a productivity coach. Plan my day from 9AM to 6PM with breaks:
- Team stand-up  
- Project work  
- Client call  
- Lunch  
- Review emails

**Output:**

9:00AM - 9:30AM: Team stand-up  
9:30AM - 11:00AM: Project work  
11:00AM - 11:15AM: Break  
11:15AM - 12:00PM: Client call  
12:00PM - 1:00PM: Lunch  
1:00PM - 2:30PM: Project work  
2:30PM - 3:00PM: Review emails  
3:00PM - 4:00PM: Project work  
4:00PM - 4:15PM: Break  
4:15PM - 6:00PM: Wrap-up tasks and planning

---

### Chain-of-Thought Prompt:
> Here are my tasks: Write blog, Record podcast, Update resume. Help me decide the best order based on creativity and focus level.

**Output:**

1. Write blog (requires highest creativity)  
2. Record podcast (medium focus)  
3. Update resume (light editing)

---

## Python Implementation – Task Organizer using ChatGPT API
```python
import openai

def organize_tasks(prompt):
    response = openai.ChatCompletion.create(
        model="gpt-4",
        messages=[{"role": "user", "content": prompt}]
    )
    return response['choices'][0]['message']['content']

if __name__ == "__main__":
    user_prompt = input("Enter your task prompt: ")
    output = organize_tasks(user_prompt)
    print("\nOrganized Tasks:\n", output)
```
---

## Result:
The prompt-based application successfully demonstrates the capability of ChatGPT to process and enhance user task lists by evolving prompts from simple lists to context-aware, productivity-optimized schedules.

---

## Conclusion:
This experiment illustrates how prompt engineering can influence the performance of AI models like ChatGPT in organizing and interpreting daily tasks. By refining prompt complexity, the responses become increasingly structured, helpful, and human-like.
