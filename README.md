# Slime Bob
Игра про слайма по имени Боб

# Дизайн-документ GetOut
## 1. Основные требования
- Платформа: **`Windows`**
- Технологии: **`C#` `MonoGame`**
- Язык: **`Русский`**
- Жанры: **`Приключения` `Платформер` `2D` `Pixel game`**
- Настроение: **`Загадочное` `Геройское`**
- Сеттинг: **`Шахты` `Подземелье`**

## 2. Сюжет
Слайм по именб Боб просыпается в загадочной пещере. Он обнаруживает, что теперь его тело может менять цвета. Ему нужно каким-то образом выбираться. Он видит перед собой множество платформ таких же цветов, как и его тело, висящих прямо над пропостью. Помогите Бобу выбраться из пещеры, пробрашись сквозь все уровни этого подземелья.

## 3. Игровой мир
Игровой мир представляется секциями с платформами различных цветов. В конце секции располагается дверь, а под платформами находится пропасть. Каждая секция является уровнем шахты. Чем выше уровень, тем сложнее секция.

## 4. Геймплей
Игроку представлен слайм, способный бегать влево и вправо, прыгать, а также менять свой цвет. Игроку необходимо добраться до конца секции, пропрыгнув через платформы разных цветов. Слайм может взаимодействовать только с "нейтральной" или с платформой соответствующего цвета, иначе он провалится сквозь платформу и упадет в пропасть. В таком случае, он начнет прохождение уровня с самого начала. На пути слайму будут встречаться как вспомогательные предметы, так и надоедливые препятствия. 

## 5. Объекты, предметы
Объекты и предметы - сущности, с которыми взаимодействует игрок.


### 1. Слайм
- Позиционирование в сцене
- Анимации/спрайт
- Способность прыгать, бегать и менять цвет
- Состояние: зеленый, синий и желтый
- Взаимодействие с предметами, платформами и препятствиями
- Гибель(падение в Пропасть)
- Успех(прохождение черезь Дверь)

### 2. Платформа
- Позиционирование в сцене
- Состояние: зеленый, синий, желтый и "нейтральный"

### 3. Пропасть
- Позиционирование в сцене
- Анимации/спрайт
- Действие: возвращение к началу текущего уровня

### 4. Дверь(КТ)
- Позиционирование в сцене
- Анимации/спрайт
- Действие: переход на следущий уровень

### 5. Предмет: Шлем
- Позиционирование в сцене
- Анимации/спрайт
- Состояние: собран или нет
- Состояние: экипирован или нет
- Действие: разрушение платформы при столкновении с ней снизу

### 6. Предмет: Крылатые сандали
- Позиционирование в сцене
- Анимации/спрайт
- Состояние: собран или нет
- Состояние: экипирован или нет
- Действие: прыжок превыщаюший длину и высоту обычного прыжка в два раза(возможность перепрыгнуть Камень)

### 7. Препятствие: Камень
- Позиционирование в сцене
- Действие: невозможность перепрыгнуть через него обычным прыжком

### 8. Препятствие: Нажимная плита
- Позиционирование в сцене
- Анимации/спрайт
- Действие: отбрасывание слайма на длину, равную четырем прыжкам

### 9. Препятствие: Портал
- Позиционирование в сцене
- Анимации/спрайт
- Действие: смена цвета слайма(меняется на предыдущий выбранный цвет)


## 6. Взаимодействия
Управление: Движение - WASD\(стрелки), прыжок - Space, смена цвета - ЛКМ\B, экипировка предмета - Tab.
Предметы располагаются на платформах, сбор происходит при приближении к предмету, экипируются автоматически на слайма. Взаимодействие с пропостью\дверью автоматически приводит к их действиям.
