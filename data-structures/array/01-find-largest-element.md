# 01 Find largest element in the array

> BRUTE FORCE

Required Sort - N logN

Two sort methods in Swift

- `.sort()` Inplace sort

- `.sorted()` Return sorted collection

```swift
var input = [1, 2, 5, 4, 3]

struct Solution {
    static func findLargestNumber(_ arr: inout [Int]) -> Int {
        arr.sort()
        return arr.last!
    }

    static func findLargestNumberV1(_ arr: inout [Int]) -> Int {
        arr.sorted().last!
    }
}
```

> OPTIMAL

```swift
var input = [1, 2, 5, 4, 3]

struct Solution {
    static func findLargestNumber(_ arr: [Int]) -> Int {
        var largestElement = arr.first!

        arr.forEach {
            if largestElement < $0 {
                largestElement = $0
            }
        }

        return largestElement
    }
}
```
Time Complexity - O(N)
