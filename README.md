# Recipe API Project

This is a Django project template for a Recipe API with Docker setup and GitHub Actions for continuous integration. The project provides a RESTful API for managing recipes and ingredients.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Python](https://www.python.org/) (for local development)

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/danicavuck/recipe-app-api.git
   cd recipe-app-api
   ```

2. Build and run the Docker containers:

   ```bash
   docker-compose up --build
   ```

   This command will build the Docker images and start the containers.

3. Access the Django development server at [http://localhost:8000/](http://localhost:8000/recipe-app-api/app)

## Django Commands

- **Run Migrations:**
  ```bash
  docker-compose run app sh -c "python manage.py migrate"
  ```

- **Create Superuser:**
  ```bash
  docker-compose run app sh -c "python manage.py createsuperuser"
  ```

- **Run Tests:**
  ```bash
  docker-compose run app sh -c "python manage.py test"
  ```

## API Endpoints

- **List Recipes:**
  `GET /app/recipes/`

- **Retrieve Recipe:**
  `GET /app/recipes/{recipe_id}/`

- **Create Recipe:**
  `POST /app/recipes/`

- **Update Recipe:**
  `PUT /app/recipes/{recipe_id}/`

- **Delete Recipe:**
  `DELETE /app/recipes/{recipe_id}/`

- **List Ingredients:**
  `GET /app/ingredients/`

- **Retrieve Ingredient:**
  `GET /app/ingredients/{ingredient_id}/`

- **Create Ingredient:**
  `POST /app/ingredients/`

- **Update Ingredient:**
  `PUT /app/ingredients/{ingredient_id}/`

- **Delete Ingredient:**
  `DELETE /app/ingredients/{ingredient_id}/`

## GitHub Actions

The repository is configured with GitHub Actions to run tests on every push. The workflow configuration is in the `.github/workflows/checks.yml` file.

## Customization

- Modify the Django app code in the `app` directory.
- Adjust the Docker configuration in the `Dockerfile` and `docker-compose.yml` files.
- Customize GitHub Actions workflow according to your project requirements.
