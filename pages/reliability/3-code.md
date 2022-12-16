<StandardTab choosen="reliability" />

<div class="my-4"></div>

<div class="flex items-end space-x-5">
  <h6>Code Implementation</h6>
  <span class="text-sm text-gray-400">Testing</span>
</div>

<div class="h-96 overflow-y-auto my-4">
```ts {5-14|5|6|9|11-13|16-30|16|28,29|32-43|32|41,42|45-56|54,55|58|58-69|67,68|71-91|72-77|80-84|86-91}
import request from "supertest";
import { createApp } from "@src/app.js";

describe("end to end testing", () => {
  it("registration failed - email and password is required", async () => {
    const data = {}
    const app = await createApp();
    
    const response = await request(app).post("/v1/register", data);
    
    expect(response.statusCode).toBe(422);
    expect(response.error.errors.email).toBe('email is required');
    expect(response.error.errors.password).toBe('password is required');
  });
 
  it("registration failed - email already exists in database", async () => {
    const data = {
      email: 'johndoe@example.com',
      password: 'mypassword123!@#'
    }
    const app = await createApp();

    // call registration endpoint twice with same email
    // second call should failed
    await request(app).post("/v1/register", data);
    const response = await request(app).post("/v1/register", data);
    
    expect(response.statusCode).toBe(422);
    expect(response.error.errors.email).toBe('email already exists in database');
  });
 
  it("registration failed - password validation failed with password length less than 8 digit", async () => {
    const data = {
      email: 'johndoe@example.com',
      password: 'mypass'
    }
    const app = await createApp();
    
    const response = await request(app).post("/v1/register", data);
    
    expect(response.statusCode).toBe(422);
    expect(response.error.errors.password).toBe('password should have greater than or equal to 8 digit');
  });
  
  it("registration failed - password validation failed with password not contains alphanumeric", async () => {
    const data = {
      email: 'johndoe@example.com',
      password: 'mypass-abcdefg'
    }
    const app = await createApp();
    
    const response = await request(app).post("/v1/register", data);
    
    expect(response.statusCode).toBe(422);
    expect(response.error.errors.password).toBe('password should contains alphanumeric');
  });
  
  it("registration failed - password validation failed with password not contains symbol", async () => {
    const data = {
      email: 'johndoe@example.com',
      password: 'mypass12345678'
    }
    const app = await createApp();
    
    const response = await request(app).post("/v1/register", data);
    
    expect(response.statusCode).toBe(422);
    expect(response.error.errors.password).toBe('password should have symbol');
  });

  it("registration success", async () => {
    const data = {
      firstName: 'John',
      lastName: 'Doe',
      email: 'johndoe@example.com',
      password: 'mypassword123!@#'
    }
    const app = await createApp();
    
    // expect response from api call
    const response = await request(app).post("/v1/register", data);
    expect(response.statusCode).toBe(201);
    expect(response.data).toHaveProperty('_id');
    expect(response.data._id).toBeNotNull();

    // expect inserted database collection
    const insertedUser = await db.find({id: response.data._id})
    expect(insertedUser.firstName).toBe(data.firstName)
    expect(insertedUser.lastName).toBe(data.lastName)
    expect(insertedUser.email).toBe(data.email)
    expect(insertedUser.password).toBe(data.password)
  });
});
```
</div>

<!--
Time: 27:00

- cara baca testing
- mindset untuk memahami delivery expectation
-->