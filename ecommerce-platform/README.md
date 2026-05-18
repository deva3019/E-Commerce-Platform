# E-commerce Platform

This is a simple e-commerce platform built with a Flask backend and a frontend that utilizes local storage for data management. The application allows users to browse products, add them to a shopping cart, and manage their selections without requiring a database.

## Project Structure

```
ecommerce-platform
├── frontend
│   ├── templates
│   │   └── index.html
│   └── static
│       └── script.js
├── backend
│   └── app.py
├── requirements.txt
└── README.md
```

## Features

- Product listings displayed on the homepage.
- Ability to add products to a shopping cart.
- Shopping cart management using local storage.
- Simple and clean user interface.

## Setup Instructions

1. Clone the repository:
   ```
   git clone <repository-url>
   cd ecommerce-platform
   ```

2. Set up a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Run the Flask application:
   ```
   python backend/app.py
   ```

5. Open your browser and navigate to `http://127.0.0.1:5000` to view the application.

## Deployment on Render

To deploy this application on Render:

1. Create a new web service on Render.
2. Connect your GitHub repository containing this project.
3. Set the build command to:
   ```
   pip install -r requirements.txt
   ```
4. Set the start command to:
   ```
   python backend/app.py
   ```
5. Ensure that the `app.py` file is configured to serve static files correctly.

## License

This project is licensed under the MIT License. See the LICENSE file for details.