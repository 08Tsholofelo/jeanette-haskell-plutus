

```haskell
-- Fibonacci.hs
-- Recursive function to compute nth Fibonacci number

-- Define the recursive Fibonacci function
fibonacci :: Integer -> Integer
fibonacci 0 = 0                    -- Base case 1
fibonacci 1 = 1                    -- Base case 2
fibonacci n = fibonacci (n - 1) + fibonacci (n - 2) -- Recursive case

-- Main function to test the Fibonacci function
main :: IO ()
main = do
    putStrLn "Enter a number (n):"
    input <- getLine
    let n = read input :: Integer
    let result = fibonacci n
    putStrLn ("The " ++ show n ++ "th Fibonacci number is " ++ show result)
```

### How to run it:

1. Save this code in a file named `Fibonacci.hs`.
2. Run it using the Haskell interpreter:

   ```bash
   runghc Fibonacci.hs
   ```

### Example Output:

```
Enter a number (n):
7
The 7th Fibonacci number is 13
```

> ⚠️ **Note**: This recursive implementation is simple but inefficient for large `n` due to repeated calculations. For large values, a more efficient version (like memoization or tail recursion) is recommended. Let me know if you'd like that version too!
