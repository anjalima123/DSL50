#include <iostream>
using namespace std;

// Node structure
struct Node {
    int data;
    Node* next;
};

Node* front = NULL;
Node* rear = NULL;

// Enqueue (Insert)
void enqueue(int x) {
    Node* temp = new Node();
    temp->data = x;
    temp->next = NULL;

    if (rear == NULL) {
        front = rear = temp;
    } else {
        rear->next = temp;
        rear = temp;
    }
    cout << x << " inserted into queue\n";
}

// Dequeue (Delete)
void dequeue() {
    if (front == NULL) {
        cout << "Queue Underflow\n";
        return;
    }

    Node* temp = front;
    cout << front->data << " deleted from queue\n";
    front = front->next;

    if (front == NULL) {
        rear = NULL;
    }

    delete temp;
}

// Display queue
void display() {
    if (front == NULL) {
        cout << "Queue is empty\n";
        return;
    }

    Node* temp = front;
    cout << "Queue elements: ";
    while (temp != NULL) {
        cout << temp->data << " ";
        temp = temp->next;
    }
    cout << endl;
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    dequeue();
    display();

    return 0;
}
