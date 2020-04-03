# Django Blog App Prototype

This is a prototype of a Blog App built on Django 3.0 with Bootstrap.

Steps to start developing over this code:

1. Install requirements.txt on your preferred environment:

    ```python
    pip install -r requirements.txt
    ```

2. Generate a new secret key using the Django Shell

    ```python
    cd ./my_website
    python3 manage.py shell
    >>> from django.core.management.utils import get_random_secret_key
    >>> print(get_random_secret_key())
    ```

    Store the secret key generated on a .env as `SECRET_KEY` file and it will be loaded in the settings.py.

3. Create the Database:

    To make sure everything is ok at this point, I recommend to start the development server. Again, from the project directory:

    ```python
    cd ./my_website
    python3 manage.py runserver.
    ```

    If everything is fine you will see the below warning message:

    ```zsh
    You have 19 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, blog, contenttypes, sessions, users.
    Run 'python manage.py migrate' to apply them.
    ```

    Just follow the instructions and run `python manage.py migrate` on the terminal.

    After the migrations are done, you will find a new file called `db.sqlite3` on `/my_website`. That's your database!

4. Start Working!

    Running the development server again should let you access the app on your machine. To access the /admin section you will have to create a superuser.

This App has been created following the [Django Course by Corey Schafer](https://www.youtube.com/watch?v=UmljXZIypDc&list=PL-osiE80TeTtoQCKZ03TU5fNfx2UY6U4p), which I totally recommend if you are starting with Django.
