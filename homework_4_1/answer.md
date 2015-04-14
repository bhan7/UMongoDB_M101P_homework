True:
db.products.find({$and:[{price:{$gt:30}},{price:{$lt:50}}]}).sort({brand:1})
db.products.find({'brand':"GE"}).sort({price:1})

False:
db.products.find({'brand':"GE"})
db.products.find({brand:'GE'}).sort({category:1, brand:-1}).explain()