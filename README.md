# PP-4.9

// * *******************************************************************
// Die.java Author: Lewis/Loftus
//
// Represents one die (singular of dice) with faces showing values
// between 1 and 6.
//********************************************************************
public class Die
{
private final int MAX = 6; // maximum face value
private int faceValue; // current value showing on the die
//-----------------------------------------------------------------
// Constructor: Sets the initial face value.
//-----------------------------------------------------------------
public Die()
{
faceValue = 1;
}
//-----------------------------------------------------------------
// Rolls the die and returns the result.
//-----------------------------------------------------------------
public int roll()
{
faceValue = (int)(Math.random() * MAX) + 1;
return faceValue;
}
//-----------------------------------------------------------------
// Face value mutator.
//-----------------------------------------------------------------
public void setFaceValue(int value)
{
faceValue = value;
}
//-----------------------------------------------------------------
// Face value accessor.
//-----------------------------------------------------------------
public int getFaceValue()
{
return faceValue;
}
//-----------------------------------------------------------------
// Returns a string representation of this die.

//-----------------------------------------------------------------
public String toString()
{
    String result = Integer.toString(faceValue);
   return result;
 }
}

////////

public class PairOfDice
{

  // Making two dice
  Die DieOne = new Die();
  Die DieTwo = new Die();

  /**
   * PairOfDice - Creates a pair of dice
   */
  public PairOfDice()
  {

  }

  /**
   * GetDieOne - Returns the value of DieOne
   */
  public int getDieOne()
  {

    return DieOne.getFaceValue(); // Returns face value of DieOne

  }

  /**
   * setDieOne - Sets value of DieOne
   * 
   * @param iValue The integer value the die will become
   */
  public void setDieOne(int iValue)
  {

    // Sets value of DieOne
    DieOne.setFaceValue(iValue);

  }

  /**
   * GetDieTwo - Returns the value of DieTwo
   */
  public int getDieTwo()
  {

    return DieTwo.getFaceValue(); // Returns face value of DieTwo

  }

  /**
   * setDieTwo - Sets value of DieTwo
   * 
   * @param iValue The integer value the die will become
   */
  public void setDieTwo(int iValue)
  {

    // Sets value of DieTwo
    DieTwo.setFaceValue(iValue);

  }

  /**
   * roll - Rolls both dice of the pair to values between 1 and 6
   */
  public void roll()
  {

    // Rolls both dice
    DieOne.roll();
    DieTwo.roll();

  }

  /**
   * getSum - Gets the sum of both dice in the pair
   */
  public int getSum()
  {

    // Calculates sum of two dice
    int iSum = DieOne.getFaceValue() + DieTwo.getFaceValue();

    return iSum; // Returns sum of two dice

  }

    class Math {

        static void random() {
            throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
        }

        public Math() {
        }
    }
}

/////////




import java.util.Scanner;
import java.util.Random;
public class RollingDice2
        
{

  // Making a pair of dice
  private static PairOfDice DiePairOne = new PairOfDice();

  /**
   * main method - Shows off methods of the PairOfDice class
   *  11/2/2022
   *  Derek Durand
   */
  public static void main(String[] args)
   
          
  {
      Scanner scan = new Scanner(System.in);
      Random ran = new Random();
      int die1;
      int die2;
    // Outputting first original dice sum
        System.out.print("Before rolling the dice the numbers were ");
        DiePairOne.roll();   
        System.out.print(DiePairOne.getSum());
        System.out.print(" and ");
         DiePairOne.roll();   
        System.out.println(DiePairOne.getSum());
        
       System.out.println("Hit Enter to Roll the Dice");
       scan.nextLine();
    DiePairOne.roll();   
    System.out.println("Dice value One");
    die1 = ran.nextInt(6) + 1;
    System.out.println(die1);
    System.out.println("");

    // Setting and outputting second dice sum
        System.out.println("Dice value One");
    die2 = ran.nextInt(6) + 1;
    System.out.println(die2);
    System.out.println("");
    
    // Setting and outputting third dice sum
    DiePairOne.roll(); 
    System.out.print("Sum of The dice ");
    System.out.println(die1 + die2);
    
   
  }

}

