# Technical Report


## Contents

Your report must be **no more than 10 pages** (including all appendices and bibliography), delivered as a `PDF` file named `report_X.pdf` at the root of your repository, `X`being the name of your team. 
Font and margins should be _reasonable_ (_i.e_, if you have to cheat on margins and font size to fit the 10 pages limit, you are probably doing it wrong).

Executive summary:

 - A first page containing project information, your team name and describes the composition of your team (1 page);
 - A technical section describing your implementation (up to 6 pages);
 - A business section describing the obtained results (up to 3 pages);
 - A project section describing your organisation in the project (up to 1 page);
 - A conclusion (up to 1/2 page)

Hints: 

  - Report can be written in English or in French;
  - Review your report before delivering it (grammar, syntax);
  - If you can take one of your sentence and write it in another report, please delete it, this is _noise_, not _signal_.
  - Be _pithy_, and state things that adds value to your project. 
  - Do not _describe_ your code, _defend_ it. We know that there is a class `C` that contains a method `m`, we can read the code. Your report must answer to these questions:  "_Why do we need a method `m` in class `C`?", "What were the other alternatives?", "Why did you chose this one?"_. 
  - Take a step back. Do not rush your report 10 minutes before the deadline. This kind of exercice is easy to fail, being able to defend your code is *way more complicated* than you think. Take time.


## Subsections

We list here points that should be described (when applicable) in your report. This is not an outline, you are free to organise these elements in any way, but we do need to retrieve these information **clearly stated** in your report.

### Technical description

  - Describe the technical difficulties associated to the implementation (Warning: reading a text file or conforming to a legacy specification is not difficult);
  - How modular/extensible is your code?
   - Can we change the input / output file format?
   - Is it possible to easily replace an algorithm by another one?
   - How easy it is to add a new optimisation metric?
   - What is the best thing in your codebase (_e.g._, small classes, easy to swap algorithm, well-tested)?
  - What is the worst thing in your codebase (_e.g._, huge classes, not-so-easy to swape algorithm, poorly-tested)?
  - What are the pros/cons of using an object-oriented approach in this case?
  - What would be the differences if your project had to be developed in a procedural language (_e.g._, C)? 
  - What are the performance bottleneck in your implementation? How to optimise them?

### Business analysis

  - What are the pros/cons of each approach from a business point of view?
  - how well/bad did you perform on the provided datasets? 
  - How does your execution-time evolve? Can you guess your execution time for 10 millions rides? Can you identify a function that describes your execution time, given a number of rides and/or cars?
  - Explain the benchmark you provide to back-up your claims.
  - Discuss about the bias introduced by the provided datasets.

### Project management

  - Explain how you manage your project during the full-time period;
  - Rate each of the following criteria on a [0,5] scale:
    - Task management (_e.g._, kanban/github issues);
    - Tests;
    - Object-oriented quality;
    - Releasing process;
    - Documentation.
  	- _(Justify in the text why you decide to give such auto-evaluation to your group)._
  - If you had `400` effort-points to spread across your 4-people team, how would you spread them?  
  	- A `100/100/100/100` points repartition means that each member of the team has provided the exact same effort in this project.
  	- A `400/0/0/0` dispatch means that only one member of the team worked on the project.
  	- Use only numbers that can be divided by `5` or `10`, no need for things like `102.7598`.


### Conclusions

  - What did you learn in this specific project?
  - Which knowledge did you use from the other courses followed this semester?
  - What are the _lessons learned_ by your team in this project?


