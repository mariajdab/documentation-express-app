# Documentation-express-app

## What is the application?

This application is a simple REST API that uses JSON as the payload encoding that is capable of adding, fetching and removing transaction records.

## Routes

- / GET Returns all the transactions in storage. On the backend it takes the array of stored records and sends it back as is, in JSON format.
- / POST Inserts a new transaction record in storage. Payload must be with the format:

json
    {
        "id": 1,
        "amount": 25.00,
        "to": "joe"
    }

On the backend it decodes the data sent by the client and stores the values on the array.

- / DELETE Removes a transaction from the records given the transaction ID. Payload must be with the format:

json
    {
        "id": 1
    }
  

On the backend it decodes the data sent by the client and looks for the element of the array with the ID equal to the one sent by the client, then the element is removed from the array. If there is no such element, an error message is returned.

## How to run the app

- Open a terminal.
- Make sure that npm and node are intalled. To install them please refer to: https://nodejs.org/en/.
- Run npm install to download all of the application dependencies.
- Run node index.js to start the application. By default it will run in port 3000 of localhost.
