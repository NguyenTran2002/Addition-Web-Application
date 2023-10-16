# Addition Web Application

This is a web application that illustrate how a multi-container docker application works.

This application demonstrate the communication ability between the following containers:
    - Add Numbers API (add_numbers folder)
    - Random A Number API (num_randomizer folder)
    - Front-end that takes user input as two numbers

The application runs in the following order

    1. The front-end (main) asks for two numbers from user.
    2. Front-end then sends a post request to the Random A Number API.
    3. The API then returns a random number within a json object.
    4. The front-end then sends a post request with a json object container the two user-inputted number to the Add Numbers API.
    5. The API then returns the result within a json object.
    6. The front-end then adds the result with the random number and display the final message to the user.

To run this application, at the root directory, use the two commands
```docker compose build```
```docker compose up```