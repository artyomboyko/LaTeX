# LaTeX
LaTeX — наиболее популярный набор макрорасширений системы компьютерной вёрстки TeX, который облегчает набор сложных документов. В основном, совместно с Markdown он используется для набора математических формул.
    
    
## Вставка формул в Markdown
Вставить формулу LaTeX в текст Markdown можно, заключив её в одиночные `$` (для строчных формул) или двойные `$$` (для отдельно стоящих формул) знаки доллара.
- Строчная формула: `$E=mc^2$` отобразится как $E=mc^2$.
- Отдельно стоящая формула: `$$\int_a^b f(x) \, dx$$`
  отобразится как:
  $$\int_a^b f(x) \, dx$$
- ***Важно!*** между `$` или `$$` с обеих сторон формулы не должно быть пробелов!


## Показатель степени и индекс
Для отображения степени числа используется символ `^`, а для индекса — символ `_`. 

**Пример использования:**
1. `$a^2$` будет отображаться как $a^2$
2. `$a^{x+y}_{1}$` будет отображаться как $a^{x+y}_{1}$

    
## Групировка элементов
В LaTeX группировка элементов — это механизм, который позволяет объединять несколько элементов в один логический блок. Это достигается с помощью фигурных скобок `{}`.

Групировка элементов используется для:
1. **Применение команд к группе:** Фигурные скобки позволяют применять команду к группе элементов, а не к одному. Например, `\textbf{этот текст будет жирным}` сделает жирным весь текст внутри скобок.
2. **Математический режим:** В математических формулах группировка определяет порядок операций и область действия команд. Например, `x^{a+b}` $x^{a+b}$ возводит x в степень `a+b`, а не только в степень `a`.
3. **Ограничение области действия:** Можно ограничить область действия команды, заключив её в фигурные скобки. Например, `{\color{red} красный}` сделает красным только текст внутри скобок - ${\color{red} красный}$.

    
## Нумерация разрядов числа
Для нумерации разрядов числа используется комада `\stackrel{разряд числа}{число}`. 

**Пример использования:**     
`${\stackrel{5}{1}\stackrel{4}{1}\stackrel{3}{0}\stackrel{2}{1}\stackrel{1}{0}\stackrel{0}{1}}_2$` будет отображаться как ${\stackrel{5}{1}\stackrel{4}{1}\stackrel{3}{0}\stackrel{2}{1}\stackrel{1}{0}\stackrel{0}{1}}_2$.

## Вставка текста в LaTeX

Для вставки текста в математическом режиме используется команда `\text{текст}`.

Пример вставки текста с пробелами в LaTeX:    
`$Y = \\{\text{множество натуральных чисел меньших 6}\\}$` будет отображаться $Y = \\{\text{множество натуральных чисел меньших 6}\\}$

