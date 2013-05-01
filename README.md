Seongjin Cho (Josh)
===================

Problem 1
---------

Let f(x) = x^2 + a*x + b be a quadratic polynomial with integer 
coefficients, for example, f(x) = x^2+x+6. Formulate a conjecture 
about when the set {f(n) : n in Z and f(n) is prime} is infinite.

Solution:
---------

Some Analysis

Let us consider $f$. If $f$ can be factored into integer coefficients 
factors, then we know it cannot generate infinitely many prime numbers. 
(In fact, we can create at most one) However, this is not only the 
necesserary condition. The $f$ also needs to be 

If $f$ is irreduciable, then we know its roots are 
either complex or irrational. 
Given any polynomial $P(x)$, we can factor $P$ out until its argebraic multiplicity 
by the consequences of Fundamental Theorem of Algebra. But So 
$P$ should be irreducible over the integers because if 
not whatever the domain value is the image will be composite.
	
Finally, when there exists complex roots, we know there should be 
a conjugate since the coefficients of 


<dl>
	<dt>Conjecture</dt>
	<dd>
	Every polynomial with integer coefficients that has an complex roots 
	have infinitely many primes in the image where its domain is $\Z$.
	</dd>
</dl>
	
Problem 2
---------

Let n=15.
(1) Plot a frequency histogram that shows how the prime numbers up to 
10^7 are distributed modulo n. <br />
(2) Make a conjecture based on your data. <br />
(3) Obtain data for other values of n and make a more general conjecture. 

Solution:
---------


Hmm.. Seems like prime numbers are uniformly distributed. But on some numbers
such as $3$, $5$, $6$, $9$, $10$, $12$, $15$, there is one or no primes, 
we can check the reason of this behavior using the definition of modular operation. 
If we take $n$ to be prime number, then all the numbers between $1$ to $n$ 
will be relatively prime to $n$. Hence prime numbers will be uniformly 
distributed on all numbers before positive integer $n$. Let us check our 
work using sage.


Ahh when I put $n = 31$ which is also a prime, Prime numbers modulo $n$ 
are distributed uniformly on all of the numbers between $1$ to $31$. So there goes 
my conjecture.

<dl>
	<dt>Conjecture</dt>
	<dd>
	Prime numbers are evenly distributed among $I$ except at the number where $x_0 \in I$
	is not relatively prime to $n$.
	</dd>
</dl>

Problem 3
---------

I made up a rational number alpha whose numerator and denominator each 
have 7 digits. Here's two facts about that rational number: <br />
(1) it is congruent to 372806624339965 modulo 37+10^15; <br />
(2) its decimal expansion begins 0.13869616280169693.... <br />
What do you think my rational number is?

Solution
--------

The grand number is ~~~ $\frac{1234567}{8901234}$.

It can be calculated by these steps:
use continued_fraction(0.13869616280169693), 
find the convergents, 
cleverly choose the last fraction which has 7 digits for both 
numerator and denomiator (and it is very noticable too), 
and compute mod(numerator,10^15+37)*mod(1/denomiator,10^15+37) and 
check whether it is same as 372806624339965. (This above method 
works because 10^15+37 is prime number.)
