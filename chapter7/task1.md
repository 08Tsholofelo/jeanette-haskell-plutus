```haskell
-- ColorEq.hs
-- Define a Color type and implement Eq manually

-- Define the Color data type
data Color = Red | Green | Blue

-- Manually implement the Eq type class
instance Eq Color where
    Red   == Red   = True
    Green == Green = True
    Blue  == Blue  = True
    _     == _     = False

-- Optional: Show instance for display
instance Show Color where
    show Red   = "Red"
    show Green = "Green"
    show Blue  = "Blue"

-- Main function to test equality
main :: IO ()
main = do
    let c1 = Red
    let c2 = Green
    let c3 = Red
    putStrLn ("Is Red equal to Green? " ++ show (c1 == c2))
    putStrLn ("Is Red equal to Red? " ++ show (c1 == c3))
```

---

### 🔍 Example Output:

```
Is Red equal to Green? False
Is Red equal to Red? True
```

---


