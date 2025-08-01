1. Defines the `Color` data type (`Red`, `Green`, `Blue`).
2. Implements the `Eq` and `Ord` type classes manually, ensuring the ordering:
   **`Red < Green < Blue`**.

---

### ✅ Full Haskell Code

```haskell
-- ColorOrd.hs
-- Define Color type and implement Eq and Ord manually

-- Define the Color data type
data Color = Red | Green | Blue

-- Implement Eq manually
instance Eq Color where
    Red   == Red   = True
    Green == Green = True
    Blue  == Blue  = True
    _     == _     = False

-- Implement Ord manually: Red < Green < Blue
instance Ord Color where
    compare Red Green  = LT
    compare Red Blue   = LT
    compare Green Blue = LT
    compare Green Red  = GT
    compare Blue Red   = GT
    compare Blue Green = GT
    compare _ _        = EQ

-- Optional: Show instance for pretty printing
instance Show Color where
    show Red   = "Red"
    show Green = "Green"
    show Blue  = "Blue"

-- Main function to test ordering
main :: IO ()
main = do
    let c1 = Red
    let c2 = Green
    let c3 = Blue
    print (c1 < c2)     -- True
    print (c2 < c3)     -- True
    print (c3 > c1)     -- True
    print (c2 > c1)     -- True
    print (c2 == Green) -- True
```

---

### 🧪 Example Output:

```
True
True
True
True
True
```

---

### 🔁 Alternative (Simpler) Version Using `deriving`:

If you define the colors in the right order, you can **auto-derive** `Eq` and `Ord` like this:

```haskell
data Color = Red | Green | Blue deriving (Eq, Ord, Show)
```

This will automatically assign the order `Red < Green < Blue` based on declaration order.


