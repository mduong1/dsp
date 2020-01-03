[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

import numpy as np

import nsfg
import first

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

print(firsts.totalwgt_lb.mean())
print(others.totalwgt_lb.mean())
print('On avg, first babies are lighter than others')

CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
print('Total weight comparison is bigger effect than pregnancy length)
