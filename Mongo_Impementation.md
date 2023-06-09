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


```

## 

```


```

## 

```


```
