# Openhaus_QA
Manual and Unit Testing Showcase


# Manual and Unit Testing Portfolio  
This repository highlights my work in manual testing, unit testing, and API validation using tools like PHPUnit and Postman. These examples demonstrate my ability to test APIs, validate responses, and ensure software quality.


## Project Overview  

In my previous role, I worked on a project involving robust testing methodologies for software applications. Below are the highlights of my contributions:  
- **API Testing**: Created and executed test cases for RESTful APIs using Postman.  
- **Unit Testing**: Wrote PHPUnit test cases to ensure backend code reliability.  
- **Manual Testing**: Verified software functionalities and identified bugs during the development phase.  

---

## Highlights  

### 1. **API Testing with Postman**  
- Tested multiple endpoints for functionality, error handling, and performance.  
- Verified response codes, response bodies, and headers.  
- Below is an example of an API testing process:  
Request: GET ```/api/v1/allprojectsv2```
**Response:**
```json
{
    "status": 1,
    "message": "Successful",
    "data": {
        "projects": [
            {
                "id": 1,
                "project_code": "prescon-mahim-01",
                "project_name": "Prescon Miracle Bay",
                "building_info": [1],
                "apartment_type_info": ["XX01", "XX02", "XX03", "XX04"]
            }
        ]
    }
}
```
**Explanation:**

Purpose: This API fetches project details.
Sample Data:
project_code: Unique identifier for the project.
building_info: Details about the buildings in the project.
apartment_type_info: Available apartment types.
 

---

### 2. **Unit Testing with PHPUnit**  
- Created comprehensive test cases to validate backend API logic.  
- Ensured code reliability by asserting expected outputs and responses.  
- Sample test case:  
 unit test written in PHPUnit
```php
public function test_allprojectsv2() {
    $response = $this->getJson('/api/v1/allprojectsv2');
    $response->assertStatus(200)
             ->assertJsonPath('status', 1)
             ->assertJsonPath('message', 'Successful')
             ->assertJsonPath('data.projects.project_code', 'prescon-mahim-01');
}
```
**Explanation:**

Purpose: This test checks the ```/api/v1/allprojectsv2``` endpoint.
Assertions:
The status code of the response is 200.
The status in the JSON response is 1.
The message is "Successful".
The project_code in the returned data matches the expected value (prescon-mahim-01).
 

---

### 3. **Manual Testing**  
- Conducted manual tests to identify issues not covered by automated testing.  
- Verified user flows and edge cases to ensure a seamless user experience.

Here’s a description of a manual test case for validating the same API:

Test Case Name: Verify Project API Response
Steps:
Send a GET request to ```/api/v1/allprojectsv2```.
Verify the response status code is 200.
Validate that the status field in the response is 1.
Check that the project_code is "prescon-mahim-01".
Expected Result:
Response matches the structure and values as shown in the example response. 

---

## Tools and Technologies  
- **Postman**: For API testing and test automation.  
- **PHPUnit**: For writing and running unit tests.  
- **Visual Studio Code**: For test script development.  

---
## Conclusion
This repository demonstrates my testing expertise, focusing on:

Writing automated test cases.
Verifying API endpoints for correctness and reliability.
Documenting detailed manual testing workflows.

