```haskell
-- FilterEvens.hs
-- Recursive function to filter all even numbers from a list

-- Define the filterEvens function
filterEvens :: [Int] -> [Int]
filterEvens [] = []                                -- Base case
filterEvens (x:xs)
    | even x    = x : filterEvens xs               -- Include even number
    | otherwise = filterEvens xs                   -- Skip odd number

-- Main function to test filterEvens
main :: IO ()
main = do
    putStrLn "Enter a list of integers separated by spaces:"
    input <- getLine
    let numbers = map read (words input) :: [Int]
    let result = filterEvens numbers
    putStrLn ("Even numbers: " ++ unwords (map show result))
```

---

### ✅ How to Run:

1. Save as `FilterEvens.hs`.
2. Execute with:

   ```bash
   runghc FilterEvens.hs
   ```

---

### 💡 Example Output:

```
Enter a list of integers separated by spaces:
1 2 3 4 5 6 7 8
Even numbers: 2 4 6 8
```


