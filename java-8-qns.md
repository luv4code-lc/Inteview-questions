1. count the no of occurences of words in given string using java8
    
    Input: "welcome to code decode and code decode welcome you"
    
    Output: [code=2, and=1, to=1,decode=2, welcome=2,you=1]
    
            String input = "welcome to code decode and code decode welcome you";
            List<String> list = Arrays.asList(input.split("\\s"));
    
            Map<String, Long> map = list.stream().collect(Collectors.groupingBy(Function.identity(),Collectors.counting()));
            sout(map);

2. Find the duplicate elements in a given integers list in java using stream functions?
  
    input: [10, 28, 87, 10, 20, 76, 28, 80, 80, 80];
    
    output: 10,28,80
      
            List<Integer> list = Arrays.asList(10, 28, 87, 10, 20, 76, 28, 80, 80, 80);
            Set<Integer> set = new HashSet<>();

            list.stream.filter(x -> !set.add(x)).collect(Collectors.toSet()).forEach(System.out::println);

3. write a program to multiply 2 no's using functional interface?
    
            @FunctionalInterface
            public interface Calc{
              int multiply(int a, int b);
            }
    
            class Test{
              public static void main(String[] args){
                Calc calc = (a,b) -> a*b;
                int total = calc.multiply(4, 5); //20
              }
            }

4. Difference between limit() and skip()
  
      ex:- input: [10, 28, 87, 10, 20, 76, 28, 80, 80, 80];
  
      limit() 
      
            => the limit(n) method is an intermediate operation that returns a stream not longer than the requested size. As before, the n parameter can't be
negative.
          
          //only 5 elements can be printed
          
            list.stream.limit(5).forEach(System.out::println);

      skip() 
      
            => the skip(n) method is another intermediate operation that discards the first n elements of a stream. the n parameter can't be negative, and if it's higer than the size of the stream, skip() returns an empty stream.
            
          //print emlements after 6 
          
                list.stream.skip(6).forEach(System.out::println);

5. what is intermediate operation?
    
       => the operations which return another stream as a result are called intermediate operations, they are lazy.
          eg:- filter(), map(), distinct(), sorted(), limit(), skip()
            
6. what is terminal operation?

        
       => the operation which return non-stream values like primitive or object or collection or return  nothing are called terminal operations.
       
       => you can chain multiple intermediate operations and none of them will do anything until you invoke a terminal operation. 
         At that time , all of the intermediate operations that you invoked earlier will be invoked along with the terminal operation.
         
         eg: forEach(), toArray(), reduce((), collect(), man(), max() count(), anyMatch(), allMatch(), noneMatch(), findFirst(), findAny()
                                          

7. diff b/w terminal and non-terminal operators
      
      Intermediate Operations                                                               Termial Operations
      ------------------------------------------------------------------------------------------------------------------------------------------------------------
      1. they return steam                                                                  they return non-stream values.


      2. they can be chained together to form                                                they can't be chained together
         a pipeline of operations
         
      3. pipeline of operations may contatin any number of intermediate operations        pipeline of operations can have maximum one terminal operation, that too at the end
         
      4. lazy loaded                                eagerly loaded
      
      5. don't produce end result                   product end result


================================================================

1. Adding date field values in table

            create table test(
                id int not null primary key auto_increment,
                name varchar(30) not null,
                email varchar(30) not null unique key,
                date_of_joining date not null
            );
    
    //insering data
    
        insert into test(name,email,date_of_joining) values ('Madhav','madhav.p.akv@gmail.com',str_to_date('06-20-1994','%m-%d-%Y'));
        
        
        
================================================================

1. Write an SQL query to find the count of the total occurrences of a particular character – ‘n’ in the FullName field.

        select fullname, length(fullname)-length(repalce,'n','')) from employeedetails;
        
2. Write an SQL query to update the employee names by removing leading and trailing spaces.

        update employeedetails set fullname= ltrim(rtrim(fullname));     
        
3. Fetch all the employees who are not working on any project.

        select empid from employeedetails where projec IS NULL;       
        
4. Write an SQL query to fetch employee names having a salary greater than or equal to 5000 and less than or equal to 10000.

        select fullname from employeedetails
        where empid in
        (select empid from employeesalary
        where salary between 5000 and 10000);
        
5.        
           
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
    
