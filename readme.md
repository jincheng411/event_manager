# Event Manager Company: Software QA Analyst/Developer Onboarding Assignment

### Docker image on docker hub: https://hub.docker.com/repository/docker/jincheng411/event-manager/general

Through this project, I gained deeper technical insights into implementing docker containerization technology to develop REST API using Python, fastAPI, Docker, Postgres, and pgadmin. I learned how to effectively use Pydantic's @validator to enforce complex rules within models, which helped me understand how validation logic can be seamlessly integrated with API request handling in FastAPI applications. The experience of writing comprehensive test cases using pytest enhanced my ability to approach software development with a test-driven mindset, ensuring that every aspect of the password validation logic was verified for different edge cases and potential vulnerabilities.

One of the primary challenges I faced was integrating the password validation logic into an existing codebase without disrupting other components. This assignment has reinforced my understanding of secure coding practices, the importance of thorough testing, and the value of collaborative problem-solving in software development.

### Issue 1: Tests failed in test_user_schemas 
The user_base_data was missing the nickname and first name it caused a key error, fixed it by adding those fields in the fixture

[See the issue](https://github.com/jincheng411/event_manager/issues/1)

### Issue 2: Tests failed in test_service.py
Test failed because of missing credentials for SMTP server, use dotenv to add them to setting and pass the test cases

[See the issue](https://github.com/jincheng411/event_manager/issues/3)

### Issue 3: Test failed due to missing token 
Tests failed due to missing access token, create method to generate tokens for them

[See the issue](https://github.com/jincheng411/event_manager/issues/5)

### Issue 4: The password is not meet the standard
Password is not meet the standard due to lack of constraint, add the constraint in the model.

[See the issue](https://github.com/jincheng411/event_manager/issues/7)

### Issue 5: The first registered user should be Admin
Instead of authenticated role, the user role should be Admin since it is the first user in the database
[See the issue](https://github.com/jincheng411/event_manager/issues/12)

### Issue 6: Not able to update user's is_professional field 
Use PUT /USER, add "is_professional": true then execute, the is_professinal still false in the database
[See the issue](https://github.com/jincheng411/event_manager/issues/14)
