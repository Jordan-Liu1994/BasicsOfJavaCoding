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

## J017_CollectionArray
package java_Basics;

public class J017_CollectionArray {

	public static void main(String[] args) {
		int a[] = { 1, 3, 5, 8, 10, 13, 16, 20 };
		System.out.println(a[3]);

		a[3] = 70;
		System.out.println(a[3]);

		System.out.println(a.length);

		String strArray[] = { "Jordan", "Kian", "Ancore", "Wong", "Terence", "Vincent", "Wanhui", "John", "Jimmy", "YK" };
		System.out.println(strArray[5]);

		for (int b = 0; b < strArray.length; b++) {
			System.out.println(strArray[b]);
		}

		int twoD[][] = { { 1, 2, 3 }, { 5, 10, 20 }, { 15, 25, 35 } };
		
		System.out.println(twoD[2][1]);

		for (int index = 0; index < twoD.length; index++) {
			for (int index2 = 0; index2 < twoD[index].length; index2++) {
				System.out.println(twoD[index][index2]);
			}
		}
	}
}

Results :  
8  

70  

8  

Vincent  

Jordan  
Kian  
Ancore  
Wong  
Terence  
Vincent  
Wanhui  
John  
Jimmy  
YK  

25  

1  
2  
3  

5  
10  
20  

15  
25  
35  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J018_CollectionForLoopExtended
package java_Basics;

public class J018_CollectionForLoopExtended {

	public static void main(String[] args) {

		List<String> strList = new ArrayList<String>();
		strList.add("Hello");
		strList.add("Jordan");
		strList.add("Fire");
		strList.add("Many");
		strList.add("Big");
		strList.add("Hey");
		
		System.out.println(strList);
				
		for (String strData : strList) {
			System.out.println(strData);
		}
	}
}

Results :  
[Hello, Jordan, Fire, Many, Big, Hey]  

Hello  
Jordan  
Fire  
Many  
Big  
Hey  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J019_ClassObject
package java_Basics;

public class J019_ClassObject {

	int a = 100;
	int b = 150;
	static int c = 100;
	static int d = 150;
	
	1.
	public static void main(String[] args) {
	
		J019_ClassObject classObject = new J019_ClassObject();
		System.out.println("J019_ClassObject = " + (classObject.a + classObject.b));
		}
	----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
	
	2.
	public static void main(String[] args2) {
		J019_ClassObject classObject = new J019_ClassObject();
		classObject.addition();
		}
		
	public void addition() {
		System.out.println("J019_ClassObject = " + (a + c));
		}
	----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
	
	3.
	public static void main(String[] args) {
		J019_ClassObject classObject = new J019_ClassObject();
		classObject.multiply(10, 10);
		}
	
	public void multiply(int a, int b) {
		System.out.println("J019_ClassObject = " + (a * b));
		}
	----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
	
	4.
	public static void main(String[] args) {
		J019_ClassObject classObject = new J019_ClassObject();
		classObject.multiply(10, 10, "Passed!");
		}
	
	public void multiply(int a, int b, String strArg) {
		System.out.println("J019_ClassObject = " + (a * b));
		System.out.println("Arguement is = " + strArg);
		}
	----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
	
	5.
	public static void main(String[] args) {
		J019_ClassObject classObject = new J019_ClassObject();
		int myInt = classObject.addition(10, 10);
		System.out.println("J019_ClassObject = " + myInt);
	}
	
	public int addition(int a, int b) {
		int addition = a + b;
		return addition;
		}
	----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
	
	6.
	public static void main(String[] args) {
		J019_ClassObject classObject = new J019_ClassObject();
		String myString = classObject.addition("Simplilearn");
		System.out.println("J019_ClassObject = " + myString);
	}

	public String addition(String strArg) {
		return "Hello " + strArg;
	}
}

Results :  
1. J019_ClassObject = 250  

2. J019_ClassObject = 200  

3. J019_ClassObject = 100  

4. J019_ClassObject = 100  
   Arguement is = Passed!

5. J019_ClassObject = 250

6. J019_ClassObject = Hello Simplilearn  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J020_Calculator
package java_Basics;

public class J020_Calculator {

	public int addValue(int a, int b) {
		int c = a + b;
		return c;
	}
	
> OR
	
	public int addValue(int a, int b) {
		return a + b;
	}
}

## J021_Calculator_Access
package java_Basics;

public class J021_Calculator_Access {

	@Test
	public void testCalculator() {
		J020_Calculator calculate = new J020_Calculator();
		Assert.assertEquals(calculate.addValue(2, 3), 5);
	}
}

Results :  
PASSED: testCalculator  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J022_ExtentReportGenerate
package java_Basics_Junit_Utility;

import com.relevantcodes.extentreports.ExtentReports;  

public class J022_ExtentReportGenerate {

	public static ExtentReports extent;
	public static String extentReportPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Report\\ReportResult.html";

