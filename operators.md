An operator is a symbol that tells the compiler to perform specific mathematical or logical functions. The C language has many built-in operators, these can be categorized as follows  

### Arithmetic Operators

|     |     |     |
| --- | --- | --- |
| Operator name | Operator Symbol | Description |
| assignment operator | =   | Stores the value to the right of the equal sign in the variable to the left of the equal sign. |
| Subtraction | -   | Subtracts second operand from the first operand |
| Addition | +   | Adds two operands |
| Division | /   | Divide numerator by denominator |
| Multiplier | *   | Multiply both operands |
| Modulo | %   | Modulus Operator and the remainder of after an integer division |

 

#### Code Example

Type the following into the Arduino IDE, any Arduino will do  
<pre>
int x = 2;
int y = 10;

void setup()
{
  // initialize serial communications at 9600:
  Serial.begin(9600);
  Serial.println("Arithmetic Operators");
  Serial.println("x = 2, y = 10");
  Serial.print("x + y = ");
  Serial.println(x + y);
  Serial.print("y - x = ");
  Serial.println(y - x);
  Serial.print("y / x = ");
  Serial.println(y / x);
  Serial.print("y * x = ");
  Serial.println(y * x);
  Serial.print("y % x = ");
  Serial.println(y % x);
}

void loop() {
  // put your main code here, to run repeatedly:

}
</pre>
Now compile and run this and open up the Serial Monitor and you will see something like this

Arithmetic Operators
x = 2, y = 10
x + y = 12
y - x = 8
y / x = 5
y * x = 20
y % x = 0

### **Comparison Operators**

You should note that you may compare variables of different data types, but that can generate unpredictable results, it is recommended to compare variables of the same data type including signed and unsigned types

|     |     |     |
| --- | --- | --- |
| **Operator name** | **Operator Symbol** | **Description** |
| equal to | ==  | Checks if the value of two operands is equal or not, if yes then the condition becomes true. |
| greater than or equal to | >=  | Checks if the value of the left operand is greater than or equal to the value of the right operand, if yes then the condition becomes true. |
| greater than | >   | Checks if the value of the left operand is greater than the value of the right operand, if yes then the condition becomes true. |
| less than or equal to | <=  | Checks if the value of the left operand is less than or equal to the value of the right operand, if yes then the condition becomes true. |
| less than | <   | Checks if the value of the left operand is less than the value of the right operand, if yes then the condition becomes true. |
| not equal to | !=  | Checks if the value of two operands is equal or not, if values are not equal then the condition becomes true. |

 

### Compound Operators

|     |     |     |
| --- | --- | --- |
| **Operator name** | **Operator Symbol** | **Description** |
| increment | ++  | The increment operator, increases integer value by one |
| decrement | --  | Decrement operator decreases integer value by one |
| compound addition | +=  | Add AND assignment operator. It adds the right operand to the left operand and assigns the result to left operand |
| compound subtraction | -=  | Subtract AND assignment operator. It subtracts the right operand from the left operand and assigns the result to left operand |
| compound multiplication | *=  | Multiply AND assignment operator. It multiplies the right operand with the left operand and assigns the result to the left operand |
| compound division | /=  | Divide AND assignment operator. It divides the left operand with the right operand and assigns the result to the left operand |
| compound modulo | %=  | Modulus AND assignment operator. It takes modulus using two operands and assigns the result to the left operand |
| compound bitwise or | \|= | bitwise inclusive OR and assignment operator |
| compound bitwise and | &=  | Bitwise AND assignment operator |

### Bitwise Operators

|     |     |     |
| --- | --- | --- |
| **Operator Name** | **Operator Symbol** | **Description** |
| and | &   | Binary AND Operator copies a bit to the result if it exists in both operands. |
| or  | \|  | Binary OR Operator copies a bit if it exists in either operand |
| xor | ^   | Binary XOR Operator copies the bit if it is set in one operand but not both. |
| not | ~   | Binary One's Complement Operator is unary and has the effect of 'flipping' bits. |
| shift left | <<  | Binary Left Shift Operator. The left operand's value is moved left by the number of bits specified by the right operand. |
| shift right | >>  | Binary Right Shift Operator. The left operand's value is moved right by the number of bits specified by the right operand. |

### Boolean Operators

|     |     |     |
| --- | --- | --- |
| **Operator Name** | **Operator Symbol** | **Description** |
| and | &&  | Called Logical AND operator. If both the operands are non-zero then condition becomes true. |
| or  | \|  | Called Logical OR Operator. If any of the two operands are non-zero then condition becomes true. |
| not | !   | Called Logical NOT Operator. Use to reverses the logical state of its operand. If a condition is true then the Logical NOT operator will make false. |
