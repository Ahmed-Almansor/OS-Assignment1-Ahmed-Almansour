# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 29, 2026, 3:00 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account using university email
- Forked the starter repository
- Renamed the repository
- Updated student ID in SchedulerSimulation.java
- Ran the program to verify it works

**Challenges**: Git was not configured properly

**Solution**: Used git config to set user.name and user.email

**Time spent**: 1 hour

---

### Entry 2 - [March 29, 2026, 4:00 PM]
**What I did**: Studied and understood the code

**Details**: 
- Read the Process class and SchedulerSimulation
- Understood how Round-Robin scheduling works
- Observed how processes move in the ready queue
- Ran the program multiple times


**Challenges**: Understanding how threads execute step by step

**Solution**: Followed execution using output and print logs

**Time spent**: 1.5 hours

---

### Entry 3 - [April 16, 2026, 1:00 PM]
**What I did**: Implemented Feature 1 (Priority)

**Details**: 
- Added priority field to Process class
- Generated random priority values (1–5)
- Displayed priority when process enters ready queue

**Challenges**: Finding the correct place to add the new field

**Solution**: Added it after existing variables and tested output

**Time spent**: 1.5 hour

---

### Entry 4 - [April 16, 2026, 2:30 PM]
**What I did**: Implemented Feature 2 (Context Switch Counter)

**Details**: 
- Added static counter variable
- Incremented counter before starting each thread
- Displayed total context switches at the end

**Challenges**: Knowing when to increment the counter

**Solution**: Placed it before currentThread.start()

**Time spent**: 1.5 hour

---

### Entry 5 - [April 16, 2026, 4:00 PM]
**What I did**: Implemented Feature 3 (Waiting Time)

**Details**: 
- Added creationTime and waitingTime variables
- Calculated waiting time using system time
- Printed summary table at the end of execution

**Challenges**: Correct calculation of waiting time

**Solution**: Used System.currentTimeMillis() and verified results

**Time spent**: 2 hours

---

## Summary

**Total time spent on assignment**: [7.5 hours]

**Most challenging part**: Understanding Round-Robin scheduling and thread execution

**Most interesting learning**: How threads simulate CPU scheduling

**What I would do differently next time**: Start earlier and test each feature more frequently
