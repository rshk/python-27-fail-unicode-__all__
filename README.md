# Weird behavior in Python 2.7.10

(completely fine with Python 3.4)

```
% python2 -c 'import mypackage'
Traceback (most recent call last):
File "<string>", line 1, in <module>
File "mypackage/__init__.py", line 5, in <module>
from .foo import *  # noqa
TypeError: Item in ``from list'' not a string``
```

```
% python2 -c 'import myotherpackage'
```


Might be related to https://bugs.python.org/issue21720
