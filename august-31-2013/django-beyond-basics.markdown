## Django: Beyond Basics
#### Arun Ravindran

Note: Missed first 15-20 minutes.

#### Why not Django?
* **Unusually* (I repeat, **unusually**) high performance needs.
* Existing legacy database models.
* Migration? South. Django v1.7 has migration support built into Django.
* Builtin features ORM/Template are not enough.
	* Replacements are available. For e.g. SQLAlchemy for ORM, Jinja2 for templates etc.

#### Best practices
* Distrust outside data. Sanitize everything!
* Don't leak implementation details.
* Fatter models/Managers and Leaner Views
* Follow PEP8 and readable names.
* Be as DRY as possible.
* Breakdown into reusable apps.

#### Novice questions
* What is QuerySet?
	* Converts database 'stuff' to Python objects.
* Why is media separate?
	* Static is everything dev has written: JS, CSS etc.
	* Media includes images, videos etc.
* Which IDE?
	* Choose whichever yor
	* PyCharm, pydev for Eclipse, emacs, vim, Sublime Text 2
* How to deploy?
	* Fabric, Chef, Puppet for deployment automation.

#### Must-learn Python Packages
* pip
* virtualenv
* IPython/BPython
* Pudb (debugger)
* Fabric

#### But what goes well with Django?
* Django-debug-toolbar
* Django_compressor
* Django-extensions
* South
* Celery
* Tastypie

#### Other cool Django packages
* Django social auth
* Django Paypal
* crispy-fonts
* ??
* Psycopg2
* django-storages

#### My Django Workflow
* Create new Django project.
* Find a 3rd party app or create an app.
* Write/improve models.py
* Play with queries on console. Run 'syncdb'
* Add a bare admin.py
* Write views.py
* If needed, add a model form to forms.py
* Add views to urls.py
* Jump to step-3 till app looks good.

PS: Make friends with Fabric, git...

#### Forms are easy
* Use bootstrap

#### Should I use CBVs?
* Absolutely YES!

#### Now what?
* Turn off DEBUG
* Use HTTPS for logins
* Set X-Frame-OptionsHeader
* Use SESSION_COOKIE_SECURE
* Change /admin/ url

PS: See [ponycheckup.com](ponycheckup.com)

#### Q&A
Q: How do you do APIs?
> A: Tastypie and others.

Q: Rails v/s Django?
> A: I'm not Rails stuff. Philosophies of these frameworks are different. Debatable stuff.

Q: Storm ORM(?) works well with Django?
> A: Arun never heard about Storm ORM. He recommends SQLAlchemy.

Q: Debugger for Python? More verbose error logs?
> A: Werkzeug(pocoo's?), Django Debug Toolbar (comes with Django Extensions).

Q: Configuration (Django) v/s Convention (Rails)?
> A: Convention-first approach has de-facto conventions for doing things. Configurations-first approach allows you more flexibility.

Q: Why is IPython better?
> A: Python console on Androids. Loads of useful features.