# Красный калькулятор

Пишем полноценный калькулятор, используя алгоритм рекурсивного спуска.

Общую идею берем из [**legacy**](https://github.com/timattt/Easy-py-calculator).
Только грамматику делаем более правильной.

## Грамматика

```
G ::= P
P ::= M {[+] M}*
M ::= T {[-] T}*
T ::= [-]+ K {[*] K}*
K ::= E {[/] E}*
E ::= [-]+ [number] | [(] P [)]
```

## Рандомизированные юнит-тесты

Чтобы протестить, что все считается иделаьно правильно, мы используем питон. Сгенерируем рандомно выражение и посчитаем значение через наш код и используем команду:

```
python -c "print( EXPR )"
```

Теперь остается только сравнить два числа и увидеть, что алгоритм работает идеально правильно.

## Сборка

Можно собрать через **cmake**. Тогда у вас будет доступно два исполняемых файла. Один запускает юнит-тесты, другой запускает сам калькулятор.