	public static ExtentReports createReport() {
		extent = new ExtentReports(extentReportPath);
		return extent;
	}
}

## J023_Listener
package java_Basics_Junit_Utility;

import org.testng.ITestContext;  
import org.testng.ITestListener;  
import org.testng.ITestResult;  
import com.relevantcodes.extentreports.ExtentReports;  
import com.relevantcodes.extentreports.ExtentTest;  
import com.relevantcodes.extentreports.LogStatus;  

import b_Cucumber_Utility_002.Extent_Report_Generate;

public class J023_Listener implements ITestListener {
	
	ExtentReports extent;
	ExtentTest test;

	@Override
	public void onStart(ITestContext context) {
		System.out.println("Start " + context.getName());
		extent = J022_ExtentReportGenerate.createReport();
		test = extent.startTest(context.getName());
	}

	@Override
	public void onTestSuccess(ITestResult result) {
		System.out.println("Test " + result.getName() + " Succeed!");
		test.log(LogStatus.PASS, result.getName() + " is passed!");
	}

	@Override
	public void onTestFailure(ITestResult result) {
		System.out.println("Test " + result.getName() + " Failed!");
		test.log(LogStatus.FAIL, result.getName() + " is failed!");
	}

	@Override
	public void onTestSkipped(ITestResult result) {
		System.out.println("Test " + result.getName() + " Skipped!");
		test.log(LogStatus.SKIP, result.getName() + " is skipped!");
	}

	@Override
	public void onFinish(ITestContext context) {
		System.out.println("End " + context.getName());
		extent.endTest(test);
		extent.flush();
	}
}

### extent-config.xml
	<?xml version="1.0" encoding="UTF-8"?>
	<extentreports>
		<configuration>
			<!-- report theme -->
			<!-- standard, dark -->
			<theme>standard</theme>

			<!-- document encoding -->
			<!-- defaults to UTF-8 -->
			<encoding>UTF-8</encoding>

			<!-- protocol for script and stylesheets -->
			<!-- defaults to https -->
			<protocol>https</protocol>

			<!-- title of the document -->
			<documentTitle>Simplilearn - Cucumber Framework</documentTitle>

			<!-- report name - displayed at top-nav -->
			<reportName>Simplilearn - Cucumber Report</reportName>

			<!-- global date format override -->
			<!-- defaults to yyyy-MM-dd -->
			<dateFormat>yyyy-MM-dd</dateFormat>

			<!-- global time format override -->
			<!-- defaults to HH:mm:ss -->
			<timeFormat>HH:mm:ss</timeFormat>

			<!-- custom javascript -->
			<scripts>
				<![CDATA[
		$(document).ready(function() {
		});
	      ]]>
			</scripts>
			<!-- custom styles -->
			<styles>
				<![CDATA[
	      ]]>
			</styles>
		</configuration>
	</extentreports>

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J024_Screenshot
package java_Basics_Junit_Utility;

import java.io.File;  
import java.io.IOException;  
import org.apache.commons.io.FileUtils;  
import org.openqa.selenium.OutputType;  
import org.openqa.selenium.TakesScreenshot;  
import org.openqa.selenium.WebDriver;  

public class J024_Screenshot {

	WebDriver driver;

	public Screenshot(WebDriver driver) {
		this.driver = driver;
	}
	
