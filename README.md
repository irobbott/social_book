# Social Media App – Capstone Project
This Django-based social media platform was built as a capstone project. The goal was to implement core features of a basic social network using Django’s built-in tools. The app focuses on user interaction through posts, likes, following, and account management.

## What the App Does
Users can:

- **Create an account** – using a signup form.
- **Log in/out** – using Django’s authentication system.
- **Upload posts** – with an image and a caption.
- **Like and unlike posts** – each user can like or unlike posts from others.
- **Follow/unfollow other users** – to build their own network.
- **View a feed** – that shows posts from users they follow.
- **Search for users** – by typing a username.
- **Edit their profile** – including profile picture, bio, and location.

---

## Core Components
### Models (models.py)
- **Profile**: Extends the default Django user to include profile picture, bio, and location.  
- **Post**: Stores image uploads, captions, timestamps, and the posting user.  
- **LikePost**: Tracks which user liked which post.  
- **FollowersCount**: Manages the follow relationship between users.

### Views (views.py)
Handles:

- Displaying feed based on followed users.
- Creating posts.
- Liking posts.
- Following/unfollowing users.
- User search.
- Profile management and settings.

### URLs (urls.py)
Maps URL routes to their corresponding views:

- `/` → homepage/feed  
- `/settings/` → update profile  
- `/upload/` → upload post  
- `/like-post` → like a post  
- `/profile/<str:pk>` → view user profile  
- `/follow` → follow/unfollow user  
- `/search` → search for users

---

## How It Works – Step by Step
1. User signs up and a `Profile` object is automatically created for them.
2. On logging in, the **feed** shows posts only from users they follow.
3. Users can:
   - Search for other users by username.
   - Visit profiles, follow/unfollow, or view all the user’s posts.
4. Users can:
   - Create posts by uploading an image and a short caption.
   - Like posts directly from the feed.
5. The **Settings** page allows users to:
   - Upload/change profile picture
   - Update bio and location
6. All media files are stored in a `media/` directory and served during development.

--

## Summary
This project demonstrates how Django can be used to build a functional social platform using its templating system, models, and view logic. It showcases practical features like user interaction, database relationships, media handling, and authentication.