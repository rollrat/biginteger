# BigInteger Library
This library provides an easy-to-use big-integer method for 64-bit system. You can use this like c++ int type. This library makes use of that 32-bit operation can be used even in 64-bit system.

### BigBase
Bigbase is a positive integer class to implement BigInteger. This class is a core class that supports addition, subtraction, multiplication, division, and logical operations. Also, gcd, lcm operations are also provided.

``` c++
int main()
{
  BigBase factorial(1);
  
  for (int i = 1; i < 100; i++)
    factorial *= i;
  
  cout << factorial.to_string() << endl;
  cout << factorial.to_hex() << endl;
  cout << factorial.to_binary() << endl;
}
```

### BigInteger
BigInteger class is a signed integer class based on BigBase. This class provides User-defined Literals, `_i`.

``` c++
int main()
{
  // print decimal integer from hex string.
  cout << "x3F4C54109C045923"_i << endl;
}
```

### BigFraction
BigFraction class provides operations in the form of irreducible fraction. This class provides User-defined Literals, `_fr`.
``` c++
int main()
{
  BigFraction bf(0);
  for (int i = 1; i < 100; i++)
    bf += BigFraction(1, i);
  cout << bf << endl.
  cout << bf.fraction_point(10) << endl;
}
```
