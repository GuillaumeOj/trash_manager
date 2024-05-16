FROM python:3.12

RUN pip install poetry==1.8.2

WORKDIR /app

COPY pyproject.toml poetry.lock ./
COPY trash_manager ./trash_manager

RUN poetry install --no-root

ENTRYPOINT ["poetry", "run", "trash_manager/manage.py", "runserver"]
