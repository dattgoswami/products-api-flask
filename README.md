# Simple Flask Products API

A basic API implemented using Flask for managing products. The API allows for standard CRUD operations on a list of items.

## Features

- Retrieve all items.
- Retrieve a specific item by ID.
- Add a new item.
- Update an existing item by ID.
- Delete an item by ID.

## Installation

Before running the application, ensure you have [Python](https://www.python.org/downloads/) and `pip` installed.

1. First, clone the repository to your local machine:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required packages:
   ```bash
   pip install flask
   ```

## Running the Application

You can run the application using the following command:

```bash
python3 products_api.py
```

Once the application is running, it will be accessible at `http://127.0.0.1:5000`.

## API Endpoints

### Get All Items

- **Endpoint:** `/items`
- **Method:** `GET`
- **Response:** A list of all items.

### Get Single Item

- **Endpoint:** `/items/<id>`
- **Method:** `GET`
- **Response:** The item with the matching ID or an error message if the item doesn't exist.

### Add New Item

- **Endpoint:** `/items`
- **Method:** `POST`
- **Body:** JSON object with the fields `name`, `price`, `url`, and `description`.
- **Response:** The newly added item or an error message if the item format is invalid.

### Update Item

- **Endpoint:** `/items/<id>`
- **Method:** `PUT`
- **Body:** JSON object with any of the fields `name`, `price`, `url`, or `description` you want to update.
- **Response:** The updated item or an error message if the item doesn't exist.

### Delete Item

- **Endpoint:** `/items/<id>`
- **Method:** `DELETE`
- **Response:** A success message or an error message if the item doesn't exist.

## Data Structure

Each item in the list has the following structure:

```json
{
    "id": <integer>,
    "name": <string>,
    "price": <float>,
    "url": <string (image URL)>,
    "description": <string>
}
```

## License

This project is licensed under the MIT License.
