```haskell
-- Define the circleArea function
circleArea :: Floating a => a -> a
circleArea radius = pi * radius ^ 2
```

### Explanation:

* The function is **pure**, meaning it depends **only on its input** and has **no side effects**.
* `Floating a => a -> a` means it works with any floating-point type (`Float`, `Double`, etc.).
* `pi` is a predefined constant in Haskell representing the mathematical π (pi).
* `radius ^ 2` squares the radius.

### Example usage:

You can test it in GHCi (Haskell interactive shell):

```haskell
> circleArea 3
28.274333882308138
```

### Full testable version:

```haskell
circleArea :: Floating a => a -> a
circleArea radius = pi * radius ^ 2

main :: IO ()
main = do
    let r = 3.0
    putStrLn $ "Area of circle with radius " ++ show r ++ " is " ++ show (circleArea r)


