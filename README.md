# Что это такое

Это довольно детальные планы занятий по программированию на Питоне с теми, кому тема ИТ изначально не очень близка, кто, скорее всего, не намерен становиться профессиональным программистом, а просто хочет приобрести новый навык для общего развития. Из контекста можно догадаться, к кому именно я обращаюсь, но это не так важно - есть желание сделать этот текст полезным для более широкого круга людей.

Очевидно, что существует много учебников по программированию, рассчитанных на разные уровни знакомства с предметом. Писать ещё один учебник просто из тяги к графоманству - отличная идея. Но это скорей именно детальные планы занятий - импровизация не моя сильная сторона. Планы будут писаться по мере нашего продвижения, и не факт, что закончатся чем-то существенным. Всё может прерваться, когда кто-то из нас потеряет интерес, или погрязнет в массе других более важных дел. Однако уже пройденные темы заслуживают того, чтобы составленный по ним конспект где-то остался.

Перед тем как начать, предупрежу, что буду использовать термины более вольно, чем это делают авторы университетских учебников. Что-то буду объяснять просто на примерах, без строгих определений.

# Кто я такой

[Довольно опытный программист](https://www.linkedin.com/in/2dkarpov/) с желанием что-то пообъяснять про основы программирования простым языком, но без большого опыта в преподавании.

# Что значит программировать

Вообще, компьютер понимает совсем не те команды, с которыми мы будем работать. Компьютер понимает *машинный код*. Машинный код удобен для компьютера, но на нём очень сложно писать программы. Придётся очень подробно рассказывать компьютеру, что ему делать. Настолько подробно, что сперва понадобится тщательно изучить, как работает компьютер на уровне железа. Мы же этого делать не будем.

Приведу аналогию: если б вместо того, чтобы попросить меня сходить в магазин за молоком, ты бы начала давать инструкции, когда какую ногу поднимать, сгибать в колене, когда и куда наклоняться, смотреть, когда и как шевелить пальцами открывая дверь магазина, как напрягать гортань, чтобы издать нужные звуки при общении с продавцом и т.д. Мне всё это не нужно, так как я сам могу перевести просьбу "сходи в магазин за молоком" в набор подробнейших инструкций. Я об этом даже не задумываюсь, ведь в нас, человеков, этот переводчик "зашивается" в первые же годы после рождения: помимо миллиона других вещей мы учимся хождению за молоком.

На компьютер же такой переводчик надо специально установить. В зависимости от деталей он называется "транслятор", "компилятор", "интерпретатор" и пр. Я предустановил интерпретатор Питона - языка программирования, с помощью которого мы будем добиваться от компьютера того, что нам надо.

# Как быть с искусственным интеллектом (ИИ)

Сейчас, конечно, можно попросить условный ChatGPT: "сделай мне веб-сайт" или "сделай мне игру". Но во-первых, ответом тебе будет, как правило, текст программы на каком-нибудь языке программирования, а во-вторых, нет гарантии того, что игра, написанная ChatGPT, будет работать именно так, как ты хотела. Ты можешь попросить что-то изменить в уже сделанной игре. Возможно, тебе повезёт, и ChatGPT в итоге сделает всё, как ты хочешь. Но чем более сложная и нестандартная задача стоит перед тобой, тем выше вероятность, что ИИ с ней не справится. По крайней мере пока такая работа с ChatGPT выглядит как взаимодействие с не очень квалифицированным программистом, у которого есть проблемы с пониманием того, что ты ему говоришь, а также серьёзные проблемы с обучением на лету. В конечном счёте, ты можешь решить, что проще всё сделать самой, потому что в отличие от запросов к ChatGPT, программный код понимается компьютером однозначно (однозначность - ключевое свойство программ!).

Изложенные соображения сильно упрощены и не включают фантазии на тему того, как будет выглядеть программирование и взаимодействие с компьютером лет через пятьдесят, но есть смутное подозрение, что и тогда "классическое" программирование будет весьма полезным навыком.

# Выполнение программ на Питоне, компиляторы, интерпретаторы

Программа на Питоне представляет собой *пошаговые инструкции*, опосредовано понятные компьютеру (переводимые в машинный код с помощью интерпретатора). Это не всегда так: программы на других языках программирования могут иметь вид, отличный от перечня действий, но Питон - преимущественно *императивный* язык, то есть мы прямо говорим компьютеру, что делать. В конечном счёте, "родной" машинный язык тоже императивный.

Интерпретатор отличается от компилятора. Компилятор переводит нашу программу в машинный код (иногда - в так называемый байт-код), и этот понятный компьютеру код сохраняется в файле. В Windows эти файлы, как правило, имеют расширение .exe (другими словами, их имена этих файлов заканчиваются на .exe) "exe" - сокращение от "executable" - "выполняемый", то есть тот, который без всяких дополнительных манипуляций может быть прочитан и выполнен компьютером. Именно поэтому так опасно открывать почтовые вложения, с расширением .exe - программа сразу начнёт выполняться и может при этом оказаться вредоносной.

Интерпретатор же не сохраняет машинный код в файл, но сразу же выполняет прочитанные строчка за строчкой команды на "человеческом" (*высокоуровневом*) языке программирования, таком как Питон. Поэтому при работе с Питоном мы будем видеть файлы .py ("py" - это от "PYthon"), которые представляют собой код на Питоне, но не будем трогать никаких "выполняемых" файлов, кроме, пожалуй, самого интерпретатора Питона, который имеет название `python` или `python.exe` в Windows. Интерпретатор - это готовая скомпилированная программа, набор машинных кодов, и эта программа будет выполнять наши программы на Питоне. Да-да, программа выполняет программу! А в конечном счёте их все выполняет компьютер.

# Первые строки, вывод на экран

Как человеческий язык состоит из слов, так же и программа состоит из них же, разделенных операторами (аналог знаков препинания). Слова и операторы назовём *лексемами*.

Разберем команду print ниже.

```python
print("Hello Kitty!")
```

Просто открой Notepad и напиши в ней эту строчку и сохрани файл на рабочем столе (File -> Save As..., или нажми Ctrl+S), дав название `kitty1.py`. Можешь выбрать какое-нибудь другое название, лишь бы заканчивалось на `.py` - я настроил Windows так, чтобы по двойному щелчку по файлам `.py` запускался интерпретатор Питона и начинал выполнять программу, сохранённую в файле. Если бы я это не настроил, тебе самой пришлось бы писать в командной строке примерно следующее:

```cmd
python.exe kitty1.py
```

Что означает "запусти интерпетатор Питона и "скорми" ему файл `kitty1.py` в качестве программы для выполнения". Также можно запускать интерпретатор в интерактивном режиме, когда он выполняет команды не из файла, а те, которые ты ему будешь вводить строчка за строчкой ~~целый роман~~, и он сразу же будет их выполнять. Кроме того, есть специализированные редакторы и даже так называемые интегрированные среды разработки (Integrated Development Environments, IDE), одной из которых является [PyCharm](https://www.jetbrains.com/pycharm/). Очень удобная штука, мы обязательно её освоим TODO!!!!!, но для начала будем следовать минималистичному подходу, чтобы состредоточиться на ключевых вещах и не отвлекаться на "приборную панель космолёта", которую из себя представляют современные IDE.

Вернёмся к разбору:

```python
print("Hello Kitty!")
```

`print` - это название действия. Затем мы открываем круглую скобку, обозначающую, что дальше идёт список того, что мы хотим, чтобы компьютер напечатал.

Дальше вместе с кавычками - это всё одна лексема `"Hello Kitty!"`. Лексемы в кавычках представляют собой текст, который мы хотим напечатать, сохранить на диск, отправить по электронной почте, и пр. Кавычки имеют примерно тот же смысл, что и в человеческих языках, они как бы обозначают прямую речь:

```
Выведи на экране: "Hello Kitty!"
```

Язык программирования, в каком-то смысле - это сильно упрощённый человеческий язык. В нём очень мало грамматических исключений и неоднозначностей, что упрощает работу с текстом программы как для человека, так и для компилятора или интерпретатора (так и для того, кто создавал этот компилятор/интерпретатор!).

В Питоне можно использовать апострофы вместо двойных кавычек (апострофы ещё называются одинарными кавычками):

```python
print('Hello Diso!')
```

Но если в тексте уже есть апостроф, то проще воспользоваться двойными кавычками:

```python
print("Diso is Polina's dad")
```

Вместо слова "текст" я буду часто употреблять "строка" ("string") или "строковое значение". Важно не путать *string*-строки и слово "строка", относящееся к той или иной строчке кода ("*line* of code"). Как быть, если в строке (string) присутствуют и апострофы, и двойные кавычки, расскажу потом, там всё не так сложно.

Очевидно, программа может состоять сразу из нескольких строк кода (команды в Питоне часто начинаются с новой строки):

```python
print("kitty")
print(42)
print(3+8)
```

Так же запиши их в Notepad, сохрани и выполни.

Заметь, здесь мы оперируем не только строками (strings), но и числами, и даже математическими выражениями. В третьей строчке мы просим компьютер сложить числа 3 и 8 и вывести на экран полученный результат. Числа отличаются от строк тем, что пишутся без кавычек. Однако если нам надо, чтобы наша строка содержала цифры, мы можем легко это сделать:

```python
print("12345")
print("Hello 333!")
```

Можешь написать в Notepad, сохранить и выполнить.

Если мы напишем слово без кавычек, компьютер будет думать, что это не строка, а какая-то команда или что-то ещё, чего он не знает, и выдаст ошибку при попытке выполнения такой программы:

```python
print(kitty)
```

Выдаст:

```
Traceback (most recent call last):
  File "...\kitty1.py", line 1, in <module>
    print(kitty)
          ^^^^^
NameError: name 'kitty' is not defined
```

# Переменные

Что есть в Питоне помимо команд, строк и чисел? Есть *переменные*. Переменные - это способ заставить компьютер что-то запоминать, пока он выполняет программу. Представь, что ты сама выполняешь какую-то сложную пошаговую инструкцию, и тебе надо запомнить разные слова и числа по ходу выполнения. Для этого тебе дали блокнот, в котором ты можешь на каждой странице записать либо число, либо текст. И при этом страницу обозначить не просто номером, а дать странице имя. Эта проименованная страница и будет переменной. А текст или число, записанное в ней - её значением.

Если нужно более строгое определение того, что такое переменная, то это *абстракция, представляющая собой проименованную область памяти в среде выполнения*. "Абстракция" - потому что в настоящем "железе" компьютера у ячеек памяти нет произвольных имён. Опуская детали, можно сказать, что у них есть номера (так называемые "адреса"). Возможность оперировать именами переменных нам даёт интерпретатор Питона. Он сам делает всю необходимую магию по переводу имён в номера/адреса, прямо в процессе выполнения твоего кода. Дальше ты убедишься, что использовать названия зачастую удобней, чем номера. А термин "среда выполнения" может означать совокупность компьютерного железа и программ, способствующих выполнению твоей программы. А может - как в примере выше - означать тебя и твою хитрую тетрадку!

Инструкция записать что-то в переменную выглядит довольно просто:

```python
kitty = 'Pet'
```

Обрати внимание, что имя переменной может состоять только из букв, цифр и символов подчёркивания. При этом имя не должно начинаться с цифры. Буквы могут быть как английскими, так и русскими, как строчными, так и заглавными. Имя, написанное строчными буквами, и такое же, но написанное заглавными, считаются разными. Также рекомендуется ограничить свою фантазию в названии переменных строчными английскими буквами и подчёркиванием.

Потом мы сможем ссылаться на запомненное значение по имени переменной:

```python
print(kitty)
```

Напиши эти две строчки кода в одном файле, сохрани, выполни. Дальше я не буду явно напоминать об этом. Ты просто пиши, всё, что тебе интересно повторить и с чем интересно поэкспериментировать. Советую не стесняться, и делать это как можно чаще. В программировании главное - практика.

Значения могут быть как строками, так и числами:

```python
hello = 4
kitty = 9
print(hello + kitty)
```

Пробелы, если что, вокруг плюса не обязательны:

```python
print(hello+kitty)
```

И вообще, пробелы мы добавляем, как правило, для лучшей читаемости наших программ.

Разумеется, можно не только складывать:

```python
print(hello * kitty)
print((hello - kitty) * hello)
```

# Конкатенация

Кстати, "складывать" можно не только числа, но и строки. Эта операция называется *конкатенация*. При конкатенации двух строк получается одна строка, состоящая из двух исходных, идущих подряд друг за другом, без всяких пробелов и знаков:

```python
hello = 'LO'
kitty = "VE"
piglet = hello + kitty
print(piglet)
```

Можно передавать выражения команде сразу, без использования переменных:

```python
print('Hello' + ' ' + 'World!')
```

Также обрати внимание, что в сложении и в конкатенации может участвовать более двух слагаемых.

А попробуй сконкатенировать строку и число, например, 42. Что получится?

```
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
```

Интерпретатор "ругнётся" при выполнении:

```
can only concatenate str (not "int") to str
```

В переводе на человеческий это значит: "Могу конкатенировать только строку со строкой (str), а строку с числом (int) не могу." int - это от "integer" - целое (не дробное) число; мы будем работать и с дробными числами, но потом TODO!!!!!.

Как нам тогда выводить комбинации текста и чисел? Можно, конечно, просто вызывать print несколько раз. Но ещё команда `print` принимает в качестве списка на вывод не только одно значение. Если нам нужно вывести сразу список значений, мы указываем их через запятую, внутри круглых скобок, принадлежащих команде `print`:

```python
print(hello, kitty, 333)
```

Все выведенные значения будут разделены пробелом. Обрати внимание, что выводимые значения могут быть разных типов: как строки, так и числа (в Питоне есть и другие типы, но о них позже TODO!!!!!).

# Чтение пользовательского ввода, программа-калькулятор

Пока наша программа не делает ничего интересного, и не предусматривает никакой реакции на действия пользователя. Пора добавить интерактива! Скомандуем компьютеру попросить пользователя ввести что-то с клавиатуры:

```python
input("What's your name?")
```

Очевидно, "What's your name?" - это вопрос, который мы хотим обратить к пользователю. Можешь написать что-нибудь другое. Выполнила программу? Что ж, для начала неплохо. Но есть два момента.

1. Пользователь начинает вводить своё имя, а оно примыкает к вопросительному знаку. Обычно это исправляется добавлением пробела в конце строки, перед закрывающей кавычкой:
   ```python
   input("Enter your name: ")
   ```
2. Второй момент более концептуальный. Окей, пользователь ввёл имя, а дальше что? Тут самое время узнать, что многие команды Питона не просто что-то делают, они ещё возвращают какое-нибудь значение. Некоторые команды вообще ничего не делают, а только возвращают какое-то значение в зависимости от переданных значений в круглых скобках. Эти переданные значения называются *параметрами* или *аргументами*. Команда `input`, как мы уже поняли, выводит на экран значение переданного аргумента, а потом считывает ввод пользователя, при этом *возвращая* введенный пользователем текст! Таким образом, мы можем сохранить это значение в переменную для дальнейшей работы с ним.
   ```python
   name = input("Enter your name: ")
   print("Hello", name)
   ```

А попробуй так:

```python
print("Hello", name + "!")
```

Теперь давай напишем программу-калькулятор. Совсем простой калькулятор, который будет спрашивать у пользователя два числа и затем выдавать их сумму. На первый взгляд программа должна выглядеть как-то так:

```python
first_number = input("Enter first number: ")
second_number = input("Enter second number: ")
print("The sum is:", first_number + second_number)
```

Кстати, заметь, как мы пишем названия переменных с использованием строчных букв и символа подчёркивания. Читаемость кода - первое дело!

Позапускай программу, посмотри, как она работает. Что неправильно? Как думаешь, почему так?

```
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
```

Да, введенный пользователем текст, даже если он состоит из одних цифр, оказывается не числовым значением, а строковым; и операция `+` в третьей строчке программы является не сложением, а конкатенацией! Попробуй "скормить" своей программе в этот раз какой-нибудь текст, вместо цифр.

Давай вернемся на шаг назад и представим, как "правильный" вариант с заданными наперёд слагаемыми выглядел бы без команды `input`. Как-то так:

```python
first_number = 3
second_number = 4
print("The sum is:", first_number + second_number)
```

Можешь, кстати, сравнить с "неправильным" вариантом без `input`, который повторял бы нашу исходную ошибку:

```python
first_number = "3"
second_number = "4"
print("The sum is:", first_number + second_number)
```

Хорошо, а можем ли мы как-нибудь скомандовать компьютеру перевести наши строковые значения в целые числа? Да, можем! Для этого есть команда `int`:

```python
first_number = int("3")
second_number = int("4")
print("The sum is:", first_number + second_number)
```

Ура! Работает! Теперь сделаем то же для полноценного варианта с командой `input`. Скомбинируем команды:

```python
first_number = int(input("Enter first number: "))
second_number = int(input("Enter second number: "))
print("The sum is:", first_number + second_number)
```

Обрати внимание на вложенные скобочки. В первой строчке мы говорим компьютеру: "Запроси у пользователя значение, переведи это значение в число и сохрани число в переменную `first_number`" Аналогично - для `second_number` во второй строке.

Как ещё можно скомбинировать команды, чтобы достичь того же результата?

```
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
```

Например так:

```python
first_number = input("Enter first number: ")
second_number = input("Enter second number: ")
print("The sum is:", int(first_number) + int(second_number))
```

Хороший вопрос - а как лучше написать? Я бы предпочёл первый вариант, т.к. в нём явно присутствует выражение `first_number + second_number`, что является сутью нашей программы, можно сказать; и это выражение не "замусорено" всякими техническими деталями типа преобразования типов (т.е. перевода из строки в число).

# Порядок выполнения команд

Может показаться, что интерпретатор выполняет команды одна за одной, читая программу сверху вниз. Часто так и есть, но если присмотреться внимательней, в каждой строчке программы, как правило, содержится несколько команд.

Взять даже простой случай:

```python
print(2 + 3)
```

Здесь мы говорим компьютеру:
1. Сложи 2 + 3
2. Выведи результат на экран

Попробуй расписать сама более сложный случай: что и в каком порядке компьютер будет делать, выполняя такую однострочную программу?

```python
print("Hello", input("Enter your name: "), 33 + 1)
```

```
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
```

Можно подумать, что сперва компьютер выведет на экран "Hello". Но это не так. Рассмотрим, как происходит выполнение очередной команды.

Да, интерпретатор читает текст программы сверху вниз, слева направо, как мы читаем книжку. И вот он видит: "`print`. Ага, надо будет что-то вывести на экран!"

Интерпретатор продолжает читать слева направо. Очевидно, после открывающей круглой скобки идёт перечисление того, что именно команда `print` должна будет вывести на экран. Сперва это будет строка (string) `"Hello"`. Тут всё понятно.

Однако интерпретатор не спешит сразу же выводить эту строку! Сперва ему надо понять, а что вообще его попросят вывести на экран. `"Hello"` мы уже разобрали, но есть ещё аргументы. Казалось бы, зачем сначала собирать полный список аргументов, почему бы сразу не выполнить команду? Потому что команды бывают разные, и некоторые не могут быть выполнены без того, чтобы собрать весь список аргументов заранее. Представь, например, аналог плюса - команду `add`.

```python
add(2, 7)
```

Интерпретатор не может выполнить add, прочитав только первый аргумент - двойку! Что прибавлять к двойке-то? Именно поэтому интерпретатор сперва собирает все аргументы для команды.

Когда я говорю "собирает", я подразумеваю кое-что ещё. Чтобы приступить непосредственно к выполнению команды, компьютеру нужны *значения* аргументов. В этом плане компьютер прост и прямолинеен, как продавец в старой рекламе: "Сколько вешать в граммах?" И если бы мы писали в машинных кодах, нам (за некоторыми исключениями) пришлось бы всё так и разжёвывать компьютеру. Однако в Питоне и других языках мы можем написать следующим образом:

```python
add(2, 4 + 3)
```

Или даже так:

```python
add(2, add(4, 3))
```

Интерпретатор, собирая список аргументов для очередной команды, не просто их куда-то там себе складывает, а предварительно *вычисляет* каждый аргумент, если, конечно, есть что вычислять. Например, первый аргумент в примере выше (двойку) вычислять не надо - это уже вычисленное значение, число 2. А вот аргумент `add(4, 3)` компьютеру надо будет сперва вычислить! Таким образом, вся связка `add(2, add(4, 3))` будет выполнена в "вывернутом наизнанку порядке":

1. Складываем 4 и 3
2. Складываем 2 и полученный результат в п.1 (т.е. 7)

Это похоже на то, когда в повествовании автор отвлекается на сторонний сюжет, а потом возвращается к основной линии повествования, при этом обогащённой сторонним сюжетом, в свете которого всё может выглядеть несколько иначе.

Так же поступим и мы и вернёмся к разбору

```python
print("Hello", input("Enter your name: "), 33 + 1)
```

Напомню, интерпретатор уже понял, что ему придётся выводить что-то на экран (команда `print`). Также интерпретатор уже прочитал первый аргумент для этой команды (`"Hello"`), а дальше встретил на своём пути `input("Enter your name: ")`.

`"Hello"` вычислять/выполнять не надо - это уже само по себе значение. А `input(...)` - это команда, и мы не узнаем значение второго аргумента `print`, пока не выполним `input`! Благо, у `input` в качестве аргумента уже готовое значение `"Enter your name: "`, поэтому `input` будет выполнен сходу: на экране появится надпись "Enter your name: ", и пользователь будет должен ввести своё имя (или что ему взбредёт в голову, но предположим, что пользователь честный). И вот результатом выполнения `input` будет строка (string) с именем пользователя, и это же и будет значение второго аргумента для команды `print`!

При этом сбор аргументов для `print` всё ещё не закончен. Следующий (и последний) на очереди - `33 + 1`. Интерпретатор понимает, что `33 + 1` - это не готовое значение (не число), а целое математическое выражение, т.е. по сути тоже набор команд (в данном случае - одна команда), которые нужно выполнить компьютеру - прибавить к тридцати трём единичку. Интерпретатор вычисляет этот сложнейший пример, и полученный результат (численное значение `34`) включает в список аргументов для команды `print`.

Дальше интерпретатор встречает закрывающую скобку и понимает, что аргументов дальше не будет, и что самое время приступить к выполнению команды `print`, так как ему, интерпретатору, уже известно всё, что нужно печатать. В результате выполнения `print` будет выведена строчка:

```
Hello Имя 34
```

(Мы помним, что `print` выводит переданные аргументы через пробелы)

Таким образом, всё выполнение этой небольшой программы будет выглядеть как:

```
Enter your name: Diso
Hello Diso 34
```

Кстати, что-то подобное мы, люди, проделываем, когда решаем примеры, особенно те, в которых много скобочек: не просто проходимся слева направо, а обходим скобочки "сперва в глубину":

```
4 * (10 - (4 + 2) + 1)
```

# Домашнее задание 1: скобки и апострофы в одной строке

В качестве домашнего задания прошу тебя самой найти способ, как в одной строчке выводить и апострофы, и двойные кавычки. Например, нам надо вывести на экран вот такой вот текст:

```
Я сказал: "Привет, д'Артаньян!"
```

В принципе, ты уже можешь что-то придумать сама, исходя из полученных знаний. Но советую также погуглить и, возможно, даже спросить [ChatGPT](https://chatgpt.com/). Умение хорошо гуглить и формулировать вопросы для ChatGPT - один из ключевых навыков современного программиста. Вполне вероятно, в выдаче Гугла у тебя будут ссылки на сайт [StackOverflow](https://stackoverflow.com/). Это очень полезный сайт, где люди задают вопросы по программированию, а другие на них отвечают. Скорее всего, твои вопросы, которые у тебя будут возникать на первых этапах изучения Питона, уже заданы, и люди со StackOverflow на них уже ответили. Поэтому вводи в строке поиска необходимые ключевые слова и внимательно читай ответы. Важно, конечно, не просто "передирать" код со StackOverflow или откуда-то ещё (это может быть даже опасно!), а стараться понимать решение, и как оно работает.

# Повтор пройденного

Код нашего складывающего калькулятора выглядит следующим образом:

```python
first_number = int(input("Enter first number: "))
second_number = int(input("Enter second number: "))
print("The sum is:", first_number + second_number)
```

1. Мы знакомы с двумя типами значений в Питоне: текстом/строками (strings) и целыми числами (integers). Текстовые значения записываются в двойных кавычках или апострофах. Числа пишутся просто цифрами.
2. Мы умеем просить компьютер выводить на экран (`print`).
3. Мы понимаем, что многие команды компьютеру в Питоне имеют следующий вид:
   ```python
   some_command_name(argument)
   another_command_name(argument1, argument2, ...)
   ```
   Кстати, бывают команды вообще без аргументов, но со скобочками (скобочки дают понять компилятору, что это именно команда):
   ```python
   third_command()
   ```
4. Мы помним, что команды помимо явного эффекта после их выполнения (как, например, выведенный на экран текст) могут "возвращать" строку, число и т.д. Прямо как функции в математике.
5. С другой стороны, команды могут иметь форму математических выражений: `(2 + 3) * 5` и пр. Возвращаемым результатом математических выражений, очевидно, являются числовые значения: так `(2 + 3) * 5` "вернёт" `25`.
6. Мы не забыли, что для строковых значений тоже есть операция `+`, но она называется не "сложение", а "конкатенация", и результат конкатенации - это новая строка, состоящая из первой и второй, идущий друг за другом подряд.
7. Мы также умеем работать с переменными - запоминать результаты выполнения команд (в том числе результаты вычисления математических выражений). Для того, чтобы записать значение в переменную, мы используем символ `=` после имени переменной. Затем в коде мы можем ссылаться на сохраненное значение по имени нашей переменной. Имя переменной должно состоять из букв, цифр, символа `_` и начинаться с буквы или `_`, но НЕ с цифры!
8. Мы помним, что команда `print` выводит все переданные ей аргументы, разделяя их на экране пробелами. При этом в качестве аргументов можно передавать как непосредственно значения (строки, числа), так и математические выражения `2 + 3` или `first_number + second_number`, а также результаты выполнения других команд. Более того, для `print` типы аргументов могут быть разными: мы можем за один раз попросить вывести на экран сразу несколько значений разных типов. Это не всегда справедливо для остальных команд. С учётом сказанного, мы можем комбинировать наши команды компьютеру:
   ```python
   print("Hello", input("Enter your name: "), 33 + 1)
   ```
9. Мы умеем пользоваться командой `input` - приказать компьютеру запросить у пользователя текст. В качестве результата `input` возвращает введённый текст. Результат можно сразу передать в качестве аргумента в другую команду (см. пример c `input` и `print` выше) или же сохранить в переменную для дальнейшего использования:
   ```python
   name = input("Enter your name: ")
   ```
10. Мы отдаём себе отчёт в том, что `input` возвращает именно string (строковое значение). Если мы хотим над вводом пользователя совершать какие-то математические операции, как в нашем калькуляторе, нам нужно результат `input`'а перевести в числовое значение. В этом нам поможет команда `int`:
   ```python
   first_number = int(input("Enter first number: "))
   ```

# Разбор домашнего задания 1

В ходе выполнения домашнего задания, можешь ввести в Гугле "python double quotes in string". Мне в топе выдачи попалась [вот эта ссылка](https://note.nkmk.me/en/python-str-literal-constructor/). Хорошая заметка, исчерпывающее объяснение. Некоторые термины могут отличаться от тех, что употреблял я, но в общем-целом должны быть понятны из контекста. Так, например, "text sequence" - это тот самый "текст" или строка (string), с которым мы до этого успели поработать. "Built-in types" ("встроенные типы") - это основные типы значений в Питоне. Пока, как отмечалось выше, мы знаем текстовый тип и целочисленный, и вскользь упомянули дробные числа. Но есть и другие встроенные типы, а есть также и "невстроенные" типы, то есть те, которые мы можем создавать сами. Но о них позже. TODO!!!!

Также можно спросить [ChatGPT](https://chatgpt.com). Не обязательно формулировать вопрос полностью корректно. Можно написать что-то типа "How to write double quotes in Python?" и получить подробный ответ.

Давай внимательно изучим какой-либо из полученных ответов, и дальше я буду подразумевать, что ты знаешь, как написать двойную кавычку с помощью обратного слэша (backslash) или использовать тройные кавычки в Питоне. Не стесняйся попробовать что-то из приведенных в статьях примерах в своем коде.

# Комментарии в коде

Кроме того, в статье, найденной в Гугле, ты могла встретить строчки, начинающиеся с символа решетки `#` Причем эти строчки как бы являются частью кода. Так и есть, они являются частью кода, но компилятор их игнорирует. Они нужны исключительно для "пометок на полях" - это *комментарии* к коду.

# Условный оператор if

Давай теперь начнём новую тему. Наш калькулятор замечательно складывает числа. Но что делать, если пользователю ещё нужно и вычитание? Конечно, в такой простой программе на Питоне можно прямо в самом коде поменять плюс на минус и получить новую "фичу". Но программы бывают огромными. Кроме того, как мы помним, многие программы распространяются в виде файлов с машинным кодом, вносить изменения в который уж очень сложно. Короче, мы хотим, чтобы наша программа спрашивала пользователя, хочет ли он складывать или вычитать. Как-то так:

```
Enter first number: 42
Enter second number: 3
If you want to add those numbers, please enter +, or any other text to subtract: +
Result of addition: 45
```

Или в случае вычитания:

```
Enter first number: 42
Enter second number: 3
If you want to add those numbers, please enter +, or any other text to subtract: -
Result of subtraction: 39
```

Пока сделаем так, чтобы было необязательно вводить минус для вычитания, а можно было бы ввести что угодно, кроме `+`. Можно даже просто нажать Enter (т.е. вести *пустую строку*):

```
Enter first number: 5
Enter second number: 1
If you want to add those numbers, please enter +, or any other text to subtract:
Result of subtraction: 4
```

Пожалуй, первые две строчки кода нашего калькулятора оставим без изменений - они делают то, что нам пригодится и в новой версии программы:

```python
first_number = int(input("Enter first number: "))
second_number = int(input("Enter second number: "))
```

А дальше нам нужно запросить у пользователя "код операции" (плюсик или "не-плюсик"). Очевидно, что это будет строковое значение, и мы не будем преобразовывать его в число, а просто сохраним в переменную как есть:

```python
operation = input("If you want to add those numbers, please enter +, or any other text to subtract: ")
```

А теперь нам нужно делать разные вещи, в зависимости от содержимого переменной operation. Грубо говоря, наша логика должна выглядеть так:

```
Если в operation содержится + , то складывай
Иначе - вычитай
```

Такое неформальное описание ещё называется *псевдокодом*. Настоящий (не псевдо-) код на Питоне будет выглядеть примерно так же, но с рядом нюансов, которые обсудим ниже. Также добавлю уже написанные нами строчки программы и пару комментариев в коде, чтобы было наглядней:

```python
# User input

first_number = int(input("Enter first number: "))
second_number = int(input("Enter second number: "))
operation = input("If you want to add those numbers, please enter +, or any other text to subtract: ")

# Calculation

if operation == "+":
    result = first_number + second_number
    print("Result of addition:", result)
else:
    result = first_number - second_number
    print("Result of subtraction:", result)
```

В непустой строке, идущей после комментария `# Calculation` мы видим новую конструкцию:

```python
if условие:
```

В нашем случае "условие" - это то, что значение переменной `operation` должно быть равно `"+"`. Заметь, что в качестве "равно" мы используем не просто символ равенства `=`, а два подряд таких символа: `==`

Ведь одиночный символ равенства у нас уже занят под присвоение значений переменным! А таким "нестандартным" написанием мы даём интерпретатору понять, что мы не сохраняем что-то в переменную, а сравниваем её значение с чем-то, что идёт справа от `==`, то есть с `"+"` в нашем случае. Такая странность присутствует не только в Питоне, но и других языках, однако, не во всех.

Следующие две строчки, идущие после двоеточия, довольно очевидны, за исключением того, что имеют отступ от края. И этот отступ в Питоне играет важную роль. Во-первых, даже если такой отступ был бы необязателен, он сам по себе улучшает читаемость программы: мы сразу видим, что есть два блока, два режима выполнения - первый для сложения, второй для вычитания. Сравни с неправильным вариантом программы без отступов:

```python
if operation == "+":
result = first_number + second_number
print("Result of addition:", result)
else:
result = first_number - second_number
print("Result of subtraction:", result)
```

Если тебе кажется, что и так сойдёт, вспомни, что многие программы состоят из сотен и тысяч строк кода; и читать один большой абзац, как у Льва Толстого - то ещё удовольствие, учитывая, что вникаешь ты, по сути, в длинную пошаговую инструкцию или рецепт, а не в описание переживаний Андрея Болконского. Помимо человеческого фактора есть ещё и чисто "интерпретаторский", т.е. формальный. Представь, что какая-то твоя программа выглядит так:

```python
if grom_gryanul:
perekrestis()
rasslabsya()
```

Как ты прочитаешь такое руководство к действию? Допустим, гром грянул. Надо перекреститься, да? А расслабиться надо? Наверное, да. А если гром не грянул? Ну, наверное, креститься не надо. А расслабляться? Из написанной инструкции не понятно, то ли команда расслабиться относится только к случаю, когда гром грянул, то ли её надо выполнять всегда, вне зависимости от грома.

А вот если мы добавим отступы, всё станет однозначно, как человеку, так и интерпретатору Питона:

```python
if grom_gryanul:
    perekrestis()
rasslabsya()
```

Ну или если расслабляться можно только после того, как перекрестился во время грома:

```python
if grom_gryanul:
    perekrestis()
    rasslabsya()
```

В других языках программирования используются не отступы, а, например, специальные скобочки вкупе с отступами:

```go
if grom_gryanul {
    perekrestis()
}
rasslabsya()
```

Причём отступы используются исключительно для читаемости человеком, а компилятор однозначно поймёт что делать, даже если вся инструкция будет написана в одну строчку:
```go
if grom_gryanul { perekrestis() } rasslabsya()
```

Смысл тот же, но синтаксические правила другие. А в Питоне бал правят отступы. Обычно один уровень отступа - это четыре пробела. В наших программах неизбежно будут и многоуровневые отступы, например, если в случае грома мужику надо сделать что-то ещё, но в зависимости от какого-то дополнительного условия (клюнул ли его жареный петух). Важно не переборщить с вложенными условиями: чем сильней мы "наворачиваем" логику, тем сложней её осмыслить, тем больше шансов самому запутаться в собственном коде, и запутать других. По ходу учёбы мы будем стараться делать наш код понятным для других людей.

Также посмотри примеры *условного ветвления* на визуальных языках и попробуй сопоставить с тем, что мы пишем на Питоне.

На языке [блок-схем](https://ru.wikipedia.org/wiki/%D0%91%D0%BB%D0%BE%D0%BA-%D1%81%D1%85%D0%B5%D0%BC%D0%B0) (это такой визуальный псевдокод для более наглядного представления программ):

![if на блок-схеме](if_block.png)

![if-else на блок-схеме](if_else_block.png)

На языке [Scratch](https://scratch.mit.edu/):

![if на Scratch](if_scratch.png)

![if-else на Scratch](if_else_scratch.png)

Видишь, мы, по сути, оформляем то же самое, но текстом. Большинство языков программирования всё-таки текстовые.

Итак, со сложением мы разобрались:

```python
if operation == "+":
    result = first_number + second_number
    print("Result of addition:", result)
```

Посмотрим на код дальше и обнаружим, что у нашей `if`-конструкции есть как бы продолжение - `else`. Оно тоже достаточно самоочевидно. Отмечу лишь, что и на `else`-блок распространяется правило отступов. Кроме того, существует и более универсальная конструкция, для случаев множественных *взаимоисключающих* условий: "если ... то, иначе если ... то, иначе если ... то, иначе ...":

```python
if условие_1:
   blah()
elif условие_2:
   blahblah()
elif условие_3:
   blahblahblah()
...
else:
   ...
```

`elif` здесь - это сокращение от `else if`. Примерно как в английском мы говорим и пишем "doesn't" вместо "does not". Только в Питоне `elif` писать обязательно. Если ты напишешь `else if`, интерпретатор тебя не поймёт.

# Домашнее задание 2: расширение функциональности калькулятора

Полагаясь на вышеобозначенную конструкцию, пожалуйста, добавь в наш калькулятор фичи умножения и деления. Cперва продумай и пропиши примеры, как будет выглядеть взаимодействие с пользователем, подобно тому, как я делал чуть раньше. Затем добавь какую-то одну фичу, скажем, умножение. Убедись, что она работает. Также убедись, что ты ничего не сломала из уже реализованных фич. А затем добавь и протестируй оставшуюся фичу - деление.

Кстати, тестирование - важнейшая часть разработки программ, но оно довольно быстро становится скучным: добавлять новые фичи гораздо веселей! Особенно бесит каждый раз перепроверять, что ты ничего не сломала из уже написанного (это называется регрессионное тестирование). Поэтому мы будем стремиться автоматизировать наши тесты. Как это делать - расскажу позже. TODO!!!!!!

И ещё. Когда пользователь вводит что-то кроме знака операции `+`, `-`, `*` или `/`, сделай так, чтобы программа выдавала сообщение `I don't understand you!`. Так наша программа будет чуть предсказуемей с точки зрения пользователя. UX (*User eXperience*) - опыт и впечателения пользователя от взаимодействия с программой - тоже очень важная штука. Чем меньше неоднозначностей и нестандартных преположений, тем лучше.

# Цикл
