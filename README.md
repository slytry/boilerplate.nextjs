# Next.js 13 boilerplate
https://paulintrognon.fr/blog/typescript-prettier-eslint-next-js
## TODO

1. Storybook - подключение + eslint
2. Jest - подключение + eslint
3. Библиотека компонентов (react-aria)

## Как приступить к работе

## Структура папок

> Меняйте структуру папок до тех пор, пока вам и вашей команде не будет удобно

- components
- lib

## Технологии

### Пакетный менеджер (PNPM)

PNPM - быстрей yarn и темболее npm. Хранит общий кэш для пакетов на OS, что позволяет экономить место но диске

### Data fetching (React-Query + Axios)

Менеджеры состояний как redux, mobx хорошо работают с состояниями на стороне клиента, но не на стороне сервера. Это связано с тем, что состояние сервера сохраняется удаленно в месте, которое клиентская сторона не может контролировать, оно может устареть, и нам необходимо создать асинхронные API для извлечения и обновления.

React Query — одна из лучших библиотек для управления состоянием сервера. Это помогает нам извлекать, кэшировать, синхронизировать и обновлять данные, не касаясь какого-либо глобального состояния.

- [Practical React Query](https://tkdodo.eu/blog/practical-react-query) - серия качественый статей для обучения
- [React-Query SSR](https://tanstack.com/query/v4/docs/guides/ssr) - подключение в nextjs

**Почему axios, а не fetch?**

- Axios изоморфный
- В axios есть interseptors

### State manager (MST)

> "un-opinionated" section

Каждый инструмент хорош под задачу, но даже это не важно. Но мы в студии не делаем продукты как: figma, miro, facebook, tilda и т.д Нужды сайтов которые мы делаем практически всегда можно покрыть Context + React Query.

Но, если вы чувствуете что неудобно, рекомендую выбирать тот который вы лучше знаете, больше нравиться. Все они хороши.

Если опыта со стейт менеджерами нет и все равно какой учить - выбирайте effector. Самый свежий, новационный. По некоторый источникам еще и работать с ним приятно. Решает проблемы предыдущих менеджеров

**redux-toolkit**

- [redux-toolkit](https://redux-toolkit.js.org/)

Есть свой инструмент для работы c API - RTK Query. Некоторые компании уходят от React Query, потому что не могут справиться с инвалидацией. Возрвращаеются обратно на Redux.
Но вообще не рекомендую. В студии нет таких проектов. Если вы делает проект на котором стало сложно с React Query, то вам не нужна эта readme и вообще вам ничего не нужно, уж все умеете/

**MobX-State-Tree**

- [MobX-State-Tree](https://mobx-state-tree.js.org/intro/welcome)

Улучешния верси Mobx. На чистом Mobx надо заботиься об архитектуре. Качественный код на Mobx написать сложнее чем на RTK. MobX-State-Tree предоставялет типы и архитектуру

**effector**

- [effector](https://mobx-state-tree.js.org/intro/welcome)
  - [Лучшая часть Эффектора](https://community.effector.dev/core/best-part-4jb1)
  - [Игорь Камышев — Как и зачем мы мигрировали Авиасейлс на Effector](https://www.youtube.com/watch?v=HYaSnVEZiFk)

### I18N (next-i18next)

Интернационализация реализуется втроенный в nextjs [Internationalized Routing](https://nextjs.org/docs/advanced-features/i18n-routing#limits-for-the-i18n-config) функционалом и библиотекой [next-i18next](https://github.com/i18next/next-i18next).


### Mocks (MSW)

## Это бибилиотеки могут быть полезны

