import random

# Sample vocabulary data (you can expand this with more words and translations)
vocabulary = {
    'hello': 'hola',
    'goodbye': 'adiós',
    'thank you': 'gracias',
    'yes': 'sí',
    'no': 'no'
}

def quiz():
    print("Welcome to the Vocabulary Quiz!\n")
    keys = list(vocabulary.keys())
    random.shuffle(keys)  # Shuffle the order of words for the quiz

    correct_count = 0
    total_questions = 5  # Number of questions in the quiz

    for i in range(total_questions):
        word = keys[i]
        correct_answer = vocabulary[word]

        print(f"What is the translation of '{word}'?")
        user_answer = input("Your answer: ")

        if user_answer.lower() == correct_answer.lower():
            print("Correct!")
            correct_count += 1
        else:
            print(f"Wrong! The correct answer is '{correct_answer}'.")

        print()  # Blank line for readability

    print(f"You answered {correct_count} out of {total_questions} questions correctly.")

if __name__ == "__main__":
    quiz()

