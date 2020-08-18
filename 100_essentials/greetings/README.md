# Greetings

Everything you need to complete this challenge can be found [here](https://docs.python.org/3.8/tutorial/controlflow.html#defining-functions).

---

Define a function named `greet` that takes in a name and a message as inputs and returns a greeting in the following format:

```python
>>> greet("Mark", "Oh, hi")
'Oh, hi, Mark!'
```

Additionally, the message should default to "Hello" if none is provided.

```python
>>> greet("Dave")
'Hello, Dave!'
```

Define a function named `greet_with_style` that takes a name as a required positional parameter, an arbitrary amount of extra positional parameters, an optional key word parameter named `msg` that defaults to 'Hello', another optional key word parameter named `sep` that defaults to ', ', and a required keyword parameter named `punctuation`. `greet_with_style` should return a greeting (name + sep + message + puncuation) with any functions passed as additional positional arguments applied to it.

```python
>>> def starify(s):
...    return "*".join(list(s))
...
>>> def capitalize(s):
...    return s.upper()
...
>>> greet_with_style("Citizen", starify, capitalize, msg="Greetings", punctuation="!", sep='*')
'G*R*E*E*T*I*N*G*S***C*I*T*I*Z*E*N*!'
```

Define a function named `add_epitaphs` that will add epitaphs to a name. `add_epitaphs` should take a name and an arbitrary amount of key word arguments as inputs and return a string that is a name with all epitaphs added to it in the following format:

```python
>>> add_epitaphs("Gregson", Son="Greg", Leader="Kobolds")
'Gregson, Son of Greg, Leader of Kobolds'

>>> shout = lambda x: x.upper()
>>> greet_with_style(add_epitaphs(
...        "Gregson", Son="Greg", Leader="Kobolds"), shout, msg="Hello", punctuation="!")
'HELLO, GREGSON, SON OF GREG, LEADER OF KOBOLDS!'
```

Add a doc string and annotations to `greet_with_style`. A good doc string might describe what the function does and any inputs and outputs. For parameter and return annotations use either [type hinting](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html) or write a short description for each parameter.

## Hints

- [Python Docs tutorial section on fuctions](https://docs.python.org/3.8/tutorial/controlflow.html#defining-functions)
- [Variable length arguments in python](https://www.youtube.com/watch?v=kB829ciAXo4)
- [Documenting Python Code](https://realpython.com/documenting-python-code/)
- [Type hint cheat sheet](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html)

## Tests

Move your terminal to the directory that contains this README and then run `python -m unittest` to run the tests for this challenge.

Good luck!