```haskell
-- SumList.hs
-- Compute the sum of elements in a list using foldr

-- Define the sumList function using foldr
sumList :: [Int] -> Int
sumList = foldr (+) 0

-- Main function to test sumList
main :: IO ()
main = do
    putStrLn "Enter a list of numbers separated by spaces:"
    input <- getLine
    let numbers = map read (words input) :: [Int]
    let result = sumList numbers
    putStrLn ("The sum of the list is: " ++ show result)
```

### How to run it:

1. Save this code in a file called `SumList.hs`.
2. Run it using:

   ```bash
   runghc SumList.hs
   ```

### Example Usage:

```
Enter a list of numbers separated by spaces:
1 2 3 4 5
The sum of the list is: 15



