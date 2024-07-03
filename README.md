# Parvej-nada-program
My first Nada Progrma

This program demonstrates a more complex computation involving division and outputting a computed result securely to `Party1`.

### New Nada Program:

```python
from nada_dsl import *


def nada_main():
    party1 = Party(name="Party1")
    my_int1 = SecretInteger(Input(name="my_int1", party=party1))
    my_int2 = SecretInteger(Input(name="my_int2", party=party1))

    # Compute the average of my_int1 and my_int2
    average = (my_int1 + my_int2) / 2

    # Output the computed average securely to Party1
    return [Output(average, "average_output", party1)]
```

### Program Explanation:

1. **Parties and Inputs**:
   - Defines `Party1` with two secret integer inputs (`my_int1` and `my_int2`).

2. **Computation**:
   - Computes the average of `my_int1` and `my_int2` using the formula `(my_int1 + my_int2) / 2`.

3. **Secure Output**:
   - Outputs the computed average securely to `Party1` using the `Output` function provided by `nada_dsl`.

### Why It’s Interesting:

- **Complex Computation**: Instead of simple arithmetic operations, the program performs a division to compute the average, showcasing more advanced usage of secure computations in multi-party scenarios.

- **Privacy-Preserving**: Demonstrates how sensitive calculations (like computing an average) can be performed securely without revealing individual inputs (`my_int1` and `my_int2`).

- **Real-World Application**: Reflects scenarios where parties need to compute aggregate statistics or averages collaboratively while ensuring data privacy and integrity.

### Purpose:

The purpose of this program is to demonstrate:
- The capabilities of `nada_dsl` in handling more complex computations beyond basic arithmetic.
- Practical applications of secure multi-party computation (MPC) in preserving privacy and enabling collaborative data analysis.
  
By extending the example to compute an average, the program illustrates how MPC frameworks like `nada_dsl` can be used to solve real-world problems involving secure data sharing and computation among multiple parties.
