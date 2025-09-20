# Movie Discovery App

A modern React-based movie discovery application that helps users find movies they'll enjoy without the hassle. Features trending movies based on search popularity and seamless movie browsing powered by The Movie Database (TMDB) API.

## 🌐 Live Demo

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20App-blue?style=for-the-badge&logo=vercel)](https://movie-app-ten-sepia-83.vercel.app/)

Try the app now - search for your favorite movies and see what's trending!

## ✨ Features

- **Smart Movie Search**: Debounced search functionality to find movies instantly
- **Trending Movies**: View the most searched movies by other users
- **Movie Details**: Display movie ratings, release year, and language information
- **Responsive Design**: Beautiful, mobile-first design with Tailwind CSS
- **Search Analytics**: Track and display trending searches using Appwrite database
- **Loading States**: Smooth loading indicators for better user experience
- **Error Handling**: Graceful error handling for API failures

## 🛠️ Tech Stack

- **Frontend**: React with Vite
- **Styling**: Tailwind CSS with custom theme
- **API**: The Movie Database (TMDB) API
- **Database**: Appwrite for search analytics
- **Hooks**: react-use for debouncing
- **Fonts**: Google Fonts (DM Sans, Bebas Neue)

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (version 16 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Environment Setup

You'll need to obtain API keys and set up the following services:

1. **TMDB API**: Get your API key
2. **Appwrite**: Set up a project

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/movie-discovery-app.git
   cd movie-discovery-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Environment Variables**
   
   Create a `.env` file in the root directory:
   ```env
   VITE_TMDB_API_KEY=your_tmdb_api_key_here
   VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
   VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
   VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
   VITE_APPWRITE_ENDPOINT=your_appwrite_endpoint
   ```

4. **Set up Appwrite Database**
   
   Create a collection with the following attributes:
   - `searchTerm` (string)
   - `count` (integer)
   - `movie_id` (integer)
   - `poster_url` (string)

5. **Add Required Assets**
   
   Ensure you have the following files in your `public` folder:
   - `hero.png` - Hero banner image
   - `hero-bg.png` - Background pattern image
   - `search.svg` - Search icon
   - `star.svg` - Star rating icon
   - `no-movie.png` - Placeholder for movies without posters

6. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

## 📱 Usage

1. **Browse Movies**: The app loads with popular movies by default
2. **Search**: Use the search bar to find specific movies
3. **View Trending**: Check out the most searched movies in the trending section
4. **Movie Details**: Each movie card shows ratings, language, and release year

## 🎨 Key Components

### App.jsx
Main application component handling:
- Movie fetching from TMDB API
- Search functionality with debouncing
- Trending movies from Appwrite
- State management for loading and errors

### MovieCard.jsx
Displays individual movie information:
- Movie poster with fallback image
- Title, rating, language, and release year
- Responsive card design

### Search.jsx
Search input component with:
- Debounced search functionality
- Clean, accessible design
- Real-time search results

## 🔧 API Integration

### TMDB API
- **Search Movies**: `/search/movie?query={searchTerm}`
- **Popular Movies**: `/discover/movie?sort_by=popularity.desc`
- **Image URLs**: `https://image.tmdb.org/t/p/w500/{poster_path}`

### Appwrite Functions
- `updateSearchCount()`: Tracks search terms and increments counts
- `getTrendingMovies()`: Retrieves top 5 most searched movies

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [The Movie Database (TMDB)](https://www.themoviedb.org/) for the comprehensive movie API
- [Appwrite](https://appwrite.io/) for the backend-as-a-service platform
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [React](https://reactjs.org/) team for the amazing framework