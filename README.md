# UniConnect

UniConnect is a PHP/MySQL student support platform designed for academic communities. It provides student and admin dashboards, item lending and borrowing management, real-time chat support, profile management, and secure authentication.

## Key Features

- Secure user registration and login with hashed passwords
- Role-based admin and student dashboards
- Equipment borrowing and lending workflows
- In-app chat backend for student support
- Student profile and account management
- Responsive interface using native PHP, HTML, CSS, and JavaScript

## Tech Stack

- PHP 8.x
- MySQL / MariaDB
- PDO for secure database access
- HTML, CSS, JavaScript

## Project Structure

- `index.php` — landing page with login and registration
- `auth/` — database connection and auth handlers (`db.php`, `login.php`, `register.php`, `logout.php`)
- `admin_dashboard.php` — admin control panel for managing students and resources
- `student_dashboard.php` — student portal and password management
- `student_profile.php` — student account details view
- `student_link.php`, `reclaim.php`, `brain_bridge.php`, `burrow_buddy.php` — app feature pages
- `chat/api.php` — chat API endpoint
- `*.png` — image assets
- `UniConnect System User Manual.pdf` — optional documentation

## Setup Instructions

1. Place the project in your local web server root.
2. Create a MySQL/MariaDB database named `uniconnect`.
3. Import the database schema and sample data as needed.
4. Update `auth/db.php` with your local database credentials:
   - `DB_HOST`
   - `DB_NAME`
   - `DB_USER`
   - `DB_PASS`
5. Open the site in your browser via `http://localhost/<project-folder>`.

## Security Notes

- `auth/db.php` currently uses local development credentials. Replace these with your own database username and password.
- Keep any production credentials out of source control.
- If you add a `.env` file later, add it to `.gitignore`.

## GitHub Upload Guidance

For a clean GitHub portfolio repo, exclude:

- `uniconnect (4).sql` — this is a database export/backup and contains user data and email addresses
- `.env` or any environment configuration files with secrets
- generated and IDE folders: `.vs/`, `bin/`, `obj/`, `vendor/`, `node_modules/`

> Note: `uniconnect (4).sql` includes user email values and should not be uploaded to GitHub if it contains real or sensitive data.

## Recommended Improvements

- Move database credentials to a secure config file outside the repo
- Add a proper schema-only SQL file if needed for setup
- Add frontend validation and session hardening for production
