* Takes **two values** of the same type `a`
* Returns the **larger one**
* Ensures that `a` is an instance of both `Eq` and `Ord`

---

### ✅ Full Haskell Code

```haskell
-- CompareValues.hs
-- Function to return the larger of two values using Eq and Ord

-- Define compareValues with appropriate type constraints
compareValues :: (Eq a, Ord a) => a -> a -> a
compareValues x y
    | x >= y    = x
    | otherwise = y

-- Main function to test compareValues
main :: IO ()
main = do
    putStrLn "Comparing numbers:"
    print (compareValues 10 20)  -- Output: 20
    print (compareValues 42 17)  -- Output: 42

    putStrLn "\nComparing characters:"
    print (compareValues 'a' 'z')  -- Output: 'z'
    print (compareValues 'm' 'c')  -- Output: 'm'

    putStrLn "\nComparing strings:"
    print (compareValues "apple" "banana") -- Output: "banana"
    print (compareValues "hello" "hi")     -- Output: "hi"
```

---

### 🧪 Example Output:

```
Comparing numbers:
20
42

Comparing characters:
'z'
'm'

Comparing strings:
"banana"
"hi"
```

---

This function works with **any type that implements both `Eq` and `Ord`**, including `Int`, `Char`, `String`, and custom types (if you implement those instances).


