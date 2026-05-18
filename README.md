# E-Commerce Platform

A modern, lightweight, and Docker-ready e-commerce demo application built with Flask and a static frontend powered by Tailwind CSS.

This project is designed for learning, rapid prototyping, local development, and simple cloud deployment using Render.

The application demonstrates a minimal full-stack architecture with:

- A Flask backend serving HTML templates and API routes
- A responsive frontend using Tailwind CSS CDN
- Browser-based cart persistence using `localStorage`
- Docker containerization support
- Deployment-ready configuration for Render using Gunicorn

---

# Features

- Clean and responsive UI
- Product listing and shopping cart functionality
- Cart persistence with browser `localStorage`
- Flask-powered backend routing
- Lightweight architecture with no external database
- Docker support for containerized deployment
- Cloud deployment ready
- Simple health monitoring endpoint

---

# Tech Stack

## Backend
- Flask
- Gunicorn

## Frontend
- HTML5
- JavaScript (Vanilla JS)
- Tailwind CSS

## Deployment
- Docker
- Render

---

# Project Structure

```bash
ecommerce-platform/
│
├── app.py                     # Flask application
├── requirements.txt           # Python dependencies
├── Dockerfile                 # Docker configuration
│
├── templates/
│   └── index.html             # Main frontend page
│
├── static/
│   └── script.js              # Frontend logic and cart handling
│
└── README.md
```

---

# Getting Started

## 1. Clone the Repository

```bash
git clone <your-repository-url>
cd ecommerce-platform
```

---

# Local Development Setup

## Create Virtual Environment

### Windows (PowerShell / CMD)

```bash
python -m venv .venv
.venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Application

```bash
python app.py
```

The application will start at:

```bash
http://localhost:5000
```

---

# Health Check Endpoint

The application includes a simple health route for deployment monitoring.

## Endpoint

```bash
GET /health
```

## Example

```bash
curl http://localhost:5000/health
```

### PowerShell

```powershell
Invoke-RestMethod http://localhost:5000/health
```

---

# Docker Setup

## Build Docker Image

```bash
docker build -t ecommerce-platform .
```

## Run Docker Container

```bash
docker run -p 5000:5000 ecommerce-platform
```

Open in browser:

```bash
http://localhost:5000
```

---

# Deploying on Render

This project is fully compatible with Render.

## Build Command

```bash
pip install -r requirements.txt
```

## Start Command

```bash
gunicorn app:app --bind 0.0.0.0:$PORT
```

> Render automatically provides the `PORT` environment variable during deployment.

---

# Frontend Cart Persistence

The shopping cart is stored in browser `localStorage`.

## Benefits

- No database required
- Fast and lightweight
- Persistent cart between page reloads

## Reset Cart Data

To clear cart data:

1. Open browser DevTools
2. Navigate to:
   - Application → Local Storage
3. Remove stored cart entries

---

# API Routes

| Route | Method | Description |
|------|------|------|
| `/` | GET | Main application page |
| `/health` | GET | Health check endpoint |

---

# Production Notes

This project is intended for:

- Learning Flask
- Portfolio projects
- Demo deployments
- Docker practice
- Frontend-backend integration examples

It is **not recommended** for:

- Real payment processing
- Sensitive customer information
- Production-scale commerce systems

For real-world production use, consider adding:

- Authentication & authorization
- Database integration
- Secure payment gateways
- Session management
- Input validation
- Rate limiting
- HTTPS configuration
- Logging & monitoring

---

# Troubleshooting

## Docker Build Issues

If Docker fails during dependency installation:

- Ensure `requirements.txt` contains only required packages
- Verify Python version compatibility
- Rebuild without cache:

```bash
docker build --no-cache -t ecommerce-platform .
```

---

## Flask Port Issues

If port `5000` is already in use:

```bash
python app.py --port 5001
```

Or stop the existing process using the port.

---

## Git Configuration (Windows)

Before pushing to GitHub:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

# Future Improvements

Potential enhancements for the project:

- User authentication
- Admin dashboard
- Product categories
- Search & filtering
- Order history
- Backend database integration
- Payment gateway integration
- REST API support
- Responsive product gallery
- Wishlist functionality

---

# Contributing

Contributions are welcome.

If you would like to contribute:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to your branch
5. Open a pull request

Please keep changes focused and include tests where applicable.

---

# License

This project is licensed under the MIT License.

Add a `LICENSE` file if one is not already included.

---

# Support

For deployment or build issues, please include:

- Error logs
- Docker build output
- Render deployment logs
- Commands executed
- Environment details

This helps reproduce and resolve issues faster.

---

# Author

Developed as a lightweight full-stack e-commerce demo using Flask and modern frontend tooling.
