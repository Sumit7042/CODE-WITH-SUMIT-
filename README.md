# CODE-WITH-SUMIT-
AUTHOR - SUMIT NAGAR
#include <stdio.h>
#include <string.h>

// Define structure to store student details
struct Student {
    char name[50];
    int roll_no;
    float grade1, grade2, grade3;
    float average;
};

// Function to calculate average of grades
float calculateAverage(float grade1, float grade2, float grade3) {
    return (grade1 + grade2 + grade3) / 3.0;
}

// Function to display student information
void displayStudentInfo(struct Student student) {
    printf("\nStudent Name: %s\n", student.name);
    printf("Roll No: %d\n", student.roll_no);
    printf("Grade 1: %.2f\n", student.grade1);
    printf("Grade 2: %.2f\n", student.grade2);
    printf("Grade 3: %.2f\n", student.grade3);
    printf("Average Grade: %.2f\n", student.average);
}

int main() {
    struct Student student;

    // Get student information from user
    printf("Enter Student Name: ");
    fgets(student.name, sizeof(student.name), stdin);
    student.name[strcspn(student.name, "\n")] = '\0'; // Remove newline character from input

    printf("Enter Roll Number: ");
    scanf("%d", &student.roll_no);

    printf("Enter Grade 1: ");
    scanf("%f", &student.grade1);
    
    printf("Enter Grade 2: ");
    scanf("%f", &student.grade2);

    printf("Enter Grade 3: ");
    scanf("%f", &student.grade3);

    // Calculate the average grade
    student.average = calculateAverage(student.grade1, student.grade2, student.grade3);

    // Display student information and results
    displayStudentInfo(student);

    return 0;
    }



