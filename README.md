# Book Mela 📚

A Flask-based web application for buying and selling books online. Created for the X-Hack 3.0 hackathon conducted by CS50xAI.

## Team Members

This is a group project developed by:
- **Prashan Chenta Rai** - [GitHub](https://github.com/PrashanRaii)
- **Aadesh Dahal**
- **Nishchal Pokhrel**
- **Sushil Kumar Mandal**

## Features

- 🔐 User Authentication (Login/Register)
- 📖 Book Listing & Search
- 📁 Category-based Book Organization
- ⬆️ Book Upload Functionality
- 👤 User Profile Management
- 🌓 Dark Mode Toggle
- 📱 Responsive Design (Mobile-friendly)
- 🔍 Advanced Search Capabilities

## Tech Stack

- **Backend:** Flask (Python)
- **Database:** SQLAlchemy with SQLite
- **Frontend:** HTML, Tailwind CSS, JavaScript
- **Authentication:** Flask-Login
- **Database Migrations:** Alembic, Flask-Migrate

## Prerequisites

- Python 3.12 or higher
- pip (Python package manager)

## Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Helix-080.git
   cd Helix-080
   ```

2. **Create a virtual environment**
   ```bash
   python3 -m venv .venv
   ```

3. **Activate the virtual environment**
   - On macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```
   - On Windows:
     ```bash
     .venv\Scripts\activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Set up environment variables** (Optional)
   Create a `.env` file in the root directory:
   ```
   SECRET_KEY=your-secret-key-here
   DATABASE_URL=sqlite:///instance/books.db
   FLASK_ENV=development
   ```

6. **Initialize the database**
   ```bash
   flask db init
   flask db migrate -m "Initial migration"
   flask db upgrade
   ```

7. **Run the application**
   ```bash
   flask run
   ```
   Or:
   ```bash
   python app.py
   ```

8. **Access the application**
   Open your browser and navigate to: `http://localhost:5000`

## Project Structure

```
Helix-080/
├── app.py                 # Main application file
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── .env                  # Environment variables (create this)
├── .gitignore            # Git ignore file
├── migrations/           # Database migration files
├── instance/             # Database file location
├── templates/            # HTML templates
│   ├── layout.html      # Base template
│   ├── home.html        # Home page
│   ├── login.html       # Login page
│   ├── categories.html  # Categories page
│   ├── upload.html      # Upload page
│   ├── profile.html     # User profile
│   └── about.html       # About page
└── static/              # Static files (if any)
```

## Usage

### For Users
1. **Register/Login**: Create an account or log in to access features
2. **Browse Books**: Explore available books by category
3. **Search**: Use the search bar to find specific books
4. **Upload Books**: Share your books with the community
5. **Dark Mode**: Toggle between light and dark themes using the button in the top-left corner

### For Sellers
1. Navigate to the "Upload" page
2. Fill in book details (title, author, price, category, etc.)
3. Submit to list your book

## Dependencies

```
alembic==1.14.1
blinker==1.9.0
click==8.1.8
Flask==3.1.0
Flask-Login==0.6.3
Flask-Migrate==4.1.0
Flask-SQLAlchemy==3.1.1
itsdangerous==2.2.0
Jinja2==3.1.5
Mako==1.3.8
MarkupSafe==3.0.2
SQLAlchemy==2.0.37
typing_extensions==4.12.2
Werkzeug==3.1.3
```

## Features in Detail

### Authentication System
- Secure user registration and login
- Password hashing
- Session management with Flask-Login

### Dark Mode
- Persistent theme preference (stored in browser localStorage)
- Smooth transitions between themes
- System preference detection

### Responsive Design
- Mobile-first approach
- Tailwind CSS for styling
- Adaptive navigation menu

## Development

### Running in Development Mode
```bash
export FLASK_ENV=development  # On macOS/Linux
set FLASK_ENV=development     # On Windows
flask run
```

### Database Migrations
```bash
# Create a new migration
flask db migrate -m "Description of changes"

# Apply migrations
flask db upgrade

# Revert migrations
flask db downgrade
```

## Troubleshooting

**Issue: ModuleNotFoundError**
- Solution: Make sure your virtual environment is activated and all dependencies are installed:
  ```bash
  source .venv/bin/activate
  pip install -r requirements.txt
  ```

**Issue: Database not found**
- Solution: Initialize the database:
  ```bash
  flask db upgrade
  ```

**Issue: Port already in use**
- Solution: Run Flask on a different port:
  ```bash
  flask run --port=5001
  ```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Future Enhancements

- [ ] Payment gateway integration
- [ ] Book ratings and reviews
- [ ] Advanced filtering options
- [ ] User messaging system
- [ ] Email notifications
- [ ] Admin dashboard
- [ ] Image upload for books
- [ ] Wishlist functionality
- [ ] Order history tracking

## License

This project was created for educational purposes as part of the X-Hack 3.0 hackathon.

## Acknowledgments

- CS50xAI for organizing X-Hack 3.0
- Flask documentation and community
- Tailwind CSS for the styling framework

## Contact

For questions or feedback, please reach out to any of the team members.

Project Link: [https://github.com/yourusername/Helix-080](https://github.com/yourusername/Helix-080)

---

Made with ❤️ by Team Helix-080 for X-Hack 3.0