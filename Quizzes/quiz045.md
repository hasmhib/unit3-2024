# Quiz 045

<img width="max" alt="Screenshot 2024-02-15 at 1 16 14 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/9253304f-48c4-49d9-a487-720b2bba26d8">


## Code

```py
import sqlite3
from Project.my_library import DatabaseBridge

haiku = """Code flows like a stream
Algorithms guide its way
In silence, it solves
"""

my_db = DatabaseBridge('quiz045.db')
create_query = """CREATE table if not exists WORDS(
    id INTEGER PRIMARY KEY, 
    length int, 
    word text
    )
"""

my_db.run_query(query=create_query)

for word in haiku.split():
    insert_query = f"""INSERT into WORDS(length, word)
    values({len(word)}, '{word}')"""
    my_db.run_query(query=insert_query)

q = "SELECT avg(length) from WORDS"
out = my_db.search(query=q, multiple=False)

print("average word length is",out)
```

## Proof of work

<img width="max" alt="Screenshot 2024-02-08 at 2 41 43 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/9fe419d8-40f7-4836-8e37-775a5e490cb9">

## ER Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/d0d371b2-937a-4835-826b-32d79e7c3cc8)


