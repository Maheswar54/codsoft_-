
import java.util.Random;
import java.util.Scanner;
public class NumberGame {
      public static void main(String args[]) {
    	  Random rnum = new Random();
    	  int chance=0;
    	  int replay=1;
    	  Scanner sc=new Scanner(System.in);
    while(replay==1)
    {
    	int won=0;
    	  int loss=0;
    	  while(chance<5) 
    	{
             int rvalue = rnum.nextInt(100)+1 ;
             System.out.println("enter your guess value from 1 to 100:");
             
              int gvalue=sc.nextInt();
                 if(rvalue==gvalue) 
                 {
        	     won=won+1;
        	      System.out.println("your guess is correct");
                 }
             else if(rvalue>gvalue)
                {
        	  loss=loss+1;
        	  System.out.println("your guess is too low");
                }
            else
            {
        	  loss=loss+1;
        	  System.out.println("your guess is too high");
            }
          chance=chance+1;
      } 
    	  if(chance==5) {
    	  System.out.println("NO chance More!!");
    	  System.out.println("Final Score:");
    	  System.out.println("Won: "+won);
    	  System.out.println("Loss: "+loss); 
    	  }
    	  
    	  System.out.println("press 'Y' to play again or press 'N' to stop the play" );
          String choice=sc.next();
          String choice1=choice.toLowerCase();
          char ch=choice1.charAt(0);
          switch(ch) 
           {
               case 'y': replay=1;
                             break;
               case 'n': replay=0;
                             break;
                 default: System.out.println("invalid option:"); 
                 
          }
          chance=0;
   
    	  
    } 
    System.exit(0);
}
}
