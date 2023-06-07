# MongoDB Concepts (theoretical)

## Compare SQL and NoSQL Database ?

![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/54c075b9-c602-40b3-ac71-0f0c6b376725)

## How is MongoDB better than other SQL databases?

MongoDB allows a highly flexible and scalable document structure. For e.g. one data document in MongoDB can have five columns and the other one in the same collection can have ten columns. 
Also, MongoDB database are faster as compared to SQL databases due to efficient indexing and storage techniques.

## Does MongoDB support foreign key constraints?

No,In MongoDB, you can model relationships between documents using **references** or **embedding**.
[Refer Data Modelling Section For references and embedding in mongoDB](https://github.com/pragyagupta333/MongoDB_Tutorial/blob/main/Basic_Overview.md)

However, MongoDB does not enforce referential integrity or provide built-in mechanisms for maintaining or enforcing foreign key constraints.

**Reason**:

MongoDB allows for flexible schema designs where each document can have its own structure. This flexibility enables easy modification of the data model without the need to update or migrate existing records. Adding foreign key constraints would impose a rigid structure on the data, which goes against the schema-less approach.
