
# TNR-R - This needs to be remembered [react]
## Эта таблица показывает, в какие моменты вызываются хуки в различных фазах жизненного цикла компонента: монтирование, обновление и размонтирование.  
### Mounting (Монтирование)
| Хук            | Описание                                       |
|----------------|------------------------------------------------|
| `useEffect`    | Выполняется после отрисовки компонента и обновления DOM.       |
| `useLayoutEffect` | Выполняется синхронно перед отрисовкой компонента и обновлением DOM.|

### Updating (Обновление)
| Хук            | Описание                                       |
|----------------|------------------------------------------------|
| `useEffect`    | Выполняется после каждого рендера компонента, если изменились указанные зависимости.       |
| `useLayoutEffect` | Выполняется синхронно после каждого рендера компонента, если изменились указанные зависимости.|
 
### Unmounting (Размонтирование)
| Хук            | Описание                                       |
|----------------|------------------------------------------------|
| `useEffect`    | Выполняется перед удалением компонента из DOM.       |
| `useLayoutEffect` | Выполняется синхронно перед удалением компонента из DOM.|
---------------------
**Различные примеры:**

 - Реализация получения данных с сервера через хук useLayoutEffect | [ CODE ](https://codesandbox.io/s/quizzical-glade-gcsklv?file=/src/App.js) | [ DEMO ](https://gcsklv.csb.app/)

-------------------------------------------------------
# Таблица всех хуков в библиотеке react и react-dom
## React 18 Хуки

| Hook | Description |
| --- | --- |
| `useCallback` | `useCallback` - это хук React, который позволяет кэшировать определение функции между повторными рендерами. Вызовите `useCallback` на верхнем уровне вашего компонента, чтобы кэшировать определение функции между повторными рендерами. |
| `useContext` | `useContext` - это хук React, который позволяет читать и подписываться на контекст из вашего компонента. Вызовите `useContext` на верхнем уровне вашего компонента, чтобы прочитать и подписаться на контекст. |
| `useDebugValue` | `useDebugValue` - это хук React, который позволяет добавить метку к пользовательскому хуку в React DevTools. Вызовите `useDebugValue` на верхнем уровне вашего пользовательского хука, чтобы отобразить читаемое значение отладки. |
| `useDeferredValue` | Основная цель `useDeferredValue` - позволить вам управлять приоритетами и тем, какие обновления могут быть отложены в вашем пользовательском хуке. Это особенно полезно для оптимизации производительности пользовательского хука и логики получения данных. |
| `useEffect` | `useEffect` - это хук React, который позволяет вам выполнять побочные эффекты в функциональных компонентах. Он заменяет методы жизненного цикла `componentDidMount`, `componentDidUpdate` и `componentWillUnmount` в классовых компонентах. |
| `useId` | `useId` - это хук React, который генерирует уникальный идентификатор для компонента. Это может быть полезно для ассоциации элементов формы с их метками. |
| `useImperativeHandle` | `useImperativeHandle` - это хук React, который позволяет родительским компонентам взаимодействовать с функциональными дочерними компонентами, используя ref. Он позволяет вам выбирать, какие значения будут доступны для родительского компонента, когда он использует ref, чтобы получить доступ к дочернему компоненту. |
| `useInsertionEffect` | `useInsertionEffect` - это хук React, который используется для выполнения побочных эффектов после того, как все DOM-мутации прошли (например, после вставки, обновления или удаления элементов). |
| `useLayoutEffect` | `useLayoutEffect` - это хук React, который такой же, как `useEffect`, но он запускается синхронно после всех мутаций DOM. Используйте этот хук, если вам нужно мутировать DOM и затем выполнять измерения. |
| `useMemo` | `useMemo` - это хук React, который возвращает мемоизированное значение. `useMemo` будет повторно вычислять мемоизированное значение только тогда, когда одно из зависимых значений изменилось. Это может быть полезно при оптимизации производительности. |
| `useReducer` | `useReducer` - это хук React, который принимает редуктор и начальное значение состояния и возвращает текущее состояние и функцию dispatch. Это альтернатива `useState` и более предпочтительна, когда состояние сложное или содержит множество подзначений. |
| `useRef` | `useRef` - это хук React, который позволяет создавать и использовать ссылки на элементы или переменные. Он возвращает изменяемый ref-объект, свойство `.current` которого инициализируется переданным аргументом (`initialValue`). |
| `useState` | `useState` - это хук React, который позволяет добавить состояние в функциональные компоненты. `useState` принимает начальное значение и возвращает массив, содержащий текущее значение и функцию для его обновления. |
| `useSyncExternalStore` | `useSyncExternalStore` - это хук React, который позволяет вам использовать внешнее (не React) хранилище внутри своих компонентов и подписываться на обновления этого хранилища. |
| `useTransition` | `useTransition` - это хук React, который позволяет управлять анимациями или переходами при изменении состояния. Он позволяет указывать, какие обновления можно отложить и какие обновления нужно выполнить немедленно. |


## React-DOM Хуки

| Хук                | Описание                                                                                     |
|--------------------|----------------------------------------------------------------------------------------------|
| `useSelection`     | Хук для получения информации о выделении текста.                                              |
| `useScroll`        | Хук для отслеживания прокрутки контейнера.                                                    |
| `useSwipeable`     | Хук для обработки событий смахивания.                                                         |
| `useMedia`         | Хук для отслеживания состояния медиа.                                                         |
| `useSound`         | Хук для управления звуковым воспроизведением.                                                 |
| `useMeasure`       | Хук для измерения размеров элементов.                                                         |
| `useGeolocation`   | Хук для получения геолокации устройства.                                                      |
| `useNetworkStatus` | Хук для отслеживания состояния сети.                                                          |
| `useIdle`          | Хук для определения активности пользователя.                                                  |
| `useBattery`       | Хук для отслеживания состояния заряда батареи.                                                 |
| `useBeforeUnload`  | Хук для обработки события `beforeunload`, которое происходит перед выгрузкой страницы.        |


