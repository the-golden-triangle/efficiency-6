efficiency#6
├── app # This is the main directory for our FastAPI application.
│   ├── main.py # This is the entry point of our FastAPI application. Here, we define our routes and start our application.
│   ├── api # This directory contains our API endpoints.
│   │   ├── __init__.py
│   │   ├── endpoints/
│   │   │   ├── lua/
│   │   │   │   └── raw_lua.py  # Endpoint for serving raw Lua files
│   │   │   ├── computers/
│   │   │   │   ├── list.py  # Endpoint for getting information about all active computers
│   │   │   │   └── control.py  # Endpoint for controlling an individual computer
│   │   │   └── auth/
│   │   │       └── authenticate.py # Endpoint for authentication
│   │   └── models # Pydantic models for our application
│   │       ├── __init__.py
│   │       ├── computercraft_models.py
│   │       └── lua_models.py
│   ├── services # Business logic modules
│   │   ├── __init__.py
│   │   └── computercraft_service # Computercraft-related logic
│   │       ├── __init__.py
│   │       ├── navigation # Navigation logic
│   │       │   └── locate.py
│   │       └── refueling # Refueling logic
│   │           └── cole.py
│   ├── utils # Utility modules
│   │   ├── __init__.py
│   │   ├── common.py # Common utility functions
│   │   ├── favicon.py # Favicon router
│   │   ├── rate_limit.py # Rate limiting middleware
│   │   ├── robots.py # Robots.txt router
│   │   ├── auth.py # Authentication methods (IF WE WANT)
│   │   └── sitemap.py # Sitemap router
│   └── frontend # Frontend application folder
│       ├── templates # HTML templates
│       │   └── index.html
│       ├── tailwindcss # Tailwind CSS setup
│       │   ├── package.json
│       │   ├── tailwind.config.js
│       │   └── styles.css
│       │       └── style.css
│       └── static # Static files (CSS, JS)
│           ├── styles.css # Tailwind CSS styles
│           └── main.js # JavaScript code
├── tests # All our pytest or unittest tests
│   ├── __init__.py
│   ├── test_main.py # Tests related to the main parts of the application
│   ├── test_computercraft.py
│   ├── test_pydantic_version.py
│   └── test_user_management.py
├── Dockerfile # This file contains the instructions to Dockerize our application.
├── .pre-commit-config.yaml # This file contains the configuration for pre#commit hooks.
├── requirements.txt # This file lists the Python dependencies of our application.
└── README.md # This file contains the documentation of our project.