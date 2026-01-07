## MySQL Local Setup

1. Install MySQL Server (8.x)
2. Create database:
   CREATE DATABASE cricket_db;
3. Create user:
   CREATE USER 'root'@'localhost' IDENTIFIED BY 'SV01@joshic';
4. Grant privileges:
   GRANT ALL PRIVILEGES ON cricket_db.* TO 'cricket_user'@'localhost';

5. Update Django settings:
   ENGINE: django.db.backends.mysql
   NAME: cricket_db
   USER: cricket_user
   PORT: 3306

6. Run migrations:
   python manage.py migrate
