questions = []
answers = []
score = 0

n = int(input("How many questions do you want to add? "))

for i in range(n):
    q = input(f"Enter question {i+1}: ")
    a = input("Enter the answer: ")
    
    questions.append(q)
    answers.append(a.lower())

print("\n--- Quiz Start ---\n")

for i in range(n):
    user_answer = input(questions[i] + " ")
    
    if user_answer.lower() == answers[i]:
        print("Correct!\n")
        score += 1
    else:
        print("Wrong! Correct answer:", answers[i], "\n")

print("Your final score is:", score, "/", n)
