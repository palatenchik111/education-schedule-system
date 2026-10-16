# 16. Правила ведения репозитория

Для проекта используются следующие основные ветки:

```text
main
develop
feature/*
fix/*
docs/*
```

## main

Содержит стабильную версию проекта.

## develop

Используется для объединения результатов разработки.

## feature/*

Используется для разработки новых функций.

Примеры:

```text
feature/schedule-crud
feature/conflict-check
feature/reference-management
feature/schedule-view
```

## fix/*

Используется для исправления дефектов.

Например:

```text
fix/conflict-time-validation
fix/schedule-filter
```

## docs/*

Используется при значительных изменениях документации.

Например:

```text
docs/project-artifacts
```

---

# 17. Правила коммитов

Один коммит должен содержать одно логически завершенное изменение.

Используются следующие обозначения:

```text
feat: новая функциональность
fix: исправление
docs: документация
test: тесты
refactor: изменение структуры кода
chore: техническое изменение
```

Примеры:

```text
docs: add project scope
docs: add architecture diagram
docs: describe module contracts
feat: add schedule DTOs
test: add conflict validation tests
```

Не допускаются малоинформативные сообщения:

```text
update
fix
work
123
изменения
```