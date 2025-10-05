# Sales Dashboard Web App

A complete data dashboard web application built with Python (Flask), SQLite, HTML, CSS, and JavaScript. The dashboard visualizes sales data using interactive charts powered by Chart.js.

## 📁 Project Structure

```
my-dashboard/
├── server/                          # Backend (Flask application)
│   ├── app.py                       # Main Flask application
│   ├── database_setup.py            # SQLite database creation script
│   ├── sales_data.db                # SQLite database (generated)
│   ├── templates/
│   │   └── index.html               # Dashboard template
│   └── static/
│       ├── style.css                # Dashboard styles
│       └── script.js                # Dashboard JavaScript
├── demo.html                        # Static demo version (no Python required)
└── README.md                        # This file
```

## 🚀 Quick Start

### Option 1: View the Demo (No Python Required)

Simply open `demo.html` in your web browser to see the dashboard with sample data.

### Option 2: Run the Full Application (Requires Python)

#### Prerequisites

- Python 3.7+ installed
- Flask installed (`pip install flask`)

#### Installation Steps

1. **Install Python**
   - Download from: https://www.python.org/downloads/
   - Make sure to check "Add Python to PATH" during installation

2. **Install Flask**
   ```bash
   pip install flask
   ```

#### Running the Application

1. **Navigate to the server directory**
   ```bash
   cd my-dashboard/server
   ```

2. **Create and populate the database**
   ```bash
   python database_setup.py
   ```

3. **Run the Flask application**
   ```bash
   python app.py
   ```

4. **Open in browser**
   - Navigate to: http://127.0.0.1:5000/

## 📊 Features

### Backend (Flask + SQLite)
- RESTful API endpoints for sales data
- SQLite database with sample sales records
- Aggregated data endpoints for analytics

### Frontend (HTML + CSS + JavaScript)
- Responsive dashboard design
- Interactive bar chart showing product quantities
- Pie chart displaying revenue distribution by product
- Modern, clean UI with hover effects

### API Endpoints
- `GET /api/sales` - Returns all sales records
- `GET /api/sales_summary` - Returns aggregated sales totals per product
- `GET /` - Serves the dashboard

## 🗄️ Database Schema

The SQLite database contains a `sales` table with the following columns:

- `order_id` (INTEGER PRIMARY KEY)
- `order_date` (TEXT)
- `customer_id` (INTEGER)
- `product_name` (TEXT)
- `quantity` (INTEGER)
- `price` (REAL)

### Sample Data

The database is populated with sample sales data for 5 products:
- Laptop ($1200 each)
- Mouse ($25 each)
- Keyboard ($75 each)
- Monitor ($300 each)
- Headphones ($150 each)

## 🛠️ Technologies Used

- **Backend**: Python, Flask, SQLite
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Charts**: Chart.js
- **Styling**: Custom CSS with modern design principles

## 📱 Responsive Design

The dashboard is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile devices

## 🔧 Development

### File Structure Details

#### `server/app.py`
Main Flask application with:
- Route handlers for API endpoints
- Template rendering for the dashboard
- Database connection management

#### `server/database_setup.py`
Database initialization script that:
- Creates the SQLite database
- Defines the sales table schema
- Populates with sample data

#### `server/templates/index.html`
Jinja2 template for the dashboard with:
- Chart.js integration
- Responsive layout
- Flask URL generation for static files

#### `server/static/style.css`
Modern CSS styling featuring:
- Clean, professional design
- Card-based layout
- Hover effects and transitions
- Mobile-responsive breakpoints

#### `server/static/script.js`
Frontend JavaScript that:
- Fetches data from Flask API
- Creates interactive Chart.js visualizations
- Handles errors gracefully
- Manages chart lifecycle

## 🚀 Deployment

To deploy this application:

1. Set up a Python environment on your server
2. Install Flask: `pip install flask`
3. Run the database setup: `python database_setup.py`
4. Start the application: `python app.py`
5. Configure your web server (nginx, Apache) to proxy to Flask

For production deployment, consider using:
- Gunicorn as WSGI server
- Environment variables for configuration
- Database migrations for schema changes

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

---

**Note**: The `demo.html` file provides a static version of the dashboard that works without Python, using hardcoded sample data. This is perfect for demonstrations or when Python is not available.
