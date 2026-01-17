# Simple Social

A full-stack social media application offering a unified platform for sharing images and videos. The project is built using a modern **FastAPI** backend and a **Streamlit** frontend, featuring secure user authentication and media management via ImageKit.

## Features

-   **User Authentication**: concise and secure signup/login/logout flow using JWT (JSON Web Tokens) backed by `fastapi-users`.
-   **Media Upload**: Support for image and video uploads with cloud storage integration using **ImageKit.io**.
-   **Social Feed**: Real-time feed displaying posts from all users with timestamps and owner details.
-   **Interactive UI**: A responsive, clean interface built with Streamlit.
-   **Database**: SQLite with asynchronous SQLAlchemy for efficient data handling.

## Tech Stack

-   **Backend**: FastAPI, Uvicorn, SQLAlchemy, Pydantic
-   **Frontend**: Streamlit
-   **Authentication**: FastAPI Users
-   **Storage**: ImageKit IO
-   **Database**: SQLite (Async)

## Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd <repository_folder>
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    # Windows
    python -m venv .venv
    .venv\Scripts\activate

    # macOS/Linux
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Environment Configuration:**
    Create a `.env` file in the root directory and add your ImageKit credentials:
    ```env
    # ImageKit Credentials
    IMAGEKIT_PRIVATE_KEY=your_private_key
    IMAGEKIT_PUBLIC_KEY=your_public_key
    IMAGEKIT_URL_ENDPOINT=your_url_endpoint

    # Secret for JWT
    SECRET=your_jwt_secret_string
    ```
    *Note: Ensure you have `SECRET` configured for fastapi-users.*

## Usage

### 1. Start the Backend Server
Run the FastAPI backend server:
```bash
python main.py
# OR
uvicorn app.app:app --reload
```
The API will be available at `http://localhost:8000`. API Docs are at `http://localhost:8000/docs`.

### 2. Start the Frontend Application
In a new terminal, run the Streamlit app:
```bash
streamlit run frontend.py
```
The application will open in your default browser (usually at `http://localhost:8501`).

