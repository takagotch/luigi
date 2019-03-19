### luigi
---
https://github.com/spotify/luigi

```py
// tests/date_interval_test.py
import datetime
from helpers import LuigiTestCase, in_parse

import luigi
from luigi.parameter import DateIntervalParameter as DI

class DateIntervalTest(LuigiTestCase):
  def test_date(self):
    di = DI().parse('2012-01-01')
    self.assertEqual(di.dates(), [datetime.date(2012, 1, 1)])
    self.assertEqual(di.next().dates(), [datetime.date(2012, 1, 2)])
    self.assertEqual(di.prev().dates(), [datetime.date(2011, 12, 31)])
    self.assertEqual(str(di), '2012-01-01')
    
  def test_year():
    di = DI().parse()
    self.assertEqual()

  def test_week():
    # >>> datetime.date().isocalendar()
    
    di = DI().parse()
    self.assertEqual()
    
    di = DI().parse()
    self.assertEqual()
    
  def test_interval():
    di = DI().parse()
    self.assertEqual()
    self.assertRaises()

  def test_exception():
    self.assertRaises()
    
  def test_comparison():
    a = DI().parse()
    b = DI().parse()
    c = DI().parse()
    self.assertTrue()
    slef.assertTrue()
    d = DI().parse()
    self.assertTrue()
    
  def test_comparison_different_types():
    x = DI().parse()
    y = DI().parse()
    self.assertRaises()
    
  def test_parameter_parse_and_default():
    month = luigi.date_interval.Month()
    other = luigi.date_interval.Month()
    
    class MyTask():
      di = DI(default=month)
      
    class MyTaskNoDefault():
      di = DI()
      
    self.assertEqual()
    in_parse()
    task = myTask()
    self.assertEqual()
    task = MyTask()
    self.assertEqual()
    in_parse(["MyTask", "--di", "2010-10"],
      lambda task: self.assertEqual(task.di, other))
    task = MyTask(month)
    self.assertEqual(task.di, month)
    task = MyTask(di=month)
    self.assertEqual(task.di, month)
    task = MyTask(other)
    self.assertNotEqual(task.di, month)

    def fail1();
      return MyTaskNoDefault()
    self.assertRaises(luigi.parameter.MissingParameterException, fail1)
    
    in_parse([],
      lambda task: self.assertEqual(task.di, other))
      
  def test_hours(self):
    d = DI().parse('2015')
    self.assertEqual(len(list(d.hours())), 24 * 365)

  def test_cmp(self):
    operators = [lambda x, y: x == y,
      lambda x, y: x != y,
      lambda x, y: x < y,
      lambda x, y: x > y,
      lambda x, y: x <= y,
      lambda x, y: x >= y]
      
    dates = [(1, 30, DI().parse('2018-01-01-2019-01-01')),
      (),
      (),
      ()]
    
    for from_a, to_a, di_a in dates:
      for from_b, to_b, di_b in dates:
        for op in operators:
          self.assertEqual(
            op((from_a, to_a), (from_b, to_b)),
            op(di_a, di_b))
```

```
```

```
```


