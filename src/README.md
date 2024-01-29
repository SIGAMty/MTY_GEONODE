# MTY_GEONODE

## Requirements

- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Instalación

1. Clonar el repositorio:

    ```bash
    git clone
    ```

2. Crear el `.env`:

    ```bash
    python create-envfile.py
    ```

3. Construir los contenedores:

    Puede tardar +10Min

    ```bash
    docker-compose build
    ```

## Uso

4. Correr los contenedores:

    ```bash
    docker-compose up -d
    ```

5. Crear las migraciones:

    ```bash
    docker-compose exec geonode python manage.py makemigrations
    ```

    ```bash
    docker-compose exec geonode python manage.py migrate
    ```

6. Crear un superuser:

    ```bash
    docker-compose exec geonode python manage.py createsuperuser
    ```

7. Collect static:

    ```bash
    docker-compose exec geonode python manage.py collectstatic --noinput
    ```

8. Restart a los contenedores:

    ```bash
    docker-compose restart
    ```

9. Open the browser and go to `http://localhost:80`