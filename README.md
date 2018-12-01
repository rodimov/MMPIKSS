# MMPIKSS
Описание
Данная система имитирует лесной пожар. Генерируется случайный лес, скорость и направление
ветра, а в конце случайным образом генерируется очаг возгорания. Поле представляет собой
разноцветные круги, где цвет круга обозначает здоровье дерева (от 0 до 100), если здоровье дерева равно 0, то дерево
удаляется с поля. Соотношение цветов и здоровья деревьев:
•	Зелёный цвет (от 100 до 75)
•	Жёлтый (от 75 до 50)
•	Оранжевый (от 50 до 35)
•	Красный (от 35 до 0)
Размеры поля можно регулировать, изменяя размеры начального окна.
Чтобы запустить модель необходимо нажать «Start Game», после этого откроется окно,
размер которого равен размеру поля. В левом нижнем углу содержится следующая информация:
•	frame – время формирования одного кадра
•	fps – количество кадров в секунду
•	Alive trees – количество деревьев со здоровьем больше 0
•	Dead trees – количество удалённых с поля деревьев
•	Wind direction – направление ветра
•	Wind speed – скорость ветра (от 0 до 100)
Каждую итерацию у каждой клетки проверяются соседи, если сосед горит, то вероятность того, что данная клетка загорится повышается (зависит от скорости ветра и направления (если в направление клетки, то 0,1 + скорость ветра / 100), если направление противоположное, то вероятность повысится на 0,1). Каждая итерация уменьшает здоровье горящего дерева на 0,25.
 
Зависимости
StdDraw - https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdDraw.html