### Linked List Overview
#
#### A linked list is a data structure that consists of nodes, where each node contains a value and a reference to the next node. It allows dynamic insertion and deletion of elements, facilitating efficient memory utilization. Linked lists are commonly used in computer science for various applications, such as implementing stacks and queues. 

 > It has Node class which consist Data and next/link/address of next node.

 > To understand Linked List Concept we need to keep in mind when we talk about head , it means a whole node which has it's data part and link part.

 > Head->data and Head->link

 > Head will we a Pointer of Node type (Name of the class)

 > To call that we need a constructor

  ``` class Node{
public : 
  int data;
  Node* next;

  Node(int val){
    this->data = val;
    this->next = NULL;
  }
};
```
#
### Single Linked List

## Main Template
```
int main() {
  Node* n1 = new Node(12);
  Node* head = n1;
  Node* tail = n1;
  
  InsertAtHead(head,10);
  InsertAtHead(head,8);
  InsertAtHead(head,6);
  InsertAtTail(tail,14);
  InsertAtMiddle(head,1,13);
  Print(head);
  
} 
```
## We are taking void as return type because we are cout the result and not return as int or anyother datatype.

 - [x] Insert at Head
   ```
   void InsertAtHead(Node* &head,int val) {
    Node* temp = new Node(val);
    temp->next = head;
    head = temp;
    }
   ```

 - [x] Insert at Tail
   ```
   void InsertAtTail(Node* &tail,int val){
    Node* temp = new Node(val);
    tail->next = temp;
    tail = temp;
    }
   ```

  - [x] Insert at Some Position
    ```
    void InsertAtMiddle(Node* &head,int position,int val){
      if(position == 1)
        {
        InsertAtHead(head,val);
        return;
        }
      Node* start = head;
      Node* temp = new Node(13);
      int pos = 1;
  
      while(pos < position-1){
        start=start->next;
        pos++;
      }

      temp->next = start->next;
      start->next = temp;
    }
    ``` 
      

  
    
