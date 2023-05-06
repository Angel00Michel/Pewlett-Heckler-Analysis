### Pewlett-Hackard-Analysis
SQL / VScode

# Overview of Analysis

This Analysis was designed for us to determine the following:
1. To determine the number of retiring employees per title.
2. To identify employees who are eligible to participate in a mentorship program.

# Results

Focusing on the first analysis : the number of retiring employees per title, we determined from our result the following

- There is a total of 72,458 employees in which are close to retirement (*see query at end of file*).
- The majority of retirees will be senior engineers (25,916) and senior staff consisting of 24,926. This tells us it will be about 70% of our near future retirees.
- There will also be 2 Managers that might retire in the near future.

![image](https://user-images.githubusercontent.com/106771574/236639260-c8e96c3f-b33a-486d-9793-0262960905b6.png)


Stepping into the second analysis : Which employess are eligible to participate in a mentorship program?

- There are 1,549 employees that are eligible to participate in the mentorship program that were born from January 1, 1965 and December 31, 1965.(*see query at end of file*).

# Summary

There are 72,458 roles that are needed to be filled in the near future. Including 25,916 senior engineers and 24,926 senior personnel. This will create quite an impact in the workforce! Since there are 1,549 retirement-ready employees acting as mentors, this might not be enough to train the next generation of employees. This depicts that there would 47 employees per every 1 mentor. 

(*)Query that would give you the count of mentors and the count of retirees are extremely useful in this situation(*):
  1. Count of mentors
SELECT COUNT(mentorship_eligibility.emp_no) FROM mentorship_eligibility
![image](https://user-images.githubusercontent.com/106771574/236639481-3aafd127-193c-4eb8-a70b-8d7822ad80d2.png)

  2. Count of employee on verge of retirement
SELECT COUNT(unique_titles.emp_no) FROM unique_titles
![image](https://user-images.githubusercontent.com/106771574/236639495-85f6caf6-46d8-4e31-ae82-5857509e74f9.png)
