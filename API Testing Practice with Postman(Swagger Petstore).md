		API Testing Practice with Postman(Swagger Petstore)

I created four requests with positive and four with negative scenarios using the REST API in Postman for the Swagger Petstore ([https://petstore.swagger.io/](https://petstore.swagger.io/)).

[https://www.postman.com/workspace-7057/qa-workspace/collection/78mu26d/domaci5?action=share\&source=copy-link\&creator=35180535](https://www.postman.com/workspace-7057/qa-workspace/collection/78mu26d/domaci5?action=share&source=copy-link&creator=35180535)

| Test case name | Type of request | Scripts |
| :---: | :---: | ----- |
| getPet | GET | \-Status code is 200  \-Response time is less       than 500ms |
| addPet | POST | \-Status code is 200  \-Response time is less       than 400ms |
| addPetEmptyBody | POST | \-Status code is 200 \-Response time is less than 200ms | AssertionError: expected 360 to be below 200 \-Should return 400 or validation error for empty body | AssertionError: expected 200 to be one of \[ 400, 422, 500 \]   |
| invalidGetPet | GET | \-Status code is 404 \-ID exists in response | AssertionError: expected { code: 1, type: 'error', …(1) } to have property 'id' |
| putSold | PUT | \-Status code is 200 \-Response time is less than 400ms  |
| invalidIDPut | PUT | \-Status code is 200 | AssertionError: expected response to have status code 200 but got 404 \-Body matches string | AssertionError: expected '{"code":1,"type":"error","message":"P…' to include 'string\_you\_want\_to\_search' \-Should return 400 for invalid ID type | AssertionError: expected response to have status code 400 but got 404  |
| deletePet | DELETE | \-Status code is 200 \-Response time is less than 400ms  |
| invalidPetIDDelete | DELETE | \-Status code is 200 | AssertionError: expected response to have status code 200 but got 404 \-Response time is less than 200ms | AssertionError: expected 498 to be below 200 \-Should return 400 for invalid ID type | AssertionError: expected response to have status code 400 but got 404  |

