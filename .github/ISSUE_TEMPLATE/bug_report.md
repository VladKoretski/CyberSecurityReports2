name: 🐞 Баг-репорт
description: Сообщить об ошибке в работе приложения
title: "[BUG] Краткое описание ошибки"
labels: ["bug", "to verify"]
body:
  - type: markdown
    attributes:
      value: |
        Спасибо за найденный баг! Пожалуйста, заполните все поля ниже.
  - type: input
    id: environment
    attributes:
      label: Окружение
      description: Браузер, ОС, разрешение экрана
      placeholder: Chrome 120, Windows 11, 1920x1080
    validations:
      required: true
  - type: textarea
    id: steps
    attributes:
      label: Шаги воспроизведения
      description: Пошаговая инструкция, как воспроизвести ошибку
      placeholder: |
        1. Открыть форму по ссылке https://...
        2. В поле "Имя" ввести "123"
        3. Нажать кнопку "Отправить"
      value: |
        1. 
        2. 
        3. 
    validations:
      required: true
  - type: textarea
    id: expected
    attributes:
      label: Ожидаемый результат
      placeholder: Система показывает ошибку "Имя должно содержать только буквы"
    validations:
      required: true
  - type: textarea
    id: actual
    attributes:
      label: Фактический результат
      placeholder: Форма отправляется без ошибок, данные сохраняются с цифрами в имени
    validations:
      required: true
  - type: textarea
    id: attachments
    attributes:
      label: Вложения
      description: Ссылки на скриншоты, логи, видео
      placeholder: |
        - Скриншот ошибки: https://i.imgur.com/...
        - Лог-файл: artifacts/error.log
    validations:
      required: false
