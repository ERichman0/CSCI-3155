2.  a. For the use of pi at line 4, the latest binding of a value to the variable is at line 3, as it's modified there right before the variable is used. For the use of pi at line 7, the latest binding of a value to the variable is at line 1, because the binding at line 3 only happens within the circumference function.

    b. For the use of x at line 3, the value is bound at line 1, right at the beginning. For the use of x at line 6, the value is still bound at line 1, since it hasn't actually been modified yet so far. For the use of x at line 10, the value is still bound at line 1, since the val x statement at line 8 is out of scope after the curly brackets end. Finally, for the use of x at line 13, the value is bound at line 1, since it's before you even go into function f.

3.  The body of g is well-typed.
- "val (a, b) = (1, (x, 3))
if (x == 0) (b, 1) else (b, a + 2)": ((Int, Int), Int) *because...*
    - "if (x == 0) (b, 1) else (b, a + 2)": ((Int, Int), Int) *because...*
        - (b,1): ((Int, Int), Int) *because...*
            - b: (Int, Int) *because...*
                - (x, 3): (Int, Int) *because...*
                    - x: Int
                    - 3: Int
            - 1: Int
        - (b, a + 2): ((Int, Int), Int) *because...*
            - b: (Int, Int) *because...*
            - a + 2: Int *because...*
                - a: Int *because...*
                    - 1: Int
                - 2: Int
