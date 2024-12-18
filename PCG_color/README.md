"Color Converter"
=================

Описание
--------

Color Converter — это интерактивное приложение, предназначенное для конвертации цветов между различными цветовыми моделями: CMYK, LAB и HSV. Приложение позволяет пользователю выбирать цвет и интерактивно изменять его, отображая при этом его составляющие во всех трех моделях одновременно. При изменении любой компоненты цвета все остальные представления этого цвета в других моделях пересчитываются автоматически.

Установка и запуск
------------------

### Системные требования

*   **Операционная система**: Windows 7 и выше.
    
*   **Python 3.x** (если запускается из исходного кода).
    
*   **Необходимые библиотеки**: tkinter (обычно включена в стандартную поставку Python).
    

### Запуск приложения

#### Использование исполняемого файла

1.  Скачайте исполняемый файл ColorConverter.exe.
    
2.  Дважды щелкните по файлу, чтобы запустить приложение.
    

#### Запуск из исходного кода

1.  Убедитесь, что у вас установлен Python версии 3.x.
    
2.  Скачайте исходный код приложения из репозитория [GitHub](https://github.com/Kirofeed/PCG_color).
    
3.  bashКопировать кодpip install tkinter
    
4.  bashКопировать кодpython ColorConverter.py
    

Пользовательский интерфейс
--------------------------

### Основные элементы

*   **Кнопка "Choose Color"**: позволяет выбрать цвет с помощью стандартного диалогового окна выбора цвета.
    
*   **Области отображения цвета**: три цветовых квадрата, отображающих текущий цвет в каждой из моделей (CMYK, LAB, HSV).
    
*   **Поля ввода**: текстовые поля для ввода значений компонентов цвета вручную.
    
*   **Ползунки**: для каждой компоненты цвета в каждой модели имеются ползунки для плавного изменения значений.
    

### Навигация по интерфейсу

#### Выбор цвета

1.  Нажмите кнопку **"Choose Color"** в верхней части окна.
    
2.  В открывшемся диалоговом окне выберите желаемый цвет.
    
3.  Выбранный цвет отобразится во всех трех моделях, значения компонентов обновятся автоматически.
    

#### Изменение цвета с помощью ползунков

1.  Используйте ползунки под каждой моделью для изменения значений компонентов.
    
2.  При изменении любого значения остальные модели обновятся автоматически.
    

#### Ввод значений вручную

1.  Введите значения компонентов в текстовое поле соответствующей модели, разделяя их запятыми.
    
2.  Нажмите **Enter** для применения изменений.
    
3.  Пример ввода для CMYK: 100, 0, 0, 0.
    

Использование приложения
------------------------

### Выбор цвета через палитру

1.  Нажмите **"Choose Color"**.
    
2.  Выберите цвет в открывшемся окне.
    
3.  Подтвердите выбор, нажав **"OK"**.
    
4.  Приложение автоматически отобразит выбранный цвет во всех моделях.
    

### Работа с ползунками

*   Ползунки позволяют плавно изменять значения компонентов цвета.
    
*   **Диапазоны значений**:
    
    *   **CMYK**: от 0 до 100 для каждого компонента.
        
    *   **LAB**: L от 0 до 100, A и B от -128 до 127.
        
    *   **HSV**: H от 0 до 359, S и V от 0 до 100.
        
*   При перемещении ползунка значения в других моделях обновляются автоматически.
    

### Ввод значений вручную

1.  Введите значения компонентов в текстовое поле под соответствующей моделью.
    
2.  Разделяйте значения запятыми, например: 50, 25, 75.
    
3.  Нажмите **Enter** для применения.
    
4.  Приложение автоматически скорректирует значения, выходящие за допустимый диапазон.
    

Особенности приложения
----------------------

### Автоматический пересчет

*   При изменении любого значения компоненты цвета в одной модели, приложение автоматически пересчитывает значения в других моделях.
    
*   Это обеспечивает согласованность и актуальность отображаемой информации.
    

### Обработка некорректных значений

*   При вводе значений, выходящих за пределы допустимого диапазона, приложение автоматически корректирует их до ближайшего допустимого значения.
    
*   Например, если ввести значение -10 для компоненты, допускающей диапазон от 0 до 100, приложение установит значение 0.
    

### Цветовые квадраты

*   Каждый цветовой квадрат отображает цвет в соответствующей модели.
    
*   Это позволяет визуально сравнить, как цвет выглядит в разных моделях.
    

Цветовые модели
---------------

### CMYK

*   **Описание**: Субтрактивная модель цвета, используемая в печати.
    
*   **Компоненты**:
    
    *   **C (Cyan)** — голубой.
        
    *   **M (Magenta)** — пурпурный.
        
    *   **Y (Yellow)** — желтый.
        
    *   **K (Key, Black)** — черный.
        

### LAB

*   **Описание**: Цветовая модель, основанная на человеческом восприятии цвета.
    
*   **Компоненты**:
    
    *   **L (Lightness)** — яркость, от 0 (черный) до 100 (белый).
        
    *   **A** — от зеленого (-128) к красному (+127).
        
    *   **B** — от синего (-128) к желтому (+127).

*   **особенности формулы преобразования для LAB**: При преобразовании LAB используем промежуточную систему XYZ.


### HSV

*   **Описание**: Модель, представляющая цвет в терминах оттенка, насыщенности и яркости.
    
*   **Компоненты**:
    
    *   **H (Hue)** — оттенок, угол в цветовом круге от 0 до 359 градусов.
        
    *   **S (Saturation)** — насыщенность, от 0 (серый) до 100 (насыщенный цвет).
        
    *   **V (Value)** — яркость, от 0 (черный) до 100 (максимальная яркость).
        

Известные ограничения
---------------------

*   **Точность преобразования**: Преобразования между цветовыми моделями могут иметь незначительные погрешности из-за математических округлений.
    
*   **Ограничение диапазонов**: Некоторые цвета могут быть недоступны в определенных цветовых моделях из-за их ограничений.
    
*   **Отображение цветов**: Цвета могут отображаться по-разному на разных мониторах из-за различий в настройках цветопередачи.
    

Исходный код
------------

Исходный код приложения доступен на [GitHub](https://github.com/Kirofeed/PCG_color)

Вы можете ознакомиться с кодом, внести свои предложения или доработки.

Обратная связь
--------------

Если у вас возникли вопросы, предложения или вы обнаружили ошибку, пожалуйста, свяжитесь с разработчиком:

*   **Email**: drozhzhakirill@gmail.com
    
*   **GitHub**: https://github.com/Kirofeed
    

Лицензия
--------

Приложение распространяется под лицензией MIT License.
