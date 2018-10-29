<h1 align="center">Vue CLI Experiments</h1>

Репозиторий для экспериментов с Vue CLI

> В качестве менеджера пакетов используется [Yarn](https://yarnpkg.com/en/docs/install)

<h2 align="center">Основные команды</h2>

### Установка зависимостей

```
$ yarn
```

### Компиляция и горячая перезагрузка (development mode)
```
$ yarn serve
```

### Компиляция и минификация проекта (production mode)
```
$ yarn build
```

### Запуск всех тестов
```
$ yarn test
```

### Проверка и исправление ошибок в коде
```
$ yarn lint
```

### Запуск unit тестов
```
$ yarn test:unit
```

<h2 align="center">Список экспериментов</h2>

> Эксперименты разделены по категориям

#### Кастомные блоки

- [ ] Создать &lt;docs&gt; блок. Полезные ссылки: [vue-loader-v14](https://vue-loader-v14.vuejs.org/ru/configurations/custom-blocks.html), [vue-loader](https://vue-loader.vuejs.org/ru/guide/custom-blocks.html), [SFC](https://vue-loader.vuejs.org/ru/spec.html#%D0%B2%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5)
- [ ] Создать &lt;test&gt; блок при помощи [vue-test-loader](https://github.com/eddyerburgh/vue-test-loader)

#### Фрагменты

- [x] Протестировать при помощи функциональных компонентов и рендер-функции. Полезные ссылки: [Can A Vue Template Have Multiple Root Nodes (Fragments)?](https://vuejsdevelopers.com/2018/09/11/vue-multiple-root-fragments/)
- [ ] Протестировать при помощи [vue-fragment](https://github.com/y-nk/vue-fragment)

#### Шаблонизаторы и (пре/пост)процессоры

- [x] Проверить [Pug](https://github.com/pugjs/pug)
- [x] Проверить [Stylus](https://github.com/stylus/stylus)
- [x] Проверить [SugarSS](https://github.com/postcss/sugarss)

#### Медиа-разрешения

- [ ] Протестировать [vue-media](https://github.com/egoist/vue-media)
- [ ] Протестировать при помощи [vue-hooks](https://github.com/yyx990803/vue-hooks)

<h2 align="center">Лицензия</h2>

[MIT](/LICENSE)
