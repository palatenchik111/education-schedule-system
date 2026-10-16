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

### Правила слияния (Merge)
1. Слияние в ветку `develop` или `main` выполняется только через Pull Request (или эквивалентный процесс ревью).
2. Перед слиянием ветка должна быть актуализирована относительно целевой ветки (`git rebase main` или `git merge main`).
3. Запрещено прямое добавление коммитов в `main` и `develop`.

### Разрешение конфликтов
1. При возникновении конфликта слияния, разработчик обязан локально разрешить его, сохранив логику обоих изменений или выбрав корректную.
2. После разрешения конфликта необходимо выполнить `dotnet build` и `dotnet test` для подтверждения работоспособности.
3. Коммит разрешения конфликта должен иметь сообщение: `fix: resolve merge conflict in <file_name>`.

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