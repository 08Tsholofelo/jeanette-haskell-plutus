* A `Shape` data type with constructors:

  * `Circle Double` (takes a radius)
  * `Rectangle Double Double` (takes width and height)
* Manual implementations of both the `Show` and `Read` type classes.

---

### ✅ Full Haskell Code

```haskell
-- ShapeShowRead.hs
-- Define Shape type and implement Show and Read manually

-- Define the Shape data type
data Shape = Circle Double | Rectangle Double Double

-- Implement Show instance
instance Show Shape where
    show (Circle r) = "Circle " ++ show r
    show (Rectangle w h) = "Rectangle " ++ show w ++ " " ++ show h

-- Implement Read instance
instance Read Shape where
    readsPrec _ input = 
        case words input of
            ("Circle":r:rest) ->
                [(Circle (read r), unwords rest)]
            ("Rectangle":w:h:rest) ->
                [(Rectangle (read w) (read h), unwords rest)]
            _ -> []

-- Main function to test Show and Read
main :: IO ()
main = do
    let s1 = Circle 5.0
    let s2 = Rectangle 4.0 6.0

    putStrLn "Original Shapes:"
    print s1
    print s2

    let s1Str = show s1
    let s2Str = show s2

    putStrLn "\nParsed back from strings:"
    print (read s1Str :: Shape)
    print (read s2Str :: Shape)
```

---

### 🧪 Example Output

```
Original Shapes:
Circle 5.0
Rectangle 4.0 6.0

Parsed back from strings:
Circle 5.0
Rectangle 4.0 6.0
```

---

### 🔎 Notes

* The `Show` instance converts the value to a string like `"Circle 5.0"` or `"Rectangle 4.0 6.0"`.
* The `Read` instance parses strings with exactly the same format.
* This works only when input strings match the pattern exactly. You can improve it later by handling parentheses, commas, etc., if needed.


