# JavaScript Quiz Application

### Overview
This is a JavaScript Quiz Application built using React, Axios, Material-UI, and React-Icons. The app fetches quiz questions from a backend API and allows users to submit their answers, receive feedback, and track their scores. 


### UI
![image](https://github.com/user-attachments/assets/40916b78-2b5b-4832-9b63-c2440129e6c0)

![image](https://github.com/user-attachments/assets/5df35eac-bf84-430f-9c28-5830cdabe2f4)

## Features

- Timed quiz with each question having 20 seconds to answer.
- A total quiz time of 60 seconds.
- Displays feedback on whether the answer is correct or incorrect.
- Shows the correct answer after submitting.
- A "Skip" button to skip the current question.
- Restart option after the quiz ends.
- Score calculation and grade display at the end of the quiz.

## Tech Stack

- **React**: Frontend framework.
- **Axios**: For making API requests.
- **Material-UI**: UI components.
- **React-Icons**: Icons used for the timer display.

## Components

### `Quiz.js`

This component handles the entire quiz functionality including fetching questions, managing timers, handling user input, and displaying feedback.

### Key States:

- `questions`: Stores the fetched quiz questions.
- `currentQuestionIndex`: Tracks the current question number.
- `timeLeft`: Timer for each individual question (20 seconds).
- `totalTimeLeft`: Timer for the entire quiz (60 seconds).
- `userAnswer`: Stores the current user's answer.
- `score`: Tracks the user's score.
- `quizOver`: Boolean to check if the quiz is over.
- `feedback`: Stores feedback about the user's answer (correct/incorrect).
- `errorMessage`: Displays any validation errors.

### Key Functions:

- `handleNextQuestion`: Advances to the next question when time runs out or an answer is submitted.
- `handleAnswerSubmit`: Submits the answer and shows feedback (correct/incorrect).
- `handleSkipQuestion`: Skips the current question and moves to the next.
- `handleStartQuizAfresh`: Restarts the quiz after it's over.
- `getGrade`: Calculates the grade based on the final score.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repository/quiz-app.git
    ```

2. Install the required dependencies:
    ```bash
    npm install
    ```

3. Start the development server:
    ```bash
    npm start
    ```

4. Ensure that your backend API is running to serve quiz questions and accept answers.

## API Endpoints

- `GET /api/questions`: Fetches the quiz questions from the backend.
- `POST /api/answer`: Submits the user's answer and returns whether it is correct along with the correct answer.

## Usage

1. After starting the app, the quiz will display the first question along with a countdown timer.
2. Enter your answer in the text field and click the "Answer" button or click "Skip" to move to the next question.
3. Feedback will be shown after each question, indicating whether your answer was correct or incorrect.
4. The quiz ends when either the time runs out or all questions are answered.
5. Your final score and grade will be displayed at the end of the quiz, and you can restart the quiz by clicking "Start Quiz Afresh."
