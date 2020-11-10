
# Practicum №1 

### Общее описание алгоритма

- Динамика по стеку
- Идем по регулярке, если встречаем слово из алфавита -> пушим его в стек (заранее превращая его в лист стека - массив из k элементов (в i-м элементе хранится 1 или 0 - имеет ли данное множество слов, в нашем случае одно слово, слова длины i по модулю K
- Если встречаем звезду Клини, достаем вершину стека, к ней применяем длину клини(пытаемся сконкатенировать массив с собой же пока это получается(максимум k - 1 раз)), после чего результат пушим в стек
- С плюсом и точкой - аналогично, достаем два верхних элемента стека,  делаем соответствующие операции, результат пушим обратно в стек.
- Если стек после выполнения всех операций состоит не из одного элемента, либо оказался пустым, когда этого не могло произойти (после удаления первой вершины в стеке во время обработки операции '+', к примеру), то регулярное выражение задано в некорректном виде - результатом является  ERROR
- Если стек пуст, и никаких эксцессов - то ответ - это в точности L-й элемент вершины стека - ведь после прохода по регулярке вершина сообщает нам длины слов, содержащихся в языке, по модулю  K


### Запуск самого решения
		git clone https://github.com/amsilevich/Formals_Practicum1.git
		cd Formals_Practicum1/
		chmod 777 ./src/scripts/run.sh
		./src/scripts/run.sh

### Тестирование проекта
		git clone https://github.com/amsilevich/Formals_Practicum1.git
		cd Formals_Practicum1/
		chmod 777 ./src/scripts/run_tests.sh
		./src/scripts/run_tests.sh

### Оценка покрытия тестами
		git clone https://github.com/amsilevich/Formals_Practicum1.git
		cd Formals_Practicum1/
		chmod 777 ./src/scripts/run_coverage.sh
		./src/scripts/run_coverage.sh
		chromuim /coverage/coverage_build/lcoverage/index.html
