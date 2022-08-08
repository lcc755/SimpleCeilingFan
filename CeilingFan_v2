import java.awt.*; 
import java.util.Scanner;

class CeilingFan {  
    static int currentSpeed = 0;
    static boolean isReversed = false;
        
    public static void main(String args[]){  

        Scanner myObj = new Scanner(System.in);  
        System.out.println("Your ceiling fan is now active. \nThere are 2 pull cords avaliable that control the: \n 1) Speed \n 2) Direction \n");
        System.out.println("Enter '1' to pull the first string or '2' to pull the second. \nEnter '0' to get the current settings.\n");

        while (true) {    
            String operation = myObj.nextLine();
            
            if (operation.equals("x")) {
                System.out.println(" => Aborting.\n");
                break;
            } else if (operation.equals("0")) {
                String reversedStr = "No";
                if (isReversed) reversedStr = "Yes";
                System.out.println(" 1) Current Speed => " + currentSpeed + "\n 2) Direction Reversed? => " + reversedStr + "\n");
            } else {
                processInput(operation);
            }
        }

        myObj.close();
    }

    private static void processInput(String input) {

        if (input.equals("1")) {
            if (currentSpeed == 3) currentSpeed = 0;
            else currentSpeed += 1;
            
            switch(currentSpeed) {
              case 0:
                System.out.println(" => Fan off (speed 0).\n");
                break;
              case 1:
                System.out.println(" => Fan on speed 1.\n");
                break;
              case 2:
                System.out.println(" => Fan on speed 2.\n");
                break;
              case 3:
                System.out.println(" => Fan on speed 3.\n");
                break;
              default: // Error
                System.out.println(" => Fan speed error. Reset to 'off' or 0.\n");
                currentSpeed = 0;
                break;
            }
        }
        
        if (input.equals("2")) {
            isReversed = !isReversed;
            
            if (isReversed) {
                System.out.println(" => Fan direction reversed.\n");
            } else {
                System.out.println(" => Fan direction back to default.\n");
            }
        }

    }
}  
