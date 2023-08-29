#include <iostream>
#include <vector>
#include <string>

int main() {
    std::vector<std::string> todoList;
    std::string task;
    
    char choice;
    do {
        std::cout << "Enter a task to add to the To-Do List: ";
        std::getline(std::cin, task);
        todoList.push_back(task);
        
        std::cout << "Do you want to add another task? (y/n): ";
        std::cin >> choice;
        std::cin.ignore(); // Clear the newline character from the buffer
        
    } while (choice == 'y' || choice == 'Y');
    
    std::cout << "\nTo-Do List:\n";
    for (size_t i = 0; i < todoList.size(); ++i) {
        std::cout << i + 1 << ". " << todoList[i] << "\n";
    }
    
    return 0;
}
