# CA1Programming
Java


//Hi Taras, i couldnt do too many changes, whe i write something, starts to show up that reds signs, and its not readind the file, but the output message error is ok! thans for your help!



package firsttry;

import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;

/**
 *
 * @author lsant
 */
public class FirstTry {
    
    String name;
    String ageS;
    String gender;
    int ageI;
    String title;
    public FirstTry(){
    
        operation();
    
    }
    
    
    public void operation(){
    
      
        
      try {
		
	BufferedReader br = new BufferedReader(new FileReader("C:/Users/lsant/Desktop/JavaProjects/SAMPLE FILES FOR CA 1-20201109/people.txt"));	
				
	name = br.readLine();
	ageS = br.readLine();
	gender = br.readLine();
        
        
        ageI = Integer.parseInt(ageS);
       
     
        
        
		
	}catch(Exception e) {System.out.print(e);
	System.out.println(" ");
    
    }
      
      
          if(!name.contains("0-9")){
          System.out.println("Sorry you name is not Valid");
      }
     
    
      if(gender.equals("M")){
          title = "Mr.";
      }else if(gender.equals("F")){
         title = "Ms."; 
      }else if(gender.equals("T")){
         title = "Mx.";  
     }else if(!gender.equals("M") || !gender.equals("F")|| !gender.equals("T") ){
         System.out.println("ERROR: Incorrect gender");
         System.exit(0);  
     }
      
    
      
      
      
      
      
      
      
      
      
      
      try{
      
      
      BufferedWriter bw = new BufferedWriter( new FileWriter(""));
      
      
      bw.write(name);
      bw.newLine();
      bw.write(ageI);
      bw.newLine();
       bw.write(gender);
      bw.newLine();
      bw.close();
    
      
      }catch(Exception e) {System.out.print(e);
	System.out.println(" ");
    
    }
    }
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        new FirstTry();
    }
    
}

