# Recursion
## Aim 
To study and impliment Recursion.

## software:
VS code, online complier, Dev cpp.

## Theory
#### Recursion:
- Recursion in C++ is a technique where a function calls itself to solve a problem.
- This approach is often used for problems that can be divided into smaller, similar subproblems. 
- A recursive function typically has two main components:
  - Base Case: A condition under which the function will stop calling itself, preventing 
  infinite recursion.
  - Recursive Case: The part of the function where it calls itself with modified arguments to 
  gradually approach the base case.
> For example:
```cpp
#include<iostream>
using namespace std;

int fact(int n)
{
    if (n<=1)
        return 1;

    else return (n*fact(n-1));
}
int main()
{
    int a;
    cout<<"Enter an integer: "<<endl;
    cin>>a;
    cout<<"Factorial is: "<<fact(a);
}
```

## Algorithms:
1. Start
2. Input an integer `a`
3. Function Definition (`fact(n)`):
    - If `n <= 1`, return 1 (base case)
    - Else, return `n * fact(n - 1)` (recursive case)
4. Call the function `fact(a)` to calculate the factorial of the number:
    - If `a` is 0 or 1, factorial is 1.
    - Otherwise, multiply `a` with the factorial of `a - 1` and keep repeating this process until `a` becomes 1 (recursive breakdown).
5. Output the result of the factorial.
6. End

Example walkthrough for `fact(5)`:   
`fact(5)` → returns `5 * fact(4)`   
`fact(4)` → returns `4 * fact(3)`   
`fact(3)` → returns `3 * fact(2)`   
`fact(2)` → returns `2 * fact(1)`   
`fact(1)` → returns `1`   
Final result: `5 * 4 * 3 * 2 * 1 = 120`.

## code:

**1.Addition of n integrals:**

//gayatri ratnaparkhi 2307013169

//addition of all integers upto n

#include<iostream>

using namespace std;

int sum(int n)

{
	
    if (n<=1)
    
        return n;
        
    else 
    
        return n + sum(n-1);
        
}

int main()

{
	
    int num;
    
    cout<<"Enter a number: "<<endl;
    
    cin>>num;
    
    cout<<"Sum is: "<<sum(num);
    
}

/*

OUTPUT: 

Enter a number: 

7

Sum is: 28

*/

**Factorial**
//gayatri ratnaparkhi 2307013169

//factorial using recusrion

#include<iostream>

using namespace std;

int fact(int n)

{
	
    if (n<=1)
    
        return 1;
        

    else return (n*fact(n-1));
    
}

int main()

{
	
    int a;
    
    cout<<"Enter an integer: "<<endl;
    
    cin>>a;
    
    cout<<"Factorial is: "<<fact(a);
    
}

/*

OUTOUT: 

Enter an integer: 

7

Factorial is: 5040

*/
**Reverse Integer:**

//gayatri ratnaparkhi 2307013169

//print integer in reverse

#include <iostream>

using namespace std; 

void reverse(int n)

{
	

   if (n < 10) 
   
   {
   	
      cout<<n;
      
      return;
      
   }

   else
   
   {
   	
      cout<<n%10;
      
      reverse(n/10);
      
   }
   
}

int main()

{
	
   int n;
   
   cout<<"Enter a four digit integer: ";
   
   cin>>n;
   
   cout<<"Reversed string: ";
   
   reverse(n);
   
}

/*

OUTPUT: 

Enter a four digit integer: 5647

Reversed String: 7465

/*
**4. Reverse the string**
//gayatri ratnaparkhi 2307013169

//print a string in reverse

#include <iostream>

using namespace std;

int length(char *str) 

{
	
    int l = 0;
    
    while (str[l] != '\0') 
    
    {
    	
        l++;
        
    }
    
    return l;
    
}

void reverse(char *str, int i, int n) 
 
{ 

    if (i == n) 
    
        return;  
        
    reverse(str, i + 1, n);  
    
    cout << str[i]; 
    
}

int main() 

{ 

    char str[50]; 
    
    cout << "Enter a string: ";
    
    cin>>str;

    int n = length(str); 
	 
    reverse(str, 0, n); 
    
    return 0; 
}

/*

OUTPUT: 

Enter a string: C++AndDataStructuresLab

baLserutcurtSataDdnA++C

*/

//ALTERNATE METHOD

#include <iostream>

using namespace std;

void print_rev(char *str)

{
	
    if (*str!='\0')
    
    {
    	
        print_rev(str+1);
        
        cout<<*str;
        
    }
    
}

int main()

{
	
    char str[]="Gayatri";
    
    print_rev(str);
    
}

//OUTPUT: irtayaG


## conclusion:
WE have have studied and implimented recursion. 
