# UnitTest
## Doctest
``` python
class Calc(object):
    def add_num(self, x, y):
        """Add
        >>> c = Calc()
        >>> c.add_num(1,1)
        2

        >>> c.add_num('1', '1')
        Traceback (most recent call last):
        ...
        ValueError
        """
        if type(x) is not int or type(y) is not int:
            raise ValueError

        return x + y

    def sub_num(self, x, y):
        return x -y

if __name__ == '__main__':
    import doctest
    doctest.testmod()
```
## UnitTest
``` python
class Calc(object):
    def add_num(self, x, y):
        if type(x) is not int or type(y) is not int:
            raise ValueError
        return x + y

    def sub_num(self, x, y):
        return x -y
```
``` python
import unittest
import calc

class CalcTest(unittest.TestCase):
    def test_add_num(self):
        cal = calc.Calc()
        self.assertEqual(cal.add_num(1,  1),  2)

if __name__ == '__main__':
    unittest.main()

```
## UnitTest Mock
