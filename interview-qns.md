what is static class?
  => we cannot create static class directly but we create nested static class.
  => static class is same as not-static class but difference is static classes are not instantiated that means we cannot crerate
  object using new keyword to create a variable of that class.
  
          public class Test{
            static class Demo{
              public void m1(){
                System.out.println("Hello world");
              }
            }

            public static void main(String[] args){
              Test.Demo demo = new Test.Demo();
              demo.m1();
            }
          }
          
How HashMap works internally?
  
What is differnce b/w hashtable and concurrentHashMap?

what is the differnce between Iterator and ListIterator?

What is fail-fast and fail-safe iterator?

what is the diff b/w comparable and comparator? when to use?

what is singleton in java? and how to create it?
  => ensure only one isntance of the class exists
  =>  -> declaring all constructors of that class private
      -> prvide static method that returns a reference to the instance. the lazy instantiation concept is used to write the
          static methods.
      -> the instance is stored as a private staic variable
      
          public class Singleton {
              private static Singleton single_instance = null;

              public String s;

              private Singleton() {
                  s = "Hello";
              }

              public static Singleton getInstance() {
                  if (single_instance == null) {
                      single_instance = new Singleton();
                  }
                  return single_instance;
              }

              public static void main(String[] args) {
                  Singleton x = Singleton.getInstance();
                  System.out.println(x);
              }
          } 
          
What is Enum?

what is serialization?

what if serialization class contains non-serializable variable?
  => it'll throw a NonSerializableException when you try to serialize it.
  -> to avoid that, make that field as transient filed. the class will not be serializable, unless the field is declared
    transient.

What are the features of java-8?
    
    -> Funcational Interfaces
    -> Lambda Expression
    -> Optional class
    -> Streams
    -> Date
    -> Method Reference
    -> Default methods
    -> Static Methods

What is functional expression?

what is lambda expression?

what is IOC in spring?

what is diff b/w singleton and prototype?

@Component, @Qualifier

how will mock final classes?

what is left outer join?

what is diff b/w delete and truncate?

what is diff b/w stored procedure and functional procedure?


diff b/w @RestController and @Controller

how do you authencticate your application?

spirng bean thread safe?
  => yes

overiding a private method?

overriding static mehtod?

how to write exception handling in your project?

finally block?
  => only one time it will not work Sytem.exit(0)
  
sql -> how to find the no of employees associated with the each department?

what is model to develope like agile
  -> usually 3 months has agile commit and  15 days for one sprint basically
  
what will you do unable to deliever particular on sprint? how will you handle the situation?
  






