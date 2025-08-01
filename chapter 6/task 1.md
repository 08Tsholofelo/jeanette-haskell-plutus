

```haskell
-- Factorial.hs
-- Recursive function to compute factorial

-- Define the factorial function
factorial :: Integer -> Integer
factorial 0 = 1                     -- Base case
factorial n = n * factorial (n - 1) -- Recursive case

-- Main function to test factorial
main :: IO ()
main = do
    putStrLn "Enter a number:"
    input <- getLine
    let number = read input :: Integer
    let result = factorial number
    putStrLn ("The factorial of " ++ show number ++ " is " ++ show result)
```

### How to run it:

1. Save the code in a file named `Factorial.hs`.
2. Compile it using GHC or run it with the interpreter:

   ```bash
   runghc Factorial.hs
   ```
3. It will prompt you to enter a number, then return the factorial.

### Example Output:

```
Enter a number:
5
The factorial of 5 is 1
