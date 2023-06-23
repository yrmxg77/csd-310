# csd-310
import pymongo
from pymongo import MongoClient

client = MongoClient("mongodb+srv://admin:admin@cluster0.69yidqp.mongodb.net/?retryWrites=true&w=majority")
db = client["pytech"]
collection = db["students"]

# Display all documents in the collection
docs = collection.find({})

for doc in docs:
    print(doc)

# Display a single document by student_id
student_doc = collection.find_one({"student_id": "1007"})
print(student_doc)
