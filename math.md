The Arduino Math library (math.h) includes a number of useful mathematical functions and constants. 

On my PC, I located the library (header file) in D:\\arduino-1.8.13\**hardware\\tools\\avr\\avr\\include -** the key part is in bold  

### Constants

 

/\*\* The constant \\a e.	*/
#define M_E		2.7182818284590452354

/\*\* The logarithm of the \\a e to base 2. */
#define M\_LOG2E		1.4426950408889634074	/* log\_2 e */

/\*\* The logarithm of the \\a e to base 10. */
#define M\_LOG10E	0.43429448190325182765	/* log\_10 e */

/\*\* The natural logarithm of the 2.	*/
#define M\_LN2		0.69314718055994530942	/* log\_e 2 */

/\*\* The natural logarithm of the 10.	*/
#define M\_LN10		2.30258509299404568402	/* log\_e 10 */

/\*\* The constant \\a pi.	*/
#define M_PI		3.14159265358979323846	/* pi */

/\*\* The constant \\a pi/2.	*/
#define M\_PI\_2		1.57079632679489661923	/* pi/2 */

/\*\* The constant \\a pi/4.	*/
#define M\_PI\_4		0.78539816339744830962	/* pi/4 */

/\*\* The constant \\a 1/pi.	*/
#define M\_1\_PI		0.31830988618379067154	/* 1/pi */

/\*\* The constant \\a 2/pi.	*/
#define M\_2\_PI		0.63661977236758134308	/* 2/pi */

/\*\* The constant \\a 2/sqrt(pi).	*/
#define M\_2\_SQRTPI	1.12837916709551257390	/* 2/sqrt(pi) */

/\*\* The square root of 2.	*/
#define M_SQRT2		1.41421356237309504880	/* sqrt(2) */

/\*\* The constant \\a 1/sqrt(2).	*/
#define M\_SQRT1\_2	0.70710678118654752440	/* 1/sqrt(2) */

Here are just a couple of the functions as you will find them defined in the library  

/**
    The cos() function returns the cosine of \\a __x, measured in radians.
 */
extern double cos(double \_\_x) \_\_ATTR\_CONST\_\_;
#define cosf	cos		/**< The alias for cos().	*/

/**
    The sin() function returns the sine of \\a __x, measured in radians.
 */
extern double sin(double \_\_x) \_\_ATTR\_CONST\_\_;
#define sinf	sin		/**< The alias for sin().	*/

/**
    The tan() function returns the tangent of \\a __x, measured in radians.
 */
extern double tan(double \_\_x) \_\_ATTR\_CONST\_\_;
#define tanf	tan		/**< The alias for tan().	*/

### Function List

Here is a list of the functions, again it is better to look at the comments beside these functions in the header file or simply look them up in your favorite search engine  

<pre>
double cos(double __x)
double sin(double __x)
double tan(double __x)
double fabs(double __x)
double fmod(double \_\_x, double \_\_y)
double modf(double \_\_x, double *\_\_iptr);
float modff (float \_\_x, float *\_\_iptr);
double sqrt(double __x)
float sqrtf (float)
double cbrt(double __x)
double hypot (double \_\_x, double \_\_y)
double square(double __x)
double floor(double __x)
double ceil(double __x)
double frexp(double \_\_x, int *\_\_pexp);
double ldexp(double \_\_x, int \_\_exp)
double exp(double __x)
double cosh(double __x)
double sinh(double __x)
double tanh(double __x)
double acos(double __x)
double asin(double __x)
double atan(double __x)
double atan2(double \_\_y, double \_\_x)
double log(double __x)
double log10(double __x)
double pow(double \_\_x, double \_\_y)
int isnan(double __x)
int isinf(double __x)
int signbit (double __x)
double fdim (double \_\_x, double \_\_y)
double fma (double \_\_x, double \_\_y, double __z)
double fmax (double \_\_x, double \_\_y)
double fmin (double \_\_x, double \_\_y)
double round (double __x)
long lround (double __x)
long lrint (double __x)
</pre>
 

### Code Example

Here are some of the more commonly used functions  

<pre>
double doubleX = 90.00 ;


void setup() 
{
   Serial.begin(9600);
   Serial.print("cosine of num = ");
   Serial.println (cos (doubleX) ); // returns cosine of x
   Serial.print("absolute value of num = ");
   Serial.println (fabs (doubleX) ); // absolute value
   Serial.print("sine of num = ");
   Serial.println (sin (doubleX) ) ;// returns sine of x
   Serial.print("square root of num : ");
   Serial.println ( sqrt (doubleX) );// returns square root of x
   Serial.print("tangent of num : ");
   Serial.println ( tan (doubleX) ); // returns tangent of x
}

void loop() 
{

}
</pre>

You will see this in the serial monitor window

<pre>
cosine of num = -0.45
absolute value of num = 90.00
sine of num = 0.89
square root of num : 9.49
tangent of num : -2.00
</pre>
