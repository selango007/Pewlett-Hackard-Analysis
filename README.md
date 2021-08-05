# Pewlett-Hackard-Analysis

# 1.0 Overview of the analysis:
The purpoe of this analysis is to:
  -- determine the number of retiring employees per title AND
  -- identify employees who are eligible to participate in a mentorship program
  -- write a report to summarize the analysis and help prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age.
  
# 2.0 Results:
2.1 From the report in retirement_titles.csv file, it seems like there are more than 10000 employees retiring. However the records in this report are not unique, since this report contains duplicate records of employees holding different positions at different times.
2.2 We generated a different report unique_titles.csv where the duplicates of the employee records sre removed. From this report it is determined there are 90398 employees that are about to retire.
2.3 To get a summary of employees (with birth date BETWEEN the years 1952 1955) count by title that are going to retire, we generated the report: retiring_titles.csv. From this report it is found:
  -- most number of employees who are 'Senior Engineers' are retiring. Employees Count: 29414.
  -- least number of employees who are 'Managers' are retiring. Employees Count: 2
2.4 From the report mentorship_eligibilty.csv, it is found that 1549 employees who are currently employed and BIRTH DATE in the year 1965 are eligible for mentorship.

# 3.0 Summary:
3.1 How many roles will need to be filled as the "silver tsunami" begins to make an impact?
    There are employees from 7 different roles are retiring. Most impacted role is 'Senior Engineer' and the least impacted role is 'Manager'. Details on employee count that are retiring in each of the 7 roles can be found in retiring_titles table or retiring_titles;.csv file.

3.2 Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
    Query to run for Retiring Titles: SELECT * FROM retiring_titles;
    
    Employees Count Retiring By Title   Employees Eligible for Mentorship    Query to Run for Mentorship
    Senior Engineer: 29414              Senior Engineer: 290                 SELECT count(*) from mentorship_eligibilty where title = 'Senior Engineer';
    Senior Staff: 28254                 Senior Staff: 411                    SELECT count(*) from mentorship_eligibilty where title = 'Senior Staff';
    Engineer: 14222                     Engineer: 405                        SELECT count(*) from mentorship_eligibilty where title = 'Engineer'; 
    Staff: 12243                        Staff: 313                           SELECT count(*) from mentorship_eligibilty where title = 'Staff'; 
    Technique Leader: 4502              Technique Leader: 77                 SELECT count(*) from mentorship_eligibilty where title = 'Technique Leader'; 
    Assistant Engineer: 1761            Assistant Engineer: 50               SELECT count(*) from mentorship_eligibilty where title = 'Assistant Engineer'; 
    Manager: 2                          Manager: 0                           SELECT count(*) from mentorship_eligibilty where title = 'Manager'; 
    TOTAL: 90398                        TOTAL: 1549                          SELECT count(*) from mentorship_eligibilty
    
    From the above, 
    -- it is determined that while “silver tsunami” is happening, Pewlett-Hackard will be well short of staff across all 7 departments.
    -- there are not enoigh qualifies staff that could fill in all positions that will be open when the retiring staff exit the company.
    -- the hiring process need to be very aggressive to recruit new candidates that could fill in these positions.
