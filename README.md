## Objective: Test cases and Test automation 

1. Navigate to the following sample application: http://computer-database.herokuapp.com/computers
2. Test CRUD operations. 
3. In this project work I have automated basic CRUD operations, and considered only positive cases.
4. This work is UI Functional testing, not a backend or webservices test automation.


What is Tested:
---------------

1. Tested on Windows 10
2. Tested positive CRUD operations.
3. Tested on Chrome browser.
4. Tested on Jenkins (local) using jenkins script (it is not full blown CI/CD). 


What is not Tested:
-------------------

1. Negative tests.
2. Not tested on Linux OS.
3. Not tested in Docker container.


Technology stack:
-----------------

1. java 8
2. cucumber
3. maven
4. selenium
5. junit 4
6. log4j 2.11
6. windows 10 OS


Open source libraries used:
---------------------------

1. junit 4
2. chromedriver
3. selenium 3.14
4. cucumber java
5. extent reports
6. log4j
    

Patterns used:
-----------------

1. page object factory from selenium.
2. singleton pattern.


Download code:
---------------

Do git clone for downloading the project to your local machine and then import project to your IDE.

Install with [git](https://git-scm.com/downloads):
	
```sh
$ git clone https://github.com/meharlist/onesite-jenkins.git
```


Running test from Jenkins:
-------------------------------

1. This was tested in my local jenkins instance using pipeline script.

2. With few tweaks you can run this project in jenkins too.

3. Please see below images and instructions to run them in jenkins.

4. install jenkins in your windows machine (this is working in windows).

5. open the instance webpage using url (`localhost:8080`)

6. create user if it is first time.

7. then you be should landed in main page of jenkins.

8. install below plugins, to have this you need to navigate to manage plugins.


&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/manage_jenkins_01.JPG "manage plugin01")

9. naviagte to manage plugins


&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/manage_jenkins_02.JPG "manage plugin02")

10. install cucumber plugins.


&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/cucumber_plugin.JPG "cucumber")

11. Next, go to main page, click create new jenkins job.

12. click `Build Triggers`
  
13. select `Pipeline script` and copy the pipeline script from `pipeline_script_to_use.txt`, this file is in `src\test\resources\com\onesite\images` .

14. paste the script in `Pipeline script` section. make sure `use Groovy Sandbox` is checked, please see below image. 


&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/pipeline_Script_01.JPG "cucumber")


15. finally save the job.

16. to run the job, you have to click `build now`

17. you should see something like this.

&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/pipeline_build_execution.JPG "cucumber")


18. to see cucumber reports, click `cucumber reports` link as shown in above image.


19. this is how report looks like.

&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/cucumber_report_jen.JPG "cucumber")




Do's and Don't:
--------------

1. Please do not execute in Linux OS.

2. If you try running on Linux then configuration needs changes, especially with file navigation, because linux file navigation uses `//` on contrast windows uses `\\`

3. Due to point 2 your execution will fail.

4. Don't run in `geckodriver`, as we seen current issue with close and quit options in firefox driver. And I haven't find alternative to this.

5. For point 4, you shouldn't be worry if you plan to run against chrome, because I have set `chrome` as browser type in `configuration.properties`.


Cucumber feature file:
----------------------

&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/cucumber_feature.JPG "scenario tags")


Test Runner class:
------------------

&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/runner_commented.JPG "test runner")


Project Structure:
------------------

&nbsp;&nbsp;
![alt text](src/test/resources/com/onesite/images/project_structure.JPG "project structure")


Conclusion:
-----------

1. Due to time constraint few things were (as stated above) not included or tested.
2. Given few more days I would have completed things which I haven't tested.

