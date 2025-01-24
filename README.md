# MoviesDatabase API Documentation

The **MoviesDatabase API** provides a comprehensive set of endpoints for accessing a vast collection of movie-related data. Users can retrieve information about movies, TV shows, actors, and more. The API supports advanced search functionalities, allowing filtering by criteria such as genre, release date, and ratings. Additionally, users can access detailed information about specific titles, including cast and crew details, reviews, and ratings.

---

## Version
**Current Version**: 3

---

## Endpoints
### Movies
- **`/movies`**: Retrieve a list of movies with filters for genre, release date, and popularity.
- **`/movies/{id}`**: Get detailed information about a specific movie using its unique identifier.

### Actors
- **`/actors`**: Access a list of actors and their filmography.
- **`/actors/{id}`**: Retrieve detailed information about a specific actor, including their biography and film credits.

### Search
- **`/search`**: Search for movies, TV shows, or actors using keywords.

### Genres
- **`/genres`**: List all available genres for filtering movie searches.

---

## Request and Response Format
### Request
All requests are made using the HTTP `GET` method. For example, to retrieve a list of movies, use:


### Response
Responses are returned in JSON format. Example response for a movies request:

```json
{
  "results": [
    {
      "id": 123,
      "title": "Action Movie",
      "release_date": "2022-05-01",
      "genre": "Action",
      "rating": 7.5
    },
    {
      "id": 124,
      "title": "Another Action Movie",
      "release_date": "2022-06-15",
      "genre": "Action",
      "rating": 8.0
    }
  ],
  "total_results": 2
}

 Authentication
Authorization: Bearer YOUR_API_KEY


Error Handling
The MoviesDatabase API provides descriptive error codes to help identify and resolve issues with requests. Below are common errors you may encounter:

400 Bad Request: The request is invalid. Check the parameters and ensure they are correctly formatted.
401 Unauthorized: Authentication failed. Verify your API key is correct and active.
404 Not Found: The requested resource could not be found. Double-check the endpoint and query parameters.
500 Internal Server Error: An unexpected error occurred on the server. This is typically temporary, so try again later.

{
  "status": "error",
  "code": 400,
  "message": "Invalid request. Missing required parameter: genre."
}

Best Practices for Handling Errors
Check Status Codes: Always inspect the HTTP response status code to determine success or failure.
Validate Inputs: Ensure all required parameters are included and properly formatted before making requests.
Retry Logic: For 500 Internal Server Error responses, implement a retry mechanism with exponential backoff.
Log Errors: Log API responses for troubleshooting and debugging.

Usage Limits and Best Practices
Rate Limits
The API enforces rate limits to ensure fair access for all users. Refer to the official documentation for specific limits (e.g., requests per minute or hour).

Best Practices
Cache Data: Cache frequently accessed data locally to reduce redundant requests.
Efficient Queries: Use filters and parameters to minimize unnecessary data retrieval and improve response times.
Monitor Usage: Track your API usage to avoid exceeding rate limits.

 Feedback and Support
If you encounter issues or have suggestions for improvement, feel free to contact the MoviesDatabase API support team.