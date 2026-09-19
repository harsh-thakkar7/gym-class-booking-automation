# Gym Class Booking Automation

A Selenium bot that logs into a gym scheduling site and automatically books class slots.

## How It Works

1. Logs in with the account credentials
2. Scans all class cards for **Tuesday** and **Thursday** classes at **6:00 PM**
3. Books each class (or joins the waitlist if it's full)
4. Verifies every booking on the "My Bookings" page

Includes a `retry()` helper that retries flaky actions (page loads, clicks) up to 7 times.

## Setup

Fill in your credentials at the top of `main.py`:

```python
ACCOUNT_EMAIL = "your_email"
ACCOUNT_PASSWORD = "your_password"
```

Then run:

```bash
python main.py
```

## Requirements

```
selenium
```