> ВАЖНО! В VSCode используется один символ `\` для экранирования специальных символов LaTeX (`{` и `}`) - `$Y = \{\text{множество натуральных чисел меньших 6}\}$`. Но на Github это отображается некоректно - $Y = \{\text{множество натуральных чисел меньших 6}\}$!

## Знаки отношений

Знаки отношений - используются в математике для сравнения двух величин или выражений. Они показывают, как эти величины соотносятся друг с другом: равны ли они, не равны, или одна больше/меньше другой.

| Знак отношения       | Команда LaTeX   | Пример          | Вывод         |
|:---------------------|:----------------|:----------------|:--------------|
| Равно                | `=`             | `$a = b$`       | $a = b$       |
| Не равно             | `\neq`          | `$a \ne b$`     | $a \ne b$     |
| Тождественно равно   | `\equiv`        | `$a \equiv b$`  | $a \equiv b$  |
| Приблизительно равно | `\approx`       | `$a \approx b$` | $a \approx b$ |
| Подобно              | `\sim`          | `$a \sim b$`    | $a \sim b$    |
| Меньше               | `<`             | `$a \lt b$`     | $a \lt b$     |
| Больше               | `>`             | `$a \gt b$`     | $a \gt b$     |
| Меньше или равно     | `\le`          | `$a \le b$`     | $a \le b$     |
| Больше или равно     | `\ge`          | `$a \ge b$`     | $a \ge b$     |    

## Математические операторы

Математические операторы - это символы, которые указывают на математические действия, которые нужно выполнить над числами или переменными.

| Оператор             | Команда LaTeX   | Пример                 | Вывод                 |
|:---------------------|:----------------|:-----------------------|:----------------------|
| Сложение             | `+`             | `$a + b$`              | $a + b$               |
| Вычитание            | `-`             | `$a - b$`              | $a - b$               |
| Умножение (крестик)  | `\times`        | `$a times b$`          | $a \times b$          |
| Умножение (точка)    | `\cdot`         | `$a cdot b$`           | $a \cdot b$           |
| Деление              | `/`             | `$frac{a}{b}$`         | $\frac{a}{b}$         |
| Квадратный корень    | `\sqrt{}`       | `$sqrt{a}$`            | $\sqrt{a}$            |
| Возведение в степень | `^`             | `$a^b$`                | $a^b$                 |
| Дробь                | `\frac{}{}`     | `$frac{a + b}{c - d}$` | $\frac{a + b}{c - d}$ |

##  Cимволы и операции теории множеств

| Операция/Символ | Команда LaTeX | Пример | Вывод |
|-----------------|---------------|--------|-------|
| Множество натуральных чисел | `\mathbb{N}` | `$\mathbb{N}$` | $\mathbb{N}$ |
| Множество целых чисел | `\mathbb{Z}` | `$\mathbb{Z}$` | $\mathbb{Z}$ |
| Множество рациональных чисел | `\mathbb{Q}` | `$\mathbb{Q}$` | $\mathbb{Q}$ |
| Множество иррациональных чисел | `\mathbb{I}` | `$\mathbb{I}$` | $\mathbb{I}$ |
| Множество вещественных (действительных) чисел | `\mathbb{R}` | `$\mathbb{R}$` | $\mathbb{R}$ |
| Множество комплексных чисел | `\mathbb{C}` | `$\mathbb{C}$` | $\mathbb{C}$ |
| Универсальное множество | `\mathbb{U}`| `$\mathbb{U}$`| $\mathbb{U}$ |
| Пустое множество | `\emptyset` | `$\emptyset$` | $\emptyset$ |
| Принадлежит     | `\in` | `$x \in A$` | $x \in A$ |
| Не принадлежит  | `\notin` | `$x \notin A$` | $x \notin A$ |
| Объединение     | `\cup` | `$A \cup B$` | $A \cup B$ |
| Пересечение     | `\cap` | `$A \cap B$` | $A \cap B$ |
| Разность        | `\setminus` | `$A \setminus B$` | $A \setminus B$ |
| Декартово произведение | `\times` | `$A \times B$` | $A \times B$ |
| Подмножество    | `\subseteq` | `$A \subseteq B$` | $A \subseteq B$ |
| Строгое подмножество | `\subset` | `$A \subset B$` | $A \subset B$ |
| Надмножество | `\supseteq` | `$A \supseteq B$` | $A \supseteq B$ |
| Строгое надмножество | `\supset` | `$A \supset B$` | $A \supset B$ |

## Греческие буквы

| Название буквы | Код LaTeX (заглавная) | Заглавная буква | Код LaTeX (строчная) | Строчная буква |
|---|---|---|---|---|
| Альфа | `A`  | A | `\alpha` | α |
| Бета | `B` | B | `\beta` | β |
| Гамма | `\Gamma` | Γ | `\gamma` | γ |
| Дельта | `\Delta` | Δ | `\delta` | δ |
| Эпсилон | `E` | E | `\epsilon` | ε |
| Дзета | `Z` | Z | `\zeta` | ζ |
| Эта | `H` | H | `\eta` | η |
| Тета | `\Theta` | Θ | `\theta` | θ |
| Йота | `I` | I | `\iota` | ι |
| Каппа | `K` | K | `\kappa` | κ |
| Лямбда | `\Lambda` | Λ | `\lambda` | λ |
| Мю | `M` | M | `\mu` | μ |
| Ню | `N` | N | `\nu` | ν |
| Кси | `\Xi` | Ξ | `\xi` | ξ |
| Омикрон | `O` | O | `\omicron` | ο |
| Пи | `\Pi` | Π | `\pi` | π |
| Ро | `P` | P | `\rho` | ρ |
| Сигма | `\Sigma` | Σ | `\sigma` | σ | 
| Тау | `T` | T | `\tau` | τ |
| Ипсилон | `\Upsilon` | Υ | `\upsilon` | υ |
| Фи | `\Phi` | Φ | `\phi` | φ |
| Хи | `X` | X | `\chi` | χ |
| Пси | `\Psi` | Ψ | `\psi` | ψ |
| Омега | `\Omega` | Ω | `\omega` | ω |

## Дополнительные математические символы

| Операция/Символ | Команда LaTeX | Пример | Вывод |
|-----------------|---------------|--------|-------|
| Знак плюс/минус | `\pm` | `$\pm 3$`| $\pm 3$|


