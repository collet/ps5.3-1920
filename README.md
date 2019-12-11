# Final Project PS5.3

  * Timeframe: 16/12/2019 → 22/12/2019
  * Staff: Philippe Collet, Mathias Cousté, Johann Mortara

## Pedagogical Objectives

  1. Integrate a project framework with legacy artefacts that are not under your control;
  2. Improve your _programming-in-the-small_ skills;
  3. Deliver as fast as possible; 
  4. Discover continuous integration; 

## Project Summary

Your client, Hubert, TODO

  - [Understand the subject](./subject/readme.md)  
  - [Develop and improve a solution](./code/readme.md)
  - [Benchmark your code and the different solutions you provide and improve](./bench/readme.md)  
  - [Write a report](./report/readme.md)

## Timeline & Deliveries

  - Monday:
    - 08:00: Kick-off presentation (amphitheater)
    - 10:00: All teams declared __properly__ in GitHub Classroom
    - 20:00: Automated clone/compile/exec for tag `REL1`
  - Tuesday:
    - 13:15: Q&A (amphitheater) ???
    - 16:00: Automated clone/compile/exec for tag `REL2`
  - Wednesday: 
    - 16:00: Automated clone/compile/exec for tag `REL3`
  - Thurdsay:
    - During the day: Demonstrations
  - Friday: 
    - 12:00: Automated clone/compile/exec for tag `REL4`
  - Saturday:
    - 18:00: Automated clone/compile/exec for tag `FINAL`
  - Sunday:
    - 18:00: Automated retrieval of report (tag `REPORT`)

## Technological Stack

  * Version control: Git (+ github classroom)
  * Programming language: Java 11
  * Unit tests: JUnit (4.12, 5.5)
  * Benchmarks: JMH

## Contact

We use Slack for discussions (strict "no email" policy), particularly the `#si3-ps5` channel. Use the public channel for questions/remarks related to the project, or direct message for questions specifically related to your group.

## Evaluation

  - Code: 30%
  - Delivery / Execution: 20%
  - Demonstration (Thursday): 20%
  - Report: 30%
  
## Frequently Asked Questions

> Will the input file always be valid?

Yes for the automatic referee, but you could create you own files for benchmarking purpose and then error should be yielded. Anyway start simple.

> Do we need to parse entirely the input file?

Yes. You won't have all the information otherwise.

> Do we have to test our code?

Yes. Obviously. Unit testing is expected and required. 

> Do we have to use git?

Yes.

> Will the code be evaluated?

Yes. Especially the complexity, clarity, and respect to OOP principles will be evaluated.

