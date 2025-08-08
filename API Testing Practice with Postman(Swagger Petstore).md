		API Testing Practice with Postman(Swagger Petstore)

I created four requests with positive and four with negative scenarios using the REST API in Postman for the Swagger Petstore ([https://petstore.swagger.io/](https://petstore.swagger.io/)).

[https://www.postman.com/workspace-7057/qa-workspace/collection/78mu26d/domaci5?action=share\&source=copy-link\&creator=35180535](https://www.postman.com/workspace-7057/qa-workspace/collection/78mu26d/domaci5?action=share&source=copy-link&creator=35180535)

| Test case name | Type of request | Scripts |
| :---: | :---: | ----- |
| getPet | GET | pm.**test**("Status code is 200", **function** () {   pm.response.to.have.status(200); }); pm.**test**("Response time is less than 500ms", **function** () {     pm.expect(pm.response.responseTime).to.be.below(500); });  |
| addPet | POST | \-pm.**test**("Response time is less than 400ms", **function** () {     pm.expect(pm.response.responseTime).to.be.below(400); }); \-pm.**test**("Status code is 200", **function** () {     pm.response.to.have.status(200); });  |
| addPetEmptyBody | POST | \-pm.**test**("Status code is 200", **function** () {     pm.response.to.have.status(200); }); \-pm.**test**("Response time is less than 200ms", **function** () {     pm.expect(pm.response.responseTime).to.be.below(200); }); \-pm.**test**("Should return 400 or validation error for empty body", **function** () {     pm.expect(pm.response.code).to.be.oneOf(\[400, 422, 500\]);});    |
| invalidGetPet | GET | \-pm.**test**("Status code is 404", **function** () {     pm.response.to.have.status(404); }); \-pm.**test**("ID exists in response", **function** () {     pm.expect(jsonData).to.have.property("id"); });  |
| putSold | PUT | \-pm.**test**("Status code is 200", **function** () {     pm.response.to.have.status(200); }); \-pm.**test**("Response time is less than 400ms", **function** () {     pm.expect(pm.response.responseTime).to.be.below(400); });   |
| invalidIDPut | PUT | \-pm.**test**("Status code is 200", **function** () {     pm.response.to.have.status(200); }); \-pm.**test**("Body matches string", **function** () {     pm.expect(pm.response.text()).to.include("string\_you\_want\_to\_search"); }); \-pm.**test**("Should return 400 for invalid ID type", **function** () {     pm.response.to.have.status(400); });   |
| deletePet | DELETE | \-pm.**test**("Status code is 200", **function** () {     pm.response.to.have.status(200); }); \-pm.**test**("Response time is less than 400ms", **function** () {     pm.expect(pm.response.responseTime).to.be.below(400); });   |
| invalidPetIDDelete | DELETE | \-pm.**test**("Status code is 200", **function** () {     pm.response.to.have.status(200); }); \-pm.**test**("Response time is less than 200ms", **function** () {     pm.expect(pm.response.responseTime).to.be.below(200); }); \-pm.**test**("Should return 400 for invalid ID type", **function** () {     pm.response.to.have.status(400); });   |

