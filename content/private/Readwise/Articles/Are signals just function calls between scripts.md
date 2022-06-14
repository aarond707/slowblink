# Are [[signals]] just function calls between scripts?

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png)

## Metadata
- Author: [[Amiya Sahu]]
- Full Title: Are [[signals]] just [[function]] calls between scripts?
- Category: #articles
- URL: https://godotengine.org/qa/66190/are-signals-just-function-calls-between-scripts

## Highlights
- It seems to me that between emitting and connecting, that [[signals]] are simply a way for performing a function call between two separate scripts/[[nodes]].
	- You don't need [[signals]] for this! Let's say you have a tree looking like this:
	  - Main-Node named "Main" (with a script called main.gd)
	  - Child-Node named "Child" (with a script called child.gd)
  If you then want to call a method foo() in child.gd from main.gd you'd do:
  get_node("Child").foo()
  If you instead want to call a method bar() in main.gd from child.gd you'd do:
  get_node("../Main").bar() # alternatively: get_parent().bar()
