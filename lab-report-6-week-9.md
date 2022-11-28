# Week 9 Lab Report

## grade.sh code :

```
CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"

rm -rf student-submission
git clone $1 student-submission

cd student-submission

if [ -f "ListExamples.java" ]
    then
        echo "Cloned successtully ListExamples file found!"
    else
        echo "Clone failed.File Not Found!"
        echo "Your score is 0%"
        exit 
fi

javac ListExamples.java 2> err.txt > out.txt

if [ $? -ne 0 ]
    then
        echo "Compile faild."
        echo "Your score is 50%"
        exit 
fi

javac ListExamples.java 2> err.txt > out.txt    
java -cp $CPATH org.junit.runner.JUnitCore TestListExamples 2> err2.txt > out.txt

if [ $? -ne 0 ]
    then
        echo "Compiled successfully."
        echo "Grade: correct. Your score is 100%"
        exit 
    else
        grep -c "Error(s) Found:" err.txt > result.txt
        cat result.txt
        echo "Your score is 50%, because faild the test."
        exit 
fi
```

# Screenshots of three different.

Using : https://github.com/ucsd-cse15l-f22/list-methods-compile-error

![image](https://user-images.githubusercontent.com/114322721/204203396-a2491f26-c327-46b7-8dd2-2f94706a733d.png)

code receive : file found but compile faild.

Using : https://github.com/ucsd-cse15l-f22/list-methods-corrected

Code receive 100%

![image](https://user-images.githubusercontent.com/114322721/204200631-4c6fccc6-4fd5-4c87-9876-b6f828655174.png)

Using : https://github.com/ucsd-cse15l-f22/list-methods-filename

code receive : 0% 

![image](https://user-images.githubusercontent.com/114322721/204201581-1a0a026e-8c81-40ef-b2b2-b384f3db8804.png)



# Tracing the Script
In the first example, we will show how the test will always run if the exit code is 0. In the code, the if statement continues to run as long as the exit code is 0. This means that the condition of every test will always be true. The first thing that happened was the removal of the student-submission directory and the creation of new contents based on the current state of the link in the repository. If the cloning process was successful, then an exit code will be returned indicating that the file has been successfully cloned. If the test is not successful, it will automatically go to the other statement which returns an echo clone failed. In this case, the clone was successful, and the return code was 0. The next step is to check if the List.java repository contains a directory with the name "ListExamples.java". If the file does not exist, an exit code of 1 is returned and the echoes file is not found, resulting in a grade of 0%. In this case, the file was found, and the exit code 0 was returned. The third if statement verifies if the file is able to compile. If it is, we are given an exit code 0 and the echoes are compiled successfully, or the file is not able to be compiled. The if statement is used to check if a file is able to be compiled, and if it is not able to compile, then we use javac to check if the grade is set to 0%. We then use the cat command to send out the compilation error message. In this case, the file was able to compile, and the exit code was 0. We then move on to the next statement. The last if statement is used to check if the contents of a file are in line with the expected test result. A 100% grade is given if the contents are in line with the expected result, while a 50% grade is given if the content is not in line with the expected result.
