# Basic-Calculator
Basic Calculator on Swift
Created a basic calculator functionality using swift concepts.

func Addition(first : Double , second : Double) -> Double{
    return first + second
}
func Subtraction(first : Double , second : Double) -> Double{
    return first - second
}
func Multiplication(first : Double , second : Double) -> Double{
    return first * second
}
func Division(first: Double, second: Double) -> Double {
    if second != 0 {
        return first / second
    } else {
        print("Error: cannot divide by 0")
        return 0.0
    }
}
func Main()
{
    print("Please Choose ")
    print(" press 1 for Addition ")
    print(" press 2 for Subtraction ")
    print(" press 3 for Multiplication ") 
    print(" press 4 for Division ")
    
    if let choice = readLine(), let Operations = Int(choice)
    {
    print("Enter First Number")
    if let input1 = readLine(), let first = Double(input1)
    {
    print("Enter Second Number")
    if let input2 = readLine(), let second = Double(input2)
    {
    var result : Double = 0.0
    switch Operations {
        case 1:
         result = Addition(first: first, second: second)
        case 2:
         result = Subtraction(first: first, second: second)
        case 3:
         result = Multiplication(first: first, second: second)
        case 4:
         result = Division(first: first, second: second)
        default:
            print("invalid operation")
            return
        }
    print("result: \(result)")
    }
    else{
            print("Invalid Second Number")
        }
    }else{
            print("Invalid First Number")
        }
    }else{
            print("Invalid Option")
        }
}
Main()
