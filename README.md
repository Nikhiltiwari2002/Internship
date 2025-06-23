public class Calculator {

    public int add(int a, int b) {
        return a + b;
    }

    
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    
    public double add(double a, double b) {
        return a + b;
    }

    
    public double add(int a, double b) {
        return a + b;
    }
}


In Java, == and .equals() are both used for comparison, but they serve different purposes:
1. == Operator:
Primitive Types:
When used with primitive data types (like int, char, boolean, double, etc.), == compares their actual values. If the values are identical, it returns true; otherwise, it returns false.
Object Types:
When used with object types, == compares the references of the objects. It checks if both references point to the exact same object in memory. If they point to the same memory location, it returns true; otherwise, it returns false, even if the objects have identical content.
2. .equals() Method:
Object Types: The .equals() method is a method defined in the Object class and can be overridden by subclasses. Its primary purpose is to compare the content or state of two objects for logical equality.
Default Behavior: In the Object class, the default implementation of .equals() is similar to == for objects; it compares references.
Overriding: For most classes (like String, Integer, Date, etc.), the .equals() method is overridden to provide a meaningful comparison of their content. For example, String.equals() compares the character sequences of two strings.
Cannot be used with Primitives: The .equals() method cannot be used directly with primitive types. 
Summary of Key Differences:
Feature
== Operator
.equals() Method
Purpose
Compares values (primitives) or references (objects)
Compares content/state of objects
Applicability
Primitives and Objects
Objects only
Overriding
Cannot be overridden
Can be overridden to define custom equality logic
Default for Objects
Compares references
Compares references (in Object class), but often overridden
