# Quiz 049
<img width="max" alt="Screenshot 2024-02-19 at 0 49 19 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/47fc04b1-2120-4d10-a89c-fa5baf9146c8">


## Code

```py
from Project.my_library import DatabaseBridge

db = DatabaseBridge(name='bitcoin_exchange.db')

create_table = '''CREATE TABLE if not exists user(
id INTEGER PRIMARY KEY,
user_id INTEGER NOT NULL, 
uname  NOT NULL,
uemail NOT Null
)'''

db.run_query(create_table)

add = '''INSERT into user (user_id, uname, uemail) values(560,'bob1','bob1@xyz'),(371,'bob2','bob2@xyz'),(488,'bob3','bob3@xyz'),(561,'bob4','bob4@xyz'),(254,'bob5','bob5@xyz'),(920,'bob6','bob6@xyz'),(438,'bob7','bob7@xyz'),(744,'bob8','bob8@xyz'),(261,'bob9','bob9@xyz')
'''
db.run_query(add)

sql_query_1 = "Select * from ledger join user on sender_id = user_id where uname = 'bob6'"
sql_query_2 = "Select * from ledger join user on receiver_id = user_id where uname = 'bob6'"
results_1 = db.search(query=sql_query_1, multiple = True)
results_2 = db.search(query=sql_query_2, multiple = True)

print(results_1)
print(results_2)
```
## Q1 Create ER diagram.
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/24a10a65-a981-4fec-bf30-3a4d60168e20)


## Q2 Create a query to get all the transactions involving user id= 920.

```py
SELECT * FROM user where user_id =920
```
## Proof of work
<img width="max" alt="Screenshot 2024-02-19 at 5 43 24 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/1cba1aa0-d280-47dc-b0dc-2c213ee6aaec">

