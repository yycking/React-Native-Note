# Fetch

* ```javascript
  fetch('http://abc.com/', {method: 'get'})
  .then(function(response) {
  }).catch(function(err) {
  })
  ```

* ```javascript
  async function getMoviesFromApi() {
    try {
      const response = await fetch('http://abc.com/');
      const responseJson = await response.json();
      return responseJson.movies;
    } catch(error) {
      console.error(error);
    }
  }
  ```

* ​

