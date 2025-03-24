# Practical 1 : API Design and Implementation

## Overview
In this practical work, I designed and implemented a RESTful API for a social media platform similar to Instagram. The goal was to create endpoints for managing resources like users, posts, comments, likes, and followers. The API follows RESTful principles, uses proper HTTP methods, and includes features like pagination, error handling, and content negotiation.

---

## Objectives
1. **Design RESTful API Endpoints**: Create clean and meaningful URIs for each resource.
2. **Implement CRUD Operations**: Build endpoints to list, create, update, and delete resources.
3. **Handle Errors Gracefully**: Implement error handling for cases like missing resources or unauthorized access.
4. **Add Pagination**: Support pagination for listing large datasets.
5. **Content Negotiation**: Allow the API to respond in both JSON and XML formats based on the client's preference.
6. **Document the API**: Create a simple HTML documentation page to describe the API endpoints.

---

## Steps Taken

### 1. Project Setup
I started by setting up a Node.js project using Express. Here's what I did:
- Created a new folder for the project and initialized it with `npm init`.
- Installed necessary dependencies like `express`, `morgan`, `cors`, and `helmet`.
- Set up a basic project structure with folders for `controllers`, `routes`, `middleware`, and `utils`.
- Created a `.env` file to store environment variables like the server port.

### 2. Designing the API
I designed endpoints for the following resources:
- **Users**: Manage user profiles (e.g., create, update, delete).
- **Posts**: Handle posts made by users.
- **Comments**: Allow users to comment on posts.
- **Likes**: Let users like posts.
- **Followers**: Manage user follow relationships.

For each resource, I created endpoints for listing, retrieving, creating, updating, and deleting items. For example:
- `GET /users` - List all users.
- `POST /users` - Create a new user.
- `PUT /users/{id}` - Update a user's profile.

### 3. Implementing the API
I used Express to implement the API. Here's a breakdown of the implementation:
- **Controllers**: I created controllers for each resource to handle the logic for CRUD operations.
- **Routes**: I set up routes to map HTTP methods to the appropriate controller functions.
- **Middleware**: I added middleware for error handling, content negotiation, and request logging.
- **Mock Data**: Since I didn’t use a real database, I created mock data in `utils/mockData.js` to simulate user and post data.

### 4. Adding Features
- **Pagination**: For listing resources, I added pagination using query parameters like `page` and `limit`.
- **Error Handling**: I created a custom error handler to return meaningful error messages and status codes.
- **Content Negotiation**: I added support for both JSON and XML responses based on the `Accept` header.

### 5. Documenting the API
I created a simple HTML documentation page (`public/docs.html`) to describe the API endpoints, including examples of requests and responses.



