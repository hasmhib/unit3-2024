```.py
class Book:
    def __init__(b,lang:str, price:int, title:str, pages:int, auth:str):
        b.language = lang
        b.price = price
        b.title = title
        b.pages = pages
        b.author = auth

    def get_author(b)->str:
        return b.author

    def get_language(b)->str:
        return b.language

    def compare_price(b, other_book)->str:
        if b.price > other_book.price:
            return f"{b.title} is more expensive than {other_book.title}."
        elif b.price < other_book.price:
            return f"{b.title} is less expensive than {other_book.title}."
        else:
            return f"{b.title} and {other_book.title}"

    def count_pages(b)->int:
        return b.pages

Book1 = Book(lang="English", price=500, title="Charlie and the Chocolate Factory", pages=500, auth="Roald Dahl")
Book2 = Book(lang="English", price=800, title="Harry Potter", pages=800, auth="J. K. Rowling")
Book3 = Book(lang="English", price=600, title="Alice in Wonderland", pages=600, auth="Lewis Carroll")

print(Book1.get_author())
print(Book2.get_author())
print(Book3.get_author())

print(Book1.compare_price())

```
