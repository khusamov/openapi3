
Roadmap
=======

Минимальная версия инструментария
---------------------------------


Валидация JSON Schema (выбрать готовый)
    https://www.npmjs.com/package/ajv (нет возможности написать nullable)
    https://www.npmjs.com/package/jsonschema
    https://www.npmjs.com/package/z-schema
    https://github.com/acornejo/jjv
    https://github.com/geraintluff/tv4
    https://github.com/playlyfe/themis Добавление ключевого слова есть, а остальное под вопросом
    https://github.com/korzio/djv (addFormat невнятный)
    https://github.com/AlexeyGrishin/schemasaurus Старый и странный

	Реализация ключевого слова nullable для AJV:
		https://github.com/epoberezkin/ajv/issues/486#issuecomment-327989030

    Списки валидаторов:
        https://github.com/ebdrup/json-schema-benchmark
        http://json-schema.org/implementations.html
        https://github.com/json-schema-org/json-schema-org.github.io

    Критерии выбора валидатора:
        Проверить как ссылаться на внешние схемы из схемы. Это нужно для реализации полиморфных узлов (discriminator).
        Проверить как добавлять ключевые слова на примере nullable и discriminator
        придумать способ хранения схем
            Например можно пользоваться конвертером https://github.com/chaliy/sequelize-json-schema

Выбрать реализацию JSON Pointer и JSON Reference
	https://tools.ietf.org/html/draft-pbryan-zyp-json-ref-03
	https://tools.ietf.org/html/rfc6901
	https://www.npmjs.com/search?q=JSON+Pointer


Объектная модель JSON Schema
    А она нужна? 
        В OOM3 схема может хранится как простой объект. Для валидатора этого достаточно.
        А доступ к внутренним объектам схемы пока не нужен. И скорее всего не понадобится вовсе.
    Попробовать найти существующий вариант.
    Написать свой вариант:
        JSON Schema Object Model
        jsonschema-object-model-spec (JSOM)
        jsonschema-object-model

Объектная модель спецификации OpenAPI
    Попробовать найти существующий вариант.
    Написать свой вариант:
        OpenAPI 3 Object Model
        openapi3-object-model-spec (OOM3)
        openapi3-object-model
        Посмотреть 
            https://github.com/metadevpro/openapi3-ts/blob/master/src/model/OpenApi.ts
            https://www.npmjs.com/package/swagger-parser
            https://github.com/OAI/OpenAPI-Specification

Написать готовый сервер на основе Express
    express-openapi3
    openapi3-server
    Разбор шваггер протокола:
        Пример сервера и клиента Шваггер /temp/swagger-sample
        https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md
        https://www.npmjs.com/package/swagger
        https://www.npmjs.com/package/swagger-editor
        https://www.npmjs.com/package/swagger-jsdoc
        https://www.npmjs.com/package/swagger-router
        https://www.npmjs.com/package/swagger-express-router
        http://editor.swagger.io/
        http://petstore.swagger.io/


Минимально функциональная версия инструментария:
    Здесь можно уже пробовать создавать примеры серверов.





Расширенная версия инструментария
---------------------------------


Кодогенератор моделей данных для сервера sequelize на основе OpenAPI
    openapi3-to-sequelize-models

Кодогенератор моделей данных для клиента на основе OpenAPI

Кодогенератор библиотеки доступа к серверу для клиента

Написать редактор OpenAPI
    Примеры АПИ https://github.com/OAI/OpenAPI-Specification/tree/master/examples/v3.0
    Примеры готовых редакторов:
        Eclipse Editor for OpenAPI 2.0 and 3.0 https://github.com/RepreZen/KaiZen-OpenAPI-Editor
        Для OpenAPI v3 https://github.com/Mermade/openapi-gui
        Для Шваггер в2 https://studio.restlet.com/
        Для Шваггер в2 https://github.com/swagger-api/swagger-editor
    Список готовых редакторов можно посмотреть тут:
        https://github.com/OAI/OpenAPI-Specification/blob/master/IMPLEMENTATIONS.md

Написать или найти готовый редактор JSON Schema.

Создание REST-клиента для тестирования API:
    Временно вместо своего REST-клиента можно использовать:
        Postman 
            https://www.getpostman.com/
        Restlet Client 
            https://restlet.com/modules/client/
            https://chrome.google.com/webstore/detail/restlet-client-rest-api-t/aejoelaoggembcahagimdiliamlcdmfm
    Глянуть на эти произведения:
        https://github.com/swagger-api/swagger-UI (Browse and test a REST API described with the OpenAPI 3.0 Specification.)
        https://github.com/koumoul-dev/openapi-viewer (Web-Based interface for visualizing and testing OpenAPI\Swagger definitions)
        https://github.com/temando/open-api-renderer (A React renderer for Open API v3)


Расширение специального плагина express-openapi3 для Express:
    Passport (https://www.npmjs.com/package/passport-openapi)
    Sessions
    Cookies
    Sequelize 
    robots.txt

Прикрутить дюк https://github.com/senchalabs/jsduck





Расширенная версия Продолжение инструментария
---------------------------------

TODO факультатив:

    Типизация обработчиков событий:
    https://www.npmjs.com/package/ts-eventemitter
    https://github.com/tenry92/typed-event-emitter

    Полезные декораторы:
    https://github.com/jayphelps/core-decorators.js

    Асинхронные обработчики событий
    https://github.com/morrisallison/event-station/blob/master/docs/Usage.md#asynchronous-listeners

    Отличный пример приложения под экспресс
    https://github.com/Microsoft/TypeScript-Node-Starter#typescript-node-starter



