
# Introduction to LazTech Skill-stack

## Preface (Nothing valuable here)

Welcome to Laztech, a dynamically developing astrophysics group led by **Full Professor Alex Lazarian** in University of Wisconsin - Madison.

The **Velocity Gradient Technique (VGT)** is a prospective technique to __map the magnetic field of the universe__ with less cost and higher accuracy.

Don't worry. No one's gonna test you about astrophysics or VGT, nor should you think that having Physics/CS/Statistics background alone can achieve great things on your own. The thing is this: you might need to understand each of them for a little bit, and learn the rest iteratively and cooperatively with our nice yet highly efficient and demanding team members. You will learn a lot -- not just hard skills, but also how to do science like doing a business.

This is the friendly documents that introduce to you what we're doing and how we do it. You're welcome to selectively read the contents at your own pace. 

I know it's hard, but you're gonna grow yourself fast to surprise yourself. Believe it or not, it's great.

## Read from here

1. Read [Get Started in LazTech Group](https://www.overleaf.com/9279691msypmpcjnpqp#/33470921/). The essential basics of physics is stated here. Make sure you read this. Here are several questions:
   1. What is VGT? Can you explain it in theory and algorithm?
   2. Can you run the code without error? Why?
   3. What's the code talks about? What's the result?
   4. How long did it take? Can it be improved?

2. Install: (detail will post later)
   1. **Julia (0.6.4, and 1.0.0), Python.** Make sure you understand: Basic Julia syntax. Matrix operation. Install/Call Julia module. Call python module. Some libraries in Julia: `HDF5`, `Stats`.Some libraries in Python: `numpy`, `matlibplot`, `astropy`.  (Some questions will be throw later)
   2. **Github**
   3. **Anaconda (prefereably 2), Jupyter Notebook / Jupyter Lab**. This is a great tool that will accelerate your workflow. Besides, @Mike will post some tutorials using the Jupyter Notebook. (If you have trouble install, you can try use these: [Julia Pro](https://juliacomputing.com/products/juliapro.html),  )


3. This week paper:

- [Velocity Gradients as a Tracer for Magnetic Fields](https://arxiv.org/abs/1608.06867)

- [Tracing interstellar magnetic field using velocity gradient technique: Application to Atomic Hydrogen data]( https://arxiv.org/abs/1701.07944)

- [Synchrotron intensity gradients as tracers of magnetic field](https://arxiv.org/abs/1701.07883)



## Questions 

or Assignments ...? You should spend sometime to review these. These are not core in the research, but would be better if you actually know how to do it safe, fast and accurately.

### Q1 [Simple]: Write a Julia program that reads all the HDF5 files from a directory, and print out file information. 

Function prototype looks like roughly: `function openHDFFiles (directoryName)`, and you can call the function like this: `openHDFFiles("path/to/some/directory")`. But you can do whatever you want. 

When you done the function writing, download some HDF5 files from google. You can tell us to send you some, but it's good that you explore some too.

#### YouNeedToKnow

1. Julia internal command to change directory (maybe not used in the function)
2. How to call python library from Julia
3. Python library function `glob` to grab all things in a directory
4. HDF5 function to show file)

#### Further Question:

1. (**Exception Handling**) How do you prevent the program from interruption when some operation throws exception (Hint: `try-catch ` statement would help you). This is useful when you write a big, overnight program and you don't want the program to stop, but some times things are not going well. (Also, how will `try-catch` influence the performance?)
2. (**Profiling**) How do you print the time of each HDF5 file being read? (Hint: `@time` directory will help you). How do you time the entire for loop? The entire function? What will the output look like? **What tool** can you use to actually see how many times are spend on each line, how many memory is being allocated? **Visualize them!!!**.
3. (**Multiple Return Value**) Make the function return these information: (1) total opened file numbers, (2) every file's size. You should call the function like this: ` filenumbers, filesize = openHDFFiles("path/to/some/directory")`. How should you get filesizes and store them? (Hint: `push!(array, element)`) How should you write the return statement? (Hint: use tuple:`return (filenumbers, filesize_array)`). 
4. (**Coding Style**) There are some general coindg styles ([Google-Java-style](https://google.github.io/styleguide/javaguide.html), [Julia-style guide](https://docs.julialang.org/en/v0.6.2/manual/style-guide/)). Just look through them a little bit. Don't spend too much time on this because the ultimate goal for us is that **your code should be: readable, easily-understood, easy to change, easy to be called by your member**. That's it.



**Q2 [Simple]**: Use Jupyter notebook