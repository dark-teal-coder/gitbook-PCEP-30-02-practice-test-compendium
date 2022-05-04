# PCEP-30-02 Practice Test Compendium – Conditional statements

## Conditional statements

01\) The **conditional statement** (the `if` statement) is a means allowing the programmer to branch the execution path and to execute (or not) selected instructions when a certain condition is met (or not).

02\) The basic form of the `if` statement looks as follows:

```python
if condition:
    instructions
```

03\) The `condition` is an **expression** – if it evaluates to `True`, or to a **non-zero numeric value**, or to a **non-empty string** and is not `None`, it is fulfilled (met), and the nested instructions placed after the `if` are **executed**.

04\) When the condition is not met, these instructions are **skipped**.

05\) When there is only one instruction that should be executed conditionally, the instruction can be written in the following form:

```python
if condition: instruction
```

06\) For example, the following snippet prints `TRUE` to the screen:

```python
counter = 1
if counter > 0:
    print('TRUE')
```

07\) The empty instruction denoted by the `pass` keyword can be used to indicate that no action should be performed in the specific context. As the `if` instruction syntax insists that there should be at least one statement after it, the following snippet does not affect program execution:

```python
if condition:
    pass
```

08\) It is suggested to use one tabulation character to make one indent level in Python code, while the recommended tab size (settable in virtually all code editors) is 4.

09\) The `else` branch can be used to specify a part of the code that should be executed when the condition is not met:

```python
if condition:
    instructions
else:
    instructions
```

10\) For example, the following snippet prints `TRUE` when the `counter` variable is greater than zero, and `FALSE` otherwise:

```python
if counter > 0:
    print('TRUE')
else:
    print('FALSE')
```

11\) To check more than one condition within one conditional block, the `elif` branch or branches may be employed. In that case, not more than one `if/elif` branch can be executed. The `else` branch is optional, and must be the last branch.

12\) For example, the following snippet prints `PLUS` when the counter variable is greater than zero, `MINUS` when it's less than zero, and `ZERO` when it's equal to zero:

```python
if counter > 0:
    print('PLUS')
elif counter < 0:
    print('MINUS')
else:
    print('ZERO')
```
