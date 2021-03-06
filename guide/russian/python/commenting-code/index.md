---
title: Python Commenting Code
localeTitle: Код комментария Python
---
Комментарии используются для комментирования, описания или объяснения кода, который является сложным или трудным для понимания. Python намеренно игнорирует комментарии при компиляции с помощью байт-кода интерпретатором. [`PEP 8`](https://www.python.org/dev/peps/pep-0008/#comments) имеет раздел, посвященный комментариям. Они также повышают удобочитаемость кода, добавляя легкий и описательный язык для лучшего понимания.

**Заблокированные** и **встроенные** комментарии начинаются с символа `#` , за которым следует пробел перед комментарием:

```python
    # This is a block comment. 
    print('Hello world!') # This is an inline commment. 
```

Python не включает формальный способ написания многострочных комментариев. Каждая строка комментария, охватывающая несколько строк, должна начинаться с `#` и пробела:

```python
    # This is the first line of a multiline comment. 
    # This is the second line. 
```

Другим типом комментариев является **docstring** , задокументированная в [`PEP 257`](https://www.python.org/dev/peps/pep-0257/) . Docstrings - это особый тип комментария, который становится атрибутом `__doc__` .

Чтобы строковый литерал являлся docstring, он должен начинаться и заканчиваться символом `\"\"\"` и быть первым выражением определения модуля, функции, класса или метода, которое он документирует:

```python
    class SomeClass(): 
        """Краткое описание этого класса. 
 
        В этой части докстринга развернутое описание самого класса и
        аргументов которые принимает этот класс при инстанциации.
        """ 
 
        def method_a(self): 
            """Описание метода и какие аргументы ему нужно предоставлять.""" 
            pass 
```

Строковые литералы, которые начинаются и заканчиваются на `"""` , которые не являются docstrings (не первый оператор), могут использоваться для многострочных комментариев. Они не станут атрибутами `__doc__` . Если они не назначены переменной, они не будут генерировать байт-код. Существует некоторая дискуссия об использовании их в виде многострочных комментариев, найденных [здесь](http://stackoverflow.com/questions/7696924/multiline-comments-in-python) .
