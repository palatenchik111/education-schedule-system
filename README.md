# 14. Инструкция сборки и запуска

## Требования

Для запуска проекта необходимы:

- .NET SDK 9;
- Git.

Проверка версии .NET:

```bash
dotnet --version
```

---

## Получение проекта

```bash
git clone <адрес-репозитория>
cd ElectronicSchedule
```

---

## Восстановление зависимостей

```bash
dotnet restore
```

---

## Сборка

```bash
dotnet build
```

---

## Выполнение тестов

```bash
dotnet test
```

---

## Запуск

```bash
dotnet run --project src/ElectronicSchedule.Api
```

После запуска API становится доступно по адресу, указанному приложением в консоли.
