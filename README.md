# FamilyBudget
Программа для подсчета семейного бюджета. Может быть интегрирована в любую другую программу и бота на любой платформе. Есть встроенное решение для telegram-бота.


### Возможности
Программа принимает информацию о расходах и доходах деля их по категориям, и выдает информацию о текущем балансе. В дальнейшем, научится делать месячные, или годовые отчеты.

## Использование

Установите telebot (для использования telegram-бота) с помощью команды:
```sh
pip install -r requirements.txt
```
Запустите setup.py и нажмите 1. В появившемся файле data/private/privateConfig.py создайте необходимое количество аккаунтов и введите токен телеграмма:
```python
FIRST = {'id': 0, 'name': ''}   # id - может быть user_id телеграма, или же любой другой системы
SECOND = {'id': 0, 'name': ''}  # name - имя пользователя отображающегося в статистике
TELEGRAM_TOKEN = ''   # Если используется оболочка телеграм-бота
USER_LIST = [FIRST, SECOND]  # Не забудьте добавить всех пользователей с id и name  в этот лист
```
Вновь запустите setup.py и нажмите 2 для иницилизации. Телеграм-бот готов к использованию через запуск run.py. 

Для использования программы в других проектах - импортируйте класс FamilyBudget из mainFiles.familyBudget:
```python
from mainFiles.familyBudget import FamilyBudget

familyBudget = FamilyBudget()    # используйте метод run всякий раз, когда хотите контактировать с бюджетом
familyBudget.run(user_id, text)  # должно корректно работать и при синхронном, и асинхронном выполнении
```

## Запуск на pythonanywhere
На сайте https://www.pythonanywhere.com/ и ему подобных, можно настроить работу бота в облаке и совершенно бесплатно.



### Зачем вы разработали этот проект?
Проект создан для личных нужд, но если он будет ещё кому-нибудь полезен - буду только рад.

## To do
- [ ] Создать отчет за месяц\год по категориям