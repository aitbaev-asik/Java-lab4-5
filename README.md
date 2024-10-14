<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README - JSP-Servlet-JDBC-MySQL CRUD Tutorial</title>
</head>
<body>
    <h1>JSP-Servlet-JDBC-MySQL CRUD Tutorial</h1>

    <h2>Описание</h2>
    <p>
        Для Lab 4 and Lab 5 реализовал связку - CRUD + JSP + JDBC + MySQL
    </p>

    <h2>Требования</h2>
    <p>Перед тем как начать, убедитесь, что у вас установлено следующее:</p>
    <ul>
        <li><strong>Java JDK 8+</strong></li>
        <li><strong>Apache Tomcat 9+</strong></li>
        <li><strong>MySQL 5.7+</strong></li>
        <li><strong>Maven</strong> (для управления зависимостями)</li>
        <li><strong>Любая IDE</strong> (например, IntelliJ IDEA, Eclipse)</li>
    </ul>

    <h2>Шаги по установке и запуску</h2>

    <h3>1. Клонируйте репозиторий</h3>
    <pre>
        <code>
git clone https://github.com/username/jsp-servlet-jdbc-mysql-crud-tutorial.git
cd jsp-servlet-jdbc-mysql-crud-tutorial
        </code>
    </pre>

    <h3>2. Настройка MySQL</h3>
    <p>В проекте уже подготовлен скрипт для создания базы данных и таблицы. Вы можете найти его в папке <code>sql</code> в файле <code>create-user-table.sql</code>.</p>
    <p>Выполните этот скрипт в вашей MySQL консоли:</p>

    <pre>
        <code>
mysql -u root -p < sql/create-user-table.sql
        </code>
    </pre>

    <p>Этот скрипт создаст базу данных и таблицу пользователей:</p>
    <pre>
        <code>
CREATE DATABASE mydatabase;

USE mydatabase;

CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    country VARCHAR(100)
);
        </code>
    </pre>

    <h3>3. Настройка подключения к базе данных</h3>
    <p>Откройте файл <code>src/main/java/com/example/util/DBUtil.java</code> и измените параметры подключения к MySQL:</p>
    <pre>
        <code>
private static final String JDBC_URL = "jdbc:mysql://localhost:3306/mydatabase";
private static final String JDBC_USER = "root";  <!-- Замените на вашего пользователя MySQL -->
private static final String JDBC_PASSWORD = "your_password";  <!-- Замените на ваш пароль MySQL -->
        </code>
    </pre>

    <h3>4. Установка зависимостей</h3>
    <p>Скомпилируйте проект и установите все зависимости с помощью Maven:</p>
    <pre>
        <code>
mvn clean install
        </code>
    </pre>

    <h3>5. Развертывание на Tomcat</h3>
    <p>Выполните следующие шаги для развертывания:</p>
    <ul>
        <li>Скопируйте полученный WAR файл из директории <code>target</code> в директорию веб-приложений Tomcat (<code>webapps</code>).</li>
        <li>Запустите Tomcat:</li>
    </ul>

    <pre>
        <code>
catalina.bat run   <!-- Windows -->
./catalina.sh run  <!-- Linux/Mac -->
        </code>
    </pre>

    <h3>6. Доступ к приложению</h3>
    <p>Откройте браузер и перейдите по следующему адресу:</p>
    <pre>
        <code>
http://localhost:8080/jsp-servlet-jdbc-mysql-crud-tutorial
        </code>
    </pre>

    <p>Теперь вы можете использовать CRUD-приложение для управления пользователями в базе данных.</p>

    <h2>Используемые технологии</h2>
    <ul>
        <li><strong>JSP</strong> — для представления данных на веб-страницах.</li>
        <li><strong>Servlets</strong> — для обработки HTTP-запросов.</li>
        <li><strong>JDBC</strong> — для взаимодействия с базой данных MySQL.</li>
        <li><strong>MySQL</strong> — реляционная база данных.</li>
        <li><strong>Tomcat</strong> — веб-сервер для выполнения сервлетов и JSP.</li>
    </ul>

    <h2>Контакты</h2>
    <p>Если у вас есть вопросы или предложения, пожалуйста, свяжитесь со мной через email: <a href="mailto:ваш_email@example.com">ваш_email@example.com</a></p>
</body>
</html>
