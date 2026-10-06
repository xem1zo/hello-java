# hello-java

Учебный проект с CI на GitHub Actions для Java-приложения.

## 📌 Цель работы

Познакомиться с Maven и Java CI, собрать минимальный Docker-образ.

## 🎯 Что узнали

- **Maven** — `pom.xml`, фазы `clean`, `verify`, `package`
- **JUnit 5** — написание и запуск тестов
- **Shade Plugin** — сборка «толстого» JAR с main-классом
- **Multi-stage Docker** — разделение сборки и запуска
- **GitHub Actions** — JDK, кэш Maven, docker build

## 📂 Структура проекта

```
hello-java/
├── .github/workflows/ci.yml
├── src/main/java/Hello.java
├── src/test/java/HelloTest.java
├── .gitignore
├── Dockerfile
├── pom.xml
└── README.md
```

## ☕ Основной код

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello from Java in Docker! ☕🐳");
        System.out.println("Java version: " + System.getProperty("java.version"));
        System.out.println("OS: " + System.getProperty("os.name"));
    }
}
```

## 🚀 Запуск локально

```bash
docker build -t hello-java .
docker run --rm hello-java
```

Ожидаемый вывод:
```
Hello from Java in Docker! ☕🐳
Java version: 17.0.x
OS: Linux
```

## ✅ Результат

При каждом push в `main` запускается CI.
На вкладке **Actions** — 🟢 зелёная галочка.

**Ссылка на Actions:**  
https://github.com/xem1zo/hello-java/actions

## 📝 Вывод

Освоил Maven (pom.xml, clean, verify, package), JUnit 5, Shade Plugin, multi-stage Docker и настройку CI для Java.