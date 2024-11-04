   # Mongodb exercise 01
## 1. Create a Database called movies?

 use movies

 ## 2. Create a collection called moviedetails?
    db.createCollection("moviedetails")

 ## 3. Create above 5 movie documents into a moviedetails collection?
    
        db.createCollection("moviesdetails")
    { ok: 1 }
    db.moviesdetails.insertMany([
    ... { "title": "Vettaiyan", "genre": "Drama", "director": "Lokesh Kanakaraj", "release_year": 2022 },
    ... { "title": "Thunivu", "genre": "Action", "director": "Gnanavel", "release_year": 2024 },
    ... { "title": "Kanguva", "genre": "Fantasy", "director": "Siva", "release_year": 2025 },
    ... { "title": "Kaithi", "genre": "Thriller", "director": "Lokesh Kanakaraj", "release_year": 2023 },
    ... { "title": "Leo", "genre": "Action", "director": "Lokesh Kanakaraj", "release_year": 2023 },
    ... { "title": "Vidamuyarchi", "genre": "Thriller", "director": "Magizh Thirumeni", "release_year": 2025 }
    ... ])

## 4. List all documents created?
 db.moviesdetails.find()


## 5. List Lokesh Kanakaraj’s movies?
 db.moviesdetails.find({ "director": "Lokesh Kanakaraj" })

## 6. List Lokesh Kanakaraj’s movies released in 2023 ?
db.moviesdetails.find({ "director": "Lokesh Kanakaraj", "release_year": 2023 })
 
## 7. Delete the movie which you don’t like?
 db.moviesdetails.deleteOne({ "title": "Vettaiyan" })
{ acknowledged: true, deletedCount: 1 }


## 8. Add the movie which is your favourite?
 db.moviesdetails.insertOne({
  "title": "Inception",
  "genre": "Sci-Fi",
  "director": "Christopher Nolan",
  "release_year": 2010
})


## 9. List movie Directed by Magizh Thirumeni in 2025?

 db.moviesdetails.find({ "director": "Magizh Thirumeni", "release_year": 2025 })


## 10. List out the Director’s Name in your document?
 db.moviesdetails.distinct("director")