	public void takeScreenShot(String fileName) {
		File screenShot = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
		try {
			FileUtils.copyFile(screenShot,
					new File("C:\\Users\\Jordan Liu\\eclipse-workspace\\Phase2-Swiggy_App_In_Diff_Env\\Screenshot\\" + fileName + ".png"));
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J025_ScrollDown
package java_Basics_Junit_Utility;

import org.openqa.selenium.JavascriptExecutor;  
import org.openqa.selenium.WebDriver;  

public class J025_ScrollDown {

	WebDriver driver;

	public Scroll_Down(WebDriver driver) {
		this.driver = driver;
	}

	public void ScrollingDown() throws InterruptedException {
		JavascriptExecutor js = (JavascriptExecutor) driver;
		js.executeScript("window.scrollBy(0,500)", "");
	}
}

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J026_Junit_Assertions
package java_Basics_Junit;

package a_Junit_001;

import static org.junit.jupiter.api.Assertions.*;  
import org.junit.jupiter.api.Test;  

public class J026_Junit_Assertions {

	@Test
	public void testM0() {
		String str1 = "abc";
		String str2 = "def";
		int val1 = 5;
		int val2 = 6;
		String str3 = new String("abc");
		String str4 = new String("abc");
		String[] arr1 = {"Jo", "Lo", "Ho"};
		String[] arr2 = {"Jo", "Lo", "Ho"};
		String[] arr3 = {"Jordan", "Loki", "Hope"};
		
		assertEquals(str1, str2);
		assertEquals(str3, str4);
		assertEquals(val1, val2);
		assertTrue(val2 > val1);
		assertFalse(val1 > val2);
		assertArrayEquals(arr1, arr2);
		assertArrayEquals(arr1, arr3);
	}
}

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J027_Junit_Assumptions
package java_Basics_Junit;

import static org.junit.jupiter.api.Assertions.*;  
import org.junit.jupiter.api.Test;  

public class J027_Junit_Assumptions {

	public String b = "Assumed correct";
	
	@Test
	public void testAssumption() {
		int a = 10;
		assumeTrue(a < 5);
		
> OR

		assumeFalse(a > 5);
	}

	@RepeatedTest(5)
	public void repeat() {
		System.out.println("Repeat");
		int a = 2;
		assertEquals(2, a);
		System.out.println(a + "-" + b);
	}
}

Results :  
Repeat  
2-Assumed correct  
Repeat  
2-Assumed correct  
Repeat  
2-Assumed correct  
Repeat  
2-Assumed correct  
Repeat  
2-Assumed correct  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J028_Junit_AtMethods
package java_Basics_Junit;

import org.junit.BeforeClass;  
import org.junit.jupiter.api.AfterAll;  
import org.junit.jupiter.api.BeforeAll;  
import org.junit.jupiter.api.BeforeEach;  
import org.junit.jupiter.api.Test;  

public class J028_Junit_AtMethods {

	@Test
	public void testM0() {
		System.out.println("Hello Junit 5 test");
	}

	@Test
	public void testM1() {
		System.out.println("Hello Junit 5 test 2");
	}

	@BeforeEach
	public void testBE() {
		System.out.println("Before each tests");
	}

	@BeforeAll
	public static void testAll() {
		System.out.println("Before all");
	}

	@AfterAll
	public static void testAAll() {
		System.out.println("After all");
	}
}

Results :  
Before all  
Before each tests  
Hello Junit 5 test  
Before each tests  
Hello Junit 5 test 2  
After all  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J029_Junit_DynamicTest
package java_Basics_Junit;

import static org.junit.jupiter.api.Assertions.*;  
import static org.junit.jupiter.api.DynamicTest.*;  
import java.util.Arrays;  
import java.util.Collection;  
import org.junit.jupiter.api.DynamicTest;  
import org.junit.jupiter.api.TestFactory;  

public class J029_Junit_DynamicTest {

	@TestFactory
	Collection<DynamicTest> dynamicM() {
		return Arrays.asList(dynamicTest("TestM1", () -> assertTrue(1 < 4)),
				     dynamicTest("TestM2", () -> System.out.println("Hello")),				
				     dynamicTest("TestM3", () -> assertEquals("He", "He")));
	}
}

Results :  
Hello  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J030_Junit_IgnoredDisabled
package java_Basics_Junit;

import org.junit.jupiter.api.Disabled;  
import org.junit.jupiter.api.Test;  
import org.junit.jupiter.api.condition.DisabledIfSystemProperty;  
import org.junit.jupiter.api.condition.DisabledOnJre;  
import org.junit.jupiter.api.condition.DisabledOnOs;  
import org.junit.jupiter.api.condition.JRE;  
import org.junit.jupiter.api.condition.OS;  

public class J030_Junit_IgnoredDisabled {

	@Test
	@DisabledOnOs(OS.WINDOWS)
	public void testDisabled() {
		System.out.println("Hello Junit 5 test");
	}

	@Test
	@DisabledOnJre(JRE.OTHER)
	public void testJRE() {
		System.out.println("Hello Junit 5 test 2");
	}
	
	@Test
	@DisabledIfSystemProperty(named = "file.separator", matches = "//")
	public void testSYSPROP() {
		System.out.println("c:"+File.separator+"test"+File.separator+"folder");
	}
	
	@Test
	@Disabled
	public void MustIgnore() {
		System.out.println("Ignore");
	}
}

Results :  
Hello Junit 5 test 2  
c:\test\folder  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J031_Junit_ParameterizedTestSource
package java_Basics_Junit;

import static org.testng.Assert.*;  
import java.lang.annotation.ElementType;  
import java.time.Month;  
import java.util.stream.Stream;  
import org.junit.jupiter.params.ParameterizedTest;  
import org.junit.jupiter.params.provider.CsvSource;  
import org.junit.jupiter.params.provider.EnumSource;  
import org.junit.jupiter.params.provider.MethodSource;  
import org.junit.jupiter.params.provider.ValueSource;  

public class J031_Junit_ParameterizedTestSource {

	@ParameterizedTest
	@ValueSource(ints = { 1, 2, 3, 4, 5 })
	public void atestValue(int num) {
		assertTrue(num < 10);
		System.out.println(num);
		System.out.println(" Value Source -------------------------");
	}

	@ParameterizedTest
	@CsvSource(delimiter = '|', value = { "'name' | 'city'", "'Jordan' | 'SG'" })
	public void btestCSV(String a, String b) {
		System.out.println(a + " - " + b);
		System.out.println(" CSV Source -------------------------");
	}

	@ParameterizedTest
	@EnumSource(Month.class)
	public void ctestEnum(Month month) {
		System.out.println(month.getValue());
		System.out.println(" Enum Source Month -------------------------");
	}

	@ParameterizedTest
	@EnumSource(value = ElementType.class)
	public void dtestEnum(ElementType e) {
		System.out.println(e.name());
		System.out.println(" Enum Source ElementType -------------------------");
	}

	@ParameterizedTest
	@MethodSource("Rmethod")
	public void eMethodS(String str) {
		System.out.println(str);
		System.out.println(" Method Source -------------------------");
	}

	static Stream<String> Rmethod() {
		return Stream.of("X", "Y","Jordan");
	}
}

Results :  
Method Source = X  
Method Source = Y  
Method Source = Jordan  
 
Enum Source ElementType = TYPE  
Enum Source ElementType = FIELD  
Enum Source ElementType = METHOD  
Enum Source ElementType = PARAMETER  
Enum Source ElementType = CONSTRUCTOR  
Enum Source ElementType = LOCAL_VARIABLE  
Enum Source ElementType = ANNOTATION_TYPE  
Enum Source ElementType = PACKAGE  
Enum Source ElementType = TYPE_PARAMETER  
Enum Source ElementType = TYPE_USE  
Enum Source ElementType = MODULE  
Enum Source ElementType = RECORD_COMPONENT  

Enum Source Month = 1  
Enum Source Month = 2  
Enum Source Month = 3  
Enum Source Month = 4  
Enum Source Month = 5  
Enum Source Month = 6  
Enum Source Month = 7  
Enum Source Month = 8  
Enum Source Month = 9  
Enum Source Month = 10  
Enum Source Month = 11  
Enum Source Month = 12  

Value Source = 1  
Value Source = 2  
Value Source = 3  
Value Source = 4  
Value Source = 5  

CSV Source = name - city  
CSV Source = Jordan - SG  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J032_Junit_Stream
package java_Basics_Junit;

import java.util.stream.Stream;  
import org.junit.jupiter.api.extension.ExtensionContext;  
import org.junit.jupiter.params.provider.Arguments;  
import org.junit.jupiter.params.provider.ArgumentsProvider;  

public class J032_Junit_Stream implements ArgumentsProvider {

	@Override
	public Stream<? extends Arguments> provideArguments(ExtensionContext arg0) throws Exception {
		return Stream.of("Apple", "Banana", "Cherry").map(Arguments::of);
	}
}

## J033_Junit_Stream_Access
package java_Basics_Junit;

import org.junit.jupiter.params.ParameterizedTest;
import org.junit.jupiter.params.provider.ArgumentsSource;

public class J033_Junit_Stream_Access {

	@ParameterizedTest
	@ArgumentsSource(Junit_Stream.class)
	public void atestArgSource(String argument) {
		System.out.println(argument);
	}
}

Results :  
Apple  
Banana  
Cherry  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

# Selenium
## J034_SeleniumIntro
package java_Basics_Selenium;

import static org.junit.Assert.assertTrue;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J034_SeleniumIntro {

	static WebDriver driver;
	static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";
	static String lineBreak = "\n";
	static String dashes = "----- ----- ----- ----- ----- ";
	public static String username = "test0102";
	public static String password = "test123";
	public static String wrongUsername = "test010";
	public static String wrongPassword = "test1234";

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		WebDriver driver = new ChromeDriver();
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the777888.com");

		String title = driver.getTitle();
		String Url = driver.getCurrentUrl();
		String windowHandle = driver.getWindowHandle();
		System.out.println(title + lineBreak + dashes);
		System.out.println(Url + lineBreak + dashes);
		System.out.println(windowHandle + lineBreak + dashes);

		WebElement doNotShowAgainToday = driver.findElement(By.xpath("//span[contains(text(),'今日不再显示')]"));
		WebElement doNotShowAgainTodayRadioBtn = driver.findElement(By.xpath("(//*[name()='svg'])[1]"));
		WebElement closeAnnouncementBtn = driver.findElement(By.xpath("(//button[@aria-label='Close'])[1]"));

		if (doNotShowAgainToday.getText().equalsIgnoreCase("今日不再显示")) {
			doNotShowAgainTodayRadioBtn.click();
			closeAnnouncementBtn.click();
			driver.navigate().refresh();
		} else {
			System.out.println("Error at " + doNotShowAgainToday.getText());
			closeAnnouncementBtn.click();
		}

		WebElement liveCasino = driver.findElement(By.xpath("//a[contains(text(),'真人')]"));
		WebElement slots = driver.findElement(By.xpath("//a[contains(text(),'电子')]"));
		WebElement fish = driver.findElement(By.xpath("//a[contains(text(),'捕鱼')]"));
		WebElement sports = driver.findElement(By.xpath("//a[contains(text(),'体育 mm')]"));
		WebElement poker = driver.findElement(By.xpath("//a[contains(text(),'棋牌 B')]"));
		WebElement lottery = driver.findElement(By.xpath("//a[contains(text(),'彩票')]"));
		WebElement eSports = driver.findElement(By.xpath("//a[contains(text(),'电竞')]"));

		if (liveCasino.getText().contains("真人")) {
			System.out.println(liveCasino.getText());
		} else {
			System.out.println("Error at " + liveCasino.getText());
		}

		if (slots.getText().contains("电子")) {
			System.out.println(slots.getText());
		} else {
			System.out.println("Error at " + slots.getText());
		}

		if (fish.getText().contains("捕鱼")) {
			System.out.println(fish.getText());
		} else {
			System.out.println("Error at " + fish.getText());
		}

		if (sports.getText().contains("体育")) {
			System.out.println(sports.getText());
		} else {
			System.out.println("Error at " + sports.getText());
		}

		if (poker.getText().contains("棋牌")) {
			System.out.println(poker.getText());
		} else {
			System.out.println("Error at " + poker.getText());
		}

		if (lottery.getText().contains("彩票")) {
			System.out.println(lottery.getText());
		} else {
			System.out.println("Error at " + lottery.getText());
		}

		if (eSports.getText().contains("电竞")) {
			System.out.println(eSports.getText());
		} else {
			System.out.println("Error at " + eSports.getText());
		}

		WebElement loginBtn = driver.findElement(By.className("login"));
		loginBtn.click();

		WebElement usernameField = driver.findElement(By.id("username"));
		WebElement passwordField = driver.findElement(By.id("password"));
		WebElement eyeIcon = driver.findElement(By.xpath("(//div[@class='ico ico-eye_close'])[1]"));
		WebElement stayLoggedIn = driver.findElement(By.xpath("//span[contains(text(),'保持登录')]"));
		WebElement stayLoggedInRadioBtn = driver.findElement(By.xpath("(//*[name()='svg'])[3]"));
		WebElement submitLoginBtn = driver.findElement(By.id("login_popup_btn"));

		Thread.sleep(1000);
		usernameField.clear();
		usernameField.sendKeys(wrongUsername);
		passwordField.sendKeys(password);
		eyeIcon.click();
		submitLoginBtn.click();

		WebElement wrongUserError = driver.findElement(By.xpath("//div[@class='error_msg error_login_username']"));

		Thread.sleep(1000);
		if (wrongUserError.getText().equals("会员帐号不存在或输入错误，请重新输入")) {
			assertTrue("会员帐号不存在或输入错误，请重新输入", true);
			System.out.println("Error message = " + wrongUserError.getText());
		}

		Thread.sleep(1000);
		usernameField.clear();
		usernameField.sendKeys(username);
		passwordField.clear();
		passwordField.sendKeys(wrongPassword);
		eyeIcon.click();
		submitLoginBtn.click();
		
		WebElement wrongPasswordError = driver.findElement(By.xpath("//div[@class='error_msg error_login_password']"));
		
		// i do not understand why the getText returns empty in console
		System.out.println(wrongPasswordError.getText());

		passwordField.clear();
		passwordField.sendKeys(password);
		eyeIcon.click();

		Thread.sleep(1500);
		if (stayLoggedIn.getText().equals("保持登录")) {
			stayLoggedInRadioBtn.click();
		} else {
			System.out.println("Error at " + stayLoggedIn.getText());
		}

		submitLoginBtn.click();

		Thread.sleep(3000);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J035_SeleniumStartDriver
package java_Basics_Selenium;

import org.openqa.selenium.By;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J035_SeleniumStartDriver {

	static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		WebDriver driver = new ChromeDriver();
		driver.get("https://www.youtube.com/");

		WebElement exploreBtn = driver.findElement(By.xpath("(//yt-icon[@id='icon'])[2]"));
		exploreBtn.click();
		
		Thread.sleep(2000);
		
		WebElement textTrending = driver.findElement(By.xpath("(//yt-formatted-string[@id='destination-label'])[1]"));
		String text = textTrending.getText();
		if (text.equalsIgnoreCase("Trending")) {
			System.out.println("Pass");
		} else {
			System.out.println("Fail");
		}

		Thread.sleep(2000);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J036_SeleniumWait
package java_Basics_Selenium;

import java.io.IOException;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  
import org.openqa.selenium.support.ui.ExpectedConditions;  
import org.openqa.selenium.support.ui.WebDriverWait;  

public class J036_SeleniumWait {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException, IOException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Wait actions = new Wait();
		actions.StartBrowser();
		actions.dynamicLoading();
		actions.loadingTest();
		actions.closeBrowser();
	}

	public void StartBrowser() throws InterruptedException {
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/");
		Thread.sleep(1500);
	}

	public void dynamicLoading() throws InterruptedException {
		WebElement dynamicLoad = driver.findElement(By.xpath("//a[normalize-space()='Dynamic Loading']"));
		dynamicLoad.click();
		WebElement dynamicLoadEx1 = driver.findElement(By.xpath("//a[normalize-space()='Example 1: Element on page that is hidden']"));
		dynamicLoadEx1.click();
	}
	
	public void loadingTest() throws InterruptedException {
		WebElement startBtn = driver.findElement(By.tagName("button"));
		startBtn.click();
		WebDriverWait wait = new WebDriverWait(driver, 10);
		WebElement resultText = driver.findElement(By.xpath("//h4[normalize-space()='Hello World!']"));
		wait.until(ExpectedConditions.visibilityOf(resultText));
		System.out.println(resultText.getText());
	}
	
	public void closeBrowser() throws InterruptedException {
		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J037_SeleniumWindowHandle
package java_Basics_Selenium;

import java.io.IOException;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  
import org.openqa.selenium.support.ui.ExpectedConditions;  
import org.openqa.selenium.support.ui.WebDriverWait;  

public class J037_SeleniumWindowHandle {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";
	
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/windows");
		
		Thread.sleep(1000);
		String parentWH = driver.getWindowHandle();
		driver.findElement(By.xpath("//a[normalize-space()='Click Here']")).click();
		Thread.sleep(1500);
		Set<String> windowHandles = driver.getWindowHandles();
		System.out.println(windowHandles.size());
		
		Iterator<String> iterate = windowHandles.iterator();
		while(iterate.hasNext()) {
			String winH = iterate.next();
			driver.switchTo().window(winH);
			System.out.println(winH);
		}
		
		System.out.println(driver.findElement(By.xpath("//h3[normalize-space()='New Window']")).getText());
		driver.close();
		driver.switchTo().window(parentWH);
		
		driver.findElement(By.xpath("//a[normalize-space()='Click Here']")).click();
		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J038_SeleniumTakeScreenshot
package java_Basics_Selenium;

import java.io.File;  
import java.io.IOException;  
import org.apache.commons.io.FileUtils;  
import org.openqa.selenium.OutputType;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.TakesScreenshot;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J038_SeleniumTakeScreenshot {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";
	public static String screenShotPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Screenshot\\";

	public static void main(String[] args) throws InterruptedException, IOException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Take_ScreenShot actions = new Take_ScreenShot();
		actions.StartBrowser();
		actions.takeScreenShot("internet-herokuapp");
		actions.closeBrowser();
	}

	public void StartBrowser() throws InterruptedException {
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/");
		Thread.sleep(1500);
	}

	public void takeScreenShot(String fileName) throws IOException {
		File screenShot = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
		try {
			FileUtils.copyFile(screenShot, new File(screenShotPath + fileName + ".png"));
		} catch (IOException e) {
			e.printStackTrace();
		}
	}

	public void closeBrowser() throws InterruptedException {
		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J039_SeleniumListOf
package java_Basics_Selenium;

import java.io.IOException;  
import java.util.List;  
import java.util.concurrent.TimeUnit;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J039_SeleniumListOf {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException, IOException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();

		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("http://demo.guru99.com/test/ajax.html");

		WebElement navigateBar = driver.findElement(By.xpath("//ul[@class='nav navbar-nav']"));
		
		driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		List<WebElement> elements = navigateBar.findElements(By.tagName("li"));
		for (WebElement WebE : elements) {
			System.out.println(WebE.getText());
		}

		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J040_SeleniumIframe
package java_Basics_Selenium;

import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J040_SeleniumIframe {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/frames");
		
		driver.findElement(By.xpath("//a[normalize-space()='iFrame']")).click();
		WebElement frame = driver.findElement(By.xpath("//iframe[@id='mce_0_ifr']"));
		driver.switchTo().frame(frame);
		WebElement content = driver.findElement(By.xpath("//p[normalize-space()='Your content goes here.']"));
		System.out.println(content.getText());
		content.clear();
		content.sendKeys("Hello world!");
		driver.switchTo().defaultContent();

		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J041_SeleniumDropdown
package java_Basics_Selenium;

import java.io.IOException;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  
import org.openqa.selenium.support.ui.Select;  

public class J041_SeleniumDropdown {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException, IOException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Dropdown actions = new Dropdown();
		actions.StartBrowser();
		actions.dropDown();
		actions.dropDownOptions();
		actions.closeBrowser();
	}

	public void StartBrowser() throws InterruptedException {
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/");
		Thread.sleep(1500);
	}

	public void dropDown() throws InterruptedException {
		WebElement dropDownBtn = driver.findElement(By.xpath("//a[normalize-space()='Dropdown']"));
		dropDownBtn.click();
	}
	
	public void dropDownOptions() throws InterruptedException {
		WebElement dropDownOptionsBar = driver.findElement(By.id("dropdown"));
		Select select = new Select(dropDownOptionsBar);
		System.out.println(select.getFirstSelectedOption());
		Thread.sleep(1000);
		select.selectByVisibleText("Option 1");
		Thread.sleep(1000);
		select.selectByIndex(2);
		Thread.sleep(1000);
	}
	
	public void closeBrowser() throws InterruptedException {
		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J042_SeleniumCheckbox
package java_Basics_Selenium;

import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J042_SeleniumCheckbox {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Checkbox actions = new Checkbox();
		actions.StartBrowser();
		actions.selectCheckboxes();
		actions.checkCheckbox();
		actions.closeBrowser();
	}

	public void StartBrowser() throws InterruptedException {
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/");
		Thread.sleep(1500);
	}

	public void selectCheckboxes() {
		WebElement checkboxBtn = driver.findElement(By.xpath("//a[normalize-space()='Checkboxes']"));
		checkboxBtn.click();
	}

	public void checkCheckbox() throws InterruptedException {
		WebElement checkbox1 = driver.findElement(By.xpath("(//input[@type='checkbox'])[1]"));
		Thread.sleep(1000);
		if (!checkbox1.isSelected()) {
			checkbox1.click();
		}
		
		WebElement checkbox2 = driver.findElement(By.xpath("(//input[@type='checkbox'])[2]"));
		Thread.sleep(1000);
		if (checkbox2.isSelected()) {
			checkbox2.click();
		}
	}
	
	public void closeBrowser() throws InterruptedException {
		Thread.sleep(3000);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J043_SeleniumBrowserAction
package java_Basics_Selenium;

import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J043_SeleniumBrowserAction {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Browser_Action actions = new Browser_Action();
		actions.StartBrowser();
		actions.closeAnnouncement();
		actions.clickPromo();
		actions.backToPage();
		actions.refreshPage();
		actions.forwardToPage();
		actions.closeBrowser();
	}

	public void StartBrowser() throws InterruptedException {
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the777888.com");
		Thread.sleep(1500);
	}

	public void closeAnnouncement() throws InterruptedException {
		WebElement doNotShowAgainTodayRadioBtn = driver.findElement(By.xpath("(//*[name()='svg'])[1]"));
		WebElement closeAnnouncementBtn = driver.findElement(By.xpath("(//button[@aria-label='Close'])[1]"));
		doNotShowAgainTodayRadioBtn.click();
		closeAnnouncementBtn.click();
	}

	public void clickPromo() throws InterruptedException {
		WebElement promoBtn = driver.findElement(By.xpath("//div[contains(text(),'专属优惠')]"));
		Thread.sleep(1500);
		promoBtn.click();
	}

	public void backToPage() throws InterruptedException {
		Thread.sleep(1500);
		driver.navigate().back();
		System.out.println("Page backed");
	}

	public void forwardToPage() throws InterruptedException {
		Thread.sleep(1500);
		driver.navigate().forward();
		System.out.println("Page forwarded");
	}

	public void refreshPage() throws InterruptedException {
		Thread.sleep(1500);
		driver.navigate().refresh();
		System.out.println("Page refreshed");
	}

	public void getCSSValue() throws InterruptedException {
		Thread.sleep(1500);
		WebElement colorBox = driver.findElement(By.id("layered_id_attribute_group_14"));
		System.out.println("Color RGB = " + colorBox.getCssValue("background"));
		System.out.println("Border = " + colorBox.getCssValue("border"));
		System.out.println("Height = " + colorBox.getCssValue("height"));
		System.out.println("Width = " + colorBox.getCssValue("width"));
		System.out.println("Class = " + colorBox.getAttribute("class"));
		System.out.println("Style = " + colorBox.getAttribute("style"));
		System.out.println("Tagname = " + colorBox.getTagName());
	}
	
	public void closeBrowser() {
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J044_SeleniumAlert
package java_Basics_Selenium;

import java.io.IOException;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.chrome.ChromeDriver;  

public class J044_SeleniumAlert {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException, IOException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/javascript_alerts");
		
		driver.findElement(By.xpath("//button[normalize-space()='Click for JS Alert']")).click();
		Thread.sleep(1000);
		driver.switchTo().alert().accept();
		System.out.println(driver.findElement(By.xpath("//p[@id='result']")).getText());
		
		driver.findElement(By.xpath("//button[normalize-space()='Click for JS Confirm']")).click();
		Thread.sleep(1000);
		driver.switchTo().alert().accept();
		System.out.println(driver.findElement(By.xpath("//p[@id='result']")).getText());
		Thread.sleep(1000);
		driver.findElement(By.xpath("//button[normalize-space()='Click for JS Confirm']")).click();
		Thread.sleep(1000);
		driver.switchTo().alert().dismiss();
		System.out.println(driver.findElement(By.xpath("//p[@id='result']")).getText());
		
		driver.findElement(By.xpath("//button[normalize-space()='Click for JS Prompt']")).click();
		Thread.sleep(1000);
		driver.switchTo().alert().sendKeys("Hello!!!");
		Thread.sleep(1000);
		driver.switchTo().alert().accept();
		System.out.println(driver.findElement(By.xpath("//p[@id='result']")).getText());
		
		Thread.sleep(1500);
		driver.quit();
	}
}

Results :  
Try it to find out yourself
----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J045_SeleniumActionBuilder
package java_Basics_Selenium;

import java.io.IOException;  
import org.openqa.selenium.By;  
import org.openqa.selenium.Point;  
import org.openqa.selenium.WebDriver;  
import org.openqa.selenium.WebElement;  
import org.openqa.selenium.chrome.ChromeDriver;  
import org.openqa.selenium.interactions.Action;  
import org.openqa.selenium.interactions.Actions;  

public class J045_SeleniumActionBuilder {

	public static WebDriver driver;
	public static String chromeDriverPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Driver\\chromedriver.exe";

	public static void main(String[] args) throws InterruptedException, IOException {
		System.setProperty("webdriver.chrome.driver", chromeDriverPath);
		driver = new ChromeDriver();
		Point browserPosition = driver.manage().window().getPosition();
		driver.manage().window().setPosition(browserPosition.moveBy(1500, 0));
		driver.manage().window().maximize();
		driver.get("https://the-internet.herokuapp.com/drag_and_drop");
		
		WebElement fromE = driver.findElement(By.id("column-a"));
		WebElement toE = driver.findElement(By.id("column-b"));

		Actions builder = new Actions(driver);
		Action act = builder.clickAndHold(fromE).moveToElement(toE).release().build();
		act.perform();
		Thread.sleep(3000);
		driver.quit();
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J046_CucumberAccess
package java_Basics_Junit_Utility;

import org.junit.runner.RunWith;  
import cucumber.api.CucumberOptions;  
import cucumber.api.junit.Cucumber;  

@RunWith(Cucumber.class)
@CucumberOptions(features = "D:\\Eclipse WorkSpace\\CucumberProject\\src\\test\\resources\\features", 
glue = {"Test_run" })
plugin = {"com.vimalselvam.cucumber.listener.ExtentCucumberFormatter:target\\cucumber-reports\\report.html" })
public class Cucumber_Runner {

	@AfterClass
	public static void writeExtentReport() {
		Reporter.loadXMLConfig(new File("D:\\Eclipse WorkSpace\\0001_Maven_Project\\src\\test\\resources\\extent-config.xml"));
		}
}

## J047_CucumberFeatureTest
> Just a sample

	Feature: Test going to a site

  	Scenario: Test going to a site
   		Given I start my browser
   		And I go to "https://the777888.com"
   		Then I see login button
   		And I click on login button  

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

## J048_ExcelWriter
package java_Basics_Junit_Utility;

import java.io.FileOutputStream;  
import java.io.IOException;  
import org.apache.poi.hssf.usermodel.HSSFRow;  
import org.apache.poi.hssf.usermodel.HSSFSheet;  
import org.apache.poi.hssf.usermodel.HSSFWorkbook;  

public class Excel_Writer {

> https://www.javatpoint.com/java-create-excel-file#:~:text=Follow%20the%20steps%20given%20below,we%20have%20written%20in%20CreateExcelFileExample1.

	static String excelPath = "D:\\Eclipse WorkSpace\\0001_Maven_Project\\Excel\\";
	
	public static void main(String[] args) throws IOException {
		HSSFWorkbook workbook = new HSSFWorkbook();
		HSSFSheet sheet = workbook.createSheet("Test");
		HSSFRow rowhead = sheet.createRow(0);
		rowhead.createCell(0).setCellValue("S.No.");  
		rowhead.createCell(1).setCellValue("Customer Name");  
		rowhead.createCell(2).setCellValue("Account Number");  
		rowhead.createCell(3).setCellValue("e-mail");  
		rowhead.createCell(4).setCellValue("Balance");
		
		HSSFRow row = sheet.createRow(1);  
		row.createCell(0).setCellValue("1");  
		row.createCell(1).setCellValue("Jordan");  
		row.createCell(2).setCellValue("22222");  
		row.createCell(3).setCellValue("me@gmail.com");  
		row.createCell(4).setCellValue("5000.00"); 
		
		FileOutputStream fileOut = new FileOutputStream(excelPath + "Testdata.xlsx");  
		System.out.println("Excel File has been created successfully.");   
		workbook.write(fileOut);
		fileOut.close();
		workbook.close();  
	}
}

Results :  
Try it to find out yourself

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----
