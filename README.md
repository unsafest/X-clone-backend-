# X-clone

A simple Node.js backend for creating and viewing posts, inspired by X (formerly Twitter).

## Dependencies

- Node.js
- Express.js
- SQLite
- JSON Web Tokens (JWT)

## Features

- **Public Endpoints**
  - View all posts: `GET /posts`
  - View a specific post: `GET /posts/:id`
- **Authenticated Endpoints**
  - Create a post: `POST /posts/create`
  - Update a post: `PUT /posts/edit/:id`
  - Delete a post: `DELETE /posts/delete/:id`
- JWT-based authentication and authorization
- SQLite database for data storage

## REST API Overview

This backend exposes a RESTful API for managing posts. Public endpoints allow anyone to view posts, while creating, editing, and deleting posts require authentication via JWT.

### Example API Flow

1. **User logs in** and receives a JWT token.
2. **User sends requests** to protected endpoints with the JWT in the `Authorization` header.
3. **Server validates** the JWT and processes the request if valid.

![REST API Sequence Diagram](https://www.plantuml.com/plantuml/png/TPB1RXCn48RlVefVFXEQ84uhLBKfbo8Y0WsKGwLe6e_QWQsTshD4WFhkZ7Up112vs99dvlj-U_UiA6Nj7bf76qqP5wrmLBUrGzd8bgB2VvvisXGPvyjB3ofr_xjX8I6qlAFCVNrnxG8ftL9X-AltRqKPh-UrP9jpWmAJqmfgi7ntjSB9DXKj9vlCf7mJppkzJrb-a4gA3UPiw8nNNtQwrlILu-bD_EdhoFesXU--WLznKTGJ_-GCQtIBqO0CnD6I6lRDzSfHg_X4hGIiAiS1i3vCnZ2P7vztXNE_h2NKXbePqmx31iDlUzzou5x6RQVzsM7KhjrOmP13Hkn4xr4nw-76OHompaEONY7XNzZmVWrUJ6Uu6CRjEV30fT0TD_3BgjY3_JD8Q333Ku_Xjh0b-NOywaX_EPrYJW4V-B7ZejN0EQSyyklLaQqesImZFWOtAew_ih5dxh_A6Jv6sdzx3dyw5rAAn3ka3DcpjRAhkLhFRB6_-1S0)

## Getting Started

### Prerequisites

- Node.js (v14+ recommended)
- npm

### Installation

1. Clone the repository:
    ```sh
    git clone <repo-url>
    cd X-clone
    ```
2. Install dependencies:
    ```sh
    npm install
    ```

3. Ensure you have an SQLite database file named `Xdatabase.db` in the project root. The database should have `users` and `posts` tables.

### Configuration

- The JWT secret can be set via the `JWT_SECRET` environment variable. Defaults to `'giga-secret_key_123'`.

### Running the Server

```sh
node server.js
```
