# Quiz 044

<img width="max" alt="Screenshot 2024-02-08 at 2 40 04 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/7017c469-e8a2-4758-8264-af064bc148b9">

## 1. Create the UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/e9ef2220-5deb-434d-a8f2-2bdb9a72a356)

## 2. Create the SQL queries to find the responsible for the fraudulent transaction.

### First I need to calculate the balance based on the transactions recorded.
```py
SELECT account_id, SUM(CASE WHEN transaction_type = 'deposit' THEN amount ELSE -amount END) AS supposed_balance
FROM transactions
GROUP BY account_id;
```
## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 1 05 18 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/d6175099-ac2f-4009-ac10-370fa42ec103">


### Next I need a reported balance
```py
SELECT account_id, balance from accounts;
```
## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 1 07 34 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/5078b258-a1c7-46f8-b641-36f2d742c8b6">


### Compare the supposed balance and reported balance. 



Account 12: supposed_balance 4600, reported_balance 5000 -> fraudulent transaction

Account 13: supposed_balance 2200, reported_balance 1400 -> fraudulent transaction

Account 15: supposed_balance 2300, reported_balance 1500 -> fraudulent transaction

Account 17: supposed_balance 2400, reported_balance 1600 -> fraudulent transaction

Account 19: supposed_balance 2500, reported_balance 1700 -> fraudulent transaction


## 3. What is the name of the customer and the problem that resulted in the bankruptcy of the bank?

```py
SELECT * FROM customers WHERE customer_id IN (12, 13, 15, 17, 19);
```

## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 1 15 08 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/ce6ab9d3-ecf7-4579-82fb-2c5d689a2bc8">


