## PyCon India 2013 Keynote
### Kiran Jonnalagadda

Note: Unfortunately, I missed first 5-10 minutes of Kiran's keynote :(

#### The story of Zine
* Kiran started searching for blogging tool. Kiran didn't liked Wordpress.
* *Zine*: Blogging platform written in Python. Kiran started using it.
* Kiran ended up becoming contributor to Zine (on Bitbucket).
* Zine used MySQL (to represent key-value pairs related stuff in RDBMS).
* For a feature (which needed key-value pairs), Kiran tried using pickles. But they like JSON more. They started supporting JSON (or pickle).
* [Armin Ronacher](http://twitter.com/mitsuhiko) (creator of Zine) rejected the JSON patch. Armin wanted to do this using migrations.
* Kiran started building his own website on a fork of Zine. He sent patches to upstream as well.
* On April 1, 2010, Armin's DENIED came out! Few lines of code to run a complete website. April Fools joke!
* And, then Armin created Flask!

#### Internal Server Error
* An Ubuntu upgrade later, Kiran's site/blog says "Internal Server Error". Till today, Kiran does not has time to fix it.
	* MySQL was incompatible with Zine.
	* Why? Because he got busy... no one else to manage/fix his fork of Zine.
* Open Source is awesome!
	* Tom Preston Werner's (GitHub's cofounder) blogpost: "Open Source (almost) everything"

* Example:
	* *Cubism.js*
	* Some web development company (--- foundation?) started open sourcing their
	* *Twitter Bootstrap*: Good JS, HTML, CSS practices in one package.
	* *Flipkart's phantom*(?) project on Github. 
* Maintaining code is more difficult than actually writing the code originally.
* Maintainence costs > authoring costs.
* Open Source is process of distributing the overhead maitainence tasks.
* The paradox of code: more or less?
	* To become a good programmer, one needs to write loads of code.
	* Hallmark of good programmer: Write less code
	* Convince others to use the open source code you wrote.

#### Q&A
Que: Is propreitary code any useful at all?
> Ans: Usage of code may not necessarily depend on code itself.

Que: Martin Fowler etc wrote about programmer productivity on basis of LOC
> Ans: Trying to measure programmer's capability is stupid. Python has huge collection of excellent libraries. 

Que: In most open source projects, number of core developers are very low. What can we do?
> Ans: Learn from what Armin did with DENIED for Flask. Today, Flask has not shortage of contributors.

Que: Importance of writing tests?
> Ans: Some people believe that writing test cases is for testers. Every programmer should write their own tests.

Que: Choice of license for open source
> Ans: Restrictive licenses (GPL, AGPL etc) and permissive licenses (BSD, MIT etc)
Kiran prefers permissive licenses.

Que: Python in Education? Is it bad because students won't get to learn about low-level stuff?
> Ans: Most of us don't use low-level stuff today. Moreover, people should be left to choose whatever they want to use. For example, mobile dev isn't done in Python (Kivy).