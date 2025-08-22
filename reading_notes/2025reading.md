# 2025 Reading

Links to articles I read in 2025 with a few notes to remind me of the topic.

## January

[Please Don't Force Dark Mode](https://iamvishnu.com/posts/please-dont-force-dark-mode)

- Dark mode on websites doesn't work for all situations.
- There are no accessibility guidelines for maximum contrast ratio.

[Ultimate guide to CI/CD: Fundamentals to advanced implementation](https://about.gitlab.com/blog/2025/01/06/ultimate-guide-to-ci-cd-fundamentals-to-advanced-implementation/)

- "Perhaps most importantly, CI/CD fosters a culture of collaboration and transparency within software development teams. When everyone can see the status of builds, tests, and deployments in real time, it becomes easier to identify and resolve bottlenecks in the delivery process. The automation provided by CI/CD also reduces the cognitive load on developers, freeing them to focus on writing code rather than managing manual deployment processes."

[How do interruptions impact different software engineering activities?](https://rdel.substack.com/p/rdel-75-how-do-interruptions-impact)

- Suggestions include minimizing high-dominance interruptions, reducing interruptions during code writing, and measuring for improvement.
- "Reduce urgent notifications from authoritative figures during critical focus periods, unless urgent. Use scheduled check-ins instead."
- "Avoid interruptions during code writing, which has the highest stress correlation. This can be achieved using “Do Not Disturb” blocks within calendar and chat, and a culture that respects that time."

## February

[3 Common Reasons Your Manager Will Fail You During Promotions And How To Have A Back Up Plan](https://news.yuezhao.coach/p/promotions-at-senior-levels)

- The common causes for promotion failure are change of manager, last-second reasons, and unclear promotion process.
- Be sure other layers of management are also included in promotion advocacy.
- "At the more senior levels, promotions are about relationships as much as they are about performance. Rather than 'what did you accomplish', it becomes also about 'what do others say about you'."
- "People leading higher visibility work or more cross-team work tend to advance faster in their careers. Say yes to those key company initiatives with high visibility if you want to grow. If you’re not in a role of high visibility, consider what projects or tasks you can take on to increase your visibility and frequency of interaction with senior executives."

[How to write a good design document](https://grantslatton.com/how-to-design-document)

- "The goal of a design document is to convince the reader the design is optimal given the situation."
- "You should anticipate every objection someone would have and preemptively show why it's invalid, so that the reader never even thinks to bring it up."

[Goodhart’s Law: How Measuring The Wrong Things Drive Immoral Behaviour](https://coffeeandjunk.com/goodharts-campbells-law/)

- Putting too much focus on a single metric results in people solely focusing on getting that number higher. A set of multiple measurements need to be taken to prevent these unintended consequences.

## March

[Only Solve One New Problem At A Time](https://www.bennadel.com/blog/4352-only-solve-one-new-problem-at-a-time.htm)

- Focus on one problem at a time. Solving multiple problems simultaneously often leads to complications and setbacks.
- Incremental integration allows for clearer project timelines, stakeholder communication, and promotes creative solutions, ultimately yielding better results by constraining thought processes and methods.

[Ask for no, don’t ask for yes](https://www.mooreds.com/wordpress/archives/3518)

- Instead of saying "Can I work on X to help with problem Y?" say "I'm going to work on X to solve Y. I'll start this on Wednesday, unless you say otherwise."
- "Pursue this approach for problems you feel are in the scope of your role but that you want to inform the boss about. It’s great when you want to offer a chance for feedback, but you are confident enough in the course of action that you don’t need feedback."

[Kotlin Sequences: An Illustrated Guide](https://typealias.com/guides/kotlin-sequences-illustrated-guide/)

- Normal collections are processed as a whole for each operation; sequences perform all operations on one item at a time.

[When to Use Sequences](https://typealias.com/guides/when-to-use-sequences/)

- Collections work well for collecting items and stateful operations (sorting, distinct).
- Sequences are good for `.forEach()` type of operations that are stateless. They can also generate values as they are requested.
- Java streams can run in parallel while Kotlin sequences cannot.

## April

[Are You Coachable?](https://novus.global/are-you-coachable/)

- Being coachable is about actively seeking out coaching - not just being open to being coached. "For once you redefine the bulls-eye of coachability as actively seeking out coaching, it creates a culture where everyone is desperate to grow and is learning to grow through utilizing the expertise, wisdom, and skills of others."

[Say no to abstract code](https://swizec.com/blog/say-no-to-abstract-code/)

- "Keep related code close together to reduce context boundaries and to limit the amount of relevant detail so it fits in your working memory."

## May

[Batching Your Meetings Saves You Hours Every Week — Here’s How](https://knowtworthy.medium.com/batching-your-meetings-saves-you-hours-every-week-heres-how-3798da6ccb02)

- Constantly switching between meetings and deep work lowers productivity. Try to rework your calendar to have large stretches of time to focus on deep work.

## June

[My AI Skeptic Friends Are All Nuts](https://fly.io/blog/youre-all-nuts/)

- "You’ve always been responsible for what you merge to main... whether or not you use an LLM."
- "Reading other people’s code is part of the job. If you can’t metabolize the boring, repetitive code an LLM generates: skills issue! How are you handling the chaos human developers turn out on a deadline?"
- "Part of being a senior developer is making less-able coders productive, be they fleshly or algebraic."
- "If truly mediocre code is all we ever get from LLMs, that’s still huge. It’s that much less mediocre code humans have to write."

## July

[AI Coding Agents Are Removing Programming Language Barriers](https://railsatscale.com/2025-07-19-ai-coding-agents-are-removing-programming-language-barriers/)

- "The real breakthrough came when I stopped thinking of AI as a code generator and started treating it as a pairing partner with complementary skills."
- AI Coding agents allow us to meaningfully contribute to projects with languages we are less familiar with.

## August

[I Know When You're Vibe Coding](https://alexkondov.com/i-know-when-youre-vibe-coding/)

- "I don’t want to know how you wrote this. I just want to know that you care about what comes out of the model. This is code you wouldn’t have produced a couple of years ago."
- "Write better prompts. Give better descriptions. Tell the LLM what library to use. Give it examples to follow. Write smaller files. There are no new principles - follow the ones that already exist."
- "Don’t leave a codebase’s maintainability to the weights of a model."

[Vibe code is legacy code](https://blog.val.town/vibe-code)

- "When you vibe code, you are incurring tech debt as fast as the LLM can spit it out. Which is why vibe coding is perfect for prototypes and throwaway projects: It's only legacy code if you have to maintain it!"
- "Vibe coding is on a spectrum of how much you understand the code. The more you understand, the less you are vibing."

[Live coding sucks](https://hadid.dev/posts/living-coding/)

- "When you’re placed in a high-stakes, time-pressured situation, like live coding, your brain reacts exactly like it would to any other threat."
- "For some people, especially those with even mild performance anxiety, it becomes nearly impossible to think clearly."
- "I like to think of live coding as a proxy for performance under stress."
- "The engineer who froze during a 30-minute LeetCode exercise might be the same person who quietly ships flawless code, writes excellent docs, and debugs complex systems. You’re not rejecting a bad engineer, you’re rejecting someone who doesn’t perform well while being watched. That’s not a skill most jobs require."

[This website is for humans](https://localghost.dev/blog/this-website-is-for-humans/)

- "If the AI search result tells you everything you need, why would you ever visit the actual website? Well, I want you to visit my website."

[Do things that don’t scale, and then don’t scale](https://derwiki.medium.com/do-things-that-dont-scale-and-then-don-t-scale-9fd2cd7e2156)

- "See a need that matters to you. Build the smallest, simplest thing that solves it. Resist the urge to make it bigger. Enjoy it."
- "AI tools make it cheap to create software for an audience of one — and sometimes, that’s the best possible audience."
