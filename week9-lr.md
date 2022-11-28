# Week 9 Lab Report

## Grade.sh File -

```
# Create your grading script here

set -e

rm -rf student-submission
git clone $1 student-submission 

cp TestListExamples.java student-submission

cd student-submission

if [[ -f student-submission/ListExamples.java]];
then
    echo "Found ListExamples.java!"
else 
    echo "File ListExamples.java not found!"
    exit 1
fi

set +e  

cp ../TestListExamples.java ./

javac ListExamples.java
javac TestListExamples.java

if [[ $? -eq 0 ]];
then 
    javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java
    java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
else
    echo "Files can't compile!!!"
    exit 2
fi

java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > grades.txt

if [[ $? -eq 0]];
then
    echo "Tests Passed!"
    exit
else
    echo "Tests not Passed!"
    exit 3
fi
```

