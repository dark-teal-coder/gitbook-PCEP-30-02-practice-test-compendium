# PCEP-30-02 Practice Test Compendium – Loops

## Loops

01\) **The `while` loop statement** is a means allowing the programmer to **repeat** the execution of the selected part of the code as long the specified condition is **true**. The condition is checked before the loop's first turn, and therefore the loop's **body** may not even be executed once.

02\) The basic form of the while statement looks as follows:

```python
while condition:
    instructions
```

03\) The `condition` is an **expression** – as long it evaluates to `True`, or to a **non-zero** numeric value, or to a **non-empty** string, it is fulfilled (met) and is not `None`, the nested instructions placed after the `while` are **executed**.

04\) When the condition is **not met**, these instructions are **skipped**.

For example, the following snippet prints `TRUE` twice to the screen:

```python
counter = 2
while counter > 0:
    print('TRUE')
    counter -= 1
```

05\) The `else` branch can be used to specify a part of the code that should be executed when the loop’s condition is not met:

```python
while condition:
    instructions
else:
    instructions
```

For example, the following snippet prints `TRUE FALSE` to the screen:

```python
counter = 1
while counter > 0:
    print('TRUE', end=' ')
    counter -= 1
else:
    print('FALSE')
```

06\) If the condition is met at the beginning of the loop and there is no chance that the condition value has changed inside the body of the loop, the execution enters an **infinite loop** which cannot be broken without the user's intervention, for example by pressing the Ctrl-C (Ctrl-Break) key combination.

For example, the following snippet infinitely prints `TRUE` to the screen:

```python
while True:
    print('TRUE', end=' ')
```

07\) The `for` loop statement is a means allowing the programmer to **repeat** the execution of the selected part of the code when the **number of repetitions can be determined in advance**. The `for` statement uses a dedicated variable called a **control variable**, whose subsequent values reflect the status of the iteration.

08\) The basic form of the for statement looks as follows:

```python
for control_variable in range(from, to, step):
    instructions
```

09\) The `range()` function is a generator responsible for the creation of a series of values starting from `from` and ending before reaching `to`, incrementing the current value by `step`.

10\) The invocation `range(i,j)` is the equivalent of `range(i, j, 1)`

11\) The invocation `range(i)` is the equivalent of `range(0, i)`

For example, the following snippet prints `0,1,2,` to the screen:

```python
for i in range(3):
    print(i, end=',')
```

For example, the following snippet prints `2 1 0` to the screen:

```python
for i in range(2, -1, -1):
    print(i, end=' ')
```

12\) The `else` branch can be used to specify a part of the code that should be executed when the loop's body is **not entered**, which may happen when the range being iterated is **empty** or when all the range's values have already been **consumed**.

For example, the following snippet prints `0 1 2 FINISHED` to the screen:

```python
for i in range(3):
    print(i, end=' ')
else:
    print('FINISHED')
```

For example, the following snippet prints `FINISHED` to the screen:

```python
for i in range(1,1):
    print(i, end=' ')
else:
    print('FINISHED')
```

13\) **The `break` statement** can be used inside the loop's body only, and causes immediate **termination** of the loop's code. If the loop is equipped with the `else` branch, it is omitted.

For example, these two snippets print `0 1` to the screen:

```python
# break inside for
for i in range(3):
    if i == 2:
        break
    print(i, end=' ')
else:
    print('FINISHED')
```

```python
# break inside while
i = 1
while True:
    print(i, end=' ')
    i += 1
    if i == 3:
        break
else:
    print('FINISHED')
```

14\) **The `continue` statement** can be used inside the loop's body only, and causes an immediate **transition** to the next iteration of the for loop, or to the `while` loop's condition check.

For example, these two snippets print `0 2 FINISHED` to the screen:

```python
# continue inside for
for i in range(4):
    if i % 2 == 1:
        continue
    print(i, end=' ')
else:
    print('FINISHED')
```

```python
# continue inside while
i = -1
while i < 3:
    i += 1
    if i % 2 != 0:
        continue
    print(i, end=' ')
else:
    print('FINISHED')
```
