# sirius-test
Тестовое для смены в сириус 2023
В рамках этого тестового вам необходимо обучить свою диалоговую языковую модель и сделать телеграм бота для взаимодействия с ней.
Что нужно сделать:
1) Скачать диалоговые данные из телеграма. Можете взять любой открытый чат
2) Затюнить открытую модель с хаггинфейса (в качестве базовой модели рекомендуем взять https://huggingface.co/tinkoff-ai/ruDialoGPT-medium)
3) Для сёрвинга модели напишите телеграм бота
4) Будет плюсом если вы обернёте телеграм бота в докер. Дополнительным плюсом будет если вы также сделаете отдельный сервис для модели и будуте сёрвить её в отдельном докере.

В качестве решения задания нужно прислать публичный репозиторий в котором должен быть код решения задачи и ридми с описанием решения. Для обучения модели рекомендуем использовать google colab

## Вспомогательные инструкции

### Как получить сырые данные из телеграма

![pic](data.png)

В настройках выгрузки нужно выбрать формат джсон и убрать галочки со всех медиа файлов. Тк данные могут скачиваться долго в репозитории лежит пример выгруженных данных.

### Как распарсить данные

`python prepare_messages.py --tg-history-path 'chata_export.json' --output-path 'data.csv'`
