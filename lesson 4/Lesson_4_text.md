## Lesson 4

Курс по программированию на языке Python 

**3 слайд**- Поток команд

В программах, которые мы до сих пор рассматривали, последовательность команд всегда
выполнялась по порядку строго сверху вниз. А что, если нам необходимо изменить
поток выполняющихся команд? Например, если требуется, чтобы программа принимала
некоторое решение и выполняла различные действия в зависимости от ситуации; ска-
жем, печатала «Доброе утро» или «Добрый вечер» в зависимости от времени суток.
Как вы уже, наверное, догадались, этого можно достичь при помощи операторов управ-
ления потоком.

В Python есть три оператора управления потоком: if , for и while .

**4 слайд** - Функция Input

За ввод в программу данных с клавиатуры в Python отвечает функция input. Когда вызывается эта функция, программа останавливает свое выполнение и ждет, когда пользователь введет текст. После этого, когда он нажмет Enter, функция input() заберет введенный текст и передаст его программе, которая уже будет обрабатывать его согласно своим алгоритмам.

Давайте рассмотрим два примера:

1) Первый пример является наиболее простым для восприятия применения функции input(). Здесь мы вводим текст и присваиваем его переменной text. Затем просто выводим с помощью метода format наш введенный текст.
2) Во втором примере мы используем гораздо более сложные конструкции. Здесь мы имеем две переменные - first и second user, и мы будем вводить их возраст. Как вы видите, здесь мы изначально испольщуем оператор input("Введите возраст первого пользователя"). И так как по умолчанию тип нашей введенной переменной является строкой(string), то мы должны преобразовать ее в тип int, для того, чтобы мы могли производить математические операции. Затем мы выводим разницу между пользователями в виде выражения с методом format. Мы находим разницу между первым и вторым пользователем, а затем находим модуль от этого значения. Функция abs используется для нахождения абсолютного значения(модуля). Она отбрасывает знак минус.

Давайте рассмотрим данные программы на примере в Thonny.

Для начала рассмотрим первый пример. Мы инициализируем переменную text, вводим функцию input, и передаем строку, которую необходимо вывести на экран. "Введите текст". Затем нам необходимо эту строку вывести. Для этого используем знакомую функцию print, метод format и сообщение - "Пользователь ввел текст: ". Используем форматирование и нашу переменную text. Давайте запустим наш код. Как вы видите у нас запрашивают ввод текста с клавиатуры. Запишем "Привет". Нажимаем на клавишу Enter, и мы выводим наш текст в функции print. Этот пример является наиболее тривиальным, так что давайте рассмотрим более сложный пример.

