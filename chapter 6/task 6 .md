```haskell
-- ElementExists.hs
-- Recursive function to check if an element exists in a list

-- Define the elementExists function
elementExists :: Eq a => a -> [a] -> Bool
elementExists _ [] = False                           -- Base case: empty list
elementExists x (y:ys)
    | x == y    = True                               -- Found the element
    | otherwise = elementExists x ys                 -- Recursive search

-- Main function to test elementExists
main :: IO ()
main = do
    putStrLn "Enter a list of elements separated by spaces:"
    inputList <- getLine
    putStrLn "Enter the element to search for:"
    element <- getLine
    let list = words inputList
    let found = elementExists element list
    if found
        then putStrLn (element ++ " exists in the list.")
        else putStrLn (element ++ " does not exist in the list.")
```

---

### 🧪 How to Run:

1. Save it as `ElementExists.hs`.
2. Run it using:

   ```bash
   runghc ElementExists.hs
   ```

---

### 💡 Example Input/Output:

```
Enter a list of elements separated by spaces:
apple banana cherry
Enter the element to search for:
banana
banana exists in the list.



