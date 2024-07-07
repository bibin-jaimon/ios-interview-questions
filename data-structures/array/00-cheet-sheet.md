# Cheet Sheet

## Loop

```swift 
var arr = [1, 2, 5, 4, 3]

arr.forEach {
    print($0)
}

for item: Int in arr {
    print(item)
}

for item: (offset: Int, element: Int) in arr.enumerated() {
    print(item)
}

for index in 0..<arr.count {
    print(arr[index])
}

```
