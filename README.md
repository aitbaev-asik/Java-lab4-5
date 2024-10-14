<div style="font-family: Arial, sans-serif;">

<div style="margin-bottom: 30px;">
    <h1>JSP-Servlet-JDBC-MySQL CRUD Tutorial</h1>
</div>

<div style="margin-bottom: 30px;">
    <h2>Описание</h2>
    <p>
        Этот проект представляет собой простое CRUD-приложение с использованием JSP, Servlets, JDBC и базы данных MySQL.
        CRUD операции включают создание, чтение, обновление и удаление данных. Приложение подключается к MySQL с помощью JDBC
        и взаимодействует с базой данных для выполнения этих операций.
    </p>
</div>

<div style="margin-bottom: 30px;">
    <h2>Требования</h2>
    <p>Перед тем как начать, убедитесь, что у вас установлено следующее:</p>
    <ul>
        <li><strong>Java JDK 8+</strong></li>
        <li><strong>Apache Tomcat 9+</strong></li>
        <li><strong>MySQL 5.7+</strong></li>
        <li><strong>Maven</strong> (для управления зависимостями)</li>
        <li><strong>Любая IDE</strong> (например, IntelliJ IDEA, Eclipse)</li>
    </ul>
</div>

<div style="margin-bottom: 30px;">
    <h2>Шаги по установке и запуску</h2>

    <div style="margin-bottom: 20px;">
        <h3>1. Клонируйте репозиторий</h3>
        <pre style="background-color: #f4f4f4; padding: 10px;">
<code>git clone https://github.com/username/jsp-servlet-jdbc-mysql-crud-tutorial.git
cd jsp-servlet-jdbc-mysql-crud-tutorial</code>
        </pre>
    </div>

    <div style="margin-bottom: 20px;">
        <h3>2. Настройка MySQL</h3>
        <p>В проекте уже подготовлен скрипт для создания базы данных и таблицы. Вы можете найти его в папке <code>sql</code> в файле <code>create-user-table.sql</code>.</p>
        <p>Выполните этот скрипт в вашей MySQL консоли:</p>
        <pre style="background-color: #f4f4f4; padding: 10px;">
<code>mysql -u root -p < sql/create-user-table.sql</code>
        </pre>
    </div>

    <div style="margin-bottom: 20px;">
        <h3>3. Настройка подключения к базе данных</h3>
        <p>Откройте файл <code>src/main/java/com/example/util/DBUtil.java</code> и измените параметры подключения к MySQL:</p>
        <pre style="background-color: #f4f4f4; padding: 10px;">
<code>private static final String JDBC_URL = "jdbc:mysql://localhost:3306/mydatabase";
private static final String JDBC_USER = "root";  // замените на вашего пользователя MySQL
private static final String JDBC_PASSWORD = "your_password";  // замените на ваш пароль MySQL</code>
        </pre>
    </div>

    <div style="margin-bottom: 20px;">
        <h3>4. Установка зависимостей</h3>
        <p>Скомпилируйте проект и установите все зависимости с помощью Maven:</p>
        <pre style="background-color: #f4f4f4; padding: 10px;">
<code>mvn clean install</code>
        </pre>
    </div>

    <div style="margin-bottom: 20px;">
        <h3>5. Развертывание на Tomcat</h3>
        <ul>
            <li>Скопируйте полученный WAR файл из директории <code>target</code> в директорию веб-приложений Tomcat (<code>webapps</code>).</li>
            <li>Запустите Tomcat:</li>
        </ul>
        <pre style="background-color: #f4f4f4; padding: 10px;">
<code>catalina.bat run   <!-- Windows -->
./catalina.sh run  <!-- Linux/Mac --></code>
        </pre>
    </div>

    <div style="margin-bottom: 20px;">
        <h3>6. Доступ к приложению</h3>
        <p>Откройте браузер и перейдите по следующему адресу:</p>
        <pre style="background-color: #f4f4f4; padding: 10px;">
<code>http://localhost:8080/jsp-servlet-jdbc-mysql-crud-tutorial</code>
        </pre>
    </div>
</div>

<div style="margin-bottom: 30px;">
    <h2>Используемые технологии</h2>
    <ul>
        <li><strong>JSP</strong> — для представления данных на веб-страницах.</li>
        <li><strong>Servlets</strong> — для обработки HTTP-запросов.</li>
        <li><strong>JDBC</strong> — для взаимодействия с базой данных MySQL.</li>
        <li><strong>MySQL</strong> — реляционная база данных.</li>
        <li><strong>Tomcat</strong> — веб-сервер для выполнения сервлетов и JSP.</li>
    </ul>
</div>

<div style="margin-bottom: 30px;">
    <h2>Контакты</h2>
    <p>Если у вас есть вопросы или предложения, пожалуйста, свяжитесь со мной через email: <a href="mailto:ваш_email@example.com">ваш_email@example.com</a></p>
</div>

</div>
