## Aggregation and filtering - for future reference

```javascript
db.posts.aggregate([
  // $match stage, to match only one user, for example by name
  {
    "$match" : { user: "maciek" }
  },
  // $project, to project all the fields that I need (user and numbers - numbers are going to filtered)
  {
    "$project": {
      "user": 1,
      "numbers": {
        $filter: {
          input: "$numbers",
          as: "num",
          cond: {
            "$and": [
              {
                $gte: [ "$$num.value", 2],
              },
              {
                $lte: [ "$$num.value", 3]
              }
            ]
          }
        } 
      }
    }
  }
]).pretty()
```

Resources that helped a lot:
* [Exactly what I was looking for](https://studio3t.com/knowledge-base/articles/filter-elements-from-mongodb-arrays/)
* [filter](https://docs.mongodb.com/manual/reference/operator/aggregation/filter/index.html)
* [aggregation](https://docs.mongodb.com/manual/aggregation/)
