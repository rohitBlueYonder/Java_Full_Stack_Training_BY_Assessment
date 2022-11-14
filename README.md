
Services and Their Port Nos: <br>

1. Eureka Server     : 8761
2. Token Sevice      : 8080
3. Admin Service     : 8081
4. Consumer Service  : 8082
5. ShopMgmt Service  : 8083
6. Shop Service      : 8084


---

Instances which are registered with the Eureka Server:\n
![Screenshot (927)](https://user-images.githubusercontent.com/112845470/201756666-768330e0-4568-4099-89ec-333a00db51b0.png)

------

POSTMAN LINK: <br>
https://www.getpostman.com/collections/62e03a70f43f02118d11

--------------

API END-POINTS: <br>

1) ADMIN SERVICES: <br>

1.1)SIGNUP: <br>

Method: POST <br>
Endpoint: http://localhost:8081/user/signup<br>
Payload:<br>
{
"username" : "Anuj",
"password" : "1234",  
"password_confirm" : "1234",
"email": "anuj@gamil.com"
}

<br>
1.2) LOGIN:<br>

Method: POST<br>
Endpoint: http://localhost:8081/user/login<br>
Payload:<br>
{
"username" : "Anuj",
"password": "1234"
}
<br>

1.3) GET-USERS:<br>

Method: GET<br>
Endpoint: http://localhost:8081/user/get-users<br>

-----------

2) SHOP SERVICES:<br>

2.1) GET-PRODUCTS:<br>

Method: GET<br>
Endpoint: http://localhost:8084/shop/products<br>

2.2) GET-PRODUCTS-BY-FIELD:<br>

Method: POST<br>
Endpoint: http://localhost:8084/shop/products<br>
Payload:<br>
{
"description": "19 KG"
}
<br>
2.3) GET-CATEGORIES:<br>

Method: GET<br>
Endpoint: http://localhost:8084/shop/categories<br>


2.4) GET-CATEGORIES-BY-FIELD:<br>

Method: POST<br>
Endpoint: http://localhost:8084/shop/categories<br>
Payload:<br>
{
"description": "Clothes"
}
<br>
--------------

3) CONSUMER SERVICES: (TOKEN REQUIRED)<br>

3.1) CATEGORIES:<br>

3.1.1) GET categories:<br>
Method: GET<br>
Endpoint: http://localhost:8082/consumer/shop-management/categories<br>

3.1.2) ADD category<br>
Method: POST<br>
Endpoint: http://localhost:8082/consumer/shop-management/add-category<br>
PAYLOAD :<br>
{
"name": "Automobiles",
"description": "Auto Related"
}
<br>
3.1.3) UPDATE category by ID<br>

Method: POST<br>
Endpoint: http://localhost:8082/consumer/shop-management/update-category-by-id/{id}<br>
PAYLOAD :<br>
{
"name" : "Clothing"
}
<br>
3.1.4) DELETE category by ID<br>
Method: DELETE<br>
Endpoint: http://localhost:8082/consumer/shop-management/delete-category-by-id/{id}<br>

3.2) PRODUCTS:<br>

3.2.1) GET Products<br>
Method: GET<br>
Endpoint: http://localhost:8082/consumer/shop-management/products<br>

3.2.2) ADD PRODUCT<br>
Method: POST<br>
Endpoint: http://localhost:8082/consumer/shop-management/add-product<br>
PAYLOAD :<br>
{
"name": "Nike Shirt",
"price" : "6000",
"description": "RED M"
}<br>

3.2.3) LINK PRODUCT WITH CATEGORY<br>
METHOD: PUT<br>
Endpoint: http://localhost:8082/consumer/shop-management/product-with-category/{product_id}/{category_id}<br>

3.2.4) UPDATE PRODUCT by ID<br>
Method: POST<br>
Endpoint: http://localhost:8082/consumer/shop-management/update-product-by-id/{id}<br>
PAYLOAD :<br>
{
"price" : 12000
}<br>
allowed fields: description OR name OR id OR price<br>

3.2.5)  DELETE PRODUCT by ID<br>
Method: DELETE<br>
Endpoint: http://localhost:8082/consumer/shop-management/delete-product-by-id/{id}<br>

------
