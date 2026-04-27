#include <iostream>
using namespace std;

struct Node {
    int data;
    Node* next;
};

Node* top = NULL;

// Push
void push(int x) {
    Node* temp = new Node();
    temp->data = x;
    temp->next = top;
    top = temp;
    cout << x << " pushed into stack\n";
}

// Pop
void pop() {
    if (top == NULL) {
        cout << "Stack Underflow\n";
        return;
    }
    cout << top->data << " popped from stack\n";
    Node* temp = top;
    top = top->next;
    delete temp;
}

// Display
void display() {
    Node* temp = top;
    if (temp == NULL) {
        cout << "Stack is empty\n";
        return;
    }
    cout << "Stack elements: ";
    while (temp != NULL) {
        cout << temp->data << " ";
        temp = temp->next;
    }
    cout << endl;
}

int main() {
    push(10);
    push(20);
    push(30);
    display();
    pop();
    display();
    return 0;
}
