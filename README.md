Java-Two-Dimensional-Arrays
===========================
import java.util.Scanner; 
import java.util.*;
import java.math.*;


public class twoDiArrays


{
    public static void main(){
        Scanner input = new Scanner(System.in);
        int[][] twoDimensional = loadRandomData();
        printData(twoDimensional);
        sum(twoDimensional);
        twoDimensional = makeNegative(twoDimensional);
        System.out.println("Input number (parametetr): ");
        int num = input.nextInt();
        findNum(num, twoDimensional);
    }
    public static int[][] loadRandomData()
    {
            Scanner input = new Scanner(System.in);
            Random rand = new Random();
        
        
            System.out.println("How many rows? ");
            int row = input.nextInt();
             
        
            System.out.println("How many columns? ");
            int columns = input.nextInt();
       
      
            int [][] arrayContents = new int[row] [columns];
            System.out.println("2d Array Contents:  \n");
      
          for(row = 0; row < arrayContents.length; row++)
          {
           for(columns = 0; columns < arrayContents[row].length; columns++)
           {
               arrayContents[row][columns] = rand.nextInt(10);                              //positive function
            }
               
           }
           return arrayContents;
        }
    public static void printData(int[][] array){                          
     
           for(int row = 0; row < array.length; row++)
            {
                for(int columns = 0; columns < array[row].length; columns++)               //this is printing out my contents
                {
                    System.out.print(array[row][columns] + " ");
                }
              System.out.println();
            }
           System.out.println("\n");
        }
    public static void sum(int[][] arrayContents){   
          int arrayTotal = 0;
          for(int r = 0; r < arrayContents.length; r++)
          {
            for(int c = 0; c < arrayContents[r].length; c++)                            //sum
            {
                arrayTotal += arrayContents[r][c];
            }
          }
           System.out.println("Sum: " + arrayTotal);
        }
           
           
           

        
     
     
    public static int[][] makeNegative(int[][] arrayContents){
              for( int row = 0; row < arrayContents.length; row++)
              {
                  for(int columns = 0; columns < arrayContents[row].length; columns++)          
                  {
                      arrayContents[row][columns] = (arrayContents [row] [columns] * -1); 
                      System.out.print(arrayContents[row][columns] + " ");   //negative function
                    }
                   System.out.println();
                }  
                return arrayContents;
            }
          
           
     
    
         public static void findNum(int num, int[][] arrayContents){       
               int count = 0;
               
             
             for( int r = 0; r < arrayContents.length; r++)
                {
                    for(int k = 0; k < arrayContents[r].length; k++)
                    {
                        if(count == 0){
                           
                        if(arrayContents[r][k] == num){
                            System.out.println("Row: " + r + " Column " + k);
                        count++;
                        }
                            else {
                                System.out.println("Not found!");
                                count++;
                            }
                        }
                    }
                         
    
    
                    }
}
}

Experimenting with two dimensional arrays by printing out its contents, computing its sums, and other functions.
