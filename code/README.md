# Develop, benchmark, and improve a solution

Here are some key points on what you have to do to achieve the project.

_NB: the list below is not exhaustive :)_

You have to be able to:
- read the input on the **standard input**
- assign rides to vehicles
- calculate the score for each ride
- print a _valid_ output on the **standard output**
- use the benchmarking to evaluate the quality of your solutions

[Here](https://fr.wikibooks.org/wiki/Programmation_Bash/Flux_et_redirections) is a link where you can find details on how to work with the standard input and output.

You may use the 5 input files located in the `input_files` directory at the root of your repository.

## Delivery process

For each delivery, a script will:

1. Build your solution: `mvn clean package`
1. For each input file:
    1. execute your solution through `mvn exec:java@run` injecting the input file as stdin and storing the stdout in an output file *(our script redirects stdin to inject each file and stdout to store the results in an appropriate output file)*
    1. check the formatting of the output file
    1. check the correctness of the score

The results of the delivery will be displayed [here](../deliveries).
For each output, the result is given as follow:

- `<nb_input> ok <score>`: the output corresponding to input `nb_input` is well-formatted and the calculated score, `score`, is correct.
- `<nb_input> nok <error_code>`: the output corresponding to input `nb_input` when an error has been detected (error_code will be defined in the execution report).

## Benchmarks

Remember that the idea here is to gather factual information about the performance of your solution. We need to measure and analyse the behaviour of the different methods you propose and improve at the non-functional (_e.g._, the average execution time) level.
  
### Performance Benchmark

You must at least decompose the execution time in three: (i) _parsing_, (ii) _computing_ and (iii) _outputing_ the solution.

To compute accurate measure, you must not consider a single execution of your program, as the JVM needs time to warm-up and uses internal optimisations that might interfere with your code. 

Students are encouraged to use the [JMH](https://openjdk.java.net/projects/code-tools/jmh/) framework to address this issue and automate benchmarks.

If you are not confident enough in your skills to use JMH (actually it is more simple than it looks like), it is perfectly fine to use the following method to approximate a reasonable average execution time:

  1. Execute `N` times (`N` being in [10,100]) your code on a given dataset;
  2. For each execution, collect the associated execution time;
  3. Remove the min and max values;
  4. Compute the average execution time with the `N-2` remaining values.

But it s clear that JMH will give you way more accurate results than this method.

**It is up to you to find the right graphical representation to present your non-functional benchmark to your customer (bar chart, moustache box, point cloud, ...), and to start with, google, as often, is your friend...**

### JMH usage

[Examples](http://hg.openjdk.java.net/code-tools/jmh/file/tip/jmh-samples/src/main/java/org/openjdk/jmh/samples/) are available to help you kickstart and [understand how things work](http://blog.soat.fr/2015/07/benchmark-java-jmh-fine-tuning/).

Writing benchmarks can be difficult and [some pitfalls must be avoided](https://www.oracle.com/technical-resources/articles/java/architect-benchmarking.html). The following research paper describes clearly those pitfalls and how to avoid them. It is easily readable and understandable as really focused on a problem/solution approach.

> [Automatic Microbenchmark Generation to Prevent Dead
Code Elimination and Constant Folding](http://diversify-project.eu/papers/rodriguez-cancio16.pdf) - _<span style="font-size: 0.7em;">Rodriguez-Cancio, Marcelino, Benoit Combemale, and Benoit Baudry. "Automatic microbenchmark generation to prevent dead code elimination and constant folding." Proceedings of the 31st IEEE/ACM International Conference on Automated Software Engineering. ACM, 2016.</span>_

## On the default setup

Once your create the project into the provided github classroom, the project is already setup with a maven pom.xml file and directories:

- the pom.xml contains last dependencies for JUnit, Mockito, and JMH. It also contains an exec-plugin specific setup that enables to:
     - run the main program with `mvn exec:java@run`
     - run a JMH benchmark example with `mvn exec:exec@bench`. `bench` is the id of the configuration execution, but we use `exec:exec` so to have a proper classpath management when forking the JVM for benchmarking. You could copy this configuration and add new ids for several benchmarks to be executable separately.
- the rest of the project is some example code in the template, you should remove it.

## Roadmap of deliveries

In order to help you to measure your progression during the week, here is an example of _"ideal"_ progression:

- Monday: project setup, problem analysis, read/write with no or ultra-naive solution
- Tuesday: benchmark setup over a solution, first solution, thinking about what and how to display benchmarks, starting report no to forget things
- Wednesday: better benchmarks with better solutions, think about how to be better, demo preparation
- Thursday: demo, demo feedback analysis, improvements
- Friday: improvements, benchmark analysis (rince and repeat), report
- Saturday: triple checking before final delivery of code, report
- Sunday: report polishing, pre-christmas chill
