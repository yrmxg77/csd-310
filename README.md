# csd-310
db = client["pytech"]
collection = db["students"]
docs = collection.find({})
for doc in docs:
    print(doc)
student_doc = collection.find_one({"student_id": "1007"})
print(student_doc)
