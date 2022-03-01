# Computer_Programming-2_Activity_2
//Lab-Candy Machine

import java.util.Scanner;

public class CandyMachine {

static Scanner s = new Scanner(System.in);

public static int Choice(){
  int price = -1;
 System.out.println("Products Available:");
 System.out.println("A.       Candy       [5]");
 System.out.println("B.       Chips       [10]");
 System.out.println("C.       Gum         [2]");
 System.out.println("D.       Cookies     [15]");
 
 System.out.println();
 System.out.print("Which product would you like to purchase (Select letter)? ");
 String Choices = s.next().toUpperCase();
 
 if(Choices.equals("A")){
   price = 5;
   return 5;
 }
  else if(Choices.equals("B")){
    price = 10;
    return 10;
  }
  else if(Choices.equals("C")){
    price = 2;
    return 2;
  }
  else if(Choices.equals("D")){
    price = 15;
    return 15;
  }
  else{
    return price;
  }
}

public static void Dispenser(int Money,int CandiesPrice){
  if(Money > CandiesPrice){
    System.out.println("Here's your order, I hope you like it!");
    int Change = Money - CandiesPrice;
    System.out.println("Here's your " + Change + " in change, Thank you for coming!!"); 
    System.out.println();
System.out.println("Please Come Again!");
  }
  else{
    System.out.println("Sorry. Your money is not enough. Here's your " + Money + ", your change.");
  }
}

public static void main(String[] args){
  System.out.println("WELCOME TO MICA ELLA'S CANDY MACHINE!");
  System.out.print("Enter how much money do you have : ");
  int Money = s.nextInt();
  
 int CandiesPrice = Choice();
 
 Dispenser(Money, CandiesPrice);
}
}
