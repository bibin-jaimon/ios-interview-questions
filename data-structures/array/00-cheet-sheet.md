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

for index in stride(from: arr.count - 2, through: 0, by: -1) {
    print(arr[index]
}

```
