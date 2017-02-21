---
layout: post
title: Recursion
tags: [algorithms]
---

Recursion is a function that calls itself. 

Here is a simple example in Java of factorial using recursion:
```
 public class Factorial
{
    public static void main(String[] args) 
    {
        int n, mul;
        Scanner s = new Scanner(System.in);
        System.out.print("Enter any integer:");
        n = s.nextInt();
        Factorial obj = new Factorial();
        mul = obj.fact(n);
        System.out.println("Factorial of "+n+" :"+mul);
    }
    int fact(int x)
    {
        if(x > 1)
        {
            return(x * fact(x - 1));
        }
        return 1;
    }
}
```

You can find more on recursion [here](http://introcs.cs.princeton.edu/java/23recursion/).
