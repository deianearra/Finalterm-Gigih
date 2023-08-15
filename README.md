# Finalterm-Gigih
 
# Tokopedia Play Clone

## Description

This project aims to create a clone of Tokopedia Play, a platform for watching videos related to products. Users can view videos, products, comments, and interact with the content.

## Features

- Home Page with video thumbnails from YouTube
- Video Detail Page with embedded YouTube video, product list, comments, and comment submission form
- Comment section for users to interact
- Real-time update of comments using WebSocket (Bonus Feature)
- User profile picture and username display (Bonus Feature)
- Search feature for easy navigation (Bonus Feature)

## How to Install & Run

1. Clone this repository to your local machine.
2. Install Node.js and npm if not already installed.
3. Install project dependencies using the command:
npm install

sql
Copy code
4. Set up a MongoDB database with appropriate collections (videos, products, comments).
5. Create a `.env` file and add your MongoDB URI:
MONGODB_URI=your_mongodb_uri_here

markdown
Copy code
6. Start the server:
npm start

vbnet
Copy code
7. Open your browser and navigate to `http://localhost:3000` to access the app.

## Schema Database

The MongoDB database consists of three collections:
- Videos: Stores video information including videoID, thumbnailUrl, and title.
- Products: Stores product information associated with videos, including productID, link, title, and price.
- Comments: Stores user comments on videos, including username, comment, timestamp, and videoID.

## API Structure

- `GET /videos`: Get a list of videos with their details.
- `GET /videos/:id`: Get details of a specific video by ID.
- `POST /videos`: Save a new video to the database.
- `GET /product/:id`: Get the product list associated with a video.
- `GET /comment/:id`: Get comments for a specific video.
- `POST /comment/:id`: Submit a new comment for a video.

## Bonus Feature: Real-time Comments

This app uses WebSocket to provide real-time updates for the comments section. When a new comment is added, all connected clients receive the update instantly.

## Bonus Feature: User Profile Display

The user's profile picture and username are displayed on the top right corner of the page, enhancing the user experience.

## Bonus Feature: Search

The search feature allows users to easily find videos by title or content, improving content discoverability.

---

Feel free to customize this README according to your project's specifics. For more information on formatting README files, you can refer to [makeareadme.com](https://www.makeareadme.com/).
Replace placeholders like your_mongodb_uri_here with your actual MongoDB URI, and ensure that the structure and content of the README suit your project's details.
