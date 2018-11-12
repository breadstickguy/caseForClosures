# caseForClosures
A lesson on closures and some of their use cases

The Case for Closures Lesson Plan:

Overview
In this lesson we will cover the basics of closures and discuss a few practical examples of their uses. 

Summary: Complete activities 01-06 in Unit

Instructor Priorities
Make sure that students tackle these activities in pairs. This is a complex topic and conversation amongst students is critical for learning!
Reinforce that this is a very technical topic and that we will only be scratching the surface of the true usage of closures. The focus is on exposure and high level understanding.
Ensure that students leave with a conceptual understanding of a closure and at least can explain at least one popular use case.

Class Objectives
Understand what a closure is and be able to define it
Explain at least one practical use for a closure
Give students exposure to working with a closure and nested scopes


0. Instructor Do: Welcome Students
Welcome the class and introduce the topic of closures
Keep the initial conversations quick and light. Let all the students know that this is a complex but critical topic. It’s perfectly OK to be confused. The goal is exposure and practice, not complete mastery of the topic

1. Instructor Do: Introduce Closures (0:10)
Ask the students if anyone has heard of a closure or can provide a definition. If there are volunteers, let them share what they know. If there are no volunteers, have the students pair up and research closures for 3-5 minutes. Share their findings!
Offer this definition of a closure: “A closure is a function and its surrounding lexical scope.” This is a technical definition, but doesn’t explain how to use one.
Explain that when you create a function within a function, a closure is created. The inner function has access to everything within the scope of the outer function and can read/write to that scope. The power of a closure comes from the fact that the inner function remembers the environment in which it was created.
Use the code in 01-ClosureExample as a guide for conversation
Be careful to keep the conversation and explanation high level. This is a deep topic and you can get off topic and off track very quickly.


2. Partners Do: Build a closure! (0:15)
Students will be building a simple closure following the example provided before
Slack out the following instructions and folder to the class
	
Instructions:
Build a closure from scratch that has the following features:
At least 3 outer scope variables
At least 1 inner function that access the outer scope
At least one outer scope variable must be modified by an inner function
Use the comments and previous example as a guide
Folder: 02-Build a closure/Unsolved

	
3. Everyone Do: Review Build a closure (0:05)
Open up the 02-Build a closure/Solved folder and use the file there to guide discussion
Emphasize that with this activity, there isn’t one right answer. The keys are that students were able to properly build out the functions and understand the scopes
Answer any questions before moving on

4. Instructor Do: Execution Context and closures (0:15) HIGH
This is a point in the lesson plan that is worth spending extra time on if needed. Take your time as you walk through execution context with your students. Reassure them that this is complex and takes lots of practice to fully understand.
Open up the file in 03-Execution Context and step through the code with the students
Explain that Javascript is “single-threaded” which means that only one command can be processed in the code at a time. This means that as we create inner functions and multiple scopes, the execution context is changing as the program is running. Don’t forget to mention that one context doesn’t have to complete before another context can start! When this happens, the current context is suspended and another context picks up. The suspended context may pick up at a later time in the code. 
Use the browser debugger and place some breakpoints into the functions. Step through the functions and the call stack with the students. This is an option step, but can provide some additional clarity to how the execution context works. 
If you decide to use the debugger to step through the functions, make sure you Step Into the function calls. This will make sure that you demonstrate everything line by line.
Again, reassure the students that it’s ok that everything doesn’t make 100% sense at this point. We are focused on high level understanding.

5. Instructor Do: But, why closures? (0:15 - 0:20) HIGH
Up to this point, we’ve talked a lot about theory and what closures are. We haven’t discussed much of what they “do” at this point. We going to discuss two important features of programming that closures can provide for us, that aren’t provided by Javascript natively. Data privacy and namespaced functions are very useful and critical components of programming as a whole, but are absent from Javascript due to it’s lack of OO tools. However, we can still take advantage of these powerful patterns without an OO toolset. Closures to the rescue!
Open up 04-DataPrivacy and look at the file with the class.
Demonstrate the functionality and briefly define an IIFE. Offer this definition or use your own if you prefer: An IIFE is a function expression that’s invoked immediately upon definition. It can be used to protect against polluting the global scope while simultaneously providing access to public methods within and prevent hoisting within code blocks. We use an IIFE to get access to the methods and data without having to assign the function to a variable
Answer questions are you go. Once you’ve covered 04, move onto 05
Open 05-Namespacing in your browser and demonstrate the functionality
Ask the class for definitions of namespacing, if they have any have them share. After that offer this definition: “Namespacing is creating a declarative region that provides scope to named functions and variables, allowing reuse of those names”
Feel free to reference https://en.wikipedia.org/wiki/Namespace and use examples from it. The surname example is a great example of reuse.
Once you have covered the concept of namespacing, revisit the file in 05-Namespacing. Show how the methods defined in our returned object can be accessed outside the closure, but still have access to the variables defined within. Show the class how the private method cannot be accessed by anything other than the containing closure.
Answer questions as needed, reminding everyone that these are complex topics and it’s perfectly OK to feel a little lost. Move onto the final activity once all questions have been answered

6. Partners do: Closure Calculator (0:20)
Slack out the starter file found in 06-Calculator/Unsolved along with these instructions
	
	Instructions:
With a partner and using the comments within the file as a guide, create a simple calculator with public and private functions along with a private data point
Be prepared to share your code with the class!

It’s very likely there will be a number of questions with this activity. Make sure that the TA’s and yourself are available and engaging with students

7. Everyone Do: Review Closure Calculator (0:10)

Ask the class for examples on how they tackled this challenge. If there are any volunteers, have them share their code with the class.
Open up the file in 06-Calculator/Solved and demonstrate the functionality
Walk through the example code step by step and answer questions as needed. Keep in mind, these are fairly simple examples of complex topics, encourage students to do more research and dive in deeper but that the goal for today is conceptual understanding.



	

