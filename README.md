# Object_detection
Задача в рамках хакатона **Nuclear IT Hack** заключалась в анализе изображений поверхностей в термоядерном реакторе и разработке алгоритма распознавания пыли, посчёте количества частиц и определении их размеров.

Задача была решена двумя вариантами:
1) Для детекции крупных пылинок вне зависимости от их взаимного расположения с помощью модели DETR (работает лучше FRCNN и YOLO), предобученной на распознавании воздушных шариков и дообученной на частицах пыли в реакторе. Пропускает некруглые пылинки и не обрабатывает больше ста штук.
2) С помощью выделения границ методом пороговой обработки threshold (+ Otsu для автоматического определения порога). Работает лучше + не зависит от количества частиц на фото.
