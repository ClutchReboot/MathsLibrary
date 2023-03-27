# Math Module
A work in progress, incomplete, library full of mathematical algorithms, constants, and functions.

## Table of Contents

- [Algorithms](#algorithm-class)
- [Constants](#constants-class)
- [Functions](#functions-class)


## **Algorithm Class**
This is a Python class that implements various algorithms, including finding the greatest common divisor using Euclid's algorithm, computing logarithms with a specified base, counting the occurrences of words in a text, and performing operations with fractions.

### `addition(*args: Union[int, float]) -> Union[int, float]`
Returns the sum of integers and/or floats.

##### **Arguments:**

    *args (Union[int, float]): A variable-length argument list of integers and/or floats

##### **Returns:**

    Union[int, float]: The sum of the integers and/or floats in *args

---
### `subtract(*args: Union[int, float]) -> Union[int, float]`
Returns integers or float of given numbers after being subtracted.

##### **Arguments:**

    *args (Union[int, float]): A variable-length argument list of integers and/or floats

##### **Returns:**

    Union[int, float]: The result of subtracting the integers and/or floats in *args from the first argument

---
### `multiply(*args: Union[int, float]) -> Union[int, float]`
Returns an integer or float of given numbers multiplied.

##### **Arguments:**

    *args (Union[int, float]): A variable-length argument list of integers and/or floats
    
##### **Returns:**

    Union[int, float]: The product of the integers and/or floats in *args

---
### `division_float(dividend: Union[int, float], divisor: Union[int, float]) -> Union[int, float]`
Returns a float of dividend divided by divisor.

##### **Arguments:**

    dividend (Union[int, float]): The number to be divided (dividend)

    divisor (Union[int, float]): The number to divide by (divisor)
    
##### **Returns:**

    Union[int, float]: The result of dividing the dividend by the divisor, as a float

---
### `division_int(dividend: Union[int, float], divisor: Union[int, float]) -> Union[int, float]`

Returns an integer of dividend divided by divisor.

##### **Arguments:**

    dividend (Union[int, float]): The number to be divided (dividend)
    divisor (Union[int, float]): The number to divide by (divisor)

##### **Returns:**

    Union[int, float]: The result of dividing the dividend by the divisor, rounded down to the nearest integer

---
### `division_remainder(dividend: Union[int, float], divisor: Union[int, float]) -> Union[int, float]`
Returns the remainder of dividend divided by divisor.

##### **Arguments:**

    dividend (Union[int, float]): The number to be divided (dividend)
    divisor (Union[int, float]): The number to divide by (divisor)

##### **Returns:**

    Union[int, float]: The remainder of dividing the dividend by the divisor

---
### `power(base: Union[int, float], exponent: Union[int, float]) -> Union[int, float]`
Returns base to the power of exponent.

##### **Arguments:**

    base (Union[int, float]): The base of the power operation
    exponent (Union[int, float]): The exponent of the power operation

##### **Returns:**

    Union[int, float]: The result of raising the base to the power of the exponent

---
### `log(self, x, base=10)`

Returns the logarithm of x with a specified base (default is 10)

##### **Arguments:**
    
        x (int/float): The value for which to compute the logarithm
        base (int/float, optional): The base of the logarithm. Defaults to 10.

##### **Returns:**

        Union[int, float]: The logarithm of x with the specified base

---
### `__ln(self, x)`

Returns the natural logarithm of x (base e)

##### **Arguments:**

        x (int/float): The value for which to compute the natural logarithm

##### **Returns:**

        The natural logarithm of x
---
### `__log10(self, x)`

Returns the logarithm of x (base 10)

##### **Arguments:**

        x (int/float): The value for which to compute the logarithm

##### **Returns:**

        The logarithm of x (base 10)
        
---
### `adding_fractions(self, *args)`

Returns the sum of multiple fractions

##### **Arguments:**

        *args (tuples): Multiple fractions represented as tuples of the form (numerator, denominator)

##### **Returns:**

        A tuple representing the sum of all fractions in reduced form (numerator, denominator)
        
---
### `find_gcd(self, a, b)`

Finds the greatest common divisor of two numbers using Euclid's algorithm.

##### **Arguments:**

        a: An integer
        b: Another integer

##### **Returns:**

        The greatest common divisor of a and b
        
---
### `count_words(text)`

Returns a dictionary containing the count of each word in the given text.

##### **Arguments:**

        text (str): The text to count the words in.

##### **Returns:**

        A dictionary where the keys are the unique words in the text and the values are the count of each word.

---
### `multiplying_fractions(self, *args)`

Returns the product of multiple fractions.

##### **Arguments:**

        *args: An arbitrary number of arguments. Each argument must be a tuple with two values, the numerator and denominator of a fraction.

##### **Returns:**

        A tuple containing the numerator and denominator of the product of the fractions.

##### **Raises:**

        ValueError: If any of the arguments are not tuples of length 2 or if any of the denominators are 0.

---
### `divide_fractions(self, *args: tuple[int, int]) -> tuple[int, int]`

Returns the result of dividing one fraction by another.

##### **Arguments:**

        *args: Two tuples, each with two values, representing the numerator and denominator of the two fractions.

##### **Returns:**

        A tuple containing the numerator and denominator of the quotient of the two fractions.

##### **Raises:**

        ValueError: If any of the arguments are not tuples of length 2.
        ZeroDivisionError: If the denominator of the second fraction is zero.
        
---        
### `proportion_rule(a: int, b: int, c: int = None, d: int = None) -> int`

Returns the fourth proportional number given three proportional numbers.
    
##### **Arguments:**

        a (int): The first proportional number.
        b (int): The second proportional number.
        c (int, optional): The third proportional number. Defaults to None.
        d (int, optional): The fourth proportional number. Defaults to None.
        
##### **Returns:**

        int: The fourth proportional number calculated from the input.
        
        If both `c` and `d` are None, `a` and `b` are assumed to be the first two proportional numbers, and `c` and `d` are set to `b` and `a` respectively. If `d` is None, `a` and `b` are assumed to be the first two proportional numbers, and `d` is calculated from `c` using the formula `d = (b * c) / a`. If `c` and `d` are both specified, `a` and `b` are assumed to be the first two proportional numbers, and the function calculates the fourth proportional number `x` using the formula `x = (b * d) / c`.
        
---
### `percentage_to_fraction(x: float) -> float`

This function converts a percantage `x` to a fraction.

##### **Arguments:**

      x (float): percentage
            
##### **Returns:**

      The fraction form of a percentage

---
### `fraction_to_percentage(numerator: int, denominator: int) -> float`

This function converts a fraction given by `numerator` and `denominator` to a percentage.

##### **Arguments:**

      numerator: The numerator of the fraction.
      denominator: The denominator of the fraction.

##### **Returns:**

      The fraction as a percentage.
            
---
### `linear_search(lst, target)`

This function searches for the `target` element in the given list `lst` and returns the index if found, otherwise returns -1.

##### **Arguments:**

        - None

##### **Returns:**

        - Index of target element or -1

---
### `binary_search(lst, target)`

This function searches for the `target` element in the given list `lst` using binary search and returns the index if found, otherwise returns -1.

##### **Arguments:**

        - None

##### **Returns:**

        - Index of target element

---
### `bubble_sort(lst)`

This function sorts the given list `lst` in ascending order using bubble sort and returns the sorted list.

##### **Arguments:**

        - None

##### **Returns:**

        - Sorted list
        
---
### `insertion_sort(lst)`

This function sorts the given list `lst` in ascending order using insertion sort and returns the sorted list.

##### **Arguments:**

        - None

##### **Returns:**

        - Sorted list using insertion point

---
### `merge_sort(lst)`

This function sorts the given list `lst` in ascending order using merge sort and returns the sorted list.

##### **Arguments:**

        - None

##### **Returns:**

        - Sorted list

---
### `square_root(num)`

This function computes the square root of a given number `num` using the Babylonian method.

##### **Arguments:**

      num (float): The number to find the square root of.

##### **Returns:**

      float: The square root of the given number.

---
### `factorial(num)`

This function computes the factorial of a given number `num`.

##### **Arguments:**
      
      num (int): The number to find the factorial of.

##### **Returns:**

      int: The factorial of the given number.
        
---
### `fibonacci(n)`

Compute the nth number in the Fibonacci sequence.

##### **Arguments:**

    n (int): The index of the desired Fibonacci number.

##### **Returns:**

    int: The nth number in the Fibonacci sequence.
    
---
### `is_prime(num)`

Check whether a given number is prime.

##### **Arguments:**

    num (int): The number to check for primality.

##### **Returns:**

    bool: True if the number is prime, False otherwise.
    
---
### `gcd(*args)`

Compute the greatest common divisor of two or more numbers.

##### **Arguments:**

    *args (int): Two or more numbers to find the GCD of.

##### **Returns:**

    int: The greatest common divisor of the given numbers.
    
---
### `lcm(*args)`

Compute the least common multiple of two or more numbers.

##### **Arguments:**

    *args (int): Two or more numbers to find the LCM of.

##### **Returns:**

    int: The least common multiple of the given numbers.
    
---
### `sort_numbers(numbers: List[Union[int, float]], reverse: bool = False) -> List[Union[int, float]]`

This function takes a list of numbers and returns a sorted list in ascending or descending order.

##### **Arguments:**

    numbers (List[Union[int, float]]): A list of integers or floats to be sorted.
    reverse (bool, optional): If True, returns the list in descending order. Defaults to False.

##### **Returns:**

    List[Union[int, float]]: A sorted list in ascending or descending order.
    
---
### `binary_search(numbers: List[Union[int, float]], target: Union[int, float]) -> int`

This function takes a sorted list of numbers and a target number and returns the index of the target number, or -1 if it is not found.

##### **Arguments:**

    numbers (List[Union[int, float]]): A sorted list of integers or floats.
    target (Union[int, float]): The number to search for in the list.

##### **Returns:**

    int: The index of the target number in the list, or -1 if it is not found.
    
---
### `linear_regression(x, y)`

Calculates the equation of the line of best fit (y = mx + b) for the given x and y values.

##### **Arguments:**

    x (list): A list of x values.
    y (list): A list of corresponding y values.

##### **Returns:**

    tuple: A tuple containing the slope (m) and y-intercept (b) of the line of best fit.
    
---    
### `matrix_addition`

This function takes in two matrices A and B of the same size, and returns their sum.

##### **Arguments:**

    A: A list of lists of floats representing the first matrix.
    B: A list of lists of floats representing the second matrix.

##### **Returns:**

    A list of lists of floats representing the sum of the matrices.
    
---
### `matrix_multiplication`

This function multiplies two matrices A and B and returns the resulting matrix.

##### **Arguments:**

    A: The first matrix.
    B: The second matrix.

##### **Returns:**

    A list of lists of floats representing the product of matrices A and B.
    
---
### `matrix_inversion`

This function inverts a matrix A and returns the resulting matrix.

##### **Arguments:**

    A: The matrix to be inverted.

##### **Returns:**

    A list of lists of floats representing the inverted matrix of A.
    
---
### `matrix_multiplication(A, B):`

Multiplies two matrices A and B and returns the resulting matrix.

##### **Arguments:**

        A (list[list[float]]): The first matrix.
        B (list[list[float]]): The second matrix.

##### **Returns:**

        list[list[float]]: The matrix product of A and B.

---
### `matrix_inversion(A):`

Inverts a matrix A and returns the resulting matrix.

##### **Arguments:**

        A (list[list[float]]): The matrix to be inverted.

##### **Returns:**

        list[list[float]]: The inverted matrix of A.
        
---        
### `newton_method(self, f, f_prime, x0, epsilon):`

Use Newton's method to find the root of a function f.

##### **Arguments:**
        
        - f (function): The function for which to find the root.
        - f_prime (function): The derivative of f.
        - x0 (float): The initial guess for the root.
        - epsilon (float): The desired level of accuracy.

##### **Returns:**
        
        - root (float): The estimated root of the function.
        
 ---   
### `gradient_descent(self, f, f_prime, x0, alpha, max_iters):`

Use gradient descent to find the minimum of a function f.

##### **Arguments:**
        
        - f (function): The function to minimize.
        - f_prime (function): The derivative of f.
        - x0 (float): The initial guess for the minimum.
        - alpha (float): The step size.
        - max_iters (int): The maximum number of iterations.

##### **Returns:**

        - minimum (float): The estimated minimum of the function.

---   
### `monte_carlo_simulation(self, n, f):`

Use Monte Carlo simulation to estimate the probability of an event.

##### **Arguments:**
        
        - n (int): The number of simulations to run.
        - f (function): A function that returns True or False for a given sample.

##### **Returns:**
        
        - probability (float): The estimated probability of the event.
        
---
### `distance(point1, point2):`

##### **Arguments:**
        
        - point1 (int/float): The position of point 1
        - point2 (int/float): The position of point 2

##### **Returns:**

        The distance between the two points
        
---
### `random_seed(seed):`

A simple pseudorandom number generator based on the linear congruential method.

##### **Arguments:**

        - seed (int): The seed value used to initialize the generator.

##### **Returns:**

        - A float between 0 and 1.
        
---
### `k_means_clustering(self, data, k):`

Use k-means clustering to group data points into k clusters.

##### **Arguments:**

        - data (list): A list of data points.
        - k (int): The number of clusters to form.

##### **Returns:**

        - clusters (list): A list of k clusters, each containing the data points assigned to that cluster.
        
---
### `exp(self, num: Union[int, float]) -> Union[int, float]:`

Returns the exponential value of a number.

##### **Arguments:**

        - num: a number whose exponential value is to be calculated

##### **Returns:**

        The exponential value of the input number
        
---
### `absolute(self, num: Union[int, float]) -> Union[int, float]:`

Returns the absolute value of a number.

##### **Arguments:**

        - num: a number whose absolute value is to be calculated

##### **Returns:**

        The absolute value of the input number
        
---
### `modulo(self, dividend: Union[int, float], divisor: Union[int, float]) -> Union[int, float]:`

Returns the remainder of dividing the dividend by the divisor.

##### **Arguments:**

        - dividend: the number to be divided
        - divisor: the number to divide by

##### **Returns:**
        
        The remainder of dividing the dividend by the divisor
        
---
### `sin(self, num: Union[int, float]) -> Union[int, float]:`

Returns the sine value of a number.

##### **Arguments:**

        - num: a number in radians whose sine value is to be calculated

##### **Returns:**

        The sine value of the input number
        
---
### `cos(self, num: Union[int, float]) -> Union[int, float]:`

Returns the cosine value of a number.

##### **Arguments:**

        - num: a number in radians whose cosine value is to be calculated

##### **Returns:**

        The cosine value of the input number

---
### `tan(self, num: Union[int, float]) -> Union[int, float]:`

Returns the tangent value of a number.

##### **Arguments:**

        - num: a number in radians whose tangent value is to be calculated

##### **Returns:**
        
        The tangent value of the input number


### `def next_prime(n):`

Finds the smallest prime number greater than n.

#### **Arguments:**
      - n (int): A positive integer.

#### **Returns:**

      - int: The smallest prime number greater than n.
            

### `def atan(x):`

Return the arc tangent of x, in radians.

#### ***Arguments:**
      - x (float): The value whose arc tangent is to be returned.

#### **Returns:**
      - float: The arc tangent of x, in radians.

### `def atan_helper(x):`

Helper function for atan. Computes the arc tangent of x in the interval [0, 1].

#### **Arguments:**
      - x (float): The value whose arc tangent is to be returned.

#### **Returns:**
      - float: The arc tangent of x, in radians.



## **Constants Class**

This is a Python class full of mathematical constants such a Pi or the speed of light.

### `speed_of_light(self):`

Returns the speed of light in meters per second

##### **Arguments:**

        - None

##### **Returns:**

        The speed of light in meters/second at 299_792_458
        
---
### `planck_constant(self):`
        pass
    
### `pi(self):`

The ratio of a circle's circumference to its diameter.

##### **Arguments:**

        - None
        
##### **Returns:**
        Pi, π, to the 20th decimal
        3.141_592_653_589_793_238_46
        
---
### `tau(self):`

the 19th letter of the Greek alphabet,
representing the voiceless dental or alveolar plosive IPA: [t].
In the system of Greek numerals, it has a value of 300.

##### **Arguments:**

        - None
        
##### **Returns:**
        tau, uppercase Τ, lowercase τ, or τ, to the 20th decimal
        6.283_185_307_179_586_476_92
        
---
### `phi(self):`

"The Golden Ratio"
In mathematics, two quantities are in the golden ratio
if their ratio is the same as the ratio of their sum
to the larger of the two quantities.

##### **Arguments:**

        - None

##### **Returns:**

        Uppercase Φ lowercase φ or ϕ: Value to the 20th decimal
        1.618_033_988_749_894_848_20
        
---
### `silver_ratio(self):`

"The Silver Ratio". Two quantities are in the silver ratio (or silver mean)
if the ratio of the smaller of those two quantities to the larger quantity
is the same as the ratio of the larger quantity to the sum of the
smaller quantity and twice the larger quantity

##### **Arguments:**

        - None
        
##### **Returns:**

        δS: Value to the 20th decimal
        2.414_213_562_373_095_048_80
        
---
### `supergolden_ratio(self):`

Returns the mathematical constant psi (the supergolden ratio).

##### **Arguments:**

        - None

##### **Returns:**
        
        ψ to the 25th decimal
        return 1.465_571_231_876_768_026_656_731_2
        
---
### `connective_constant(self):`

Returns the connective constant for the hexagonal lattice.

##### **Arguments:**

        - None
        
##### **Returns:**

        μ to the 4th decimal
        1.687_5
        
---
### `kepler_bouwkamp_constant(self):`

In plane geometry, the Kepler–Bouwkamp constant (or polygon inscribing constant)
is obtained as a limit of the following sequence.
Take a circle of radius 1. Inscribe a regular triangle in this circle.
Inscribe a circle in this triangle. Inscribe a square in it.
Inscribe a circle, regular pentagon, circle, regular hexagon and so forth.

##### **Arguments:**

        - None
        
##### **Returns:**

        K': to the 20th decimal
        0.114_942_044_853_296_200_70
        
---
### `def wallis_constant(self):`

Returns Wallis's constant.

##### **Arguments:**

        - None
        
##### **Returns:**

      Value to the 20th decimal
      2.094_551_481_542_326_591_48
      
---
### `eulers_number(self):`

A mathematical constant approximately equal to 2.71828 that can be characterized in many ways.
It is the base of the natural logarithms.
It is the limit of (1 + 1/n)n as n approaches infinity, an expression that arises in the study of compound interest.
It can also be calculated as the sum of the infinite series

##### **Arguments:**

        - None
        
##### **Returns:**

      e: Value to the 20th decimal. math.e
      2.718_281_828_459_045_235_36
      
---
### `natural_log(self):`

Natural logarithm of 2.

##### **Arguments:**

        - None
        
##### **Returns:**
        
      ln 2: Value to the 30th decimal. math.log(2)
      0.693_147_180_559_945_309_417_232_121_458
      
---
### `lemniscate_constant(self):`

The ratio of the perimeter of Bernoulli's lemniscate to its diameter, analogous to the definition of π for the circle.

##### **Arguments:**

        - None
        
##### **Returns:**
        
      ϖ: Value to the 20th decimal. math.sqrt(2)
      2.622_057_554_292_119_810_46 
      
---
### `eulers_constant(self):`

Not to be confused with Euler's Number.
Defined as the limiting difference between the harmonic series and the natural logarithm

##### **Arguments:**

        - None
        
##### **Returns:**

      γ: Value to the 50th decimal
      0.577_215_664_901_532_860_606_512_090_082_402_431_042_159_335_939_92
      
---
### `Erdős_Borwein_constant(self):`

The sum of the reciprocals of the Mersenne numbers

##### **Arguments:**

        - None
        
##### **Returns:**
        
      E: Value to the 20th decimal. sum([1 / 2 ** (2 ** i) for i in range(40)])
      1.606_695_152_415_291_763_78
      
---
### `omega_constant(self):`

Defined as the unique real number that satisfies the equation Ωe**Ω = 1.

##### **Arguments:**

        - None
        
##### **Returns:**
        
      Ω: Value to the 30th decimal
      0.567_143_290_409_783_872_999_968_662_210
      
---
### `Apérys_constant(self):`

The sum of the reciprocals of the positive cubes.

##### **Arguments:**

        - None
        
##### **Returns:**
        
      ζ(3): Value to the 45th decimal
      1.202_056_903_159_594_285_399_738_161_511_449_990_764_986_292
      
---
### `laplace_limit(self):`

The maximum value of the eccentricity for which a solution to Kepler's equation, in terms of a power series in the eccentricity, converges.

##### **Arguments:**

        - None
        
##### **Returns:**

      Value to the 35th decimal
      0.662_743_419_349_181_580_974_742_097_109_252_90
      
---
### `ramanujan_soldner_constant(self):`

A mathematical constant defined as the unique positive zero of the logarithmic integral function.

##### **Arguments:**

        - None
        
##### **Returns:**

      μ ≈: Value to the 45th decimal
      1.451_369_234_883_381_050_283_968_485_892_027_449_493_032_28
      
---
### `gauss_constant(self):`

Transcendental mathematical constant that is the ratio of the perimeter of
Bernoulli's lemniscate to its diameter, analogous to the definition of π for the circle.

##### **Arguments:**

        - None
        
##### **Returns:**
        
      G == ϖ /π ≈ 0.8346268: Value to the 7th decimal
      0.834_626_8
      
---
### `second_hermite_constant(self):`

_summary_

##### **Arguments:**

        - None
        
##### **Returns:**
        
      γ2 : Value to the 20th decimal
      1.154_700_538_379_251_529_01
---
### `liouvilles_constant(self):`

A real number x with the property that, for every positive integer n,
there exists a pair of integers (p,q) with q>1.

##### **Arguments:**

        - None
        
##### **Returns:**

      L: Value to the 119th decimal
      0.110_001_000_000_000_000_000_001_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_000_01

---
### `first_continued_fraction(self):`

_summary_

##### **Arguments:**

        - None
        
##### **Returns:**
        
      C_{1}: _description_
      0.697_774_657_964_007_982_01
      
---
### `ramanujans_constant(self):`

The transcendental number, which is an almost integer, in that it is very close to an integer.

##### **Arguments:**

        - None
        
##### **Returns:**

      e**{{\pi {\sqrt {163}}}}: Value to the 18th decimal
      262_537_412_640_768_743.999_999_999_999_250_073
      
---
### `glaisher_kinkelin_constant(self):`

A mathematical constant, related to the K-function and the Barnes G-function.

##### **Arguments:**

        - None
        
##### **Returns:**

      A: Value to the 20th decimal
      1.282_427_129_100_622_636_87
      
---
### `catalans_constant(self):`

Computes the Catalan's constant to the specified number of decimal places using the formula:

##### **Arguments:**

      n (int): The number of terms to sum to approximate the constant.

##### **Returns:**

      float: The computed value of the Catalan's constant.

##### **Example:**

      >>> catalan_constant(1000000)
      0.915965594177219

---
### `dottie_number(self):`

Calculates the unique real root of the equation cos(x) = x, known as the Dottie number, to the 20th decimal place.

The Dottie number is a constant that arises in the study of iterative methods and has connections to chaos theory.

##### **Arguments:**

        - None
        
##### **Returns:**

         float: The Dottie number, i.e., the unique real root of the equation cos(x) = x, to the 20th decimal place.
    
##### **Example:**

       >>> dottie_number()
       0.73908513321516064165

---
### `meissel_mertens_constant(self):`

Returns the Meissel-Mertens constant M to the 40th decimal place.

The Meissel-Mertens constant M is defined as the sum of the reciprocal of the primes up to n, where n is an arbitrary positive integer. It has important connections to prime number theory and the Riemann hypothesis.

This function uses a precomputed value of M to return the constant to the 40th decimal place.

##### **Arguments:**

        - None
        
##### **Returns:**

      M (float): The Meissel-Mertens constant M to the 40th decimal place.
      return 0.261_497_212_847_642_783_755_426_838_608_695_859_051_6

##### **Example:**

        meissel_mertens_constant()
        0.2614972128476427837554268386086958590516

---
### `universal_parabolic_constant(self):

The ratio, for any parabola, of the arc length of the parabolic segment formed by the latus rectum to the focal parameter.

##### **Arguments:**

        - None
        
##### **Returns:**

      P: Value to the 20th decimal
      2.295_587_149_392_638_074_03
      
---
### `cahens_constant(self):`

The value of an infinite series of unit fractions with alternating signs.

##### **Arguments:**

        - None
        
##### **Returns:**

      C: Value to the 20th decimal
      0.643_410_546_288_338_026_18
      
---
### `gelfonds_constant(self):`

Calculates Gelfond's Constant, which is defined as e raised to the power of pi.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Gelfond's Constant, which is approximately 23.1406926327792690057292.

            - return self.eulers_constant**self.pi
    
---
### `gelfond_schneider_constant(self):`

Returns the Gelfond-Schneider constant, which is a transcendental number defined as the value of 
2^(1/2) raised to the power of itself, or approximately 2.6651441426902251886502972498731.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Gelfond-Schneider constant.

            - pass

---
### `second_favard_constant(self):`

Returns the Second Favard constant, which is a mathematical constant defined as the limit of the 
arithmetic mean of the reciprocal of consecutive odd numbers, or approximately 0.661707182...

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Second Favard constant.

            - pass

---
### `golden_angle(self):`

Returns the golden angle constant, which is the angle subtended by the smaller of the two angles 
formed by dividing the circumference of a circle in the golden ratio. It is equal to 
(3 - sqrt(5)) * 180 degrees / pi, or approximately 137.5077640500378546463487 degrees.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the golden angle constant in degrees.

            - pass

---
### `sierpinskis_constant(self):`

Returns Sierpiński's constant, which is the fractal dimension of the Sierpiński triangle, a 
self-similar fractal shape. It is equal to log(3)/log(2), or approximately 1.585.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Sierpiński's constant.

            - pass

---
### `landau_ramanujan_constant(self):`

Returns the Landau-Ramanujan constant, which is a mathematical constant that appears in the 
asymptotic expansion of the partition function. It is equal to e^(pi * sqrt(163)), or approximately
2.2932021438344677e+17.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Landau-Ramanujan constant.

            - pass

---
### `first_nielsen_ramanujan_constant(self):`

Returns the First Nielsen-Ramanujan constant, which is a mathematical constant that appears in 
certain partition identities. It is equal to the product of a series involving the gamma function, 
or approximately 0.866081804933.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the First Nielsen-Ramanujan constant.

            - pass

---
### `gieseking_constant(self):`

Returns Gieseking's constant, which is a mathematical constant that appears in the theory of 
harmonic analysis. It is equal to (2*pi)^(-3/4), or approximately 0.7511255444649425.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Gieseking's constant.

            - pass

---
### `bernsteins_constant(self):`

Returns Bernstein's constant, which is a mathematical constant that appears in the theory of 
Fourier analysis. It is equal to pi/sqrt(2), or approximately 2.221441469079183.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Bernstein's constant.

            - pass

---
### `tribonacci_constant(self):`

Returns the Tribonacci constant, which is a mathematical constant defined as the unique real root 
of the polynomial x^3 - x^2 - x - 1, or approximately 1.8392867552141612.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Tribonacci constant.

            - pass

    
---
### `bruns_constant(self):`

Returns the limiting value of the sequence a(n) = sum(k=1 to n) 1/prime(k),
where prime(k) is the kth prime number.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Bruns constant, accurate to 42 decimal places.

            - pass

---
### `twin_primes_constant(self):`

Returns the limiting value of the sequence of twin primes (pairs of prime
numbers that differ by 2).

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the twin primes constant, accurate to 36 decimal places.

            - pass

---
### `plastic_number(self):`

Returns the unique positive real root of x^3 = x + 1.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the plastic number, accurate to 32 decimal places.

            - pass

---
### `blochs_constant(self):`

Returns the limiting value of the sequence of numbers that represent the
Bloch wall widths in ferromagnets.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Bloch's constant, accurate to 34 decimal places.

            - pass

---
### `z_score_975_percentile(self):`

Returns the value that has 97.5% of the area under a standard normal distribution
to the left of it.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the z-score at the 97.5th percentile, accurate to 9 decimal places.

            - pass

---
### `landaus_constant(self):`

Returns the limiting value of the sequence of numbers that represent the
probability that a random permutation of n elements will have no cycle of length
greater than log(n).

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Landau's constant, accurate to 19 decimal places.

            - pass

---
### `landaus_third_constant(self):`

Returns the limiting value of the sequence of numbers that represent the
probability that a random permutation of n elements will have no cycle of length
greater than sqrt(n) * log(n).

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of Landau's third constant, accurate to 20 decimal places.

            - pass

---
### `prouhet_thue_morse_constant(self):`

Returns the limiting value of the sequence of numbers that represent the
differences in density between the 0's and 1's in the Prouhet-Thue-Morse
sequence.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Prouhet-Thue-Morse constant, accurate to 20 decimal places.

            - pass
    
---
### `golomb_dickman_constant(self):`

The Golomb-Dickman constant represents the limiting distribution of the ratio of the k-th smallest
number in a sample of n random numbers to n^(1/k) as n approaches infinity. It is denoted by G.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Golomb-Dickman constant G, approximately 0.6243299885435508.

            - return 0.6243299885435508

---
### `lebesgue_asymptotic_behavior_constant(self):`

The Lebesgue asymptotic behavior constant describes the average size of the level sets
of a random walk in d dimensions. It is denoted by L(d).

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Lebesgue asymptotic behavior constant L(3), approximately 3.912023005428146.

            - return 3.912023005428146

---
### `feller_tornier_constant(self):`

The Feller-Tornier constant is the probability that a random walk on the integers
returns to the origin infinitely often. It is denoted by F.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Feller-Tornier constant F, approximately 0.259183.

            - return 0.259183

---
### `base_10_champernowne_constant(self):`

The Champernowne constant is formed by concatenating the base 10 representations of
successive integers, and is represented by C_10. 

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the base 10 Champernowne constant C_10, approximately 0.12345678910111213...

---
### `salem_constant(self):`

The Salem number is a complex number that is a root of a certain polynomial
with integer coefficients. It is denoted by s.

##### **Arguments:**

            - none

##### **Returns:**
            - complex: The value of the Salem constant s, approximately (1+sqrt(2)) * e^(pi*sqrt(2)/4).

            - return (1 + 2 ** 0.5) * Algorithm.exp(Constants.pi * 2 ** 0.5 / 4)
    
---
### `khinchins_constant(self):`

The Khinchin constant is a number that appears in the theory of continued fractions. 
It is denoted by K.

##### **Arguments:**

            - none

##### **Returns:**
            - float: The value of the Khinchin constant K, approximately 2.6854520010653065.

            - return 2.6854520010653065

---
### `levys_constant(self):`

Levy's constant, also known as the Levy–Khinchin constant, is a mathematical constant that arises in the study of 
Levy processes, which are stochastic processes that exhibit properties such as long-range dependence and heavy tails. 
It is defined as the limit of the average absolute difference between two random variables divided by their 
root-mean-square difference, as the sample size tends to infinity. The value of Levy's constant is approximately 
1.3303872425, with high precision being 1.33038724246235217434246.
            
##### **Symbol:**

            - γ or K

##### **Arguments:**

            - none


##### **Returns:**

            - float: The value of Levy's constant.
    
            - return 1.330_387_242_462_352_174_342_46

---
### `levys_constant_two(self):`

Calculate the value of e to the power of Levy's constant.

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of e to the power of Levy's constant.

            - return Algorithm.exp(self.levys_constant)

---
### `copeland_erdos_constant(self):`

Copeland-Erdős constant is the smallest number that is not the sum of 
distinct non-negative integer powers of 2.

##### **Symbol:**
            - C_E

##### **Arguments:**

            - none

##### **Returns:**

            - float
    
---
### `gompertz_constant(self):`

Gompertz constant is a mathematical constant named after Benjamin Gompertz,
it is the limit of the ratio between the life expectancy of a certain age 
and the remaining life expectancy.

##### **Symbol:**
            - γ

##### **Arguments:**

            - none

##### **Returns:**

            - float
    
---
### `de_bruijn_newman_constant(self):`

De Bruijn–Newman constant is the limit of the sequence of coefficients a_n
such that the entire function f(z) = Π_(n=1)^∞ [(1 - z/a_n) * exp(z/a_n)] has
no zeros in the complex plane.

##### **Symbol:**

            - λ

##### **Arguments:**

            - none

##### **Returns:**

            - float

---
### `van_der_pauw_constant(self):`

The van der Pauw constant is a constant used in measuring resistance of flat samples,
and is defined as the ratio of the natural logarithm of the quotient of two measured
resistances to the constant π.

##### **Symbol:**

            - K

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of the van der Pauw constant to the highest precision.

            - return Algorithm.exp(Constants.pi * MathFunctions.copysign(1, MathFunctions.acos(1/Constants.pi)))


---
### `magic_angle(self):`

        Magic angle is an angle of rotation for the bilayer graphene where the
        electronic properties of the material exhibit a number of interesting
        phenomena.

##### **Symbol:**

            - θ

##### **Arguments:**

            - none

##### **Returns:**

            - float: The magic angle in radians.

            - return Constants.arctan(Algorithm.square_root(3))


---
### `arctan(x):

Calculates the arctangent of x using a Taylor series approximation.

##### **Arguments:**
            x (float): A real number.

##### **Returns:**
            - float: The arctangent of x in radians.


---
### `artins_constant(self):`

The Artin's constant is a number that appears in the formula to calculate the Artin-Mazur zeta function.
It is defined as the infinite product of (1 - p^(-s)) where p ranges over all prime numbers and s is the reciprocal
of the prime number.

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of the Artin's constant to the highest precision.

---
### `porters_constant(self):`

Porter's constant is a mathematical constant that appears in the field of information theory. It is defined as
the limit of the ratio of the maximum number of different words of length n over the number of possible words of
length n as n approaches infinity.

##### **Symbol:**

            -

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of Porter's constant to the highest precision.

            - return Algorithm.exp**(1/Constants.euler_mascheroni_constant)

---
### `euler_mascheroni_constant(self):`

Returns the Euler-Mascheroni constant, a mathematical constant that appears in many areas of mathematics.
It is defined as the limit of the difference between the harmonic series and the natural logarithm of n as n approaches infinity.
        
The function calculates the value of the Euler-Mascheroni constant using a sum of the harmonic series and the natural logarithm of n.
The sum is taken over a large number of terms to achieve a high degree of accuracy.
        
Note that the function uses the 'math' module to calculate the natural logarithm, so it must be imported before the function can be called.

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of the Euler-Mascheroni constant to a high degree of accuracy.

---
### `lochs_constant(self):`

Lochs' constant is a mathematical constant defined as the limiting ratio of the perimeter of an inscribed regular
decagon to its diameter.

##### **Symbol:**

            - 

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of Lochs' constant to the highest precision.

            - return Algorithm.square_root(2 + Algorithm.square_root(2 + Algorithm.square_root(2 + Algorithm.square_root(2 + Algorithm.square_root(2)))))


---
### `deviccis_tesseract_constant(self):`

The De Vries - De Vos - Barendrecht - De Klerk - Smit - Smit constant (also known as De Vries' tesseract constant)
is defined as the number that describes the maximum ratio of the content of a hypercube inscribed in a tesseract to
the content of the hypercube circumscribed about the tesseract.

##### **Symbol:**

            -

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of De Vries' tesseract constant to the highest precision.

            - return Algorithm.square_root(2 + Algorithm.square_root(2)) / (2 * Algorithm.square_root(2))


---
### `liebs_square_ice_constant(self):`

The Lieb's square ice constant is the infinite sum of alternating sign reciprocals of the squares of odd positive integers.
It appears in the square ice problem in statistical mechanics.

##### **Symbol:**

            - 

##### **Arguments:**

            - none

##### **Returns:**

            - float: The value of the Lieb's square ice constant to the highest precision.

            - return Constants.pi / (Algorithm.square_root(3) * Algorithm.log((3 + Algorithm.square_root(8)) / 2))

---
### `nivens_constant(self):`

Niven's constant is a mathematical constant that is the only known integer x that is divisible by the sum of its digits
when written in decimal base. The constant is also related to the convergence of certain infinite series.

##### **Symbol:**

            - 

##### **Arguments:**

            - none

##### **Returns:**

            - int: The value of Niven's constant to the highest precision.
    
---
### `mills_constant(self):`

Mills constant is the smallest positive real number A such that the 
floor function of the double exponential function is a prime number,
where the double exponential function is f(n) = A^(3^n).

##### **Symbol:**

            - A

##### **Arguments:**

            - none

##### **Returns:**

            - float

---
### `artins_constant(self):`

            - pass
    
---
### `porters_constant(self):`

            - pass
    
---
### `lochs_constant(self):`

            - pass
    
---
### `deviccis_tesseract_constant(self):`

            - pass
    
---
### `liebs_square_ice_constant(self):`

            - pass
    
---
### `nivens_constant(self):`

            - pass

---
### `stephens_constant(self):`

            - pass

---
### `regular_paperfolding_sequence(self):`

            - pass

---
### `reciprocal_fibonacci_constant(self):`

            - pass
    
---
### `chvatal_sankoff_constant(self):`

For the binary alphabet
        
##### **Symbol:**

            - \gamma _{2}

            - pass
    
---
### `Feigenbaum_constant(self):`

Feigenbaum constant δ

##### **Symbol:**

            - \delta

            - pass
    
---
### `chaitins_constant(self):`

_summary_

##### **Symbol:**
            
            - \Omega 

##### **Raises:**
            
            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `robbins_constant(self):`

Summary

##### **Symbol:**
        
            - \Delta (3)

##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `weierstrass_constant(self):`

            - pass
    
---
### `fransen_robinson_constant(self):`

_summary_

##### **Symbol:**
            
            - F

##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `feigenbaum_constant(self):`

feigenbaum constant α

##### **Symbol:**
            
            - \alpha 

##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `second_du_bois_reymond_constant(self):`

Second du Bois-Reymond constant

##### **Symbol:**
            
            - C_{2}
             
##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `erdos_tenenbaum_ford_constant(self):`

_summary_

##### **Symbol:**
            
            - \delta
            
##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `conways_constant(Self):`

_summary_

##### **Symbol:**
            
            - \lambda
            
##### **Arguments:**

            - Self (_type_): _description_

##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `hafner_sarnak_mccurley_constant(self):`

_summary_

##### **Symbol:**

            - \sigma
        
##### **Raises:**

            - ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `backhouses_constant(self):`

_summary_

##### **Symbol:**
            
            - B
            
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `viswanath_constant(self):`

            - pass
    
---
### `komornik_loreti_constant(self):`

_summary_

##### **Symbol:**
            - q
            
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `embree_trefethen_constant(self):`

_summary_

##### **Symbol:**

            - {\displaystyle \beta ^{\star }}
            
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `heath_brown_moroz_constant(self):`

_summary_

##### **Symbol:**

            - C
            
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `mrb_constant(self):`

_summary_

##### **Symbol:**
            
            - S
        
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `prime_constant(self):`

_summary_

##### **Symbol:**

            - \rho 
        
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `somos_quadratic_recurrence_constant(self):`

_summary_

##### **Symbol:**

            - \sigma
        
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `foias_constant(self):`

_summary_

##### **Symbol:**
            
            - \alpha
        
##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `logarithmic_capacity(self):`

Logarathmic capacity of the unit disk

##### **Raises:**

            ValueError: _description_

##### **Arguments:**

            - none

##### **Returns:**

            - _type_: _description_

            - pass
    
---
### `taniguchi_constant(self):`

            - pass

---

## **Functions Class**

A class containing various mathematical functions.


### `area_of_circle(self, r: float) -> float:`

Calculates the area of a circle given its radius.

##### **Arguments:**

        - r: The radius of the circle.

##### **Returns:**

        - The area of the circle.
        - return 3.141592653589793238 * r ** 2

---
### `volume_of_sphere(self, r: float) -> float:`

Calculates the volume of a sphere given its radius.

##### **Arguments:**

        - r: The radius of the sphere.

##### **Returns:**

        - The volume of the sphere.
        - return 4 / 3 * 3.141592653589793238 * r ** 3

---
### `perimeter_of_rectangle(self, l: float, b: float) -> float:`

Calculates the perimeter of a rectangle given its length and breadth.

##### **Arguments:**

        - l: The length of the rectangle.
        - b: The breadth of the rectangle.

##### **Returns:**

        - The perimeter of the rectangle.
        - return 2 * (l + b)

---
### `pythagoras_theorem_length(self, a: float, b: float) -> float:`

Calculates the length of the hypotenuse of a right-angled triangle given the lengths of its two other sides.

##### **Arguments:**

        a: The length of one of the sides of the triangle.
        b: The length of the other side of the triangle.

##### **Returns:**

        The length of the hypotenuse of the triangle.
        return (a ** 2 + b ** 2) ** 0.5

---
### `square_root(self, x: float) -> float:`

Calculates the square root of a given number.

##### **Arguments:**

        x: The number to take the square root of.

##### **Returns:**

        The square root of x.
        return x ** 0.5

---
### `factorial(self, n: int) -> int:`

Calculates the factorial of a given number.

##### **Arguments:**

        n: The number to calculate the factorial of.

##### **Returns:**

        The factorial of n.

        fact = 1
        for i in range(1, n+1):
            fact *= i
        return fact

---
### `gcd(self, a: int, b: int) -> int:`

Calculates the greatest common divisor of two numbers.

##### **Arguments:**

        a: The first number.
        b: The second number.

##### **Returns:**

        The greatest common divisor of a and b.
        
        while(b):
            a, b = b, a % b
        return a

---
### `lcm(self, a: int, b: int) -> int:`

Calculates the least common multiple of two numbers.

##### **Arguments:**

        a: The first number.
        b: The second number.

##### **Returns:**

        The least common multiple of a and b.

        return a * b // self.gcd(a, b)

---
### `exponential(self, x: float) -> float:`

Calculates the value of e raised to a given power.

##### **Arguments:**

        x: The exponent.

##### **Returns:**

        The value of e raised to x.

        e = 2.718281828459045235
        return e ** x

---
### `logarithm(self, x: float, base: float) -> float:`

Calculates the logarithm of a given number to a given base.

##### **Arguments:**

        x: The number to take the logarithm of.
        base: The base of the logarithm.

##### **Returns:**

        The logarithm of x to the base.

        return (Functions.log(x) / Functions.log(base))

---
### `log(x):`

Calculates the natural logarithm of a given number.

##### **Arguments:**

        x: The number to take the natural logarithm of.

##### **Returns:**

        The natural logarithm of x.

        if x <= 0:
            return float('nan')
        elif x == 1:
            return 0.0
        else:
            return Functions.integrate(1/x, 1, x)

---
### `integrate(f, a, b):`

Approximates the definite integral of a function over a given interval using the trapezoidal rule.

##### **Arguments:**

        f: The function to integrate.
        a: The lower limit of the interval.
        b: The upper limit of the interval.

##### **Returns:**

        The approximate value of the definite integral of f over the interval [a, b].

        n = 1000 # Number of trapezoids to use
        dx = (b - a) / n
        x_values = [a + i * dx for i in range(n+1)]
        y_values = [f(x) for x in x_values]
        return (dx/2) * (y_values[0] + y_values[-1] + 2*sum(y_values[1:-1]))

---
### `surface_area_of_cylinder(self, r: float, h: float) -> float:`

Calculates the surface area of a cylinder given its radius and height.

##### **Arguments:**

        r: The radius of the cylinder.
        h: The height of the cylinder.

##### **Returns:**

        The surface area of the cylinder.

        return 2 * 3.14159265358979323846 * r * (r + h)

---
### `volume_of_cylinder(self, r: float, h: float) -> float:`

Calculates the volume of a cylinder given its radius and height.

##### **Arguments:**

        r: The radius of the cylinder.
        h: The height of the cylinder.

##### **Returns:**

        The volume of the cylinder.

        return 3.14159265358979323846 * r ** 2 * h

---
### `area_of_triangle(self, b: float, h: float) -> float:`

Calculates the area of a triangle given its base and height.

##### **Arguments:**

        b: The base of the triangle.
        h: The height of the triangle.

##### **Returns:**

        The area of the triangle.

        return 0.5 * b * h

---
### `sine(self, x: float) -> float:`

Calculates the sine of a given angle in radians.

##### **Arguments:**

        x: The angle in radians.

##### **Returns:**

        The sine of the angle.

        x = x % (2 * 3.141592653589793238)
        sign = 1 if x > 0 else -1
        x *= sign
        if x > 3.141592653589793238:
            x -= 2 * 3.141592653589793238
            sign *= -1
        return sign * (
            x - x ** 3 / 6 + x ** 5 / 120 - x ** 7 / 5040 + x ** 9 / 362880
        )
        
### `copysign(self, x, y):`

Return a float with the magnitude of x and the sign of y.

##### **Arguments:**

      - x (float): The magnitude of the result.
      - y (float): The sign of the result.

##### **Returns:**

      - float: A float with the magnitude of x and the sign of y.


---

### `acos(self, x):`

Return the arc cosine of x, in radians.

##### **Arguments:**

      - x (float): The value whose arc cosine is to be returned.

##### **Returns:**

      - float: The arc cosine of x, in radians.
        """

---

## **class Sequences:**

### `harmonic_number(self):`

      pass
---

### `gregory_coefficients(self):`

      pass
---

### `bernoulli_number(self):`

      pass
    
### `hermite_constants(self):`

      pass
---

### `hafner_sarnak_mccurley_constant(self):`

      pass
---

### `stieltjes_constants(self):`

      pass
---

### `favard_constants(self):`

      pass
---

### `generalized_bruns_constant(self):`

      pass
---

### `champernowne_constants(self):`

      pass
---

### `lagrange_number(self):`

      pass
---

### `fellers_coin_tossing_constants(self):`

      pass
---

### `stoneham_number(self):`

      pass
---

### `beraha_constants(self):`

      pass
---

### `chvatal_sankoff_constants(self):`

      pass
---

### `hyperharmonic_number(self):`

      pass
---

### `gregory_number(self):`

      pass
---

### `metallic_mean(self):`

      pass
