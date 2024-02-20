# Quiz 048
<img width="max" alt="Screenshot 2024-02-17 at 8 06 14 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/d1d13344-015a-4840-be3f-663e37725a6f">


## Code

```py
from Project.my_library import DatabaseBridge, get_hash, check_hash

db = DatabaseBridge("../Project/bitcoin_exchange.db")

query = "SELECT * from ledger"
results = db.search(query=query, multiple = True)
print(results)
db.close()

for row in results:
    id= row[0]
    sender_id = row[1]
    receiver_id = row[2]
    amount = row[3]
    signature = row[4]

    text = f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}"
    hash = get_hash(text)
    valid = check_hash(input_hash = signature, text = text)
    total_amount = 0
    if valid == True:
        total_amount += amount
    print(total_amount)
```

## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 4 17 05 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/6bda0af2-df37-4ae4-9d41-da7ed93290fd">

## ER Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/26d855a6-df7d-434e-b901-b8dac6a687ae)
