You can set a seed, so that a set of randomly generated data can be re-quoted. 
Without setting a seed, the randomly generated data can vary from time to time (of course they CAN be the same, as they are random).

The form is `set.seed(n)`, where n is a number you assign to this seed and is not involved in calculations (like a name of this seed). 
The different seeds may have different sets of random data (of course, they CAN have the same).
```R
#Without seed
> rnorm(10)
 [1]  0.08988614  0.09627446 -0.20163395  0.73984050  0.12337950 -0.02931671
 [7] -0.38885425  0.51085626 -0.91381419  2.31029682
> rnorm(10)
 [1] -0.4380900  0.7640606  0.2619613  0.7734046 -0.8143791 -0.4384506
 [7] -0.7202216  0.2309445 -1.1577295  0.2470760

#With seeds
> set.seed(100)
> rnorm(10, 0, 1)
 [1] -0.50219235  0.13153117 -0.07891709  0.88678481  0.11697127  0.31863009
 [7] -0.58179068  0.71453271 -0.82525943 -0.35986213
> set.seed(99)
> rnorm(10)
 [1]  0.2139625  0.4796581  0.0878287  0.4438585 -0.3628379  0.1226740
 [7] -0.8638452  0.4896243 -0.3641169 -1.2942420
> set.seed(100)
> rnorm(10)
 [1] -0.50219235  0.13153117 -0.07891709  0.88678481  0.11697127  0.31863009
 [7] -0.58179068  0.71453271 -0.82525943 -0.35986213
#same data for same seed (100)
```
