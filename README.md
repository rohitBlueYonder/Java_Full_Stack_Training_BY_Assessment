
Services and Their Port Nos:

1. Eureka Server     : 8761
2. Token Sevice      : 8080
3. Admin Service     : 8081
4. Consumer Service  : 8082
5. ShopMgmt Service  : 8083
6. Shop Service      : 8084




Instances which are registered with the Eureka Server:\n
![Screenshot (927)](https://user-images.githubusercontent.com/112845470/201756666-768330e0-4568-4099-89ec-333a00db51b0.png)

POSTMAN LINK:
https://www.getpostman.com/collections/62e03a70f43f02118d11


API END-POINTS:

1) ADMIN SERVICES:

1.1)SIGNUP:

Method: POST
Endpoint: http://localhost:8081/user/signup
Payload:
{
"username" : "Anuj",
"password" : "1234",  
"password_confirm" : "1234",
"email": "anuj@gamil.com"
}


1.2) LOGIN:

Method: POST
Endpoint: http://localhost:8081/user/login
Payload:
{
"username" : "Anuj",
"password": "1234"
}


1.3) GET-USERS:

Method: GET
Endpoint: http://localhost:8081/user/get-users

---------------------------------------------------------------------------

2) SHOP SERVICES:

2.1) GET-PRODUCTS:

Method: GET
Endpoint: http://localhost:8084/shop/products

2.2) GET-PRODUCTS-BY-FIELD:

Method: POST
Endpoint: http://localhost:8084/shop/products
Payload:
{
"description": "19 KG"
}

2.3) GET-CATEGORIES:

Method: GET
Endpoint: http://localhost:8084/shop/categories


2.4) GET-CATEGORIES-BY-FIELD:

Method: POST
Endpoint: http://localhost:8084/shop/categories
Payload:
{
"description": "Clothes"
}


-------------------------------------------------------------------------
3) CONSUMER SERVICES: (TOKEN REQUIRED)

3.1) CATEGORIES:

3.1.1) GET categories:
Method: GET
Endpoint: http://localhost:8082/consumer/shop-management/categories

3.1.2) ADD category
Method: POST
Endpoint: http://localhost:8082/consumer/shop-management/add-category
PAYLOAD :
{
"name": "Automobiles",
"description": "Auto Related"
}

3.1.3) UPDATE category by ID
Method: POST
Endpoint: http://localhost:8082/consumer/shop-management/update-category-by-id/2
PAYLOAD :
{
"name" : "Clothing"
}

3.1.4) DELETE category by ID
Method: DELETE
Endpoint: http://localhost:8082/consumer/shop-management/delete-category-by-id/1

3.2) PRODUCTS:

3.2.1) GET Products
Method: GET
Endpoint: http://localhost:8082/consumer/shop-management/products

3.2.2) ADD PRODUCT
Method: POST
Endpoint: http://localhost:8082/consumer/shop-management/add-product
PAYLOAD :
{
"name": "Nike Shirt",
"price" : "6000",
"description": "RED M"
}

3.2.3) LINK PRODUCT WITH CATEGORY
METHOD: PUT
Endpoint: http://localhost:8082/consumer/shop-management/product-with-category/{product_id}/{category_id}

3.2.4) UPDATE PRODUCT by ID
Method: POST
Endpoint: http://localhost:8082/consumer/shop-management/update-product-by-id/{id}
PAYLOAD :
{
"price" : 12000
}
allowed fields: description OR name OR id OR price

3.2.5)  DELETE PRODUCT by ID
Method: DELETE
Endpoint: http://localhost:8082/consumer/shop-management/delete-product-by-id/{id}


---------------------------------------------------------------------------------------------------	
