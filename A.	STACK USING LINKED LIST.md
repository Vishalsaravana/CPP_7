# STACK USING LINKED LIST

## PROGRAM STATEMENT:

To write a CPP Program to insert five special character elements in to stack using linked list.

## ALGORITHM:  

1.	Start the program/
2.	Define a stack of type char to hold elements.
3.	Input the number of elements (n) to be pushed onto the stack.
4.	Use a loop to input n characters and push them onto the stack.
5.	Output the current size of the stack using s.size().
6.	Output the top element of the stack using s.top(), then pop the element and repeat for the second pop operation.
7.	After two pop operations, output the new top element and the size of the stack.
8.	End the program.

## PROGRAM:
```
#include<iostream> #include<stack>

usingnamespacestd; int main()
{
stack<char>s; int n;
char data; cin>>n;
for(int i=0;i<n;i++){ cin>>data; s.push(data);
}
cout<<"Current size of the stack is "<<s.size()<<endl; cout<<"Thetopelement ofthe stack is "<<s.top()<<endl; s.pop();
cout<<"Thetopelement after 1 popoperation is "<<s.top()<<endl; s.pop();
cout<<"The top element after 2 pop operations is "<<s.top()<<endl; cout<<"Size ofthestack after 2 popoperations is "<<s.size()<<endl;

}
 ```

## OUTPUT :
![image](https://github.com/user-attachments/assets/71fff065-96ee-4ea5-8f43-76a647ab5483)

## RESULT:

Thus, the C++ program to insert five special character elements in to stack using linked list is created successfully.


