# WordPress Docker Template

This repository serves as a default template for setting up a WordPress environment using Docker. It includes WordPress, MySQL, and phpMyAdmin services configured via Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. **Clone the repository:**

    ```sh
    git clone https://github.com/your-username/wordpress-template.git
    cd wordpress-template
    ```

2. **Create a `.env` file:**

    Create a `.env` file in the root directory of the project with the following content:

    ```plaintext
    MYSQL_ROOT_PASSWORD=your_mysql_root_password
    MYSQL_DATABASE=your_mysql_database
    MYSQL_USER=your_mysql_user
    MYSQL_PASSWORD=your_mysql_password
    WORDPRESS_DB_USER=your_mysql_user
    WORDPRESS_DB_PASSWORD=your_mysql_password
    WORDPRESS_DB_NAME=your_mysql_database
    ```

3. **Build and start the containers:**

    ```sh
    docker-compose up -d
    ```

4. **Access the services:**

    - WordPress: [http://localhost:8000](http://localhost:8000)
    - phpMyAdmin: [http://localhost:8080](http://localhost:8080)

## Directory Structure

- `db_data/`: MySQL data directory (ignored by Git and Docker)
- `wordpress/`: WordPress data directory (ignored by Git and Docker)
- `.env`: Environment variables file (ignored by Git and Docker)
- `docker-compose.yaml`: Docker Compose configuration file

## Customization

You can customize the services by modifying the `docker-compose.yaml` file and the environment variables in the `.env` file.

## Security

Sensitive information such as database credentials is stored in the `.env` file, which is ignored by Git to prevent accidental exposure.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.