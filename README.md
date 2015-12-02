# School


import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;
import java.util.HashMap;
import java.util.Map;


public class Main {

	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub
		
		//File file = new File("src/TD2.txt");
		//FileReader fileReader = new FileReader(file);
		BufferedReader in = new BufferedReader(new FileReader("src/TD1.txt"));

		//Unique Operands
		int o1=0;//holder for uniques
		int o2=0;//holder for uniques
		int o3=0;//holder for uniques
		int o4=0;//holder for uniques
		int o5=0;//holder for uniques
		int o6=0;//holder for uniques
		int o7=0;//holder for uniques
		int o8=0;//holder for uniques
		int o9=0;//holder for uniques
		int o10=0;//holder for uniques
		
		//operands
		int inputs = 0;
		int charx = 0;
		int stars = 0;
		int node1=0;
		int node2=0;
		int two =0;
		int one=0;
		int three=0;
		int stk =0;
		int length=0;
		File file = new File("src/TD1.txt"); // Read in the file	
		
		Map<String,Integer> operators; //Map to hold my operators
		Map<String,Integer> operands; //Map to hold my operands
		String[] JavaReservedWords = { "abstract","assert","boolean","break","byte","case",
				"catch","char","class","const","continue","default","do","double","else","extends",
				"false","final","finally","float","for","goto","if","implements","import","instanceof",
				"int","interface","long","native","new","null","package","private","protected","public",
				"return","short","static","strictfp","super","switch","synchronized","this","throw","throws",
				"transient","true","try","void","volatile","while","StringTokenizer","synchronized","instanceof",
				"implements","protected","interface","transient","Exception","Character","ArrayList","volatile",
				"continue","strictfp","boolean","default","extends","finally","package","Integer","Scanner","Matcher",
				"Pattern","return","double","native","switch","throws","String","System","while","break","catch","const",
				"final","float","short","super","false","regex","case","byte","enum","goto","long","this","void","null","true","charAt",
				"Math","File","util","java","try","for","new","out","do","if","io",".","(",")","{","}","[","]",">",
				"<","+","++","-","--","/","*", "=", "!", "&&", "||","\'", "\"", ";"};  // These are the operators that I'm looking for completely.
		
		operators = new HashMap<String,Integer>();// Hash Map: Key | Value
		operands = new HashMap<String,Integer>(); // Hash Map: Key | Value
		
		   try {
		    	
			     FileReader fileReader = new FileReader(file); // allow my file to be read
			     
			     BufferedReader br = new BufferedReader(fileReader); //my parser for looking for specific value
			     
			     
			     
			     String line = br.readLine(); // read the line
			     
			     while((line = br.readLine()) != null ){ // while there is more lines
				    for (String s: JavaReservedWords){ // traverse all operators
				    	if (line.contains(s)){ // if the line contains something in the list
				    		Integer value = operators.get(s); // get the value
				    		if (value==null) value=0; // s does not exist in hash map
				    		operators.put(s, value+1); // place in list and increment the value
	    		
	
				    	}
				    	
				    }
			    	// operands search
			    		   if (line.contains("input")) {//if operand "input" is encountered
			    			   inputs = inputs+1; // increment value
			    			   o1=1;
			    		   }
			    		   if (line.contains("charx")) {//if operand "charx" is encountered
			    			   charx = charx+1;// increment value
			    			   o2=1;
			    		   }
			    		   if (line.contains("stars")) {//if operand "stars" is encountered
			    			   stars = stars+1;// increment value
			    			   o3=1;
			    		   }
			    		   if (line.contains("node1")) {//if operand "node2" is encountered
			    			   node1 = node1+1;// increment value
			    			   o4=1;
			    		   }
			    		   if (line.contains("node2")) {//if operand "node1" is encountered
			    			   node2 = node2+1;// increment value
			    			   o5=1;
			    		   }
			    		   if (line.contains("stk.")) {//if operand "stk" is encountered
			    			   stk = stk+1;// increment value
			    			   o6=1;
			    		   }
			    		   if (line.contains("stk.")) {//if operand "stk" is encountered
			    			   stk = stk+1;// increment value
			    			   
			    		   }
			    		   if (line.contains("-2")){//if operand "-2" is encountered
			    			   two=two+1;// increment value
			    			   o7=1;
			    		   }
			    		   if (line.contains("-3")){//if operand "-3" is encountered
			    			   three=three+1;// increment value
			    			   o8=1;
			    		   }
			    		   if (line.contains("-1")){//if operand "-1" is encountered
			    			   one=one+1;// increment value
			    			   o9=1;
			    		   }
			    		   if (line.contains("length")){//if operand "length" is encountered
			    			   length=length+1;// increment value
			    			   o10=1;
			    		   }
			    		   
			  
			     }
		  }
		 catch (FileNotFoundException e) { // catches exceptions
				    	
		  }

