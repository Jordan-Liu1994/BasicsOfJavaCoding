# BasicsOfJavaCoding
All the basics of JAVA coding by Simplilearn

----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- ----- -----

# J001_PrintInConsole
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

# J002_LoopDoWhile
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

# J003_LoopFor
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
