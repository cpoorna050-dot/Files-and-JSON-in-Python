# Files-and-JSON-in-Python
json
import json
books = [
  {"title": "The Alchemist", "author": "Paulo Coelho", "price": 12.99, "in_stock": True},
  {"title": "1984", "author": "George Orwell", "price": 9.99, "in_stock": True}
]
new_book ={"title": "Atomic Habits", "author": "James Clear", "price": 14.99, "in_stock": True}

with open("inventory.json","w") as file:
    json.dump(books,file,indent=4)
#print("Books Saved!")

with open("inventory.json","r") as file:
    inventory = json.load(file)
#print(inventory)

inventory.append(new_book)

with open("inventory.json","w") as file:
    json.dump(inventory,file,indent = 4)
#print("book upadted")

with open("inventory.json","r") as file:
    inventory = json.load(file)
    for Updated_books in inventory:
        print(f"Title:{Updated_books['title']} | Author: {Updated_books['author']} | Price: ${Updated_books['price']} ")
