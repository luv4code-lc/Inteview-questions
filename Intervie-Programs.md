1. Reverse a String

            String input = "javatpoint";

            //reverse string using string inbuild functions
            StringBuffer sb = new StringBuffer(input);
            sb.reverse;

            //using iteration
            char[] ch =input.toCharArray();
            String reverse = "";
            int length = ch.length-1;

            for(int i=length;i>=0;i--){
              reverse += ch[i];
            }
2. check given string is a palindrome or not
            
            To reverse a string and comparing a original string if two string are same it is palindrome otherwise not palindrome.
            
3. capitalize each word in java
            
            String input = "my name is madhav";
            String[] words = input.split("\\s");
            String capitalizeWord = "";
            
            for(String word: words){
               String first = word.substring(0,1);
               String afterFirst = word.substring(1);
               capitallizeWord += first.toUpperCase()+afterFirst+" ";
            }
            
            sout(capitalizeWord.trim());
            
            output: My Name Is Madhav
            
4. reverse each word is string
            
            String input = "my name is madhav";
            String[] words = input.split("\\s");
            String reveseInput = "";
            
            for(String word:words){            
                        StringBuilder sb = new StringBuilder(word);
                        sb.reverse();
                        reverseInput += sb.toString()+" ";
            }
            sout(reverseInput.trim());
            
            output: ym eman si vahdam
            
5. toggle string 

            String input = "this is javatpoint";
            String[] words = input.split("\\s");
            String toggleInput = "";

            for (String word : words) {
                  String first = word.substring(0, 1);
                  String afterFirst = word.substring(1).toUpperCase();
                  toggleInput += first + afterFirst + " ";
            }
            System.out.println(toggleInput.trim());  
            
            output: tHIS iS jAVATPOINT
            
            
            
