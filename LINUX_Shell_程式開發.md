#
```
Complete Bash Shell Scripting [Video]  [April 2020]
By Narendra Kumar Reddy Polu
https://github.com/packtpublishing/complete-bash-shell-scripting-

1.	Introduction
2.	Basics of Bash Shell Scripting
3.	Filter Commands: grep
4.	Filter commands:cut
5.	Filter commands: awk (Part-A: awk as a command for shell scripting)
6.	Operations on Strings
7.	Input and output Commands
8.	Arithemetic operators for Shell Scripting
9.	test command, commands chanining and conditional statements
10.	Scheduling jobs with at and crontab
11.	Loops and Loop control statements: Part-1
12.	Working with remote Servers: Part-1
13.	Loops and Loop control statements: Part-2
14.	Functions
15.	Complete printf command in one video
16.	Arrays
17.	AWK Command and AWK Scripting
18.	Complete sed command
19.	Real Time Practice (Low Level To High Level)
20.	Windows Subsystem for Linux
```

# 14.	Functions  函數開發與使用技術
```
#!/bin/bash


read_inputs()
{
  read -p "Enter first num: " num1
  read -p "Enter second num: " num2
}

addition()
{
  sum=$((num1+num2))
  echo "The addition of $num1 and $num2 is: $sum"
}

subtraction()
{
  sub=$((num1-num2))
  echo "The sub of $Num1 and $num2 is: $sub"
}


read_inputs
addition
subtraction
```
```
#!/bin/bash
define_variables()
{
 local x=6
 echo "$x"
}


y=$(define_variables)
echo "The y value is: $y"
```
```
# Document-httpd-info.sh
#!/bin/bash
httpd_v=$(httpd -v 2>&1 | awk -F '/' 'NR==1{print $2}' | awk '{print $1}')
httpd_s=$(systemctl status httpd | grep Active | awk '{print $2}')
httpd_p=$(cat /etc/httpd/conf/httpd.conf | grep ^Listen | awk '{print $2}')
echo "The httpd version is:  $httpd_v"
echo "The current status of httpd is: $httpd_s"
echo "The port for httpd is: $httpd_p"
```
