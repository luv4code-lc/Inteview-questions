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
               
7. Write a SQL query to find all employees who have bonus record in bonus table 
    
            => select e.* from emploee e 
               join bonus b
               on 
               e.employee_id = b.employee_ref_id;
               
8. Write a SQL query to find only odd rows from employee table

            => select *from employee where mod(employee_id,2)<>0;  
            
9. Write a SQL query to fetch first_name from employee table in upper case            
          
            => select upper(first_name) as 'First Name' from employee;
            

10. Write a SQL query to get combine name (first name and last name) of employees from employee table 

            => select concat(first_name,' ',last_name) as 'Full Name' from employee;
            //upper case full name
            => select upper(concat(first_name, ' ',last_name) as 'Full Name' from employee;
            
11. Write a SQL query to print details of employee of employee 'Jennifer' and 'James'.  

            => select *from employee where first_name in('Jennifer','James');
            
12. Write a SQL query to fetch records of employee whose salary lies between

            => select first_name,last_name,salary from employee where salary between 100000 and 500000;
            
13. Write a SQL query to get records of employe who have joined in Jan 2017  

            => select first_name,last_name,joining_date from employee where year(joining_date)=2017 and month(joining_date)=1; 
            => select first_name,last_name, joining_date from employee where joining_date between '2017-01-01' and '2017-02-01';                  
            
14. Write a SQL query to get the list of employees with the same salary   

            => select e1.first_name, e2.last_name from employee e1, employee e2 where e1.salary = e2.salary and e1.employee_id != e2.employee_id;
            
15. Write a SQL query to show all departments along with the number of people working there. 

            =>  select department, count(*) as 'Number of Employees' from employee 
                group by department
                order by count(department); 
                
16. Write a SQL query to show the last record from a table.

            => select *from employee where employee_id=(select max(employee_id) from employee);  
            
17. Write a SQL query to show the first record from a table.
            
            => select *from employee where employee_id=(select min(employee_id) from employee);
            
18. Write a SQL query to get last five records from a employee table.

            => (select *from employee order by employee_id dsec limit 5) order by employee_id;
            
19. Write a SQL query to find employees having the highest salary in each department.      
20. Write a SQL query to fetch three max salaries from employee table.

            => select distinct salary from employee order by salary desc limit 3; 
            
21. Write a SQL query to fetch departments along with the total salaries paid for each of them.

            => select department, sum(salary) as "Total Salary" from employee group by department order by sum(salary);
            
22. Write a SQL query to find employee with highest salary in an organization from employee table.

            => select upper(concat(first_name,' ',last_name)) from employee where salary = (select max(salary) from employee);
            
23. --
24. --
25. write a SQL query to find employees with same salary

            => select e1.first_name, e1.last_name, e1.salary from employee e1, employee e2
            where e1.salary = e2.salary and e1.employee_id != e2.employee_id;
                       

