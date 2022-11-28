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

Using : https://github.com/ucsd-cse15l-f22/list-methods-corrected

Code receive 100%

![image](https://user-images.githubusercontent.com/114322721/204200631-4c6fccc6-4fd5-4c87-9876-b6f828655174.png)

Using : https://github.com/ucsd-cse15l-f22/list-methods-filename

code receive : 0% 

![image](https://user-images.githubusercontent.com/114322721/204201581-1a0a026e-8c81-40ef-b2b2-b384f3db8804.png)

Using : https://github.com/ucsd-cse15l-f22/list-methods-compile-error

![image](https://user-images.githubusercontent.com/114322721/204203396-a2491f26-c327-46b7-8dd2-2f94706a733d.png)

code receive : file found but compile faild.

