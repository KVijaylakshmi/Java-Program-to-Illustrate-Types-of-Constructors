# Java-Program-to-Illustrate-Types-of-Constructors
// Class to demonstrate constructors
class ConstructorDemo {
    int x, y;

    // Default constructor
    public ConstructorDemo() {
        x = 0;
        y = 0;
        System.out.println("Default Constructor called: x = " + x + ", y = " + y);
    }

    // Parameterized constructor
    public ConstructorDemo(int a, int b) {
        x = a;
        y = b;
        System.out.println("Parameterized Constructor called: x = " + x + ", y = " + y);
    }

    // Copy constructor (Java doesn't provide one by default, so we define our own)
    public ConstructorDemo(ConstructorDemo obj) {
        this.x = obj.x;
        this.y = obj.y;
        System.out.println("Copy Constructor called: x = " + x + ", y = " + y);
    }

    // Method to display values
    public void display() {
        System.out.println("Values: x = " + x + ", y = " + y);
    }
}

public class ConstructorTest {
    public static void main(String[] args) {
        // Using default constructor
        ConstructorDemo obj1 = new ConstructorDemo();
        obj1.display();

        // Using parameterized constructor
        ConstructorDemo obj2 = new ConstructorDemo(10, 20);
        obj2.display();

        // Using copy constructor
        ConstructorDemo obj3 = new ConstructorDemo(obj2);
        obj3.display();
    }
}
