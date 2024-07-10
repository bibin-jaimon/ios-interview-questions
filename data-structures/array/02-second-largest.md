## Find second largest element in the given array

```swift
let input = [20, 1, 3, 4, 7, 7, 5, 11]

struct Solution {
    /// Brute force Time N log N + N
    static func findSecondLargestBFS(_ arr: [Int]) -> Int {
        let temp = arr.sorted()
        let largest = temp.last!
        let secondLargest = Int.min
        for index in stride(from: temp.count - 2, through: 0, by: -1) {
            if temp[index] == largest {
                continue
            }
            return temp[index]
        }
        return secondLargest
    }

    /// Better Time comp = N + N
    static func findSecondLargestBS(_ arr: [Int]) -> Int { 
        var largest = Int.min

        for item in arr {
            if largest < item {
                largest = item
            }
        }

        var secondLargest = Int.min
        for item in arr {
            if secondLargest < item && item < largest {
                secondLargest = item
            }
        }
        return secondLargest
    }

    //Optimal O (N)
    static func findSecondLargestOS(_ arr: [Int]) -> Int { 
        var largest = arr[0]
        var secondLargest = Int.min

        for index in stride(from: 1, through: arr.count - 1, by: 1) {
            let item = arr[index]
            if largest < item {
                secondLargest = largest
                largest = item
            } else if secondLargest < item {
                secondLargest = item
            }            
        }
     
        return secondLargest
    }
}
print(Solution.findSecondLargestOS(input))

```
