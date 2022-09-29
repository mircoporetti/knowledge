
XP approach for driving the development by testing with the goal of clean and simple design.
With TDD the focus is on the requirements. It’s about design and development, not simply testing or coverage.

TDD != Test First -> TDD is an iterative process based on needs not on already thought solutionsProcess:
* RED: Write a test that fails
* GREEN: Create the minimum code to make it pass
* REFACTOR: Remove duplication and improve your code without changing its behavior

TDD lets the design emerging exploring a problem iteratively and incrementally.
It is a tool that gives us feedback on the quality of the design. 
If the tests are difficult to write, the design is probably poor.

## How tests should be
* Tests express intent
* Focus on business requirements
* Tests not coupled with production code
* Tests should be easy to understand
* One problem for every broken test (TDD by Example) -> rewrite tests that are coupled and that can be broken for the same reason -> design!

## Outside in or Inside out
Choose a test that teach you something valuable and that you are able to write (TDD by Example).Start from the most obscure and valuable part of the problem.
It’s not a fixed rule but a general suggestion. Personally I usually go outside in and then I jump into more detailed tests based on the complexity of the problem but it happens that I start from inside if I recognize that there is a clear aspect of the problem that is more complex or interesting.

## Suggestions
Start from a todo list of requirements -> tests
Not implement new tests for a new class but a new test for a new requirement.Tests the exported stable module, not every single class (they are details and will change frequently)
Stay simple. Be ready for new requirements

When code is simple? (XP Explained)
* All tests green
* Express intent
* No duplication
* With minimum number of elements.

## Mocks
Mocks are a powerful tool used for controlling the behavior of a component inside your test.They are helpful in some situation but they can be abused and become a smell.
When the test is full of mocks probably the design is poor. If I think about the reasons I recognize mainly 2 scenarios:
* Even if you practice TDD you can fall into the trap of thinking about the structure of the classes before or while writing the test. This is a common mistake and I think that 99% of devs experience at some point especially at the start of the TDD learning process;	
*  Mocks are often a way to be able to write tests on an already existing poor design without spending time on		refactoring.
If you focus on requirements and not on classes when writing tests, likely you will tend to mock less. Mock boundaries if needed!

## Thoughts
TDD HELPS/DRIVE you in building a simple design but at the end YOU are the responsible of good or bad design.
You need design knowledge especially for refactoring to really achieve simple design.
Even if you don’t use TDD as your “go to” approach, having some experience with it will help you in making better design decision when you have to do that in your daily work.
It will helps you in recognizing smells when you need to write tests for an existing code because if the design is bad the tests will be difficult to write (and vice versa).

### References:
[Clean Coder - TDD Harms Architecture](https://blog.cleancoder.com/uncle-bob/2017/03/03/TDD-Harms-Architecture.html#:~:text=Yes!,architecture%20%E2%80%93%20TDD%20or%20no%20TDD)

[Clean Coder - When to Mock](https://blog.cleancoder.com/uncle-bob/2014/05/10/WhenToMock.html)

TDD by Example

XP Explained

