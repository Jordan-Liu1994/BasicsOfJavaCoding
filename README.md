# BasicsOfJavaCoding
All the basics of JAVA coding by Simplilearn

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

**## J001_PrintInConsole**
package java_Basics;

public class J001_PrintInConsole {
	  
	public static void main(String[] args) {
		
		System.out.println("-----Hi QC-----");
		System.out.println("-----Hello World!-----");
		System.out.println("-----Hello Simplilearn!-----");
		System.out.println("-----Hello QA/QC Team!-----");
	}
}

Results :  
-----Hi QC-----  
-----Hello World!-----  
-----Hello Simplilearn!-----  
-----Hello QA/QC Team!-----  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J002_LoopDoWhile
package java_Basics;

public class J002_LoopDoWhile {

	public static void main(String[] args) {

		int a = 1;
		while (a < 5) {
			System.out.println(a + " is not more than 5");
			a = a + 1;
		}
	}
}

Results :  
1 is not more than 5  
2 is not more than 5  
3 is not more than 5  
4 is not more than 5  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J003_LoopFor
package java_Basics;

public class J003_LoopFor {

	public static void main(String[] args) {

		int a = 1;
		do {
			System.out.println(a + " is not more than 5");
			a++;
		} while (a < 5);
		System.out.println("Do While Loop has finished & stopped");
	}
}

Results :  
1 is not more than 5  
2 is not more than 5  
3 is not more than 5  
4 is not more than 5  
Do While Loop has finished & stopped  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J004_LoopWhile
package java_Basics;

public class J004_LoopWhile {

	public static void main(String[] args) {

		int a = 1;
		while (a < 5) {
			System.out.println(a + " is not more than 5");
			a = a + 1;
		}
	}
}

Results :  
1 is not more than 5  
2 is not more than 5  
3 is not more than 5  
4 is not more than 5  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J005_Typecasting
package java_Basics;

public class J005_Typecasting {

	public static void main(String[] args) {

		int a = 10;
		System.out.println("1. " + "Value a = " + a);

		double b;
		b = 10.5;
		System.out.println("2. " + "Value b = " + b);

		int c;
		c = (int) b;
		System.out.println("3. " + "Value c = " + c);

		int d = 50;
		short e = 2;
		long f;

		f = d;
		System.out.println("4. " + "Value f = " + f);
		f = e;
		System.out.println("5. " + "Value f = " + f);

		d = (int) f;
		System.out.println("6. " + "Value d = " + d);
		e = (short) f;
		System.out.println("7. " + "Value e = " + e);

		char g = 'a';
		System.out.println("8. " + "Character g = " + g);

		int myInt = c;
		System.out.println("9. " + "Value myInt = " + myInt);

		float myFloat = c;
		System.out.println("9. " + "Value myFloat = " + myFloat);

		int myInta = 100;
		String strCasting = Integer.toString(myInta);
		String strCasting2 = String.valueOf(myInta);
		System.out.println("10. " + "Value strCasting = " + strCasting);
		System.out.println("11. " + "Value strCasting = " + strCasting2);
	}
}

Results :  
1. Value a = 10  
2. Value b = 10.5  
3. Value c = 10  
4. Value f = 50  
5. Value f = 2  
6. Value d = 2  
7. Value e = 2  
8. Character g = a  
9. Value myInt = 10  
9. Value myFloat = 10.0  
10. Value strCasting = 100  
11. Value strCasting = 100  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J006_AccessModifier
package java_Basics;

public class J006_AccessModifier {

	//	other package & class can access these variables
	public int a = 100;
	public int b = 200;

	//	only accessible to current class
	private int c = 150;
	private int d = 250;

	//	only accessible to current package
	protected int e = 200;
	protected int f = 300;
}

## J007_AccessModifier_Access
package java_Basics;

public class J007_AccessModifier_Access {

	public static void main(String[] args) {

		Java_Modifiers modAccess = new Java_Modifiers();
		System.out.println("Value = " + modAccess.a);

		int c = modAccess.a * modAccess.b;
		System.out.println("Public value = " + c);

		System.out.println("Private can only be use in it's own class file");

		int g = modAccess.e * modAccess.f;
		System.out.println("Protected value = " + g);
	}
}

Results :  
Value = 100  
Public value = 20000  
Private can only be use in it's own class file  
Protected value = 60000  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J008_AccessModifier_InDifferentPackage
package java_Basics_2;

import java_Basics.J006_AccessModifier;

public class J008_AccessModifier_InDifferentPackage {

	public static void main(String[] args) {

		System.out.println("Hello");
		System.out.println("你好");
		System.out.println("สวัสดี");
		System.out.println("halo");
		System.out.println("xin chào");
		System.out.println("नमस्ते");
		
		J006_AccessModifier modAccess = new J006_AccessModifier();
		int g = modAccess.a + modAccess.b;
		System.out.println("Value = " + g);
		System.out.println("Private can only use in it's own class file");
		System.out.println("Protected can only use in it's own package file");
	}
}

Results :  
Hello  
你好  
สวัสดี  
halo  
xin chào  
नमस्ते  
Value = 300  
Private can only use in it's own class file  
Protected can only use in it's own package file  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J009_InheritParent
package java_Basics;

