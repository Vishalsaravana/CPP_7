# QUEUE USING LINKED LIST

## PROGRAM STATEMENT:

To write a CPP Program to implement Queue using Linked List, insert integer elements in to Queue and delete two items from Queue.

## ALGORITHM:  

1.	Start the program.
2.	Define Node: Create a Node class with data and next pointer.
3.	Push: Insert a new node at the rear of the queue.
4.	Pop: Remove the front node.
5.	Display: Print the queue from front to rear.
6.	Display Front/Rear: Print front and rear node data.
7.	Main: Perform pop(), push(), and display queue operations.
8.	End the program.

## PROGRAM:
```
#include<iostream> using namespace std;

class Node{ public:
double data; Node*next;
}*rear,*front,*temp;
voidpush(){
temp = new Node; cin>>temp->data; temp->next=NULL; if(rear == NULL){
front =temp; rear = temp;
}
else{
rear->next =temp; rear = rear->next;
}
}

voidpop(){
 
if(rear == NULL){ cout<<"Underflow."<<endl;
}
else{
temp= front;
front = front->next; temp->next =NULL; free(temp); }
}
void display(){ temp= front;
while(temp!=NULL){ cout<<temp->data<<" "; temp = temp->next;
}
}
void disp(){ temp= front;
cout<<"Queue Front : "<<temp->data; while(temp->next !=NULL){
temp = temp->next;
}
cout<<endl;
cout<<"Queue Rear : "<<temp->data;
}

int main()
{
int n; cin>>n; pop();

for(inti=0;i<n;i++){ push();
}
cout<<"Queue :"; display();
pop();
pop(); cout<<endl;
cout<<"After DeQueue:"; display();
cout<<endl; disp();
 
}
```
## OUTPUT :
![image](https://github.com/user-attachments/assets/a88f12eb-aeaa-4f07-9997-34fad4eafb78)

## RESULT:

Thus, the C++ program to implement Queue using Linked List, insert integer elements in to Queue and delete two items from Queue is created successfully.

