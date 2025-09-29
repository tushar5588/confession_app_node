# Confession App Backend

A Node.js backend API for a confession app built with Express and MongoDB.

## Setup

1. Install dependencies:
```bash
npm install
```

2. Make sure MongoDB is running locally on port 27017

3. Start the development server:
```bash
npm run dev
```

The server will run on `http://localhost:5000`

## API Endpoints

### Posts

- **GET /posts** - Fetch all posts
- **POST /posts** - Add a new confession
  - Body: `{ "text": "Your confession here" }`

- **POST /posts/:id/like** - Like/unlike a post
  - Body: `{ "deviceId": "unique-device-id" }`

- **POST /posts/:id/comment** - Add a comment to a post
  - Body: `{ "text": "Your comment here" }`

## Database Schema

### Post Model
- `text` (String, required) - The confession text
- `likes` (Number, default: 0) - Number of likes
- `comments` (Array) - Array of comment objects
- `likedBy` (Array) - Array of device IDs that liked the post
- `createdAt` (Date, default: Date.now) - Creation timestamp

### Comment Schema
- `text` (String, required) - The comment text
- `createdAt` (Date, default: Date.now) - Creation timestamp
# confession_app_node
