# Concurrency
## Goroutines
## Channels
## WaitGroup
## Deferring functions
# Structs 
## Methods
# Interfaces
```
type Shape interface {
  Area() float64
  Perimeter() float64
}
```
## Struct & Methods
- Struct Rectangle implicitly implements interface Shape by implementing all of its methods.
```
type Rectangle struct {
  Length, Width float64
}

func (r Rectangle) Area() float64 {
  return r.Length * r.Width
}

func (r Rectangle) Perimeter() float64 {
  return 2 * (r.Length + r.Width)
}

func main() {
  var r Shape = Rectangle{Length: 3, Width: 4}
  fmt.Printf("Type of r: %T, Area: %v, Perimeter: %v.", r, r.Area(), r.Perimeter())
}
```
