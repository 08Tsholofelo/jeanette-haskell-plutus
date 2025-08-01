```haskell
-- Digits.hs
-- Recursive function to extract digits of a number

-- Define the digits function
digits :: Integer -> [Integer]
digits n
    | n < 10    = [n]                                 -- Base case: single-digit number
    | otherwise = digits (n `div` 10) ++ [n `mod` 10] -- Recursive case

-- Main function to test digits
main :: IO ()
main = do
    putStrLn "Enter a positive number:"
    input <- getLine
    let number = read input :: Integer
    if number < 0
        then putStrLn "Please enter a non-negative number."
        else putStrLn ("Digits: " ++ show (digits number))
```

---

### ✅ How to Run:

1. Save the file as `Digits.hs`.
2. Run it using:

   ```bash
   runghc Digits.hs
   ```

---

### 💡 Example:

```
Enter a positive number:
12345
Digits: [1,2,3,4,5]
```

---
