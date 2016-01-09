# Java-Assignment1
section 3
                                       Group 5 members name                          Id
                              1.Dawit Abebe                                   EITM/ur83632/07
                              2.Michael Terefa                               EITM/ur83892/07
                              3.Yayney Berhe                                  EITM/ur84083/07
                              4.Yifrashewa Tekkola                        EITM/ur163821/06 
                              5.Tesfay Nigus                                   EITM/ur84043/07
                              6.Yohannes Kelem                              EITM/ur163827/06
Question 1
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package fibonancie.q1;

import java.util.Scanner;

/**
 *
 * @author abrish
 */
public class FibonancieQ1 {

     public static void fibonachi(int l){
         int a=0;
        System.out.println(a);
        int b=1;
        for (int i=0;i<=l;i++)
        {b=a+b;
        a=a+b;
        System.out.println(b);
                System.out.println(a);
}}
      public static void factorial(int n){
        int f=1;
        for(int i=1;i<= n;i++)
        {f=f*i;
        }
        System.out.println("the factorial is "+f);
    }
    public static void main(String[] args) {
        Scanner h=new Scanner(System.in);
        System.out.println("enter the number");
        int g=h.nextInt();
        fibonachi(g);
        factorial(g);
    }
}

    ///////////////////////////////////////////////
Qustion 2
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package encrypt.q2;

import java.util.Scanner;

/**
 *
 * @author abrish
 */
public class EncryptQ2 {
	static Scanner scan=new Scanner(System.in);
	public static void convert( char[] letter, char[] repr, char[] input, int limit){
		int[] index=new int[30];
		int counter=0;
		for(int i=0;i<limit;i++){
		for(int j=0;j<52;j++){
			if(input[i]==letter[j]){
				index[counter]=j;
				counter++;
				
				break;
			}
		}
		
		}
		for(int k=0;k<limit;k++){
			int val=index[k];
			
			System.out.print(repr[val]);
		}
		}
    public static void main(String[] args) {
	char[] letters={'A','a','B','b','C','c','D','d','E','e','F','f','G','g','H','h','I','i','J','j','K','k','L','l','M','m','N','n','O','o','P','p','Q','q','R','r','S','s','T','t','U','u','V','v','W','w','X','x','Y','y','Z','z'};
	char[] encodin={'%','9','@','#','1','2','3','4','5','6','7','8','0','}','{',']','[',',','.','>','<','/','0','-','|',':',';','+','$','%','^','&','*',',',':','~','`','5','\\','+','=','7','~',':','2','*',']','8','$','_','+',')'};
char[] converted=new char[30];
	System.out.println("please enter words limited to 20 and please dont enter spaces");
String str=scan.nextLine();
System.out.println(letters.length);
System.out.println(encodin.length);
str.getChars(0, str.length(), converted, 0);

convert(letters,encodin,converted,str.length());
    }
    }
/////////////////////////////////////////////
Qustion 3
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package banksystem.q3;

import java.util.Scanner;

/**
 *
 * @author abrish
 */
