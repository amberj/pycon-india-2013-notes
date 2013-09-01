## Keynote (Day-2)
### [Kenneth Reitz](github.com/kennethreitz)

Note: Unfortunately, I missed first 30-35 minutes of the Kenneth's talk. If someone has notes for the same, please send a pull request.

* Learn to say "No"
	* New pull request, new features, but increases complexity...then say no.
	* As few SLOC as possible.

> Simplicity is always better than functionality -- Pieter Hintjens

* Simple code is good
	* Less code written, less code to maintain.
	* Negative diffs are best diffs.

* Complex code is bad
	* Tight coupling
	* Monolithic codebases
	* High maitainence burden
	* Self-serving instead of problem-solving

* Open source makes the world a better place!

#### Q&A

Q: Requests v/s Mechanize
> A: Kenneth himself uses Mechanize himself.

Q: How to get community involved like Kenneth did with
> A: Good documentation. What the project is, how to use it, how to install it etc. If it is a good idea and it resonates well with others, it'll get the kickstart that it needs.

Q: Documentation v/s TDD?
> A: Write the README, integration tests, unit tests, write docs.

Q: How to decide which features to include and which to exclude when starting a project?
> A: Depends on audience. Ken makes a balance between the two. He is a user of code he writes.

Q: What is Ken's take on creating a plugins ecosystem for software someone wrote?
> A: To keep code simple, creating a plugins ecosystem is good. Gives users lots of power.