# The Movie Database API (TMDb) Integration

## Overview
This project integrates with **The Movie Database API (TMDb)** to provide functionalities such as account management, favorites, watchlists, movie details, and more. TMDb is a popular API offering extensive data on movies, TV shows, and actors.

---

## API Features

### Account Management
- **Login:** Authenticate users.
- **Get Account Details:** Retrieve account-related information.
- **Add to Favorites:** Mark movies or TV shows as favorites.
- **Add to Watchlist:** Add movies or TV shows to the user's watchlist.
- **Retrieve Favorites & Watchlists:** Access lists of favorite and watchlisted movies or TV shows.
- **Retrieve Ratings:** View movies or TV shows rated by the user.

### Genre Information
- **Movie Genres:** Fetch a list of official genres for movies.
- **TV Genres:** Fetch a list of official genres for TV shows.

### Movie Lists
- **Now Playing:** Get movies currently in theaters.
- **Popular Movies:** Get a list of movies ordered by popularity.
- **Top-Rated Movies:** Fetch movies with the highest ratings.
- **Upcoming Movies:** Get details about soon-to-be-released movies.

### Search Functionality
- **Search Movies:** Search for movies by title.
- **Search TV Shows:** Search for TV shows by title.
- **Search People:** Search for actors, directors, and other people in the industry.
- **Search Keywords:** Find movies or TV shows by keywords.

### Movie Operations
- **Get Movie Details:** Fetch detailed information about a movie by its ID.
- **Lists a Movie Belongs To:** Retrieve lists associated with a movie.
- **Add/Delete Ratings:** Rate or delete ratings for movies.
- **Add a Movie to a List:** Include a movie in a custom list.

---

## API Endpoints
Below is a summary of the API endpoints. For detailed usage, refer to the [TMDb API Documentation](https://www.themoviedb.org/documentation/api).

### Account
- **Login:** `POST /login`
- **Account Details:** `GET /account`
- **Add to Favorites:** `POST /account/{account_id}/favorite`
- **Add to Watchlist:** `POST /account/{account_id}/watchlist`
- **Favorite Movies:** `GET /account/{account_id}/favorite/movies`
- **Favorite TV Shows:** `GET /account/{account_id}/favorite/tv`
- **Rated Movies:** `GET /account/{account_id}/rated/movies`
- **Rated TV Shows:** `GET /account/{account_id}/rated/tv`
- **Watchlist Movies:** `GET /account/{account_id}/watchlist/movies`
- **Watchlist TV Shows:** `GET /account/{account_id}/watchlist/tv`

### Genres
- **Movie Genres:** `GET /genre/movie/list`
- **TV Genres:** `GET /genre/tv/list`

### Movies
- **Now Playing:** `GET /movie/now_playing`
- **Popular Movies:** `GET /movie/popular`
- **Top-Rated Movies:** `GET /movie/top_rated`
- **Upcoming Movies:** `GET /movie/upcoming`
- **Movie Details:** `GET /movie/{movie_id}`
- **Add Rating:** `POST /movie/{movie_id}/rating`
- **Delete Rating:** `DELETE /movie/{movie_id}/rating`
- **Add to List:** `POST /list/{list_id}/add_item`

### Search
- **Search Movies:** `GET /search/movie`
- **Search TV Shows:** `GET /search/tv`
- **Search People:** `GET /search/person`
- **Search Keywords:** `GET /search/keyword`

---

## Authentication
TMDb API requires authentication via an API key. Obtain an API key by signing up at [TMDb](https://www.themoviedb.org/).

## Examples

### Add to Favorites
**Endpoint:** `POST /account/{account_id}/favorite`  
**Request Body:**
```json
{
  "media_type": "movie",
  "media_id": 550,
  "favorite": true
}
```

### Search for a Movie
**Endpoint:** `GET /search/movie?query=Inception`  
**Response:**
```json
{
  "results": [
    {
      "title": "Inception",
      "release_date": "2010-07-16",
      "overview": "A thief who steals corporate secrets..."
    }
  ]
}
```
