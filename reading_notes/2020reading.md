# 2020 Reading

Links to articles I read in 2020 with a few notes to remind me of the topic.

## January

[The Fear Cycle](https://www.michaelnygard.com/blog/2015/07/the-fear-cycle/)

["Rely on" vs "Work with"](https://blog.atomist.com/rely-on-vs-work-with/)

[Growing our team with retrospectives](https://blog.plaid.com/growing-our-team-with-retrospectives/)

[Who are you trying to impress with your deadlines?](http://jatins.gitlab.io/me/why-deadline/)

[I don't want the best](https://blog.jessitron.com/2020/01/09/i-dont-want-the-best/)

## February

[Strong Opinions, Weakly Held](https://medium.com/@ameet/strong-opinions-weakly-held-a-framework-for-thinking-6530d417e364)

- "Allow your intuition to guide you to a conclusion, no matter how imperfect — this is the ‘strong opinion’ part. Then –and this is the ‘weakly held’ part– prove yourself wrong. Engage in creative doubt. Look for information that doesn’t fit, or indicators that pointing in an entirely different direction. Eventually your intuition will kick in and a new hypothesis will emerge out of the rubble, ready to be ruthlessly torn apart once again. You will be surprised by how quickly the sequence of faulty forecasts will deliver you to a useful result."
- Reasons it works well: "1. Leverage your team's collective wisdom. 2. Overcome your biases. 3. Have an on-demand decision."

[Why do we fall into the rewrite trap?](https://www.justindfuller.com/2020/01/why-do-we-fall-into-the-rewrite-trap/)

- "It's harder to read code than to write it." Don't rewrite because you don't understand it.
- Prefer refactoring over rewriting.
- Once you understand confusing code, refactor to make it easier for someone else to understand.
- Refactor before making other changes. "Make the change easy (warning: this may be hard), then make the easy change." -Kent Beck
- Only rewrite when better functionality is needed.

[Eradicating Non-Determinism in Tests](https://martinfowler.com/articles/nonDeterminism.html)

- Non-deterministic tests are useless and ruin the test suite. Can cause you to ignore test failures.
- Keep tests isolated: rebuild state on each or cleanup when done.
- Asynchronous calls can utilize callbacks or polling.
- Remote services can use Test Double or Contract Tests.
- Time based calls should be wrapped with a clock stub. Same for resource limiting - wrap the calls with a stub.

[Optimizing for iteration speed](https://erikbern.com/2017/07/06/optimizing-for-iteration-speed.html)

- "Two-week or three-week sprints are mini waterfall and sacrifices a lot of flexibility for the purpose of providing external stakeholders a bit more predictability."
- "Splitting up tasks into small, incremental pieces and shipping each of them separately is the fastest way to deliver value."
- Teams and individuals should be cross-functional, able to complete a full-stack task themselves.

[The art of reviewing code](https://blog.usejournal.com/the-art-of-reviewing-code-e10a3a830a2e)

- Trust each other to timely and thoughtfully review code.
- Be flexible in how you review code - understand the priority and audience.
- Guide rather than tell to allow for growth.

[How to write usefully](http://paulgraham.com/useful.html)

- An essay should make correct statements. It should tell something important that some people don't already know or haven't yet put into words.
- Don't publish until you feel confident in the writing. Proof-read to get to that point.
- Write about something important to you that you think about often.

[The SSCCE](http://sscce.org/)

- Short, Self Contained, Correct (compilable), Example
- Prepare example code that follows this format for others to see and help out.

[test && commit || revert](https://medium.com/@kentbeck_7670/test-commit-revert-870bbd756864)

- if tests fail, changed code is reverted.
- encourages very small changes.

## March

[Programming Bottom-Up](http://www.paulgraham.com/progbot.html)

- "When you work bottom-up, you usually end up with a different program. Instead of a single, monolithic program, you will get a larger language with more abstract operators, and a smaller program written in it."

[Excuses](http://blog.cleancoder.com/uncle-bob/2017/12/18/Excuses.html)

- double entry bookkeeping is similar to test driven development
- excuses that an accountant wouldn't use shouldn't be used for writing tests

[Numeric Separators in TypeScript](https://mariusschulz.com/blog/numeric-separators-in-typescript)

- Typescript 2.7 introduces underscores in numeric literals i.e. 4_000_000

[Declare what you need, not what you get](https://blog.atomist.com/declare-what-you-need-not-what-you-get)

- Typescript lets you pick specific properties from a type to store into another type. This lets you state exactly which properties you actually need.

[Programming Isn't Manual Labor, But It Still Sucks](https://mashable.com/2014/04/30/programming-sucks)

- meandering rant and analagies galore about programming life.

[Why Scaling Agile Doesn't Work](https://www.youtube.com/watch?v=2zYxWEZ0gYg) (video)

- focus on value, not cost
  - estimated cost is worthless compared to finding out if people will actually use the software
  - quickly deliver the things that provide the most value (other requirements can be delayed)
- small feedback loops to validate assumptions
  - you can get value from software before you finish building it

## April

[Incorporate the Modern World Into the Software’s World](https://blog.atomist.com/modern-software-world)

- all code is technical debt
- utilize existing tools and frameworks

[Letting tools make choices](https://www.jackfranklin.co.uk/blog/letting-tools-make-choices)

- much time can be wasted by fussing over project configuration when it doesn't really matter

[My life as a Code Economist (Four Questions)](https://ericsink.com/articles/Four_Questions.html)

- "Every time you fix a bug, you risk introducing another one."
- Determine these four things about each bug: Severity, Frequency, Cost, Risk
- Understand market windows and expectations
