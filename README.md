# Food delivery Service System Design

## Table of contents
- [Food delivery Service System Design](#food-delivery-service-system-design)
  - [Table of contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Forecast](#forecast)
  - [Competitors](#competitors)
  - [Goals](#goals)
  - [Stakeholders](#stakeholders)
  - [Assumptions](#assumptions)
  - [Customer journey](#customer-journey)

## Introduction

В период локдауна услуги по доставке еды мгновенно взлетели до небес. Все стремились получить необходимые продукты и блюда, доставленные к порогу дома. Таким образом, период карантина открыл широкие возможности для бизнеса доставки еды.

Хотя может показаться, что гиганты индустрии контролируют рынок, это не совсем так. Во время пандемии по всему миру стали появляться стартапы по доставке еды по требованию, и они до сих пор набирают популярность.

Glovo, испанский стартап, который сотрудничает предприятиями для доставки еды из ресторанов, продуктов и других товаров, получил финансирование в размере 528 миллионов долларов. Аналогичным образом, Gousto, британский сервис по доставке наборов еды, привлек 41 миллион долларов во время пандемии.

Gorillas, продуктовый стартап, цель которого - доставка товаров за десять минут или меньше, привлек 290 миллионов долларов, превысив первоначальную оценку в 1 миллиард долларов.

Рынок доставки готовой еды и бакалеи начал развиваться в Казахстане около 4 лет назад. На динамику его роста повлияли: 

* появление крупных международных игроков на рынке в 2019 году;
* пандемия Ковид-19, которая изменила покупательские привычки и операционные решения компаний.

Большинство из этих услуг доступны во всех крупных городах Казахстана - Алматы, Астане, Шымкенте, Усть-Каменогорске, Караганде, Таразе и других. В небольших городах службы доставки распространены меньше.

![C4 Context](images/map.png)

Тренд на доставку в регионах  только зарождается в Казахстане - интернет-магазины и доставка из ресторанов слабо представлены в регионах. И это является точкой роста для рынка.

## Forecast

* Ожидается, что в 2024 году рынок доставки еды в Казахстане будет приносить доход в размере 53,80 млн долларов США.
* Согласно этому прогнозу, совокупный годовой темп роста (CAGR 2024-2028) составит 7,97%, в результате чего к 2028 году объем рынка составит 73,11 млн долларов США.
* Что касается рынка платформ доставки, размер рынка в Казахстане, по прогнозам, достигнет 26,98 млн долларов США в 2024 году.
* Однако, по сравнению с другими странами, наибольший доход ожидается в Китае, где он составит 182 900,00 млн долларов США в том же году.
* Средний доход на одного пользователя (ARPU) на рынке доставки еды в Казахстане составит 32,58 доллара США в 2024 году.
* Ожидается, что к 2028 году количество пользователей на рынке доставки еды достигнет 2,2 миллиона человек.
* С точки зрения проникновения пользователей, рынок доставки еды в Казахстане достигнет 8,4% в 2024 году.
* Несмотря на растущую популярность услуг по доставке еды в Казахстане, традиционная домашняя еда по-прежнему доминирует на рынке.

## Competitors

Сравним крупнейших игроков на казахстанском рынке: Wolt, Glovo, Chocofood и Yandex Food.

**1st place**

![alt_text](images/glovo.png "image_tooltip")

_10 заведений назвали эту услугу самой популярной среди своих клиентов._

Рестораны объясняют популярность этого сервиса тем, что он удобнее для их пользователей, чем другие сервисы. Поэтому большинство заведений ставят его на 1-е место в своем личном рейтинге. Стоит также отметить, что стоимость доставки этой службы может быть гораздо дешевле, чем заказ такой же доставки из самого заведения. Услуга GLOVO представлена в 20 из 21 опрошенных заведений.

**2nd place**

![alt_text](images/wolt.png "image_tooltip")

_9 заведений назвали этот сервис самым популярным среди своих клиентов._

Слишком маленький отрыв от первого места, что может говорить об похожем удобстве и скорости работы сервиса! А главным преимуществом является бесплатная доставка, которая теперь доступна в сервисе, а также вы можете получить кешбэк в размере 30% при оплате картой VISA. Это очень серьезное преимущество перед конкурентами. Сервис WOLT представлен в 18 из 21 опрошенных заведений.

**3rd place**

![alt_text](images/chocofood.png "image_tooltip")

_2 ресторана высказались как о самой популярной услуге среди своих клиентов._

Давно известный и любимый многими жителями Алматы, остается в рейтинге довольно высоким, по той причине, что его использование уже стало очень привычным, а в зависимости от района проживания иногда самым интересным и быстрым предложением. Стоимость доставки невысока, а в некоторых местах даже предлагается абсолютно бесплатная доставка при заказе через этот сервис. Услуга Chocofood представлена в 17 из 21 опрошенного заведения.

**4th place**

![alt_text](images/yandex.png "image_tooltip")

_Ни один ресторан не назвал эту услугу самой популярной среди своих клиентов._

Даже учитывая популярность этой услуги, к сожалению, она не имеет плюсов и преимуществ для клиентов. Цена за доставку напрямую зависит от расстояния, что также не может радовать. Поэтому на данный момент эта услуга менее популярна. Зато Яндекс может привезти заказ в любую точку, куда вы пожелаете. Это удобно для тех, у кого нет другого выхода. Сервис Яндекс Еда представлен в 13 из 21 опрошенного заведения.

На рынке Казахстана есть и другие менее популярные службы доставки, на которые вы также можете обратить свое внимание, учитывая, что некоторые из них могут быть ближе к вам, а значит, быстрее привезут вам заказ.

## Goals

Мы собираемся запустить онлайн-платформу доставки еды, которая позволит потребителям, ресторанам и службам доставки взаимодействовать в режиме реального времени. Мы должны поддерживать как мобильные приложения для всех клиентов, так и веб-приложение для административных функций. Мы уверены, что станем следующим большим и популярным проектом, и ожидаем значительного и быстрого роста в ближайшие несколько лет.

Мы предполагаем три значимые вехи развития:

1. MVP решение на коленке, чтобы прощупать рынок на одного из регионов Казахстана, собрать команду и отработать основные технологические решения.
2. Масштабировать решения на рынок Казахстана, обеспечить стабильность сервиса и явные конкурентные преимущества.
3. Обеспечить возможности для быстрого выхода на другие рынки.

## Stakeholders

* **SH-1**: Клиент
    * Понятный и простой пользовательский интерфейс
    * Полезные услуги
    * Быстрая и недорогая доставка
    * Большое количество ресторанов и блюд
* **SH-2**: Ресторан
    * Простое в использовании веб-приложение с каталогом блюд
    * Быстрая доставка еды
    * Минимальное количество проблем для клиентов
* **SH-3**: Курьер
    * Простое в использовании мобильное приложение
    * Высокая стоимость доставки
* **SH-4**: Администратор (из нашей компании)
    * Привлечение различных типов клиентов
    * Повышение качество предоставляемых блюд и услуг
    * Открытие новых ниш для развития бизнеса
* **SH-5**: Служба поддержки
    * Легкий доступ к информации о падениях услуг, ошибках и исключительных ситуациях
* **SH-6**: Разработчик
    * Упрощение разработки и поддержки системы
* **SH-7**: Системный администратор
    * Удобные средства мониторинга
    * Удобные средства конфигурирования и масштабирования

## Assumptions

* **ASN-1**: В период между открытием и закрытием ресторана можно есть неограниченное количество еды. Таким образом, нет необходимости проверять количество доступных блюд. Не требуется управление запасами.
* **ASN-2**: У ресторанов нет собственной системы/инфраструктуры онлайн-заказа, все заказы они будут принимать только у нас.
* **ASN-3**: Клиентам будут показаны рестораны в определенном радиусе, скажем, 10 километров.
* **ASN-4**: Клиенты могут заказывать еду только из одного ресторана одновременно в онлайн-заказе. Пункты меню из нескольких ресторанов не могут быть объединены в одном заказе.

## Customer journey

Ниже показано схематичное высокоуровневое описание всего жизненного цикла клиента включая регистрацию всех участников на платформе, формирование заказа, оплату заказа, уведомление ресторана о появлении нового заказа в системе и доставку готовых блюд клиенту.

![alt_text](images/Context-activity-diagram.png "image_tooltip")

Жизненный цикл представляет собой следующие шаги:

1. **Регистрация/вход в систему:** Клиенты, рестораны и курьеры могут зарегистрироваться в приложении, указав свои имена, номера телефонов, идентификаторы электронной почты и пароли. Они могут войти в систему, если были зарегистрированы ранее.
2. **Список ресторанов:** Клиентам предлагается список ресторанов, расположенных поблизости от их местонахождения. Они также могут искать конкретные рестораны по различным атрибутам.
3. **Размещение заказа:** Клиенты могут сделать заказ в любом из перечисленных ресторанов, указав адрес доставки.
4. **Обработка платежей:** Клиенты могут оплачивать свои заказы через любой из многочисленных платежных шлюзов приложения.
5. **Уведомление ресторанов:** Ресторан получает уведомления о новом заказе
6. **Назначение заказов курьерам:** Курьеры могут принимать или отклонять отправленные им запросы на доставку еды. В случае принятия они отправляются в рестораны, чтобы забрать заказ для доставки.
7. **Отслеживание заказов:** Клинеты могут отслеживать состояние своего заказа до тех пор, пока он не будет доставлен.
8. **Рейтинги и отзывы:** После получения заказа клиенты могут оценить и просмотреть блюда и услуги доставки.
