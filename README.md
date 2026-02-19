#ifndef STUDENT_H
#define STUDENT_H

#include <string>

class Student {
private:
    std::string name;
    std::string indexNumber;

public:
    // Constructor
    Student(std::string n, std::string idx);

    // Getters
    std::string getName() const;
    std::string getIndexNumber() const;

    // Display student info
    void display() const;
};

#endif




#include "Student.h"
#include <iostream>

Student::Student(std::string n, std::string index) : name(n), indexNumber(index) {}

void Student::display() const {
    std::cout << "Index: " << indexNumber << " | Name: " << name << std::endl;
}

std::string Student::getIndexNumber() const {
    return indexNumber;
}



8#include <iostream>
#include <vector>
#include "Student.h"

void addStudent(std::vector<Student>& students) {
    std::string name, index;
    std::cout << "Enter Student Name: ";
    std::getline(std::cin >> std::ws, name);
    std::cout << "Enter Index Number: ";
    std::cin >> index;
    
    students.push_back(Student(name, index));
    std::cout << "Student added successfully!\n";
}

void viewStudents(const std::vector<Student>& students) {
    std::cout << "\n--- Registered Students ---\n";
    for (const auto& s : students) {
        s.display();
    }
}
