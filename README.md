
# Analog 4chan Web Site

## Overview

The **Analog 4chan Web Site** is a minimalist, text-oriented web forum inspired by the early era of internet imageboards such as 4chan.
This project emphasizes simplicity, anonymity, and lightweight performance. It seeks to recreate the nostalgic experience of early web communities, focusing on text-based discussions and image sharing in a retro-themed interface.

The system is built using Django on the backend and minimal HTML/CSS on the frontend, resulting in an efficient, low-resource platform suitable for experimental social web applications or nostalgia-driven community projects.

---

## Features

### Core Functionality

* **Anonymous Posting** – Users can post messages and images without registration or authentication.
* **Threaded Discussions** – Posts are organized into threads, allowing structured yet simple conversations.
* **Text-Based Interface** – Focuses on content rather than user profiles or visual clutter.
* **Image Upload Support** – Allows attaching images to posts with size and type validation.
* **Retro Aesthetic** – Inspired by early web forums, featuring minimal design, monospaced fonts, and simple color schemes.
* **Lightweight Architecture** – Optimized for speed and minimal resource consumption.

### Future Enhancements (Optional)

* Captcha or post-rate limitation for spam prevention.
* Optional moderation tools (thread locking, content deletion).
* Theme customization for different ASCII/ANSI styles.
* API endpoints for third-party integrations or mobile clients.

---

## Technologies Used

* **Frontend:** HTML5, CSS3 (handcrafted static templates)
* **Backend:** Django (Python 3.x)
* **Database:** SQLite3 (default), with support for PostgreSQL in production
* **Version Control:** Git / GitHub
* **Deployment:** Can be hosted on any WSGI-compatible platform (e.g., Gunicorn + Nginx, Heroku, or Docker)

---

## Project Structure

```
Analog-4chan-Web-Site/
│
├── manage.py
├── requirements.txt
├── README.md
│
├── analogchan/               # Django project configuration
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
│
├── board/                    # Core application (threads and posts)
│   ├── models.py             # Thread, Post, and Image models
│   ├── views.py              # Logic for creating and displaying posts
│   ├── forms.py              # Forms for post and thread creation
│   ├── urls.py               # URL routing for the board
│   └── templates/            # HTML templates for the forum pages
│
└── static/                   # CSS, images, and static assets
```

---

## Installation and Setup

### Prerequisites

* Python 3.8 or higher
* Django 4.x
* SQLite3 (included by default)
* Node.js and npm (for static asset management, optional)

### Setup Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/waratecs123/Analog-4chan-Web-Site.git
   cd Analog-4chan-Web-Site
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate       # macOS/Linux
   venv\Scripts\activate          # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply migrations**

   ```bash
   python manage.py migrate
   ```

5. **Run the development server**

   ```bash
   python manage.py runserver
   ```

6. Open your browser and visit:

   ```
   http://127.0.0.1:8000
   ```

---

## Alternative Frontend Setup (Optional)

If you want to manage frontend assets with npm (for CSS compilation or live reloading):

```bash
# Install dependencies
npm install

# Start local development environment
npm start
```

This setup can be customized to include SCSS compilation, minification, or asset bundling if required.

---

## Usage

1. Visit the main page to view existing threads.
2. Click **"Create Thread"** to start a new discussion.
3. Add a message and optionally upload an image.
4. Reply to any existing post directly in its thread view.
5. All posts are anonymous by default — no accounts or authentication required.

---

## Deployment

This project can be deployed using standard Django deployment procedures.

**Recommended steps:**

* Configure environment variables for `SECRET_KEY`, `DEBUG`, and `ALLOWED_HOSTS`.
* Switch to a production-ready database (e.g., PostgreSQL).
* Serve static and media files via Nginx or a CDN.
* Use **Gunicorn** or **uWSGI** as the application server.
* Enable HTTPS with SSL certificates (e.g., Let’s Encrypt).

Example with Gunicorn and Nginx:

```bash
gunicorn analogchan.wsgi:application
```

---

## Testing

Run the Django test suite to verify that the core functionality is working as intended:

```bash
python manage.py test
```

Tests can be extended to cover posting, thread creation, image uploads, and form validation.

---

## Contributing

Contributions are welcome. To propose changes or improvements:

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/new-functionality
   ```
3. Commit your changes and include clear commit messages.
4. Push to your fork and open a pull request for review.

All submissions should follow **PEP 8** guidelines and maintain Django best practices.

---

## License

This project is distributed under the **MIT License**.
You may freely use, modify, and distribute this software, provided that the original copyright notice and license are included.

---

## Author

**Developed by Waratecs**
For inquiries, feature requests, or collaboration, please contact via GitHub or open an issue in the repository.

