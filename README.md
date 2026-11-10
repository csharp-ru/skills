# C# Skills

Навыки для AI-агентов, работающих с C# и .NET. Формат совместим с [skills CLI](https://github.com/vercel-labs/skills).

## Установка

Выбрать навыки и агента интерактивно:

```sh
npx skills add csharp-ru/skills
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
| [csharp-backend-review](skills/csharp-backend-review/SKILL.md) | Ревью C#/.NET backend: границы адаптеров, HTTP-контракты, DI, EF Core, транзакции и проверки. |

## Использование

Например, в Codex:

```text
$csharp-backend-review проверь текущий diff перед code review
```

Навык учитывает правила репозитория и не требует одинаковой архитектуры от всех проектов. Ревью не дает агенту разрешение менять код, делать commit, push или отвечать от имени пользователя.

## Добавление навыков

Создайте `skills/<skill-name>/SKILL.md` с YAML-полями `name` и `description`. Имя каталога должно совпадать с `name`. Дополнительные материалы размещайте рядом с навыком и ссылайтесь на них из `SKILL.md`.

Публикуйте общие рекомендации без внутренних ссылок, персональных данных и деталей закрытых проектов.
