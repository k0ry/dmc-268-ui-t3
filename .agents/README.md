# AI-разработка frontend: учебный набор команды

AGENTS.md создаёт техлид. Этот пакет даёт скиллы, правила и шаблоны под задачи спринта; не заменяет инструкции рабочей ветки.

| Задача | Что открыть |
| --- | --- |
| Изменить React/TypeScript код | [reviewer-frontend](skills/reviewer-frontend/SKILL.md) |
| Проверить поведение | [reviewer-frontend-tests](skills/reviewer-frontend-tests/SKILL.md) |
| Понять архитектуру и решения | [правила](rules/frontend.md) |
| Подготовить запрос агенту | [реализация](templates/implement.md), [тест-план](templates/test-plan.md), [PR](templates/pull-request.md) |
| Практика | [упражнение](learning.md) |

Пример: «Прочитай `.agents/skills/reviewer-frontend/SKILL.md` и выполни issue #N; объясни контракт ответа и покажи фактические проверки». Если редактор не поддерживает project skills, приложите SKILL.md и его ссылки вручную.

Проверено 2026-09-10, исходный main `a7e6ed8`: React 18, TypeScript strict, Vite; scripts `dev`, `build`, `preview`. ESLint, Vitest, Zod, Zustand и pnpm-lock.yaml пока отсутствуют. Команда `pnpm build` требует предварительно установленных зависимостей. `pnpm test`, `pnpm lint` пока не определены. `vite test` из задания понимаем как Vitest, а не реальную команду Vite.

Файлы `templates/*.example` — учебные исходники для переноса после отдельной настройки Zod/Vitest. Сейчас они не входят в сборку и не являются готовой интеграцией backend. Не используйте frozen-lockfile, пока команда не добавит актуальный lockfile. Версию Node согласовать и закрепить отдельно; её нет в текущем manifest.

Общие инварианты и системные промпты AI-ревью ведутся в [backend .agents](https://github.com/larchanka-training/dmc-268-api-t3/tree/main/.agents). До merge backend PR эта ссылка может быть недоступна: используйте соответствующую ветку PR. Frontend не хранит отдельную копию системного промпта, чтобы форматы не расходились.
