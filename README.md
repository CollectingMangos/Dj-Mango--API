This project is a Django-based API for managing notes, using `django-tastypie` to provide RESTful endpoints.

## Features

- Create, read, update, and delete notes
- RESTful API using `django-tastypie`
- Basic setup and configuration for quick deployment

## Requirements

- Python 3.12
- Django 3.x or 4.x
- django-tastypie

## Installation

1. **Clone the repository:**

    ```shell
    git clone https://github.com/CollectingMangos/Dj-Mango-API.git
    cd notable-django-api
    ```

2. **Create and activate a virtual environment:**

    ```shell
    python3 -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3. **Install the required packages:**

    ```shell
    pip3 install django
    pip3 install django-tastypie
    ```

4. **Apply migrations:**

    ```shell
    python3 manage.py migrate
    ```

5. **Run the development server:**

    ```shell
    python3 manage.py runserver
    ```

6. **Access the API:**

    Visit `http://127.0.0.1:8000/api/v1/note/` to interact with the API.

## Project Structure

- `api/models.py`: Defines the Note model.
- `api/resources.py`: Defines the NoteResource for the Tastypie API.
- `api/urls.py`: Contains URL configurations for the API endpoints.
- `notable_django/urls.py`: Main URL configurations, including the API routes.
- `settings.py`: Django settings file, where `tastypie` is added to `INSTALLED_APPS`.

## Usage

### Create a Note

Send a `POST` request to `http://127.0.0.1:8000/api/v1/note/` with the note data in the body.

### Get All Notes

Send a `GET` request to `http://127.0.0.1:8000/api/v1/note/`.

### Get a Specific Note

Send a `GET` request to `http://127.0.0.1:8000/api/v1/note/{note_id}/`.

### Update a Note

Send a `PUT` request to `http://127.0.0.1:8000/api/v1/note/{note_id}/` with the updated note data in the body.

### Delete a Note

Send a `DELETE` request to `http://127.0.0.1:8000/api/v1/note/{note_id}/`.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
