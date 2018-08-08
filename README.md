# Extra_Ex3_17

/*
(Game: scissor, rock, paper) Write a program that plays the popular scissor-rockpaper
game. (A scissor can cut a paper, a rock can knock a scissor, and a paper can
wrap a rock.) The program randomly generates a number 0, 1, or 2 representing
scissor, rock, and paper. The program prompts the user to enter a number 0, 1, or
2 and displays a message indicating whether the user or the computer wins, loses,
or draws. */

package com.personal.Extra3_17;

import java.util.Scanner;

public class Extra3_17 {

	public static void main(String[] args) {

		Scanner sc = new Scanner(System.in);
		int computer,user;
		do {
		 computer=(int)(Math.random()*3 );
		 System.out.println(computer);
		System.out.println("press 0 as rock  OR" +"/n"+
		" press 1 as paper OR " + "/n" +"press 2 as scissor ");
		 user= sc.nextInt();
		 if( computer == user) {
			 System.out.println("both input same, pleaase try again " );
		 continue;
		 }
			 if(computer==0 && user==1) {
				 System.out.println("The computer is rock. You are paper. You won");
				 break;}
				 else if(computer==1 && user==0) {
					 System.out.println("The computer is paper. You are rock. You lose");
				 break;
				 }
				 
			 if(computer==0 && user==2) {
				 System.out.println("The computer is rock. You are scissor. You lose");
				 break;
				 }
			 else if(computer==2 && user==0) {
				 System.out.println("The computer is scissor. You are rock. You won");
				 break;
				 }
			 
			 if(computer==1 && user==2) {
				 System.out.println("The computer is paper. You are scissor. You won");
				 break;
				 }
			 else if(computer==2 && user==1) {
				 System.out.println("The computer is scissor. You are paper. You lose");
				 break;
				 }
		
				 }while(computer != user);
	}

}
