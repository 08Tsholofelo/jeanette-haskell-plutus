

* Takes a **radius** as input
* Returns the **circumference** of the circle
* Works with both `Integral` and `Floating` types (e.g., `Int`, `Integer`, `Float`, `Double`)

---

### ✅ Full Haskell Code

```haskell
-- CircleCircumference.hs
-- Function to calculate the circumference of a circle

-- Use realToFrac to convert Integral to Floating
circleCircumference :: (Real a, Floating b) => a -> b
circleCircumference r = 2 * pi * realToFrac r

-- Main function to test circleCircumference
main :: IO ()
main = do
    putStrLn "Enter the radius of the circle:"
    input <- getLine
    let radius = read input :: Double  -- You can change this to Int or Integer
    let result = circleCircumference radius
    putStrLn ("The circumference is: " ++ show result)
```

---

### 🔍 Type Explanation

```haskell
circleCircumference :: (Real a, Floating b) => a -> b
```

* Accepts any `Real` number (e.g. `Int`, `Integer`, `Float`, `Double`)
* Returns a `Floating` result (e.g. `Float`, `Double`)
* Converts using `realToFrac` to handle both `Integral` and `Floating` seamlessly

---

### 🧪 Example Output

```
Enter the radius of the circle:
7
The circumference is: 43.982297150257104