Инициализируем две переменные. Первая переменная это first_user равная int(), затем input() и сообщение Введите возраст первого пользователя. Как я говорил ранее, изначально происходит вызов функции input, но в формате строки(string). Затем нам необходимо преобразовать его в тип int для выполнения математических операций.
Тоже самое сделаем и для второго user-a. А затем найдем разницу в их возрасте. print(f"Разница в возрасте между первым и вторым пользователем равна: ", опять форматирование, затем будем использовать функцию abs(нахождение модуля) и разницу first_user - second_user. Давайте запустим наш код для проверки. Это будет 23, а у второго 15. И как вы видите разница в возрасте между первым и вторым пользователем равна 8. Если же мы введем в первом случае 15, а во втором 23, то мы получим так же 8. Хотя вы знаете, что разница между большим и меньшим числом равна отрицательному числу. Поэтому мы применили функцию abs, для того, чтобы убрать минус.

**5 слайд** - Оператор if

Далее рассматриваем оператор условий или оператор if.

Оператор if используется для проверки условий: если условие верно , выполняется блок
выражений (называемый «if-блок»), иначе выполняется другой блок выражений (назы-
ваемый «else-блок»). Блок «else» является необязательным.

В этой программе мы принимаем варианты от пользователя и проверяем, сов-
падают ли они с заранее заданным числом. Мы устанавливаем переменной
number значение любого целого числа, какого хотим. Например, 23 . После
этого мы принимаем вариант числа от пользователя при помощи функции
input() .

Мы передаём встроенной функции input строку, которую она выводит на
экран и ожидает ввода от пользователя. Как только мы ввели что-нибудь и на-
жали клавишу Enter , функция input() возвращает строку, которую мы вве-
ли. Затем мы преобразуем полученную строку в число при помощи int() ,
и сохраняем это значение в переменную guess . Вообще-то, int – это класс,
но на данном этапе вам достаточно знать лишь, что при помощи него можно
преобразовать строку в целое число (предполагая, что строка содержит целое
число).

Далее мы сравниваем число, введённое пользователем, с числом, которое мы
выбрали заранее. Если они равны, мы печатаем сообщение об успехе. Обра-
тите внимание, что мы используем соответствующие уровни отступа, чтобы
указать Python, какие выражения относятся к какому блоку. Вот почему отсту-
пы так важны в Python. Я надеюсь, вы придерживаетесь правила «постоянных
отступов», не так ли?
Обратите внимание, что в конце оператора if стоит двоеточие – этим мы показываем, что далее следует блок выражений.
После этого мы проверяем, верно ли, что пользовательский вариант числа
меньше загаданного, и если это так, мы информируем пользователя о том,
что ему следует выбирать числа немного больше этого.
Выражения elif и else также имеют двоеточие в конце логической строки,
за которым следуют соответствующие блоки команд (с соответствующим чис-
лом отступов, конечно).
Внутри if-блока оператора if может быть другой оператор if и так далее – это
называется вложенным оператором if .
Помните, что части elif и else не обязательны.

Давайте рассмотрим это в коде. Для начала создадим переменную number и присвоим значение 23. Затам нам необходимо взять с клавиатуры число.
Для этого создадим переменную guess равную int, внутри будет функция input и сообщение "Введите целое число". 
Затем мы применяем оператор условия if. Если guess равен number, оператор сравнения, как вы помните,то мы выводим на экран print("Поздравляем вы угадали"). Иначе, имея другое условие, иначе-если guess меньше, чем number (то есть мы ввели число меньше 23), то мы выводим на экран "Нет, загаданное число должно быть немного больше". Это у нас два условия, но так же есть и другие варианты. Допустим число может быть больше, чем число, которое было у нас изначально. Для этого мы можем ввести "elif" и вместо знака меньше поставить знак больше, но так как у нас больше других вариантов быть не может мы просто ставим оператор else, который выполняется в любых других случаях, которые не были учтены в нашей программе. "Нет загаданное число должно быть немного меньше этого". 

Давайте запустим наш код, и проверим как он выполняется. Вводим число 14. В данном случае мы проверяем наше число в каждом блоке. Первый блок является ложным, возвращает False, так как 14 не равно 23. И мы переходим в следующий блок. В данном блоке условие удовлетворяется, так как 14 меньше 23 и мы выводим функцию print с данным сообщением. Так как мы выполнили данный блок, то остальные блоки не рассматриваются. Давайте попробуем еще раз, для этого запустим снова программу и введем 54. В данном случае мы пропускаем первые блоки условий, так как они ложные и выводим последний блок. Давайте наконец угадаем данное число. 23 и поздравляем, вы угадали. То есть подобным образом работает оператор if.

**6 cлайд** - Оператор while

Оператор while позволяет многократно выполнять блок команд до тех пор, пока выпол-
няется некоторое условие. Это один из так называемых операторов цикла. Он также может
иметь необязательный пункт else .

В этой программе мы продолжаем играть в игру с угадыванием, но преиму-
щество состоит в том, что теперь пользователь может угадывать до тех пор,
пока не угадает правильное число, и ему не придётся запускать программу
заново для каждой попытки, как это происходило до сих пор. Это наглядно
демонстрирует применение оператора while .
Мы переместили операторы input и if внутрь цикла while и установили
переменную running в значение True перед запуском цикла. Прежде всего
проверяется, равно ли значение переменной running True , а затем происхо-
дит переход к соответствующему while-блоку. После выполнения этого блока
команд условие, которым в данном случае является переменная running , про-
веряется снова. Если оно истинно, while-блок запускается снова, в противном
случае происходит переход к дополнительному else-блоку, а затем – к следу-
ющему оператору.

Блок else выполняется тогда, когда условие цикла while становится ложным ( False )
– это может случиться даже при самой первой проверке условия. Если у цикла while
имеется дополнительный блок else , он всегда выполняется, если только цикл не будет
прерван оператором break .
True и False называются булевым типом данных, и вы можете считать их эквивалент-
ными значениям 1 и 0 соответственно.

Давайте введем данный код в Thonny. Модифицируем нашу программу для того, чтобы она была немного удобнее. Для этого вводим переменную running и присваиваем ей значение True. Затем мы вводим наш оператор while, то есть пока наша программа запущена (переменная running равна True), мы будем продолжать выбирать наши числа. Однако если мы не будем менять переменную running, то данный цикл будет вечным. Затем после того, как мы угадаем, присвоим переменной running значение False. То есть мы завершаем программу при выполнении первого условия. Затем введем блок else и выведем "Цикл while закончен"

Давайте запустим нашу программу. Вводим целое число 45. Мы не угадали, попробуем еще раз. 13,  и опять же мы не угадали. Теперь введем число 23. И поздравляю, мы угадали и цикл while является завершенным. Здесь нет необходимости каждый раз запускать программу, на каждой итерации, после провальной попытки. Здесь можно играть бесконечно. И как только мы угадываем наше число, программа завершается.
**7 слайд** - Цикл for

Оператор for..in также является оператором цикла, который осуществляет итерацию по
последовательности объектов, т.е. проходит через каждый элемент в последовательности.

В этой программе мы выводим на экран последовательность чисел. Мы гене-
рируем эту последовательность, используя встроенную функцию range.
Мы задаём два числа, и range возвращает последовательность чисел от перво-
го числа до второго. Например, range(1,5) даёт последовательность [1, 2, 3, 4] . По умолчанию range принимает значение шага, равное 1. Если мы
зададим также и третье число range , оно будет служить шагом. Например,
range(1,5,2) даст [1,3] . Помните, интервал простирается только до второ-
го числа, т.е. не включает его в себя.
Обратите внимание, что range() генерирует последовательность чисел, но
только по одному числу за раз – когда оператор for запрашивает следую-
щий элемент. 
Затем цикл for осуществляет итерацию по этому диапазону - for i in
range(1,5) эквивалентно for i in [1, 2, 3, 4] , что напоминает при-
сваивание переменной i по одному числу (или объекту) за раз, выполняя блок
команд для каждого значения i . В данном случае в блоке команд мы просто
выводим значение на экран.

Помните, что блок else не обязателен. Если он присутствует, он всегда выполняется один
раз после окончания цикла for , если только не указан оператор break.
Помните также, что цикл for..in работает для любой последовательности. В нашем слу-
чае это список чисел, сгенерированный встроенной функцией range , но в общем случае
можно использовать любую последовательность любых объектов!

Рассмотрим цикл for. Для него мы применяем ключевое слово "for" и навзвание переменной number(или i, как это было на слайде), затем i in range и вводим два аргумента. То есть начиная единицей, заканчивая пятеркой, не включая ее. Выводим нашу переменную number, через print. Затем после окончания цикла мы выводим блок else. print("Цикл завершен"). Вы видите, что функция print выводит каждое число по одному разу. Чиcло 1, 2, 3, заканчивая 4, не включая 5. И в самом конце, как только наша последовательности заканчивается, мы приступаем к блоку else и выводим на экран "цикл завершен".

**8 слайд** - Оператор break 

Оператор break служит для прерывания цикла, т.е. остановки выполнения команд даже
если условие выполнения цикла ещё не приняло значения False или последователь-
ность элементов не закончилась.
Важно отметить, что если циклы for или while прервать оператором break, соответству-
ющие им блоки else выполняться не будут.

В этой программе мы многократно считываем пользовательский ввод и выво-
дим на экран длину каждой введённой строки. Для остановки программы мы
вводим специальное условие, проверяющее, совпадает ли пользовательский
ввод со строкой 'выход' . Мы останавливаем программу прерыванием цикла
оператором break и достигаем её конца.
Длина введённой строки может быть найдена при помощи встроенной функ-
ции len .
Помните также, что оператор break может применяться и в цикле for.
Рассмотрим эту программу в thonny. Задаем наш вечный цикл while True, то есть он будет выполняться бесконечно, так как здесь не используются переменные. Затем вводим какую-либо строку - input("Введите что-нибудь"). Затем с помощью условия if мы проверяем равна ли наша строка, строке "выход". И если она равна строке выход, то мы завершаем наш бесконечный цикл с помощью break оператора. Если наше условие не соблюдается, то мы выводим на экран длину введеной строки. Длина строки(то есть это количество символов) len(s). И в самом конце мы выводим завершение цикла. Давайте запустим наш код. Вводим любую строку 'Привет мир'. Так же можем ввести цифру, которая будет считаться строкой. Длина строки три символа. И для выхода из данного цикла мы используем слово 'выход'. И как вы видите происходит завершение - наш цикл остановился

