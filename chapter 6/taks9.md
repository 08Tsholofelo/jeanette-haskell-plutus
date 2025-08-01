```haskell
-- MyMap.hs
-- Custom implementation of the map function

-- Define the myMap function
myMap :: (a -> b) -> [a] -> [b]
myMap _ []     = []                   -- Base case: empty list
myMap f (x:xs) = f x : myMap f xs     -- Recursive case: apply f to x

-- Example function to apply (e.g., double a number)
double :: Int -> Int
double x = 2 * x

-- Main function to test myMap
main :: IO ()
main = do
    putStrLn "Enter a list of integers separated by spaces:"
    input <- getLine
    let numbers = map read (words input) :: [Int]
    let result = myMap double numbers
    putStrLn ("Doubled list: " ++ unwords (map show result))
```

---

### ✅ How to Run:

1. Save it as `MyMap.hs`.
2. Run it using:

   ```bash
   runghc MyMap.hs
   ```

---

### 💡 Example Output:

```
Enter a list of integers separated by spaces:
1 2 3 4 5
Doubled list: 2 4 6 8 10
```

---

This code demonstrates:

* A **custom recursive `map` implementation**.
* Applying a named function (`double`) to each list element.


