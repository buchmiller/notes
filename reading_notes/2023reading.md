# 2023 Reading

Links to articles I read in 2023 with a few notes to remind me of the topic.

## January

[Get your work recognized: write a brag document](https://jvns.ca/blog/brag-documents/)

- "[These ideas] help me reflect on themes in my work, what’s important to me, what I’m learning, and what I’d like to be doing differently."
- "The tactic is pretty simple! Instead of trying to remember everything you did with your brain, maintain a “brag document” that lists everything so you can refer to it when you get to performance review season!"

[4 steps to transforming developers into security people](https://techbeacon.com/security/4-steps-transforming-developers-security-people)

- "To reach your developers with the message of security requires a four-phase process of application security connection. Open their eyes, fill their brains, task their hands, and embrace the gathering"

[Flaw: Constructor does Real Work](http://misko.hevery.com/code-reviewers-guide/flaw-constructor-does-real-work/)

- If it is difficult to test an object, the contructor might be doing too much.
- "Think about one fundamental question when writing or reviewing code: How am I going to test this?"
- "Do not create collaborators in your constructor, but pass them in" (builder, factory, provider, dependency injection, etc.)
