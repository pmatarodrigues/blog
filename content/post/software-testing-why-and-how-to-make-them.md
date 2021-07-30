+++
authors = ["Pedro Mata Rodrigues"]
date = 2021-07-29T23:00:00Z
draft = true
excerpt = "ime is scarce and everything must be done at the speed of light, there's no time for testing. the thing is, the time you spent writing tests now, is the time you'll save later."
hero = ""
timeToRead = 2
title = "on software testing"

+++
it's way harder to find a nice tutorial about testing, in comparison to tutorials about tools or languages or frameworks, and that's maybe because nobody is looking for ways to improve their ability in writing automated tests.

the truth is that we all want to get the job done, especially when working on side projects or on small companies, where getting the job done is much more important than the quality of the code we write.

I've met a lot of software developers that do not write any tests, despite this being **one of the best ways for building maintainable software**. I understand them, because I was one of those that can't waste time on something that will not be on the final product.

time is scarce and everything must be done at the speed of light, there's no time for testing. the thing is, **the time you spent writing tests now, is the time you'll save later** fixing bugs and rewriting your old code.

![](/images/aint-nobody-got-time-for-that.gif)

# but why should you write tests?

* **tests are not for now**

tests should not be written just because of your current features, but with the thinking that you'll have to add many more and those can break your previous code. this step will make it faster and easier to check that those changes do not break anything.

* **they faster and more efficient than manual tests**

it's pretty hard for a developer to remember every feature that needs to be tested before marking that code as safe. this is especially true when it's something that's been worked on for the same people for a long time, which means new developers will have a hard time trying to work on that without breaking old things and without requiring manual testing by the old developers.

* **improve code quality**

if every function and class need to have unit tests, developers must weight their decisions and think about architecture and code structure before starting to code.

* **minimize bugs and avoid risks**

bugs should definitely not make it to production. if this happens, the cost of fixing it is many times higher than the cost of fixing it on implementation. of course this is not at all easy to find, but with automated tests the possibility of finding implementation bugs is higher than without them.

# conclusion

tests have a fundamental part on software developing, not only because of performance improvements and code quality and stability, but also because of long-term cost and risk reduction.

and don't forget: tests are supposed to fail at first, that way you know some change you implemented is not working as supposed and is changing how others features are working.