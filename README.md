# Assignment2
# Myth or Fact Flashcard Quiz App

## Project Overview

The **Myth or Fact Flashcard Quiz App** is a native Android application developed using **Kotlin** in **Android Studio** . The app is designed to help users test their knowledge by answering a series of **True or False** flashcard-style questions.

The main idea behind the app is to provide a simple, interactive, and educational quiz experience. Users are shown statements that may either be myths or facts, and they must decide whether each statement is true or false. At the end of the quiz, the app calculates the user’s score and displays feedback based on their performance.

This project demonstrates core Android development concepts such as:

- Activity navigation
- User interface design using XML layouts
- Button click handling
- Data storage using arrays
- Conditional logic
- Passing data between screens using intents
- Basic scoring and feedback systems

---

## Purpose of the App

The purpose of this app is to create an easy-to-use mobile flashcard quiz that helps users learn by interacting with short True or False questions.

The app can be used to:

- Help users identify common myths and facts
- Encourage learning through repetition
- Provide immediate feedback after each answer
- Track the user’s score during a quiz session
- Display final performance feedback at the end of the quiz

The app is suitable for educational use, especially for beginner-level learning activities where users need to revise simple facts in an engaging way.

---

## Target Users

The app is designed for:

- Students who want to learn through flashcards
- Teachers who want a simple quiz tool
- General users interested in myth-or-fact questions
- Beginner Android developers learning Kotlin app development

---

## App Features

### 1. Welcome Screen

The welcome screen introduces the app to the user and provides a **Start Quiz** button.

Main features:

- Displays the app title
- Provides a short description of the quiz
- Allows the user to begin the quiz

---

### 2. Flashcard Question Screen

The question screen displays one question at a time. The user selects either **True** or **False** .

Main features:

- Displays the current question
- Shows the question number
- Provides True and False answer buttons
- Gives immediate feedback after the user answers
- Prevents the user from answering the same question more than once
- Allows the user to move to the next question

---

### 3. Score Screen

The score screen appears after all questions have been answered.

Main features:

- Displays the final score
- Shows the total number of questions
- Provides feedback based on the user’s performance
- Allows the user to restart the quiz
- Allows the user to exit the app

---

## Design Considerations

### 1. Simplicity

The app was designed to be simple and easy to understand. Since the target users may include students and beginner users, the interface avoids unnecessary complexity.

The app uses:

- Clear text labels
- Large buttons
- Simple navigation
- Minimal screens
- Easy-to-read questions

This makes the app user-friendly and accessible.

---

### 2. User Experience

The app provides a smooth quiz flow from start to finish.

The user journey is:

1. Open the app.
2. Read the welcome message.
3. Tap **Start Quiz** .
4. Answer each flashcard question.
5. Receive feedback after each answer.
6. Continue until all questions are answered.
7. View the final score.
8. Restart or exit the app.

Immediate feedback improves the learning experience because users instantly know whether their answer was correct or incorrect.

---

### 3. Screen Navigation

The app uses multiple Android activities:

| Screen | Activity | Purpose |
|---|---|---|
| Welcome Screen | `MainActivity` | Introduces the app and starts the quiz |
| Question Screen | `QuestionActivity` | Displays questions and handles answers |
| Score Screen | `ScoreActivity` | Displays the final score and feedback |

Navigation between activities is handled using Android **Intents** .

For example:

- `MainActivity` opens `QuestionActivity`
- `QuestionActivity` opens `ScoreActivity`
- `ScoreActivity` can restart the quiz by opening `QuestionActivity` again

---

### 4. Data Handling

The quiz questions and answers are stored in arrays inside `QuestionActivity`.

Example structure:

- A `questions` array stores the question text.
- An `answers` boolean array stores the correct answers.

Each question has a matching answer at the same index.

For example:

```kotlin
questions[0] = "Lightning never strikes the same place twice."
answers[0] = false
