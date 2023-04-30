1)   Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»
stanislav@stanislav:-% mkdir Игрушки_для_школьников
stanislav@stanislav:-% mkdir Игрушки_для_дошколят

2)   Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»
stanislav@stanislav:-% cd Игрушки_для_школьников
stanislav@stanislav:-% touch Роботы.txt
stanislav@stanislav:-% touch Конструкторы.txt
stanislav@stanislav:-% cd ..

3)    Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»
stanislav@stanislav:-% cd Игрушки_для_дошколят.txt
stanislav@stanislav:-% touch Мягкие_игрушки.txt
stanislav@stanislav:-% touch Куклы.txt
stanislav@stanislav:-% touch Машинки.txt

4)   Объединить 2 директории в одну «Имя Игрушки»
stanislav@stanislav:-cd ..
stanislav@stanislav:-% mkdir Имя_игрушки
stanislav@stanislav:-% cp-rl Игрушки_для_школьников/* Игрушки_для_дошколят/* Имя_игрушки 
stanislav@stanislav:-% tree Имя_игрушки
stanislav@stanislav:-% rm -rf Игрушки_для_школьников
stanislav@stanislav:-%rm -rf Игрушки_для_дошколят

5)   Переименовать директорию «Имя Игрушки» в «Игрушки»

stanislav@stanislav:-% mv Имя_Игрушки Игрушки
6)   Просмотреть содержимое каталога «Игрушки».
stanislav@stanislav:-% cd Имя_игрушки
stanislav@stanislav:-% ls-la
7)   Установить и удалить snap-пакет. (Любой, какой хотите)
stanislav@stanislav:-% sudo snap intall (имя пакета) -установка
stanislav@stanislav:-% sudo snap remove (имя пакета) -удаление
8)   Добавить произвольную задачу для выполнения каждые 3 минуты 
9)   (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).
stanislav@stanislav:-% crontab -e
*/3 * * * * echo 'Hello world' >>/home/User_Name/Игрушки/Роботы.txt
(до-запись в файл каждые 3 минуты)