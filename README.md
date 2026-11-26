# Campus Portal — Django Templates Laboratory Activity

**Course:** Python Programming 2 (PC15)  
**Activity:** Week 14 — Django Templates (DTL), Template Inheritance, & Static Assets  
**Student:** [Your Name]  
**Section:** [Your Section]

## Overview

This project implements a small branded student web portal for a college department using [Django](https://www.djangoproject.com/) and Django Template Language (DTL). It features **Home** and **About** pages built on a shared base layout (`base.html`), a reusable navigation partial (`navbar.html`), custom external styling (`style.css`), and a local logo asset loaded via Django's static-file tags.

## Features

- **Home Page (`/`)**: Displays the portal name, welcome message, and core portal highlights (Announcements, Class schedules, Resources).
- **About Page (`/about/`)**: Outlines the portal's purpose, intended student audience, and accessibility considerations.
- **Template Inheritance & Partials**: Uses `{% extends %}`, `{% block %}`, and `{% include %}` to keep headers, navigation, footers, and content blocks modular and maintainable.
- **Static Asset Management**: Configures `STATIC_URL` and app-level static directories (`portal/static/portal/`) with `{% load static %}` and `{% static %}` for CSS and images.
- **Responsive & Accessible UI**: Includes accessible contrast, descriptive `alt` text for images, keyboard-friendly focus indicators (`:focus-visible`), and mobile-friendly navigation layout adjustments.

## Project Structure

```text
campus_portal/
├── campus_portal/
│   ├── settings.py
│   └── urls.py
├── portal/
│   ├── static/
│   │   └── portal/
│   │       ├── css/
│   │       │   └── style.css
│   │       └── images/
│   │           └── logo.png
│   ├── templates/
│   │   └── portal/
│   │       ├── partials/
│   │       │   └── navbar.html
│   │       ├── about.html
│   │       ├── base.html
│   │       └── home.html
│   ├── urls.py
│   └── views.py
├── manage.py
└── README.md