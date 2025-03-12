# Practical 2 : API Design and Implementation (Tiktok)

## Overview
In this practical work, I designed and implemented a RESTful API for a TikTok-like social media platform. The API allows users to manage videos, users, comments, likes, and followers. The project was built using Node.js and Express, with in-memory data storage for simplicity.

---

## Objectives
1. **Design RESTful API Endpoints**: Create meaningful URIs for resources like videos, users, and comments.
2. **Implement CRUD Operations**: Build endpoints to list, create, update, and delete resources.
3. **Handle Relationships**: Manage relationships between users, videos, and comments (e.g., likes, followers).
4. **Error Handling**: Implement proper error handling for invalid requests or missing resources.
5. **Testing**: Test the API using tools like Postman or `curl`.

---

## Steps Taken

### 1. Project Setup
I started by setting up a Node.js project using Express. Here's what I did:
- Created a new folder for the project and initialized it with `npm init`.
- Installed necessary dependencies like `express`, `cors`, `morgan`, and `body-parser`.
- Set up a basic project structure with folders for `controllers`, `routes`, `models`, and `middleware`.
- Created a `.env` file to store environment variables like the server port.

### 2. Designing the API
I designed endpoints for the following resources:
- **Videos**: Manage video uploads, updates, and deletions.
- **Users**: Handle user profiles, followers, and following relationships.
- **Comments**: Allow users to comment on videos and manage those comments.

For each resource, I created endpoints for listing, retrieving, creating, updating, and deleting items. For example:
- `GET /api/videos` - List all videos.
- `POST /api/videos` - Create a new video.
- `PUT /api/videos/:id` - Update a video.

### 3. Implementing the API
I used Express to implement the API. Here's a breakdown of the implementation:
- **Controllers**: I created controllers for each resource to handle the logic for CRUD operations.
- **Routes**: I set up routes to map HTTP methods to the appropriate controller functions.
- **Middleware**: I added middleware for error handling, logging, and request parsing.
- **Mock Data**: Since I didn’t use a real database, I created mock data in `src/models/index.js` to simulate video, user, and comment data.

### 4. Adding Features
- **Likes and Followers**: I implemented functionality for users to like videos and follow other users.
- **Error Handling**: I created custom error handlers to return meaningful error messages and status codes.
- **Validation**: I added basic validation to ensure required fields are provided in requests.

### 5. Testing the API
I tested the API using `curl` commands to ensure all endpoints worked as expected. For example:
- `curl -X GET http://localhost:3000/api/videos` - List all videos.
- `curl -X POST http://localhost:3000/api/videos -d '{"title": "My Video", "url": "https://example.com/video.mp4", "userId": 1}'` - Create a new video.
