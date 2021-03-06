# \# Test Impact Analysis для Android и JVM

По мере роста команды и продукта неумолимо начинает расти количество фич, которые находятся в разработке.
При всём при этом бизнес хочет все быстрее и быстрее доставлять новые функции до пользователей, а значит, 
вы должны каким-то образом ускорять регресс.

В этом нам здорово помогают автотесты. Но что делать, когда их становится слишком много? 
**2, 3, 4, 5, 10 тысяч тестов**, и всё это нужно где-то запускать прямо перед регрессом! А как это все поддерживать?

В этом нам помогает импакт-анализ — инструмент, который позволяет четко понимать, какой из тестов должен быть запущен на пулл-реквесте.

Я как раз написал такой инструмент — с помощью Jacoco и EmmaRT мы инструментируем байт-код, 
составляем карту загружаемых классов и методов во время исполнения теста, а затем, на пулл-реквесте, 
парсим <code-inline>git diff</code-inline> и понимаем, какие именно UI-тесты нам нужно будет запустить.

[overview]: <>

<iframe width="640" height="480" 
    src="https://www.youtube.com/embed/3FCeOL8kgZg">
</iframe>