Цените интегрированные системы

Ruby on Rails можно использовать для разных целей, но его конек - это монолитные интегрированные системы. Такие системы нацелены на решение всей задачи совокупно. Через Rails проходит все, начиная от генерации JavaScript для мгновенного обновления страниц, и заканчивая миграцией базы данных от одной версии к другой, когда проект уже в эксплуатации.

Как уже было сказано раньше, в такой постановке задача весьма широка, но она вполне по силам одному человеку. Rails специально спроектирован так, чтобы один разносторонний специалист или небольшая группа могли создать полноценную систему. В противном случае специалисты забиваются в свои узкоспециализированные ниши, и чтобы реализовать серьезный проект, из этих специалистов приходится собирать целую команду.

Именно упор на расширение возможностей отдельного разработчика подталкивает нас к интегрированным системам. Интегрированная система позволяет убрать ненужные абстракции, уменьшить дублирование между слоями (например, использовать одни и те же шаблоны на сервере и на клиенте), а самое главное - до последнего не допустить перехода к распределенной архитектуре.

Основная сложность распределенных систем связана с появлением новых границ, которые затрудняют передачу данных между элементами. Вызвать в одном объекте метод другого объекта намного проще, чем из одного микросервиса удаленно вызвать процедуру в другом микросервисе. В распределенных системах неожиданно появляется множество осложнений, например, планирование обновлений зависимостей, недоступность сервисов и задержки.

Увы, иногда без распределенной архитектуры не обойтись. Если вашему веб-приложению нужен API-интерфейс, к которому пользователи будут обращаться по HTTP, то ничего не поделаешь - придется решать почти все упомянутые проблемы. Остается порадоваться, что работа со входящими запросами куда проще, чем с исходящими, ведь если ваш интерфейс какое-то время не будет работать, то проблемы будут не у вас, а у потребителя этого интерфейса. По крайней мере в таком случае неудобства, которые вам как разработчику придется претерпеть, не столь велики.

Плохо, когда система преждевременно дробится на сервисы или, что еще хуже, на микросервисы. Бытует мнение, что при разработке "Современного Интернет-Приложения" неизбежно придется строить одну и ту же систему много раз: один раз на стороне сервера, один раз на стороне клиента в виде JavaScript MVC, по одному разу для каждой мобильной платформы, и так далее. Но это требование ничем не обусловлено, так делать совершенно необязательно!

Можно запросто использовать одни и те же элементы системы для разных задач и способов доступа. Завести единый набор контроллеров и представлений и для десктопных браузеров, и для нативных мобильных приложений. Сосредоточить как можно больше функций в монолитной интегрированной системе.

При этом практически не страдают ни скорость, ни удобство использования, ни другие характеристики, ради оптимизации которых разработчики бросаются проектировать распределенное приложение.

Все наши силы направлены на то, чтобы получить все преимущества отлично подогнанного распределенного приложеня в простой, удобной и понятной единой интегрированной системе.