# Week 9 Lab Report

Grade.sh file has been provided below -

```
rm -rf student-submission

git clone $1 student-submission

if [ -f ./student-submission/ListExamples.java ]
then
    echo "Found file!"
else
    echo "File not found"
    exit 1
fi

cp ./TestListExamples.java ./student-submission
cp -r ./lib ./student-submission

cd ./student-submission

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

if [ $? -eq 0 ]
then
    echo "Successfully Complied!"
else
    echo "Compile Error"
    echo $?
    exit 1
fi

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > results.txt

echo "Test output:"
grep -i "test" results.txt
```

Screenshots of three different outputs have also been provided below - 


<img width="737" alt="Screenshot 2022-11-28 at 12 24 02 AM" src="https://user-images.githubusercontent.com/114549600/204229058-363075bd-dc96-4cac-9058-283e93bf9074.png">


<img width="766" alt="Screenshot 2022-11-28 at 12 26 08 AM" src="https://user-images.githubusercontent.com/114549600/204229337-5fe397aa-64b8-4027-9bb7-03ca35718990.png">


<img width="760" alt="Screenshot 2022-11-28 at 12 27 05 AM" src="https://user-images.githubusercontent.com/114549600/204229450-b6bbe339-0352-4497-a727-6f71a197f7ac.png">





