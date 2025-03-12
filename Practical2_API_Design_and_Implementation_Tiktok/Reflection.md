# Reflection on Practical 2 : API Design and Implementation (Tiktok)

## What I Learned
This practical work was a fantastic learning experience. Here are some key takeaways:
- **RESTful Design**: I now have a better understanding of how to design RESTful APIs. I learned how to structure endpoints, use HTTP methods correctly, and follow best practices for URI design.
- **Error Handling**: I implemented custom error handling for the first time. It was interesting to see how middleware can catch errors and return consistent responses.
- **Relationships Between Resources**: I explored how to manage relationships between resources, such as users liking videos or following other users. This was a new challenge, but it helped me understand how to model real-world scenarios in an API.
- **Testing**: I learned how to test APIs using `curl` commands, which was a useful skill for verifying that my endpoints worked as expected.

---

## Challenges Faced
While working on this project, I encountered a few challenges:
1. **Managing Relationships**: Implementing features like likes and followers was tricky because I had to ensure that relationships were properly maintained between users, videos, and comments.
   - **Solution**: I used arrays to store likes and followers in the mock data and added logic to handle adding and removing relationships.

2. **Error Handling**: At first, I wasn’t sure how to handle errors properly. I wanted to make sure the API returned meaningful error messages and status codes.
   - **Solution**: I created a custom error handler middleware that catches errors and sends consistent error responses with appropriate status codes.

3. **Validation**: Ensuring that required fields were provided in requests was a challenge, especially for complex operations like creating a video or following a user.
   - **Solution**: I added basic validation in the controllers to check for required fields and return errors if they were missing.

---

## What I Enjoyed
- **Building Something Real**: It was satisfying to build an API that mimics a real-world social media platform. I enjoyed thinking through the design and seeing it come to life.
- **Problem Solving**: I liked tackling challenges like managing relationships and implementing error handling. It felt rewarding to find solutions and see them work.
- **Testing**: Testing the API with `curl` commands was fun and gave me confidence that my endpoints worked as expected.

