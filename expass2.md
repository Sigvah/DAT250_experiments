Problems
1.  tried to install derby database, gave up and installed the repo with maven
2.  Trouble with JAVA_HOME used lots of time, but fixed it by adding it to bash_profile with vim
3. Could not get main to work -fixed by doing the changes the path like instruction said.
4. lombok was a bit of a hassle, but after restarting maven with ctrl shift a "reload all maven projects" everything worked
5. Found it to be a hassle making a new project for step 6 and did not see a reason I could not do it in the same project. --Fix did that.
6. junittests worked the first time, but afterwards "checkFamiliy" test fails. No solution found


Problems finding the database - fix look to the left side in inteij where you can find "database" 
In part two the relasion person address does not work proparly. I still don't have a proper fix as you can see from the screenshot (halfbaked connection between person2 and address). I think the problem might be that I have two primarykeys in Address.

Code:
https://github.com/Sigvah/jpa_example

Experient 1
![Alt text](https://github.com/Sigvah/DAT250_experiments/blob/main/Screenshot%20from%202021-09-08%2018-07-08.png)
Experient 2
To inspect it I used intelijes database tool found on the right side, from there I entered Apache Derby, entered the path I wanted to store the database entered user: test password: test and voila I could inspect from intelij. 
![Alt text](https://github.com/Sigvah/DAT250_experiments/blob/main/Screenshot%20from%202021-09-16%2016-08-04.png)


