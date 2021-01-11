# Elements of Programming Interviews (C++) 
Notes for EPI (Version 2.0.0)

## The EPI editorial style 
Problems: 
1. Establish context (e.g, real-world scenario)
2. State the problem to be solved (does not specify detailed constraints, input format, etc...)
4. Give a short hint (only read this if stuck)

Solutions: 
1. Develop simple brute-force
2. Aanalyze brute-force to get intution for inefficiencies and where to improve
3. Develop more efficient algorithm 
4. Apply program to concrete input
5. Give code for key steps
6. Analyze space and time complexity
7. Outline variants - problems whose solution is similar to the solved problem 

## Recommended algorithm books (for those who require prerequisite knowledge)
Algorithms by Dasgupta, et al.  ("succinct and beautifully written")
Introduction to Algirhtms by Cormen, et al. ("amazing reference")           

## Study guide 
Hackacthon (weekend entirely devoted to preparation)            
Finals cram (one week, 3-4 hours a day)         
Term project (four weeks, 1.5-2.5 hours per day)        
Algorithms class (3-4 months, 1 hour per day)

## The interview lifecycle
1. Identify companies you are interested in. Ideally find people you know at these companies. 
2. Prepare resume. Submit through personal contact (preferred)
3. Perform phone screening (question-answer with engineer). Might require submitting code via shared document. Don't take this casually - can be very challenging.  
4. Go for an on-site interview. One-on-one interviews with engineers and managers, and a convo with your HR contact. 
5. Receive offers. Usually starting point for negotiations. 

## The resume (this advice makes more sense for full-time positions than internships, or really sought-after internships)
1. Have a clear statement of your objective (tailor resume for a given employer)
2. The most important points (the differentiating points) should come first. Logical order comes second to this principle. 
    - list significant class projects, standardized test scores (if exceptionsal), etc... 
3. The resume should be high-quality: no spelling mistakes, good formatting, capitilzations, numberings, correct grammar/punction. Use few fonts. PDF is preferred.
4. Concact information, LinkedIn profile, URL to personal homepage with examples of work. 
5. If you can work at company without special processing (e.g., green card) make note of it. 
6. Have friends review your resume. It is better to write something quickly and then refine based on feedback. 
7. Resume does not have to be one page, two pages is appropriate (more than two is likely not). This advice does not apply to juniors/first internship. 
8. Prefer not to see a list of hobbies/ECs unless they are different "olympic" or high level achievements

## Mock interviews 
Get a friend. Code on paper. Give hints when stuck. Record and review session. Give feedback both positive and negative.        

## Language review
C++ best practices: 
- follow Google's C++ style guide: 
    - input arguments are either values or const references. 
    - use pointers to pass output arguments to functions
    - use `deque<bool>` for Boolean arrays, `vector<bool>` is not an STL container. 

Review the [Google C++ style guide](https://google.github.io/styleguide/cppguide.html) 

# Strategies For A Great Interview 
A typical one hour interview will be 5 minutes of introduction/questions about resume, 5-15 minutes of questions on basic programming concepts. The core of the interview is one or two detailed design questions where candidate will present a solution. 

## Aproaching the problem 
Clarify the question
- good way to clarify is state a concrete exmaple of the problem (example case)
- ask interviewer about complexity they would like, they might refuse but no harm in asking and you may get some clues. 

Work on concrete examples            

Spell out the brute-force solution:
- good idea and shows ur problem solving process 
- can be detrimental if it takes long time to describe the brute-force approach

Think out loud: 
- helps u stay on track 
- gives interviewers ability to guide you in right direction

Apply patterns: 
- good data structure, general algorithm technique, etc.. 

##Presenting solution: 
- once you have algorithm it is important to present it in clear manner. 

Libraries: 
-  don't reinvent the wheel (unless asked to)

Focus on the top-level algirhtm: 
- for example use BST and implement it later
- add TODO comment to portions u want to come back to 

Manage the white board: 
- you will likely use more space than you expect

Assum valid inputs          

Test corner cases           

Syntax 
- don't have lots of syntax erroes (a few small ones is ok)

Memory management 
- avoid memory management operations altogether

## Know your interviewers & the company 
TODO

## General conversation 
TODO 




