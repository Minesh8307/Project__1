# Project__1
A Quiz Game is an interactive application that presents users with multiple-choice questions to test their knowledge on various topics. It tracks scores, provides feedback at the end, and may include features like timers, categories, and answer reviews.


import java.util.Scanner;

public class QuizGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int score = 0; // Initialize the score to zero

        // Array to store correct answers for each question
        char[] correctAnswers = {'a', 'b', 'c', 'd', 'a'};

        // Array to store questions
        String[] questions = {
            "1. What is the capital of France?\n" +
            "a) Paris\n" +
            "b) Rome\n" +
            "c) Madrid\n" +
            "d) Berlin\n",

            "2. Who wrote 'Romeo and Juliet'?\n" +
            "a) William Shakespeare\n" +
            "b) Charles Dickens\n" +
            "c) Jane Austen\n" +
            "d) J.K. Rowling\n",

            // Add more questions here
        };

        // Loop through each question
        for (int i = 0; i < questions.length; i++) {
            System.out.println(questions[i]);
            char userAnswer = scanner.next().charAt(0); // Read user's answer

            // Compare user's answer with correct answer
            if (userAnswer == correctAnswers[i]) {
                score++; // Increment score if answer is correct
            }
        }

        // Calculate and display the final score
        double percentage = (double) score / questions.length * 100;
        System.out.println("Your score: " + score + "/" + questions.length);
        System.out.println("Percentage: " + percentage + "%");

        scanner.close();
    }
}
