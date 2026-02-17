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
