# lab04
exercise lab04
public class IncreasedProduction {

    public static void main(String[] args) {
        //declare variables
        
        double rate = .06;
        double production = 4;
        
        //column titles
        System.out.println("(Parts produced measured in thousands)\n\n"+ "Month" + "   " + "Parts Produced\n");
        
            //counts the number of each iterations
            for(int month = 1; month > 0; month++)
            {   
                production = production*Math.pow(1.0 + rate, month);                                
                
                //displays the monthly total parts produced
                if( month < 25 )
                {
                    //Displays monthly total
                    System.out.println("  " + month + "      " + String.format("%.2f",production) + "\n");
                    
                    //calculates the moment when 7000 parts are first produced and displays a message
                    if( production >= 7 && (production/1.06) < 7) {
                        System.out.println(">>>  You produced 7000 parts in " + month + " months, you deserve a raise. <<<\n");
                }}
                else
                {   //displays number of month and total parts produced at the end of 24 months
                    
                    System.out.println("\nIn " + month + " months you produced " + String.format("%.2f",production) + " parts!");
                    //break
                    month = -1;
                
                }
            }       
    }
