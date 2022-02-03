1. Write a SQL query to find the nth highest salary from employee table.
    ex:- finding 3rd highest salary from employee table
    
        //find all employees order by salary descending order
          => select *from employee order by salary desc;
        //find 3rd highest salary 
          => select distinct salary from employee order by salary desc limit 2,1;
          
2. Write a SQL query to find top n records? 
    ex:- finding top 5 records from employee table
          
          =>   select *from employee order by salary desc limit 5;
          
3. Write a SQL query to find the count of employees working in department 'Admin'
    
          =>   select count(*) from employee where department='Admin;
          
4. Write a SQL query to fetch department wise count employees sorted by department count in desc order.
          
            => select department, count(*) as employeecount
               from employee
               group by department
               order by employeecount desc;

5. Write a query to fetch only the first name(string before space) from the FullName column of user_name table.

6. Write a SQL query to find all the employees from employee table who are also managers

            => select e1.first_name, e2.last_name from employee e1
               join employee e2
               on e1.employee_id = e2.manager_id; 
          

