# 5. Архитектурная схема

Для проекта выбрана модульная архитектура.

```mermaid
flowchart TB
    User(["Пользователь"])
    
    subgraph Host ["ASP.NET Core API Host"]
        Api["ApiHost"]
        
        subgraph Modules ["Модули"]
            Schedule["ScheduleModule"]
            Conflict["ConflictModule"]
            Reference["ReferenceModule"]
        end
    end
    
    User -->|HTTP| Api
    Api --> Schedule
    Api --> Reference
    Schedule -->|"проверка конфликтов"| Conflict
    Schedule -->|"проверка справочных данных"| Reference
```

Центральным модулем бизнес-процесса является `ScheduleModule`.

При создании заказа он:

1. получает справочные данные;
2. проверяет существование группы, преподавателя, дисциплины и аудитории;
3. проверяет конфликты;
4. сохраняет занятие;
5. при необходимости публикует расписание.