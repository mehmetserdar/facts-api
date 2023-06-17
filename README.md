# facts-api

Facts API is a user-friendly and efficient platform that serves as a repository for a wide range of interesting and informative facts. It offers a straightforward and intuitive interface that allows users to access factual information easily.

The core functionality of Facts API revolves around storing and retrieving facts. Users can make HTTP requests to specific endpoints to interact with the API and retrieve facts based on their preferences or requirements. The API is designed to handle these requests swiftly and deliver the requested information in a structured format.
### Endpoint: [https://raw.githubusercontent.com/mehmetserdar/facts-api/main/facts.json]

## Fetch Random facts
Below is the JavaScript code that can be used to fetch a random facts from an API using the fetch function:

```javascript
function getRandomfacts() {
    fetch('https://raw.githubusercontent.com/mehmetserdar/facts-api/main/facts.json')
        .then(function(response) {
            return response.json();
        })
        .then(function(data) {
            var facts = data.facts;
            var randomIndex = Math.floor(Math.random() * facts.length);
            var facts = facts[randomIndex];

            var TextArea = document.getElementById('text-area');
            TextArea.value = facts;
        })
        .catch(function(error) {
            console.log('An error occurred while fetching the random facts:', error);
        });
}

document.getElementById('random-facts-button').addEventListener('click', function() {
    getRandomfacts();
});

```




## Contributing
Additional contributions are welcome. If you know of a positive facts that would be useful to add, please contribute to this open-source project.

