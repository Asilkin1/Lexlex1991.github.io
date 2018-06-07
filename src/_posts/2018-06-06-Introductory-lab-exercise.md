---
layout: post
title: Introductory Lab Exercise
data: 2018-06-06 7:00:00
author: Alex Silkin
tags: notes
---

Just a reminder of how to use Visual Studio.

```c++
/*
    Enhancement 1: Prevent Overdrafts on the Bank Account
*/ 

if (amount > balance)
    cout << "Not enough money";
else:
    balance -= amount;

/* 
    Enhancement 2: Set Annual Interest Percentage 
*/ 

monthlyInterestRate = annualInterestRate / MONTHS_PER_YEAR;
monthlyInterestCoefficient = monthlyInterestRate / 100;

/*
    Enhancement 3: 
    - Calculate Interest for One Month 
    - Add to Balance
*/ 

interestThisMonth = balance * monthlyInterestCoefficient;

/* 
    Enhancement 4: Format the Output
    Print float numbers to monitor like $100.00
*/ 

cout << fixed << setprecision(2);
```
