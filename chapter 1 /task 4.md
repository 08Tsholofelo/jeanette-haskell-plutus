
 




```haskell
-- Extracts player names from a list of (name, score) tuples
extractPlayers :: [(String, Int)] -> [String]
extractPlayers = map fst

-- Sorts players by score in descending order
sortByScore :: [(String, Int)] -> [(String, Int)]
sortByScore = reverse . sortBy (\(_, s1) (_, s2) -> compare s1 s2)

-- Returns the top three players (tuples)
topThree :: [(String, Int)] -> [(String, Int)]
topThree = take 3

-- Compose the functions to get top three player names
getTopThreePlayers :: [(String, Int)] -> [String]
getTopThreePlayers = extractPlayers . topThree . sortByScore

-- Example usage
main :: IO ()
main = do
  let players = [("Alice", 85), ("Bob", 92), ("Charlie", 78), ("Diana", 95), ("Eve", 88)]
  let topPlayers = getTopThreePlayers players
  putStrLn "Top 3 Players:"
  mapM_ putStrLn topPlayers
```

### How it works:

* `extractPlayers` pulls out just the names.
* `sortByScore` orders the list from highest to lowest score.
* `topThree` grabs the first 3 elements.
* `getTopThreePlayers` composes all three into a pipeline.

### Output when you run the program:

```
Top 3 Players:
Diana
Bob
Eve
```


