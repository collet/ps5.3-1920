# Develop and improve a solution

Here are some key points on what you have to do to achieve the project.

_NB: the list below is not exhaustive :)_

You have to be able to:
- read the input file on the **standard input**
- assign rides to vehicles
- calculate the score for each ride
- print a _valid_ output file on the **standard output**
- use the [benchmarking](../bench/README.md) to evaluate the quality of your solutions

You may use the 5 input files located in the `input_files` directory at the root of your repository.

## Delivery process

For each delivery, a script will:
1. Build your solution: `mvn clean package`
1. For each input file:
    1. execute your solution: `mvn exec:java` 
    1. check the formatting of the output file
    1. check the correctness of the score

The results of the delivery will be displayed [here](https://www.youtube.com/watch?v=dQw4w9WgXcQ).
For each output, the result for each file is given as follow:

- `<nb_input> ok <score>`: the output file for input `nb_input` is well-formatted and the calculated score, `score`, is correct.
- `<nb_input> nok 1`: the output file for input `nb_input` is well-formatted but the calculated score is incorrect.
- `<nb_input> nok 2`: the output file for input `nb_input` is not well-formatted.

## Roadmap of deliveries

In order to help you to measure your progression during the week, here is an example of _"ideal"_ progression:

- Monday: TODO
- Tuesday: TODO
- Wednesday: TODO
- Thursday: TODO
- Friday: TODO
- Saturday: TODO
