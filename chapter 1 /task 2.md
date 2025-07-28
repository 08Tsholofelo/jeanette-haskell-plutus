```haskell
-- Define the circleArea function
circleArea :: Floating a => a -> a
circleArea radius = pi * radius ^ 2

-- Main function to test circleArea
main :: IO ()
main = do
    let radius = 5.0
    let area = circleArea radius
    putStrLn $ "The area of a circle with radius " ++ show radius ++ " is " ++ show area
```

### Explanation:

* `circleArea` is a **pure function**: it uses only its input and does not interact with any external state.
* `pi` is a predefined constant in Haskell.
* `Floating a => a -> a` allows the function to work with both `Float` and `Double`.

### To run this code:

1. Save it as `Main.hs`
2. Run it using:

   ```bash
   runghc Main.hs
   ```

   or compile it:

   ```bash
   ghc Main.hs -o main && ./main
   ```

### Output:

```
The area of a circle with radius 5.0 is 78.53981633974483
```
