```haskell
-- ReverseList.hs
-- Recursive function to reverse a list

-- Define the reverseList function using recursion
reverseList :: [a] -> [a]
reverseList []     = []                     -- Base case: empty list
reverseList (x:xs) = reverseList xs ++ [x]  -- Recursive case

-- Main function to test reverseList
main :: IO ()
main = do
    putStrLn "Enter a list of elements separated by spaces:"
    input <- getLine
    let elements = words input
    let result = reverseList elements
    putStrLn ("Reversed list: " ++ unwords result)
```

### How to run it:

1. Save it as `ReverseList.hs`.
2. Run using:

   ```bash
   runghc ReverseList.hs
   ```

### Example Input & Output:

```
Enter a list of elements separated by spaces:
a b c d e
Reversed list: e d c b a

