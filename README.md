# prime_portraits

You can run the notebook in binder online which removes the need of having a powerful enough machine to look for large primes.
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ACFaul/prime_portraits_binder/HEAD)

I've added the picture of [Gauss](https://en.wikipedia.org/wiki/Carl_Friedrich_Gauss) from the German 10 DM bank note. He started the discussion of the [frequency of primes](https://en.wikipedia.org/wiki/Prime_number_theorem). He has his own notion of special primes, as part of [Gaussian integers](https://en.wikipedia.org/wiki/Gaussian_integer). If you want to know more about primes and the developments in Mathematics they inspired, I recommend [The Music of the Primes](https://en.wikipedia.org/wiki/The_Music_of_the_Primes) by [Marcus du Sautoy](https://en.wikipedia.org/wiki/Marcus_du_Sautoy). The investigation of the primes led to the still unsolved [Riemann hypothesis](https://en.wikipedia.org/wiki/Riemann_hypothesis). 

This implementation uses the [Miller–Rabin primality test](https://en.wikipedia.org/wiki/Miller%E2%80%93Rabin_primality_test). [Primify](https://github.com/LeviBorodenko/primify/) is another implementation. It uses the [Baillie–PSW primality test](https://en.wikipedia.org/wiki/Baillie%E2%80%93PSW_primality_test). This test is certain for numbers below 2<sup>64</sup> $\approx$ 1.845  10<sup>19</sup>. That is for numbers with up to 18 digits.

Alternatively, to run the prime portraits, you can follow the following steps: 
1. install docker compose
2. type docker-compose up

Alternatively, clone this repository and in the folder run: 
```bash
docker build -t primeportraits dockerfiles
docker run -it -p 8888:8888 -v $(pwd):/notebooks primeportraits
```
After you do this a jupyter notebook server should be started at http://localhost:8888/ . The password should be 'abc'
There you can open the jupyter notebook and find your own prime portrait!

