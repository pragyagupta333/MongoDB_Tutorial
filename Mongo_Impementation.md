# MongoDB Practice

## 1. Find the price per night of the first record in the listingsAndReviews collection.
```

MongoPractice> db.listandreviews.findOne().price

```
![Screenshot from 2023-06-09 10-13-51](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549040/bcaacb49-6a8b-40e6-8f89-b1680cc0178f)

## 2. Retrieve the cleaning fee of the first record in the listingsAndReviews collection.

```

db.listandreviews.findOne().cleaning_fee

```
![Screenshot from 2023-06-09 10-20-42](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549040/00ba943a-185f-49e2-9dfb-90e618bd52e0)

## 3. Find the host_name, host_location, host_about of the first record in the listingsAndReviews collection.

```
db.listingsAndReviews.find().limit(1).forEach(function(doc) {
print("Host Name: " + doc.host.host_name);
print("Host Location: " + doc.host.host_location);
print("Host About: " + doc.host.host_about);
});

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/9e49bbac-311d-4e8d-8f0d-33897a780d21)

[ForEach()](https://examples.javacodegeeks.com/software-development/mongodb/mongodb-foreach-example/)
## 4. Retrieve the number of bedrooms in the first record in the listingsAndReviews collection.

```
db.listandreviews.findOne().bedrooms

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/e2c36b56-91d4-498a-bc0f-a32aba2ba32c)

## 5. Retrieve the number of guests are included in the first record in the listingsAndReviews collection.


```
db.listandreviews.findOne().guests_included

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/c9d6e00b-758c-4101-8e3d-fb6aeabf7e4d)


## 6. Write a MongoDB query to check whether the host have a profile picture in the first record in the listingsAndReviews collection.

```
db.listandreviews.findOne().host.host_has_profile_pic

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/6c10d4a6-5fbf-4824-a6bc-91056881cf8d)


## 7. Write a MongoDB query to check whether the host's identity have been verified in the first record in the listingsAndReviews collection.

```
db.listandreviews.findOne().host.host_identity_verified

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/f613a1b3-37b4-4ddf-bc06-bdd789e7581d)

## 8. Write a MongoDB query to find how many listings does the host have in the first records in the listingsAndReviews collection.

```
db.listandreviews.findOne().host.host_total_listings_count

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/cf884c78-84e7-40aa-a481-41a5dac137dc)


## 9. Write a MongoDB query to find the street address of the first record in the listingsAndReviews collection.

```
db.listandreviews.findOne().address.street

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/0e67fe1a-4a4b-4cb3-abc0-1c22c30c44e5)


## 10. Find all the listings in the listingsAndReviews collection where the property_type field is set to "House".

```
db.listandreviews.find({"property_type": "House"})

```
![image](https://github.com/pragyagupta333/MongoDB_Tutorial/assets/125549428/94d77291-da51-41a0-b0c2-04054748d5c9)


## 

```


```

## 

```


```
