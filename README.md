
# MongoDB_Tutorial

**MongoDB** is a *NoSQL* document database. It can store large amount of data in a type of JSON format (key-value pairs.) called BSON.

NoSQL : Not Only Structured Query Language.

![02](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/4e19ca91-0366-432c-86f3-c850fdcd0ba2)  ![03](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/87dcd780-188d-40eb-8af0-ce0edb48abe1)



## How NoSQL Could Be Better Than RDMS?

- In **RDMS** when data is needed, it is **queried from multiple tables** to join the data back together. Use of **JOINS** could be **expensive**. In **NoSQL** Excessive JOINS can be avoided by saving data in nested structures and Arrays 

-  **Input/Output operations are less costly** due to support of embedded documents(nested documents) 
   - Consider a user Documemt in Users schema. One user might have additional fields like "age," "address," or "phone number," while another user might not have these fields at all. This flexibility can be beneficial when dealing with evolving or dynamic data, as you can **easily add or remove fields as needed without altering the entire collection's schema.**

![01](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/ba57afd0-0ca4-43ab-b7ae-71a35f6e0e02)

- MongoDB is that it is a schema-less database. No schema migrations anymore. 

## MongoDb And RDBMS Terminology

![04](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/87290755-06c8-417a-808a-87a7c55c8001)

## Database 
- MongoDB consists of a set of databases.
- Database in MongoDB is nothing but a container for collections. 

![07](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/add9b4b5-8e12-4634-ae6f-6492b8e16445)

## Collections 
- Collection is a group of MongoDB documents.

![06](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/b1f1ef90-5d02-4837-bfc3-494df71db92f)


## Documents 
- Documents within a collection in MongoDB can have different structures and fields.

![05](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/a0e443c3-f1ac-409d-9ace-cdb73c90bbbf)

### What do you mean by "MongoDB has Dynamic Schema" ?
Schema design determines the way an application handles its data. With traditional relational databases, you must define your schema before you can add any data. 
This inflexibility means you can’t change your schema as your data, application requirements or business evolves.

MongoDB allows you to insert data without a predefined schema.

For example : Consider a collection named "products" that stores information about different products. 
![09](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/97e2dcf2-e17a-4591-8644-43f7f7e91a88)

![10](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/7beb0ecd-dbfc-465f-942a-66213383aa6e)

Both documents belong to the "products" collection, but they have different sets of fields.

Therfore,The collection can store products with varying attributes without requiring a uniform schema across all documents.



### Primary Key 

![11](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/861456b7-48ec-4c54-971f-7f5efdacb7d9)

- In above figure, field  "_id" represents the primary key identifier of the given document. 
- _id is a 12 bytes hexadecimal number which assures the uniqueness of every document
-  These 12 bytes first 4 bytes for the current timestamp, next 3 bytes for machine id, next 2 bytes for process id of MongoDB server and remaining 3 bytes are simple incremental VALUE.


## Comparision With RDBMS

![04](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/1036e5c6-b0f9-42fd-b751-b7299e9b929f)


## Data Modelling
There are 2 ways in which the relationships between the data can be established in MongoDB:

- Embedded Documents
Embedded documents capture relationships between data by storing related data in a single document structure. MongoDB documents make it possible to embed document structures in a field or array within a document. These denormalized data models allow applications to retrieve and manipulate related data in a single database operation.

![14](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/ac2a8d0e-9b33-4d1d-86b6-12b6c541a918)

- Reference Documents
References store the relationships between data by including links or references from one document to another. Applications can resolve these references to access the related data. Broadly, these are normalized data models.

Ex :
- Users Collection
```
{
  "_id": ObjectId("user1"),
  "name": "John Doe",
  "email": "john@example.com"
}
```

- Posts Collection ( references Users Collections)

```
{
  "_id": ObjectId("post1"),
  "title": "My First Post",
  "content": "This is the content of my first post.",
  "user_id": ObjectId("user1")
}
```

### DataTypes In MongoDb

![datatypes](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/3c8edcc1-2755-43c6-89df-a6c5a3b3f560)

## Commands In MongoDB
- ### View list Of Database
   
         show dbs
         show databases

![c01](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/6bdc7b41-ecd9-4e2d-a414-928f73376d26)

- ### Create Database / Switch To a Database : 
Create a new database if it doesn't exist, otherwise it will return the existing database.

        use database_name

![c02](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/786e7e10-49a9-420e-b2f6-ae3d2d8ee204)

- ### Drop Database
Drops Currently Connected Database

        db.dropDatabase() 

![c03](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/ce1bdf05-4894-420b-abd7-129123122e8f)

- ### Create Collections
 Name will be the name of the collection, Options is Optional

        db.createCollection(name, options)

- ### Creating a Capped Collection

![c04](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/034e4dd5-eec0-4cc3-94e1-008c367254e3)


This will create a collection named student, with maximum size of 5 megabytes and maximum of 5000 documents.

- ###  Insert data into collection

         db.collection.insert()        
    To Insert One Document into collection :

         db.COLLECTION_NAME.insertOne({document})
    
     To Insert Many Documents into collection :

         db.COLLECTION_NAME.insertMany({document1},{document2})

![insert](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/cd5cc81e-00af-4dcc-af66-090caaf06340)


- ### Read Data

        db.collection_name.find()

![readDoc](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/0eee7e3a-b9ec-4c8c-9802-ccde327eece3)

![findOne](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/a6045d17-eaf8-409a-8e8f-b8978dc29357)

Display only particular data from each documents :

![projection_displayparticularvalue](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/9cb353eb-c4cb-4a55-9033-ae1e3856789d)

- ### Delete Operations 

![deleteOne](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/d70596bb-ecd2-4cea-89d5-d981b06d3cc9)

![deleteMany](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/4edfa417-8a90-405d-8cee-2d2b53d2a9be)

Similar to truncate of SQL :

![truncates](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/50187c3b-1d5c-4aba-984c-7b70406ddfd7)

- ### Update Operations 

![Update1](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/86aab2a4-6949-4e77-9468-89b2c79e2513)

![updateMany](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/6386b076-c47a-4ad3-b1cc-99919c16fc12)

- ### Filter (Where) Operations

- Filter Using 'In' (for list of values)

![where_in](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/3619dc8d-1602-48a2-8221-1a9670d71f16)

- Greator than equal to ($gte)

![wheregte](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/e87ed1af-3264-4722-a319-a241a3c32bb5)

-  Not equal to ($ne)

![where_notEqual](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/df07a193-0b3e-4163-82ed-e1d0b6d94b66)

- AND Operation

![and](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/e1782e2e-78ef-4500-ad77-c15b2ddb1941)

- OR Operation

![or](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/551d2aae-3c9f-4aaf-8bf8-3d04fc77d538)

### Sorting 

![ascSort](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/a5817b97-d04a-4a98-9637-424f35ac8d9e)

![desc](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/9eb2499b-0371-4095-8ffd-8bc07407a472)

### Limit 

![limit](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/ca91f68e-59a7-456d-8293-12cdd80b780c)

### Skip 

![skip](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/281cbc5c-13ee-4acb-b106-b732526c703e)

### Limit & Skip

![limitSkip-Skips1record DisplayNext2](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/ee72160c-0333-4f3a-a3a0-2e4359520f06)
