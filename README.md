
### Prerequisites

What things you need to install the software:

- Docker
- PHP
- Composer

### Installing and Running

A step-by-step series of examples that tell you how to get a development environment running:

1. **Install Dependencies**:  
   Run `composer install` in the project directory to install PHP dependencies.

2. **Set Up the Environment File**:
   - Create a `.env` file based on `.env.example`.
   - Set your database and other environment configurations in the `.env` file.

3. **Start MySQL with Docker**:
   - Run the following command to start a MySQL container:
     ```bash
     docker run --name mysql-laravel -e MYSQL_ROOT_PASSWORD=yourpassword -e MYSQL_DATABASE=laravel -e MYSQL_USER=user -e MYSQL_PASSWORD=secret -p 3306:3306 -d mysql:latest
     ```
   - Make sure the credentials match those in your `.env` file.

4. **Run Migrations** (Optional):
   - If your application uses a database, run `php artisan migrate` to set up your database tables.

5. **Clear Cache if Necessary**:
   - If you encounter any problems, run `php artisan config:clear` to clear the configuration cache.

6. **Run the Application**:
   - Use `php artisan serve` to start the Laravel application.
   - Access it at `http://localhost:8000`.

## Notes

- Make sure Docker is running before starting the MySQL container.
- Adjust the `.env` file settings according to your local environment.

