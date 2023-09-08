# Image_Search

accessKey: This is an API access key required to make requests to the Unsplash API.
form, searchInput, searchResults, showMoreButton: These variables are used 

searchImages(): This function is used to fetch images from the Unsplash API based on the user's input.
It constructs a URL with the search query, page number, and the API access key.
It sends a request to the API using fetch(), and when the data is received, it parses it as JSON.
It clears the previous search results if it's the first page of results (page 1).
It then loops through the results and creates HTML elements to display each image and a link to the image source.
The page variable is incremented to load more results in subsequent searches.
If it's not the first page of results (page > 1), it displays the "Show More" button.

form.addEventListener "submit": This listens for a form submission event (e.g., when the user hits Enter after typing a query).
It prevents the default form submission behavior.
It resets the page variable to 1 and calls searchImages() to initiate the search.
showMoreButton.addEventListener"click": This listens for a click event on the "Show More" button.
When clicked, it calls searchImages() to load more search results.
