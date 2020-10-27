# Stress-Testing-Using-Python


Stress testing is a software testing activity that determines the robustness of software by testing beyond the limits of normal operation. Stress testing is particularly important for "mission critical" software, but is used for all types of software. Stress tests commonly put a greater emphasis on robustness, availability, and error handling under a heavy load, than on what would be considered correct behavior under normal circumstances.

A collection of scripts to generate common competitive programming testcases on Linux Operating System.



What is Stress Testing?


Have you ever been in sitauation where you have written a state-of-the-art algorithm for some task but it your code is generating incorrect output? If yes, have you ever felt lazy to manually generate test cases to detect the bug in your code? Well stress testing solves this very problem. The idea is that instead of generating test cases manually, you write a simple brute force solution that solves the same problem that you are trying to solve with your state-of-the-art algorithm and then leave it to your computer to randomly generate test cases till the ouptuts of both programs don't match.

How to use

Write a bruteforce solution, compile it, and name the executable brute.
Compile the solution you want to stress-test and name the executable A.
At the end of gen.py, add your code to generate desired test cases.
Let the stress testing begin! Run test.sh and let it do the hard work for you. Once it finds a mismatch, it will print "Wrong Answer" on your screen and the failed testcase can be found in testcase.in. Your program's output on this test case can be found in the file A.out and your bruteforce solution's output can be found in B.out

What does each file do?

gen.py : Use this to generate random testcases by invoking the various functions provided
    check.py : Script used by test.sh to check if outputs of the two executable programs match.
    test.sh : This shell scripts creates a random testcase, runs two exectuables simultaneously on the random testcase and checks if the outputs match. It repeats this for 10,000 random test cases.


Note: Supports Linux Operating System only
