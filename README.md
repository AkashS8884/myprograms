# myprograms
public class Assignment1{
  	public static void main(String[] args){
    int a=10;
   	  int b=5;
  	   int c=5;
 	    String s=null;
     int d[]=new int[5];
     try{
  	    System.out.println(a/(b-c));
 	    }  catch(ArithmeticException ae){
     	  System.out.println("division by zero error"+ae);
  	   }
  	   try{
     	 System.out.println(s.length());
   	  }
catch(NullPointerException ne){
      	System.out.println("String is null"+ne);
   	  }
    	 try{
     	 d[10]=50;
   	  }
    	 catch(ArrayIndexOutOfBoundsException aoe){
    	   System.out.println("array index exceeded"+aoe);
   	  }
   }
}
Screenshot of excecution:
/*Assignment2
import java.util.Scanner;
 import java.io.*;

class notPrime extends Exception{
	public String toString(){
		return "Not a Positive number";
		}
}

class checkPrime{
 public static void main(String[] args){
	Scanner sc=new Scanner(System.in);
	System.out.println("enter a number");
	int n=sc.nextInt();
	try{
		if(n>0){
			for(int i=2;i<=n/2;i++){
				if(n%i==0){
					System.out.println(n+" is not a prime number");
				}
				else{
					System.out.println(n+" is a prime number");
				}
			}
		}
		else{
			throw new notPrime();
		}
	}catch(notPrime np){
		System.out.println(np.toString());
}
}
}
/*Assignment3
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
public class SubString {
	public static void main(String args[]) throws IOException {
	//File f=new File("sdmcet.txt");
	FileReader f=new FileReader("Sdmcet.txt");
	BufferedReader br= new BufferedReader(f);
	String s1="SDMCET";
	String s2="";
	while((s2=br.readLine())!=null) {
		try {
			if(s2.contains(s1)) {	
System.out.println("SDMCET string found succesfully at position:"+s2.indexOf(s1) );
			}
	 		else
throw new StringNotFoundException("String not found");
		}catch(StringNotFoundException se) {
				se.printStackTrace();
			}
		}
}
}
class StringNotFoundException extends Exception{
	private String se;
	StringNotFoundException(String s){
		this.se=s;
	}
/*Assignment4
import java.util.*;
import java.io.*;
class Assignment4 {
		public static void main(string[] args){
		try{
		FileInputStream fin=new FileInputStream("C:\Users\PRATHAMA M HEGADE\Documents\4th sem\Alphabet.txt");
			FileOutputStream fout=new FileOutputStream("C:\Users\PRATHAMA M HEGADE\Documents\4th sem\consonant.txt");
			int ch;
			while(ch=fin.read()!=-1){
				if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'){
					throw new vowelNotAllowedException();
				}
				else
					fout.write(ch);
				}
			}catch(vowelNotAllowedException e){
				System.out.println(e.toString());
			}
}
}
class vowelNotAllowedException extends Exception{
	public String toString(){
		return "vowels are not allowed";
}
}
