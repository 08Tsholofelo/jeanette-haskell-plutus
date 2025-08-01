```haskell
-- ListLength.hs
-- Recursive function to compute the length of a list

-- Define the listLength function
listLength :: [a] -> Int
listLength []     = 0                          -- Base case: empty list
listLength (_:xs) = 1 + listLength xs          -- Recursive case

-- Main function to test listLength
main :: IO ()
main = do
    putStrLn "Enter a list of elements separated by spaces:"
    input <- getLine
    let elements = words input
    let result = listLength elements
    putStrLn ("The length of the list is: " ++ show result)
```

---

### ✅ How to Use:

1. Save the code to a file named `ListLength.hs`.
2. Run it with:

   ```bash
   runghc ListLength.hs
   ```

---

### 💡 Sample Run:

```
Enter a list of elements separated by spaces:
red green blue
The length of the list is: 3



