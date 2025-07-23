-- Define the double function
double :: Int -> Int
double x = x * 2

-- Define the increment function
increment :: Int -> Int
increment x = x + 1

-- Compose functions: double first, then increment
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Main function to test it
main :: IO ()
main = do
    let input = 5
    let result = doubleThenIncrement input
    putStrLn ("Input: " ++ show input)
    putStrLn ("Result of doubleThenIncrement: " ++ show result)

