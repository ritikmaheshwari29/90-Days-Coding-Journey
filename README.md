# 90-Days-Coding-Journey
## https://leadcoding.in/dsa-courses/

## 1 - RECURSION: a function that call itself again and again. Stack recursion(1 function call another function in stack manner. Internal stack is there that's why space complexity)
### Space complexity:  height of tree
### time complexity: nodes 
##### Ques1. Factorial of a number.
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

##### Ques2. Sum of n natural number.
#include <iostream>
using namespace std;
 int sum(int x){
     while(x!=0){
         return x+sum(x-1);
     }
 }

int main() {
   int n;
   cin>>n;
   cout<<sum(n);
    return 0;
}

##### Ques3.Fibonacci Number (time O(2^n) (space O(n))
class Solution {
public:
    int fib(int n) {
        if(n==0) return 0;
        if(n==1 || n==2) return 1;
        
        return fib(n-1)+fib(n-2);
    }
};
    
##### Ques4.Power(X,N)
class Solution {
public:
    double myPow(double x, int n) {
        if (n==0) return 1;
        if (n < 0)
    {
      x = 1 / x;
      n = abs(n);
    }
        double temp = myPow(x,n/2);
        if(n%2==1) 
            return temp*temp*x;
        
        return temp*temp;
        
    }
};
