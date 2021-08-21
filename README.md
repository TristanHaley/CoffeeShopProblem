# Coffee Shop Test

## Test Overview

A small coffee shop wants you to improve their software.\
Users can:
- Enter customer details
- Print a report containing the financial details and other shop details

You have been asked to:
- Refactor the code using clean coding principles to make the code maintainable
- Add new features
- Write tests to prevent functionality from breaking

We recommend you spend 4 hours on your solution.

## What we look for

When reviewing the test, we look for a solution which:
- Is clean, easy to understand, and maintainable
- Shows an understanding of software craftmanship
- Doesn't break the existing functionality

Your solution will form the main part of your technical interview, where we'll discuss your design decisions.

## System Description
There are three types of customer currently in use:

| Customer | Benefits |
|:---:|---|
| General | Normal paying customer |
| Loyalty | Repeat customers who get benefits for buying coffee |
| Employee | Employees of the Coffee Shop drink for free |

The Coffee Shop charges a base price for a drink,
which loyalty members can choose to pay with their loyalty points.
Loyalty points are given to loyalty members for certain drinks.
The amount depends on the drink.

This input:
```
add general Christopher
add loyalty Damian 1000 true
add loyalty Craig 0 false
add loyalty Kirsty 60 false
add employee Andrzej
add general Matt
add general Colin
print summary
```
Generates this summary report:
```
Coffee Shop Summary

Total customers: 7
    General sales: 3
    Loyalty member sales: 3
    Employee Complimentary: 1

Total revenue from drinks: 500
Total costs from drinks: 350
Coffee Shop generating profit of: 150

Total loyalty points given away: 10
Total loyalty points redeemed: 100

Coffee Shop will open tomorrow
```

## New Features
1. **The Coffee Shop would like a new type of customer**
   1. The new type will have the following benefits / restrictions:
      1. Cannot accrue loyalty points
      2. Will only be charges at 75% of the normal price
2. **The employee benefit of free drinks has been reviewed and no longer viable**
   1. You must change the system to ensure the following rules are implemented
      1. An Employee must pay the full price if the Shop profit is <50
      2. Employees can only receive a maximum of 2 free drinks each
3. **The shop would like to track their supply of coffee beans used and have this information shown on the summary report. Additionally, the Coffee Shop cannot open the following day if they have less than 25% of the beans left**
   1. The system must have:
      1. Show bean count information on the Summary Report
   2. You should use the following assumptions:
      1. A shop starts with 1000 beans
      2. 1 cup uses 150 beans

## Guidance
- You must not break any existing functionality. The solution should generate the same summary report (along with any additional information)
- There is a sample console application which demonstrates how a user might interact with the Coffee Shop system
- Your submission must be a single compressed file. Please remember to exclude any .exe file types