public class J009_InheritParent {

	static int a = 25;
	static int b = 50;
	static String string = "Hello World!";

	public static void printMyName() {
		System.out.println(string);
	}
}

## J010_InheritChild
package java_Basics;

public class J010_InheritChild extends J009_InheritParent {

	public static void main(String[] args) {
		System.out.println("Value = " + (a * b));
		printMyName();
	}
	
	public static int additionMethod() {
		return (a * b) + a;
	}
}

Results :  
Value = 1250  
Hello World!  

## J011_InheritGrandChild
package java_Basics;

public class J011_InheritGrandChild extends J010_InheritChild {

	public static void main(String[] args) {
		System.out.println(additionMethod());
		System.out.println(a - b);
	}
}

Results :  
1275  
-25  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J012_ExceptionHandling
package java_Basics;

public class J012_ExceptionHandling {

	public static void main(String[] args) {

		int a = 1;
		int b[] = { 1, 2, 3, 4, 5 };

		System.out.println("Statement " + a++);
		System.out.println("Statement " + a++);
		System.out.println("Statement " + a++);
		System.out.println("Statement " + a++);
		
		try {
			System.out.println("--------------------------------------------------");
			System.out.println(b[5]);			
		} catch (ArrayIndexOutOfBoundsException e) {
			System.out.println("There is an error with ARRAY INDEX!");
			e.printStackTrace();			
		} catch (ArithmeticException e) {
			e.printStackTrace();
		} finally {
			System.out.println("Continue the process!");
			System.out.println("--------------------------------------------------");
		}
		
		System.out.println("Statement " + a++);
		System.out.println("Statement " + a++);
		System.out.println("Statement " + a++);
	}
}

Results :  
Statement 2  
Statement 3  
Statement 4    
There is an error with ARRAY INDEX!  
java.lang.ArrayIndexOutOfBoundsException: Index 5 out of bounds for length 5 at a_Java_001.Java_Exception_Handling.main(Java_Exception_Handling.java:18)  
Continue the process!    
Statement 5  
Statement 6  
Statement 7  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J013_ForcedException
package java_Basics;

public class J013_ForcedException {

	public static void main(String[] args) throws InterruptedException {

		System.out.println("Statement 1");
		
		try {
			Thread.sleep(1500);
		} catch (InterruptedException e) {
			e.printStackTrace();
		}
		System.out.println("Statement 2");
		
		Thread.sleep(1500);
		System.out.println("Statement 3");
	}
}

Results :  
Statement 1  
Statement 2  
Statement 3  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J014_Constructor
package java_Basics;

public class J014_Constructor {

	public Java_Constructor() {
			System.out.println("Constructor executed!");
		}

	public Java_Constructor(int a, int b) {
			System.out.println(a * b);
		}
}

## J015_Constructor_Access
package java_Basics;

public class J015_Constructor_Access {

	public static void main(String[] args) {

		J014_Constructor constructorMethod = new J014_Constructor();
		J014_Constructor constructorMethod2 = new J014_Constructor(10, 15);
	}
}

Results :  
Constructor executed!  
150  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J016_Collection
package java_Basics;

public class J016_Collection {

	public static void main(String[] args) {
		List<Integer> intList = new ArrayList<Integer>();
		intList.add(500);
		intList.add(40);
		intList.add(75);
		intList.add(2);
		intList.add(230);
		intList.add(13);
		System.out.println(intList);

		Collections.sort(intList);
		System.out.println(intList);

		Collections.reverse(intList);
		System.out.println(intList);
		System.out.println(intList.get(2));

		List<String> strList = new ArrayList<String>();
		strList.add("Hello");
		strList.add("Jordan");
		strList.add("Fire");
		strList.add("Many");
		strList.add("Big");
		strList.add("Hey");

		System.out.println(strList);

		Collections.sort(strList);
		System.out.println(strList);

		Collections.reverse(strList);
		System.out.println(strList);
		System.out.println(strList.get(2));

		Map<String, String> myMap = new HashMap<>();
		myMap.put("Name", "Jordan");
		myMap.put("Name2", "Jord");
		myMap.put("Name3", "Jor");
		myMap.put("Name4", "Dan");
		myMap.put("Name5", "Ord");

		System.out.println(myMap);
		System.out.println(myMap.get("Name"));
		
		Map<String, String> myM1 = mapMethod();
		System.out.println(myM1.get("Name5"));
	}

	public static Map<String, String> mapMethod() {
		Map<String, String> myM = new HashMap<>();
		myM.put("Name", "Jordan");
		myM.put("Name2", "Jord");
		myM.put("Name3", "Jor");
		myM.put("Name4", "Dan");
		myM.put("Name5", "Ord");
		return myM;
	}
}

Results :  
[500, 40, 75, 2, 230, 13]  
[2, 13, 40, 75, 230, 500]  
[500, 230, 75, 40, 13, 2]  
75  
[Hello, Jordan, Fire, Many, Big, Hey]  
[Big, Fire, Hello, Hey, Jordan, Many]  
[Many, Jordan, Hey, Hello, Fire, Big]  
Hey  
{Name3=Jor, Name4=Dan, Name5=Ord, Name=Jordan, Name2=Jord}  
Jordan  
Ord  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
