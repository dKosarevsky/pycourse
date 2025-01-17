# главная

```
 __      ___       __         __  ___   __   __   __  
|__) \_/  |  |__| /  \ |\ |  /  \  |   /  \ |  \ (_    /\  |
|     |   |  |  | \__/ | \|  \__/  |   \__/ |__/ __) ./--\ |
```

!!! danger "о чём это всё"

    В этом чудесном месте планируется затронуть основные моменты Python (с упором на машинное обучение): база, как работать с основными библиотеками, что есть правильный код, асинхронность, тесты и т.д. и т.п. Кто-то без умолку уронит замечание, дескать, этого всего сполна, но тут упор делаем на примеры в той самой промышленности. Будем рады любой помощи в составлении материалов, практики и иного доброго словца – [contributing.md](https://github.com/open-data-science/pycourse/blob/master/contributing.md).

    Проект вот запустился и находится в стадии разработки «основы python».

    [Посмотреть прогресс курса](https://github.com/orgs/open-data-science/projects/1/views/1){ .md-button .md-button--primary }

----

Python есть такой язык программирования, который позволяет сообщить компьютеру о том, что нужно сделать, чтобы достичь некоего результата. За последнее десятилетие он получил быстрое распространение и сейчас является одним из самых популярных языков программирования в мире. Входной порог для его использования достаточно низок: можно использовать Python для решения своих задач даже если никогда не имели дела с программированием.

## Что такое Python?

Python – это язык программирования ^^общего назначения^^, используемый во многих приложениях, например:

- [x] разработка веб-приложений
- [x] создание игр
- [x] продвинутая аналитика данных, в том числе с использованием нейронных сетей
- [x] компьютерная графика
- [x] геофизика
- [x] психология
- [x] химия
- [x] теория графов

Python используют практически все крупные компании, о которых слышим каждый день: Сбер, Авито, Лента, VK, МТС, Мегафон, Miro, Лаборатория Касперского, Яндекс.. список можно продолжать почти что бесконечно.

<figure markdown>
  ![](./assets/blackhole.png)
  <figcaption>
  [Рассчитанная в Python симуляция преломлений света черной дырой](https://github.com/Python-simulation/Black-hole-simulation-using-python)
  </figcaption>
</figure>

## Чем примечателен Python?

В основе разностороннего применения и популярности лежит ^^простота изучения^^: всё чаще люди начинают свой путь в программировании с Python, поскольку он очень ^^дружелюбен к новичкам^^ и позволяет максимально быстро перейти к решению целевой задачи.

Сюда же можно отнести ^^многообразие библиотек^^ (или _расширений функциональности_, то есть кода, написанного другими людьми, который можно переиспользовать). Хотите изучить физику небесных тел и симулировать их взаимодействия? Можно найти и скачать библиотеку, позволяющую за один вечер провести вычисления, о которых в прошлом веке можно было лишь мечтать. Хотите создать прототип мобильного приложения? И на этот случай есть библиотека. Вам нравится квантовая физика и хотите использовать её вместе с умными компьютерными алгоритмами? Что ж, тогда снова по адресу.

<figure markdown>
  ![](./assets/aero_python.png)
  <figcaption>
  [Пример моделирования аэродинамики в Python с помощью библиотеки AeroPython](https://lorenabarba.com/blog/announcing-aeropython/)
  </figcaption>
</figure>

Python – это ^^высокоуровневый язык для быстрой разработки и/или прототипирования^^, на нем очень удобно проверять гипотезы и идеи. «_Высокоуровневый_» означает, что не нужно вникать в устройство компьютера и тонкости взаимодействия с ним, чтобы перейти к задаче. Многое «сделано за нас»: работаем с простыми _абстракциями_ (или удобными представлениями), а не боремся с компьютером из-за непонимания сложностей его устройства.

Еще один плюс в копилку популярности языка – это ^^элегантность и краткость синтаксиса^^ (принципов написания кода, как будто это абзацы в тексте или колонки в газете). Вместе с вышеупомянутым обилием библиотек можно буквально за 5 минут и 10 строк кода – а это меньше половины листа А4 – воспроизвести научную статью, в которую вложено несколько человеко-лет. А еще такой синтаксис делает ^^код легким для чтения, запоминания и понимания^^.

Стоит отметить, что Python – это ^^интерпретируемый^^ язык, а значит, компьютер каждый раз перед выполнением программы читает код строчку за строчкой и определяет (интерпретирует), что нужно сделать дальше, не проводя никаких оптимизаций и предварительных расчетов. Это негативно влияет на общую скорость работы: Python является одним из самых медленных языков. Тем не менее он отлично подходит для академических целей, например, исследовательской работы или других задач, где скорость работы не является критически важной. Настоящая сила Python заключается в том, что это ^^«язык-клей»^^: он обеспечивает удобный доступ к различным библиотекам, написанным на высокоэффективных языках, например, на C/C++, Fortran, CUDA C и других.

## И в чем подвох?

В простоте языка и его доступности для быстрого старта таится одна из проблем: _можно не понимать, что происходит внутри_, поэтому иногда бывает сложно разобраться в причинах ошибок и неточностей, возникающих по ходу работы над задачей. В целом к Python применим следующий принцип: «легко научиться, трудно овладеть». Возвращаясь к примеру элегантности кода, когда 10 строк кода выполняют всю работу: важно понимать, что за ними стоят еще _сотни_ или даже _тысячи строк кода_, а это может приводить к ситуациям, когда поиск ошибки в минимальном наборе команд растягивается на несколько дней.

## Интересные факты

Еще немного дополнительной информации про Python:

- Разработчик языка Гвидо ван Россум назвал его в честь популярного британского комедийного телешоу 1970-х «Летающий цирк Монти Пайтона»
- Актуальной версией Python считаются версии `3.6` и выше (`3.7`, `3.8.12`..). Долгое время (до 2020) года существовал `Python2`, который ныне не поддерживается и не обновляется. Если видите кусок кода на `Python2` и вам предстоит работать с ним, возможно, сначала придется его переписать, хотя большая часть кода имеет совместимость и работает корректно. Естественно тут не будем изучать `Python2`
- Довольно огромное сообщество: большинство проблем, с которыми можете столкнуться, уже было озвучено и даже решено. Это означает, что используя поисковик, можете решить практически все проблемы в течение 10-30 минут. Главное – научиться правильно формулировать свои вопросы
- При работе с Python следует придерживаться принципа «должен существовать один и, желательно, только один очевидный способ сделать это». Другие принципы (`Дзен Питона`) на русском языке – [по ссылке](https://tyapk.ru/blog/post/the-zen-of-python)
- Python – это ^^открытый проект^^, в который каждый может внести изменения (но они должны быть предварительно одобрены), например, [тут](https://mail.python.org/archives/list/python-ideas@python.org/)
- Есть целый набор рекомендаций и предложений по улучшению кода (`PEP`, [Python Enhancement Proposals](https://www.python.org/dev/peps/)). Они содержат указания на то, как следует писать код и чего стоит избегать, а также дискуссии о будущих изменениях в языке
- Язык постоянно развивается, в нем появляются новые возможности, улучшается производительность (скорость выполнения)
- Сборник всех существующих в открытом доступе библиотек находится по адресу [pypi.org](https://pypi.org/)
- Если столкнетесь с багом (системной ошибкой, вызванной внутренним механизмом языка), то сообщить об этом можно [на специальном сайте](https://bugs.python.org/)