		   System.out.println("			Operators:			"		);
		   System.out.println("_______________________________________________________");
		   
		   
		   // OUTPUT STATEMENTS FROM HERE DOWN
		   //-----------------------------------------------------------------
		   System.out.println("Unique operators:   Frequency of Occurence:");
		   for (Map.Entry entry: operators.entrySet()){
			   System.out.println(entry.getKey()+":			"+entry.getValue());
			
		   }
		   System.out.println("			Operands:			"		);
		   System.out.println("_______________________________________________________");
		   System.out.println();
		   
		   System.out.println("Unique Operands:		Frequency of Occurance:");
		   System.out.println("Input:"+ "				"+inputs);
			 System.out.println("Charx:"+ "				"+charx);
			 System.out.println("Stars:"+ "				"+stars);
			 System.out.println("Node1:"+ "				"+node1);
			 System.out.println("Node2:"+ "				"+node2);
			 System.out.println("Stk:"+ "				"+stk);
			 System.out.println("3:"+"				"+three);
			 System.out.println("2:"+"				"+two);
			 System.out.println("1:"+"				"+one);
			 System.out.println("length:"+"				"+length);
		  //--------------------------------------------------------------------
		//INITIALIZE VALUES FOR METRIC CALCULATIONS
		 int N1 = 0;
		 for (Map.Entry entry: operators.entrySet()){
			   N1 = N1+(int) entry.getValue(); // counting unique operators
			 
		   }
		 float N2 = inputs+charx+stars+node1+node2+stk+length; // Counting Frequency of operands
		 float n1 = operators.size(); // getting size of operators
		 float n2=o1+o2+o3+o4+o5+o6+o7+o8+o9+o10; // counting unique operands
		 float N = N1+ N2; // Length
		 float n = n1+n2; // Vocab
		 float time =  0; //initialize 
		 float volume = 0; //initialize
		 float difficulty = 0; // Initialize
		 float L =(float)0 ;// initialize
		 float E =0; //initialize
		 int S =18; // constant for time
		 
		
		 
		 //Getting my values
		 L = levelmet(n1,n2,N2,L); // Calls metric method
		 volume = (float) (N*Math.log(n)); // Does Volume Calculation
		 difficulty = difficultymet(L,difficulty); // Calls difficulty method
		 E = effortmet(volume,L,E); // calls effort method
		 time = timemet(S,E,time); // calls time method
		 
		 
		 
		 System.out.println("		Unique/Total Operators and Operands:	");
		 System.out.println("_______________________________________________________");
		 System.out.println("\nTotal Occurences of operatorss, N1 = "+N1 );
		 System.out.println("Total Occurences of operands, N2 = "+N2 );
		 System.out.println("Unique operators, n1 = "+n1 );
		 System.out.println("Unique operands, n2 = "+n2+"\n" );
		 
		 System.out.println("			Metrics:		");
		 System.out.println("_______________________________________________________");
		 
		 System.out.println("Vocab: " + n);
		 System.out.println("Length: " + N);
		 System.out.println("Volume: " + volume);
		 System.out.println("Level: " + L);
		 System.out.println("Difficulty " + difficulty);
		 System.out.println("Effort " + E);
		 System.out.println("Time " + time/60); // Divide time by 60 for minutes
		
	}
	
	public static float volumemet(int N, int n, float volume){
		volume = (float) (N * Math.log(n));
		
		return volume;
	}
	public static float levelmet(float n1, float n2, float N2, float L){
		L = (2/n1) * (n2/N2);
		
		return L;
	}
	public static float difficultymet(float L, float difficulty){
		difficulty = (float) (1.0/L);
		return difficulty;
	}

	public static float timemet(int S, float E, float time){
		time = E/S;
		return time;
	}
	public static float effortmet(float volume,float L, float E){
		
		E = (float) volume/L;
		return E;
		
	}
}



