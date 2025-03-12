# Reflection on Practical 1 : API Design and Implementation

## What I Learned
This practical work was a fantastic learning experience. Here are some key takeaways:
- **RESTful Design**: I now have a better understanding of how to design RESTful APIs. I learned how to structure endpoints, use HTTP methods correctly, and follow best practices for URI design.
- **Error Handling**: I implemented custom error handling for the first time. It was interesting to see how middleware can catch errors and return consistent responses.
- **Pagination**: Adding pagination was a new challenge for me. I learned how to use query parameters to control the amount of data returned in each response.
- **Content Negotiation**: I explored how to support multiple response formats (JSON and XML) based on the client's preferences. This was a bit tricky, but it was rewarding to see it work.

---

## Challenges Faced
While working on this project, I encountered a few challenges:
1. **Content Negotiation**: Implementing XML responses was tricky because I had to convert JSON objects to XML format. I spent some time researching how to do this and eventually wrote a function to handle the conversion.
   - **Solution**: I created middleware that checks the `Accept` header and formats the response accordingly. For XML, I wrote a function to convert JSON objects to XML strings.

2. **Error Handling**: At first, I wasn’t sure how to handle errors properly. I wanted to make sure the API returned meaningful error messages and status codes.
   - **Solution**: I created a custom error handler middleware that catches errors and sends consistent error responses with appropriate status codes.

3. **Pagination**: Implementing pagination required careful calculation of start and end indices. I had to think through how to handle edge cases, like when there are no more pages to display.
   - **Solution**: I used query parameters (`page` and `limit`) to calculate the correct slice of data to return. I also added pagination metadata in the response, like `next` and `prev` links.

---

## What I Enjoyed
- **Building Something Real**: It was satisfying to build an API that mimics a real-world social media platform. I enjoyed thinking through the design and seeing it come to life.
- **Problem Solving**: I liked tackling challenges like content negotiation and pagination. It felt rewarding to find solutions and see them work.
- **Documentation**: Creating the API documentation was fun. It made me appreciate how important clear documentation is for developers who use APIs.

---

## Screenshots
Here are some screenshots of the API in action:

1. **Listing Users with Pagination**:
   ![List Users](/Practical1_API_Design_and_Implementation/screenshots/users.png)

2. **Creating a New User**:
   ![Create User](/Practical1_API_Design_and_Implementation/screenshots/create.png)