public class BankSystemQ3 {
    String name;
    long bankaccount;
    double balance;
public BankSystemQ3(String s1,long d1,double d2){
    name = s1;
    bankaccount = d1;
    balance = d2;
}
public void deposit(){
    Scanner bb =new Scanner(System.in);
    System.out.println("Enter the money you want to diposite");
    double dep=bb.nextDouble();
balance=balance+dep;
System.out.println("your balace is : "+balance);
}
public void withdraw(){
Scanner uu=new Scanner(System.in);
System.out.println("Enter the money you wish to withdraw");
double aa=uu.nextDouble();
if (aa<=balance){
    balance=balance-aa;
System.out.println("your current balance after the withdrawal is : "+balance);}
else {
    System.out.println("Your balance is insuficent that is more than your balance.");}
   }
public static void main(String[] args) {
        Scanner jj=new Scanner(System.in);
        System.out.println("Welcome to Enat Bank.");
        System.out.println();
        System.out.print("Enter your name : ");
        String vv=jj.nextLine();
        System.out.print("Enter the your account number");
        long  ss=jj.nextLong();
        System.out.println("Enter your intial account");
        double mm=jj.nextDouble();
        System.out.println("ok,"+vv+" what do you want to do ?");
        System.out.println("1--Deposite money ");
        System.out.println("2--Withdraw money");
        int yy=jj.nextInt();
        BankSystemQ3 b=new BankSystemQ3(vv,ss,mm);
        switch(yy){
            case 1:b.deposit();
                break;
            case 2: b.withdraw();
                break;
            default :
                System.out.println("wrong choice.");
                break;
        }
        System.out.println("If you want to back again press: y");
        System.out.println(" if not press : N");
        Scanner qq=new Scanner (System.in);
        String p=qq.nextLine();
        String sr="y";
        if (p.equals(sr))
        {String[]s2=null;
        main(s2);
        }
}
}
    /////////////////////////////////////////
Qustion 4
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package reverse.q4;

import java.util.Scanner;

/**
 *
 * @author abrish
 */
public class ReverseQ4 {
    public static void main(String[] args) {
    Scanner s=new Scanner(System.in);
       char aa,bb,a;
       System.out.println("Enter the string.");
       String s1=s.nextLine();
       char [] c1=s1.toCharArray();
      aa=c1[0];
      bb=c1[2];
      c1[0]=c1[1];
      c1[1]=aa;
      c1[2]=c1[3];
      c1[3]=bb;
      for (char z:c1)
          System.out.print(z);
         System.out.print(" is the reverse of this string ");

    }
}
///////////////////////////////////////////////////
Qustion 5
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package oepsl.q5;

import java.util.Scanner;

/**
 *
 * @author abrish
 */
public class OEPSLQ5 {
    public static void main(String[] args) {
      
        Scanner bi=new Scanner(System.in);
 System.out.println("Enter the how many no : ");
 int x=bi.nextInt();
 System.out.println("Enter the the numbers : ");
 double[]numbers=new double[x];
 for(int i=0;i<x;i++)
 {
 numbers[i]=bi.nextDouble();
 }
  System.out.println("******MENU*******:");
 System.out.println("Press 1.Display even numbers");
 System.out.println("Press 2.Display the maximum numbers of all");
 System.out.println("Press 3.Display the manimum numbers of all");
 System.out.println("Press 4.Display find the odd numbers");
 System.out.println("Press 5.Display the prime  number enterd");
 System.out.println("!!!!!!Choice what you want to do!!!!!!!!");
 int c=bi.nextInt();
 switch(c){
     case 1: even(numbers); break;
     case 2: System.out.println("The maximum no is : " + maxNum(numbers)); break;
     case 3:System.out.println("The minimum no is "+ minNum(numbers)); break;
     case 4:odd(numbers); break;
     case 5:prime(numbers); break;

     default: System.out.println("!!!!!!!!!!you enter wrong choice!!!!!!!!!!");
    }

    }
 
public static void even(double[]r){
for(int i=0;i<r.length;i++)
if (r[i]%2==0){
 System.out.println(r[i]);
}}
public static double minNum(double[] z){
    double smallest = z[0];
    for(int i=1;i<z.length;i++){
        if(z[i]<smallest){
            smallest=z[i];}
}
        return smallest;
}
public static void odd(double[] s){
    for(int i=0;i<s.length;i++)
    if (s[i]%2!=0){
        System.out.println("the odd numbers are " +s[i]);
}
   }
public static double maxNum(double[] y){
double maximum=y[0];
for (int i=0;i<y.length;i++){
if(y[i]>maximum){
maximum=y[i];}
}
return maximum;
    }

public static void prime(double[] k){
for(int i =0;i<k.length;i++){
    int f=0;
   for(int j=2;j<k[i];j++) {
       if(k[i]%j==0){
       f=f+1;}}
if(f==0)
        System.out.println(k[i]);}
    }   }
