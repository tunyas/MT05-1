# Проект №5 — Front-end тестирование 

Привет, участник Школы 21! В этом проекте мы наконец познакомимся с такими понятиями, как Front-end и Back-end, разберёмся с тем, как устроены современные веб-приложения и как их необходимо тестировать. 😇

## Instructions

Новая команда и новый групповой проект! Распределяйте задачи в команде так, чтобы добиться максимальной эффективности. Тимлида также должен отслеживать процесс выполнения заданий.

Напоминаем, что все созданные отчёты и файлы вам нужно будет загрузить в папку `src/` в корне проекта (обязательно в ветку _develop_). 

## Contents 

1. [Chapter I](#chapter-i) \
    1.1. [Общая инструкция](#общая-инструкция) 
2. [Chapter II](#chapter-ii) \
    2.1. [Веб-приложения](#веб-приложения) \
    2.2. [Клиент-серверное взаимодействие](#клиент-серверное-взаимодействие) \
    2.3. [Front-end и Back-end](#front-end-и-back-end) \
    2.4. [Задание №1](#задание-1-mpa-spa-pwa) \
    2.5. [Задание №2](#задание-2-архитектура) 
3. [Chapter III](#chapter-iii) \
    3.1. [Основные Frontend технологии](#основные-frontend-технологии) \
    3.2. [HTML](#html) \
    3.3. [JavaScript](#javascript) \
    3.4. [XPath](#xpath) \
    3.5. [Задание №3](#задание-3-xml-html-и-xpath) 
4. [Chapter IV](#chapter-iv) \
    4.1. [UX/UI](#uxui) \
    4.2. [Задание №4](#задание-4-ui-тестирование) 

<h2 id="chapter-i">Chapter I</h2> 

<h3 id="общая-инструкция">Общая инструкция</h3>

Методология Школы 21 может быть не похожа на тот образовательный опыт, который случался с тобой ранее. Её отличает высокий уровень автономии: у тебя есть задача, ты должен её выполнить. По большей части тебе нужно будет самому добывать знания для её решения. Второй важный момент — это peer-to-peer обучение. В образовательном процессе нет менторов и экспертов, перед которыми ты защищаешь свой результат. Ты это делаешь перед таким же учащимися, как и ты сам. У них есть чек-лист, который поможет им качественно выполнить приемку вашей работы.

Роль Школы 21 заключается в том, чтобы обеспечить через последовательность заданий и оптимальный уровень поддержки такую траекторию обучения, при которой ты не только освоишь hard skills, но и научишься самообучаться.

- Не доверяй слухам и предположениям о том, как должно быть оформлено ваше решение. Этот документ является единственным источником, к которому стоит обращаться по большинству вопросов;
- твое решение будет оцениваться другими учащимися;
- подлежат оцениванию только те файлы, которые ты выложил в GIT (ветка develop, папка src);
- в твоей папке не должно быть лишних файлов — только те, что были указаны в задании;
- не забывай, что у вас есть доступ к интернету и поисковым системам;
- обсуждение заданий можно вести и в Rocket.Chat;
- будь внимателен к примерам, указанным в этом документе — они могут иметь важные детали, которые не были оговорены другим способом;
- и да пребудет с тобой Сила!

<h2 id="chapter-ii">Chapter II</h2>

<h3 id="веб-приложения">Веб-приложения</h3>

Несколько раз в этом курсе упоминалось слово "веб-приложение", но чем же веб-приложения отличаются от обычных сайтов? Какие бывают веб-приложения? Давайте разбираться!

Сначала разберёмся в том, что такое сайт. **Сайт**, или **веб-сайт**, — это одна или несколько логически связанных между собой веб-страниц. Сайты могут содержать контент разного формата: текст, картинки, музыка и прочее. Зачастую сайты не так связаны с сервером, как веб-приложения, они не предоставляют излишней интерактивности, их задача — выводить блоки текста с различными медиа-файлами.

В свою очередь, веб-приложения — это клиент-серверные приложения, доступ к которым осуществляется при помощи браузера. Они позволяют пользователям вводить, получать и манипулировать данными. Грубо говоря, веб-приложения — это сайт, в который добавили различные кнопки, поля и формы для ввода данных.

Основные отличия веб-сайта от веб-приложения:

- Веб-сайт является просто источником информации, в то время как веб-приложение работает в интерактивном режиме;
- Пользовательский интерфейс веб-приложения намного сложнее, чем интерфейс веб-сайта;
- Веб-приложение может быть составной частью сайта либо отдельным ресурсом;
- Разработка веб-сайта требует гораздо меньше времени, чем разработка веб-приложения.

<h3 id="клиент-серверное-взаимодействие">Клиент-серверное взаимодействие</h3>

Вы, пользуясь веб-приложением, постоянно взаимодействуете с сервером. Допустим, регистрация в какой-нибудь социальной сети непременно приведёт к появлению ваших данных на сервере. Так и любое приложение, размещённое в сети Интернет, основывается на связке "клиент-сервер". И это не только электронные формы. Даже простое "перелистывание" страниц некоторого сайта в Интернете — пример клиент-серверного взаимодействия, ведь страницы хранятся не на каждом компьютере, а подгружаются извне.

Что же понимается под "клиентом" и "сервером"? 🤔

**Клиент** — в нашем случае это компьютер, оснащённый специальным программным обеспечением, которое позволяет пользователю отправить запрос к другой машине и получить ответ. Код, выполняемый на стороне клиента, чаще всего называют клиентским кодом. Он обеспечивает создание пользовательского интерфейса. Здесь, когда речь заходит о браузере, важную роль играет язык программирования JavaScript и библиотеки расширения.

**Сервер** — это компьютер, который оснащён специальным программным обеспечением, которое позволяет решить задачи предоставления пользователю доступа к некоторым услугам и ресурсам, которыми владеет и управляет данный сервер. Код, выполняемый на стороне сервера, называют серверным кодом или серверным сценарием. Он обеспечивает обработку данных. Здесь важную роль играют серверные языки программирования. Примерами таких языков являются PHP и Python.

Таким образом, базовый концепт заключается в том, что клиент посылает запрос на сервер, а сервер ему отвечает (с запросам и протоколами взаимодействия мы обязательно познакомимся в следующем проекте😉).

Из преимуществ такого подхода можно отметить:

- Низкие требования к устройствам клиентов
- Гибкая архитектура

Но также существуют и недостатки:

- Высокая стоимость оборудования
- Сложное обслуживание

Обычно все говорят о двух "сторонах" веб-приложения, однако, в алгоритме подобного взаимодействия довольно активно принимает участие еще одна "сторона" — **база данных**. Вся динамическая информация приложения (учетные, пользовательские данные и пр) хранится именно здесь. Базам данных посвящён целый проект в нашем курсе, потому позже мы их обязательно обсудим!

<h3 id="front-end-и-back-end">Front-end и Back-end</h3>

Вот мы и дошли до этих терминов. В IT сфере их можно услышать почти везде, где идёт речь о разработке веб-приложений. Так что же мы понимаем под словами Front-end и Back-end? На самом деле, всё очень просто.

**Front-end (frontend, фронтенд)** — это клиентская часть веб-приложения, пользовательский интерфейс и связанные с ним компоненты. То есть фронтенд — всё, что браузер может читать, выводить на экран и/или запускать.

**Back-end (backend, бэкенд)** — это внутренняя, скрытая от пользователя часть веб-приложения. То есть бэкенд — всё, что работает на сервере, "не в браузере". 

<h3 id="задание-1-mpa-spa-pwa">Задание №1. MPA, SPA, PWA</h3>

MPA, SPA, PWA... Кажется, мы совсем запутались в этих аббревиатурах... Сможете нам помочь? У нас возникло много-много вопросов 😔.

Создайте файл `exercise1.md`, в котором:
- расшифруйте три аббревиатуры: MPA, SPA и PWA, дайте этим терминам определения и опишите их различия, недостатки и преимущества;
- приведите по 3 различных примера к каждому термину (с ссылками на реальные приложения);
- ответьте на вопросы:
    - Зачем вообще нужны PWA? Почему нельзя ограничиться SPA или MPA?
    - Какие технологии используются для реализации PWA?
    - Как можно понять (и можно ли), что перед нами PWA, а не другие виды приложений?
    - Чем отличается между собой тестирование SPA и MPA?
    - Как тестировать PWA?

<h3 id="задание-2-архитектура">Задание №2. Архитектура</h3>

Создайте файл `exercise2.md`, в котором дайте ответы на следующие вопросы:
- Какие существуют уровни веб-приложения?
- За что отвечает каждый из них?
- Что такое монолитная и микросервисная архитектуры веб-приложения?
- Каковы различия между монолитом и микросервисами?
- Почему не все приложения построены на микросервисной архитектуре?
- Каковы особенности тестирования монолитных и микросервисных веб-приложений?


<h2 id="chapter-iii">Chapter III</h2>

<h3 id="основные-frontend-технологии">Основные Frontend технологии</h3>

Для разработки фронтенд части приложения нужны разнообразные инструменты, которые помогут создать структуру, красиво оформить продукт и сделать его интерактивным. Среди подобных инструментов нужно отметить:

- HTML
- CSS
- JS (JavaScript)

<h3 id="html">HTML</h3>

**HTML (HyperText Markup Language)** — это язык гипертекстовой разметки текста. HTML-код используется для структурирования и отображения веб-страницы и её контента. Чтобы посмотреть на HTML-код любой страницы в Интернете, просто нажмите на клавишу `F12` и перейдёте во вкладку `Elements`. Также можно разом посмотреть код всей страницы: для этого надо нажать правой кнопкой мыши на пустую область сайта, а после на кнопку "Посмотреть код страницы". 

HTML-код состоит из ряда элементов. Когда вы заходите на сайт, браузер подгружает HTML-файл с информацией о структуре и контенте веб-страницы. HTML как бы выстраивает визуальный фундамент сайта, он указывает, где будут располагаться элементы, какой у них будет базовый дизайн, откуда брать стили для элементов и скрипты (обычно их пишут на JavaScript). Элементы же состоят из тегов и контента. 

Конечно, тема HTML очень обширная, её попросту нельзя раскрыть за один проект. Существуют целые курсы по изучению HTML и вёрстки сайтов. Поэтому подробно рассматривать данную тему мы не станем, но изучим основные теги на примере построения XPath'ов.

<h3 id="css">CSS</h3>

**CSS (Cascading Style Sheets, каскадные таблицы стилей)** — это код, который используется для стилизации веб-страницы. Он позволяет "украсить" ваши HTML-элементы, по умолчанию у которых почти никаких стилей нет. CSS позволяет реализовать анимации, переходы, реакции элементов на движение мыши и прочее.

<h3 id="javascript">JavaScript</h3>

А вот **JavaScript** — это полноценный язык программирования, который можно встроить в веб-страницу. Этот язык позволяет реализовывать сложные вещи в веб-приложении, например, отображать периодически обновляемый контент, интерактивные графики и так далее.

_P.S.: очень советуем изучить вышеперечисленные технологии подробнее, ведь вам ещё не раз придётся с этим столкнуться!_

<h3 id="xpath">XPath</h3>

**XPath (XML Path Language)** — это язык запросов к элементам XML-документа. Представьте, что в документе Word вы сочетанием клавиш `Ctrl + F` вызываете функцию поиска контента. Вписывая что-то в поле ввода, вы можете осуществить поиск элементов в вашем документе. То же самое можно делать и в коде HTML, только тут функционал поиска расширяется как раз за счёт XPath'ов, при помощи которых вы можете либо точно указать позицию элемента, либо найти элементы, относящиеся к конкретному классу и многое-многое другое. 

Самый простой способ получить XPath — это во вкладке `Elements` нажать правой кнопкой на элемент и нажать на "Copy full XPath", тем самым скопировав _абсолютный_ XPath. Выглядеть он будет примерно следующим образом: `/html/body/div[11]/div/div`. Означает это то, что наш элемент (конечный блок `div`) располагается в другом блоке, который располагается 11-ым по счёту блоком в третьем блоке `div`, который, в свою очередь, располагается в `body`, который находится в главном теге `html`. Но в подобных абсолютных указателях есть два огромных недостатка:

1. Это совершенно неудобно читать и не сразу понятно, о каком элементе идёт речь.
2. Если HTML-код данной страницы хотя бы немного поменяется, например, добавится новый блок и тем самым сдвинет наш элемент выше или ниже, то такой XPath будет указывать уже на совсем другой элемент.

Для _относительного_ XPath путь начинается с середины структуры HTML DOM. Он начинается с двойной косой черты (`//`), что означает, что он может искать элемент в любом месте на веб-странице. Далее используется имя тега нужного нам узла, указывается атрибут узла и значение этого атрибута: `//tagname[@Attribute='value']`. Например, представим, что мы пишем XPath до поля ввода Email адреса в простом веб-приложении, тогда он может быть написан двумя способами:

- `/html/body/div/div/form/table/tbody/tr/td/input`
- `//input[@id='email']`

Второй XPath выглядит гораздо лучше первого, не так ли?

<h3 id="задание-3-xpath">Задание №3. XML, HTML и XPath</h3>

Создайте файл `exercise3.1.md`, в него добавьте ответы на вопросы:
- Что такое язык разметки?
- Какие вы знаете языки разметки? Опишите каждый из них.
- Что такое XML?
- Что такое теги, атрибуты и элементы в XML?
- Чем XML отличается от HTML?
- Что такое DTD? Расшифруйте и приведите примеры использования в различных документах.
- Из чего состоит HTML-документ?

А теперь перейдите на сайт [СберСтрахования](https://online.sberbankins.ru/store/property-insurance/). Ознакомьтесь с основным функционалом приложения. Создайте файл `exercise3.2.md`, в котором опишите XPath'ы на первой странице ("1. Оформление") для:
- Каждой кнопки;
- Каждого поля для ввода текста;
- Каждого чекбокса;
- Каждого датапикера;
- Логотипа "СБЕР СТРАХОВАНИЕ";
- Слайдера в блоке выбора срока страхования;
- Хедера "Данные страхователя";
- Текстовых блоков: "Укажите дату начала действия полиса и срока страхования", "Является законсервированным, под реконструкцией, незавершенным строительством";

_P.S.: XPath'ы нужно писать для каждого элемента отдельно_

Далее при помощи вкладки `Elements` отредактируйте какой-либо атрибут трех любых элементов на странице (шрифт, цвет, расположение, прочее — на усмотрение команды). Сделайте скрины этих элементов до и после редактирования, присвойте им названия: `1-before.png` — до, `1-after.png` — после (в итоге получится 6 скринов).

<h2 id="chapter-iv">Chapter IV</h2>

<h3 id="uxui">UX/UI</h3>

Работая с фронтенд-составляющей приложения, можно часто встретиться с такими аббревиатурами, как UX и UI. Есть даже UI и UX виды тестирования.

Аббревиатура UI расшифровывается как user interface — это оформление сайта: сочетания цветов, шрифты, иконки и кнопки.

UX — user experience, то есть "пользовательский опыт". Простыми словами, это то, каким образом пользователь взаимодействует с интерфейсом и насколько приложение для него удобно.

Если функциональное тестирование — это тестирование ПО для проверки реализуемости функциональных требований, то **UI-тестирование** — это тестирование ПО с целью проверки всех визуальных индикаторов и иконок, меню, переключателей, текстовых полей, флажков и так далее.

**UX-тестирование (юзабилити-тестирование)** отличается от других видов тестирования, которые мы рассматривали ранее, тем, что оно подразумевает проведение проверки на реальных пользователях. Потому проводить UX-тестирование в данном проекте мы не будем, но от UI-тестирования не откажемся!

<h3 id="задание-4-ui-тестирование">Задание №4. UI-тестирование</h3>

Ознакомьтесь с технологией проведения UI-тестирования. В TestIT создайте общее рабочее пространство, в нём создайте проект и назовите его "СберСтрахование". Добавьте тест-кейсы, которые позволяют провести полное ручное UI-тестирование одной из страниц [СберСтрахования](https://online.sberbankins.ru/store/property-insurance/): "1. Оформление". 

После выполнения задания выгрузите полученные тест-кейсы в формате xlsx, назовите файл `exercise4.1.xlsx` и загрузите его в папку `/src`.

Добавьте в созданное рабочее пространство новый проект. Теперь вам необходимо создать тест-кейсы, которые позволят провести полное ручное UI-тестирование официального сайта [TestIT](https://testit.software/) (проверять нужно только главную страницу и два первых раздела: "О продукте" и "Цена", включая подразделы, но не затрагивая поддомены и другие сайты). Файл с выгруженными тест-кейсами назовите `exercise4.2.xlsx` и загрузите его во всю ту же папку `/src`!

<h3 id="double-check">Double-check</h3>

Перед загрузкой выполненного проекта в репозиторий перепроверьте наличие всех необходимых файлов, которые требовалось создать во время его выполнения:

```
exercise1.md
exercise2.md
exercise3.1.md
exercise3.2.md
1-before.png
1-after.png
2-before.png
2-after.png
3-before.png
3-after.png
exercise4.1.xlsx
exercise4.2.xlsx
```
💡 [Нажми здесь](https://forms.gle/KVQB1xuhVAu3ZU4V7) **чтобы отправить обратную связь по проекту**. 
