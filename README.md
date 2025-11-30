# Temporary Email API

A lightweight Flask-based API for generating temporary email accounts, authenticating them, and managing inbox messages.  
Designed for testing, automation, and any workflow that requires disposable email addresses without exposing real mailboxes.

## Features

- Create random temporary email accounts
- Generate secure passwords automatically
- Authenticate accounts and receive access tokens
- Fetch inbox messages (paginated)
- Read the content of a specific message
- Delete messages from the inbox
- Retrieve information about the authenticated account

## Endpoints

### `GET /domains`
Returns a list of available email domains.

### `GET /create_random_account`
Creates a fully random temporary account (email + password) and returns the credentials along with a token.

### `GET /token?address=<email>&password=<password>`
Authenticates an existing account and returns an access token.

### `GET /messages?page=<n>`
Lists messages in the authenticated user's inbox.

### `GET /messages/<message_id>`
Fetches the full content of a specific message.

### `DELETE /messages/<message_id>`
Deletes a message from the inbox.

### `GET /me`
Returns account information for the authenticated session.

## Installation

```bash
git clone https://github.com/yourusername/temp-email-api.git
cd temp-email-api
pip install -r requirements.txt
