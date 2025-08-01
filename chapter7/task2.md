Here's the complete and correct Haskell code defining a `Color` data type with `Red`, `Green`, and `Blue` as constructors, and a manual implementation of the `Eq` type class:

```haskell
-- Define the Color data type
data Color = Red | Green | Blue

-- Manually implement the Eq type class for Color
instance Eq Color where
  Red   == Red   = True
  Green == Green = True
  Blue  == Blue  = True
  _     == _     = False

-- Example usage
main :: IO ()
main = do
  print (Red == Red)     -- True
  print (Red == Blue)    -- False
  print (Green == Green) -- True
```

### How to Run This Code

1. Save it in a file, e.g., `ColorEq.hs`.
2. Run it with:

   ```bash
   runhaskell ColorEq.hs
   ```

Let me know if you want this added to your GitHub repo or university readme as an example.
