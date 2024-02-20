# Quiz 047
<img width="max" alt="Screenshot 2024-02-15 at 1 18 21 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/60a4a363-2a28-429d-83f0-606c5d7554bd">


## Code

```py
from Project.my_library import DatabaseBridge, get_hash, check_hash

db = DatabaseBridge("../Project/bitcoin_exchange.db")
sql_query = "SELECT * from ledger"
results = db.search(query=sql_query, multiple = True)
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
    print(valid)

```

## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 4 10 04 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/6bee5662-e81e-4968-879f-8513b4299d71">

## ER Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/26d855a6-df7d-434e-b901-b8dac6a687ae)


