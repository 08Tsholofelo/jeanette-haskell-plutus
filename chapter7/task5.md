* Calculates the **area of a square** given its **side length**
* Works with **any numeric type** (`Num a => a -> a`)

---

### ✅ Full Haskell Code

```haskell
-- SquareArea.hs
-- Function to calculate the area of a square

-- Define squareArea with a polymorphic numeric type
squareArea :: Num a => a -> a
squareArea side = side * side

-- Main function to test squareArea
main :: IO ()
main = do
    putStrLn "Enter the side length of the square:"
    input <- getLine
    let side = read input :: Double
    let area = squareArea side
    putStrLn ("The area of the square is: " ++ show area)
```

---

### 🧪 Example Usage

```
Enter the side length of the square:
4.5
The area of the square is: 20.25
```

---

### 🔎 Notes

* The function `squareArea` is **polymorphic**, meaning it works with `Int`, `Float`, `Double`, etc.
* In the `main` function, we explicitly use `Double` for flexibility with decimal input.
* You can change `Double` to `Int` if you want only whole-number input/output.


