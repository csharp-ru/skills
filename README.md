# C# Skills

Навыки для AI-агентов, работающих с C# и .NET. Формат совместим с [skills CLI](https://github.com/vercel-labs/skills).

## Установка

Выбрать навыки и агента интерактивно:

```sh
npx skills add csharp-ru/skills
```

Установить отдельный навык можно с `--skill`. Например, C# Feature Development глобально:

```sh
npx skills add csharp-ru/skills --skill csharp-feature-development --global
```

Установить C# Backend Review глобально:

```sh
npx skills add csharp-ru/skills --skill csharp-backend-review --global
```

Для конкретного агента можно добавить `--agent codex` или выбрать его в интерактивном меню. Без `--global` навык устанавливается в текущий проект.

## Обновление

```sh
npx skills update csharp-backend-review --global
```

Обновить все глобально установленные навыки:

```sh
npx skills update --global
```

## Доступные навыки

| Навык | Назначение |
| --- | --- |
| [csharp-feature-development](skills/csharp-feature-development/SKILL.md) | Preflight, минимальная реализация и self-review backend-фичи с учетом правил команды. |
| [csharp-backend-review](skills/csharp-backend-review/SKILL.md) | Ревью C#/.NET backend: сложность, адаптеры, SQL, DI, контракты, тесты и готовность к review. |

## Использование

Например, в Codex:

```text
$csharp-feature-development изучи проект, подготовь минимальный план и реализуй новую backend-фичу
$csharp-backend-review проверь текущий diff перед code review
```

Навыки учитывают правила репозитория и не требуют одинаковой архитектуры от всех проектов. Разработка не заменяет независимое ревью. Сам навык не дает разрешение на commit, push или публикацию ответов от имени пользователя.

## Добавление навыков

Создайте `skills/<skill-name>/SKILL.md` с YAML-полями `name` и `description`. Имя каталога должно совпадать с `name`. Дополнительные материалы размещайте рядом с навыком и ссылайтесь на них из `SKILL.md`.

Публикуйте общие рекомендации без внутренних ссылок, персональных данных и деталей закрытых проектов.
