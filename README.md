### Инструкция по запуску тестов:

**Запуск SUT**
1. Склонировать проект и открыть его в приложении IntelliJ IDEA.
2. В терминале IntelliJ IDEA с помощью команды`docker-compose up` разворачиваем контейнер, необходимый для дальнейшей работы.

**Запуск SUT с поддержкой БД:**

- _MySQL:_ в новом окне терминала запустить SUT командой `java -jar artifacts/aqa-shop.jar --spring.profiles.active=mysql`

- _PostgreSQL:_ в новом окне терминала запустить SUT командой `java -jar artifacts/aqa-shop.jar --spring.profiles.active=postgresql`

**Запуск тестов**

- _Для БД MySQL:_ в новом окне терминала запустить тесты командой `./gradlew test -DdbUrl=jdbc:mysql://localhost:3306/app-db`

- _Для БД PostgreSQL:_ в новом окне терминала запустить тесты командой` ./gradlew test -DdbUrl=jdbc:postgresql://localhost:5432/app-db`

**Завершение работы приложения**
1. Остановить работу SUT комбинацией клавиш `Ctrl+C`.
2. Остановить контейнер командой `docker-compose down`.
