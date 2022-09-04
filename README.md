# 90-Days-Coding-Journey

## 1 - RECURSION: a function that call itself again and again.
##### Ques. Factorial of a number.
#include <iostream>
using namespace std;

int factorial(int x){
    if(x==0) return 1;
    
    return x*factorial(x-1);
}

int main() {
   int n;
   cin>>n;
   if(n<0){
       cout<<"Error";
   }
   else{
       cout<<factorial(n);
   }
   
   

    return 0;
}
