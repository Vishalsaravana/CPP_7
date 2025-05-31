# STACK APPLICATION USING LINKED LIST

## PROGRAM STATEMENT:

To write a CPP program for Infix to Prefix Conversion using Linked List Stack STL.

## ALGORITHM:  

1.	Start the program.
2.	Define a Node structure with a data field and a pointer to the next node. Initialize top as NULL.
3.	Implement a push function to add elements to the stack, creating a new node, assigning it the input data, and setting its next pointer to the current top.
4.	Implement a pop function to remove the top element from the stack, adjust the top pointer, and delete the popped node.
5.	Implement an isEmpty function to check if the stack is empty.
6.	Implement a precedence function to return the precedence value for the operators: 1 for +, -, 2 for *, /, and 3 for others (like parentheses).
7.	Convert an infix expression to prefix using the stack by reversing the input expression, processing each character based on precedence, and constructing the prefix expression. Return the converted prefix expression.
8.	End the program.

## PROGRAM:
```
#include<bits/stdc++.h> using namespace std; #include<iostream> #include<cstring>
struct Node{ char data;
struct Node*next;
}*top=NULL;

void push(char x){
struct Node *p = new Node; if(p==NULL){
p->data= x;
p->next =top; top = p;
}
else{
p->data= x;
p->next =top;
 
top = p; }

}

char pop(){ int x=-1;
struct Node *p; if(top==NULL){
cout<<"\nStack is empty";
}
else{
p=top;
x= p->data; top=top->next; delete p;
}
return x;
}
int isEmpty(){ returntop?0:1;
}
int precedence(char ch){ if(ch=='+'||ch=='-')
return 1;
else if(ch=='*'||ch=='/') return 2;
else
return 3;
}

string infixToPrefix(string infix){ stack<char> s;
int length=0,i,t; stringprefix="";
length = infix.length(); reverse(infix.begin(),infix.end()); for(i=0;i<length;i++){
t = precedence(infix[i]); if(t==3){
prefix += infix[i]; continue;
}
else{
if(s.empty()|| t>=precedence(s.top())){ s.push(infix[i]);
 
continue;
}
else{
while(!s.empty() && t<precedence(s.top())){ prefix+=s.top();
s.pop();
}
s.push(infix[i]); continue;
}
}
}

while(!s.empty()){ prefix += s.top(); s.pop();
}

reverse(prefix.begin(),prefix.end()); returnprefix;
}

int main(){
char *infix = new char; cin>>infix; cout<<infixToPrefix(infix);
}
 ```
## OUTPUT :
![image](https://github.com/user-attachments/assets/f5c24b63-5eb4-48a3-bcb1-52cc0aef8e22)

## RESULT:

Thus, the C++ program for Infix to Prefix Conversion using Linked List Stack STL is created successfully.
 


