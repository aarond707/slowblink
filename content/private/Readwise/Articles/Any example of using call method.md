# Any example of using call method

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)

## Metadata
- Author: [[Amiya Sahu]]
- Full Title: Any example of using call method
- Category: #articles
- URL: https://godotengine.org/qa/91929/any-example-of-using-call-method

## Highlights
- As shown in your own example, once you write down a function, and attach the script to a node, from now on that node has this new method that can be called from any other script with
  node.method()
  The tricky part is only how to access said node.
  If the calling script is the parent of the called node, you can use $
  $NameOfTheChildNode.method()
  Otherwise you have to state the path to reach that note by using
  var node=get_node(path) or get_child(x) or get_parent(), and probably other ways.
  This is of course valid for the built-in methods and properties as well
- var method_name=""
  func _process(delta):
  if method_name!="":
  call(method_name)
  func Test1():
  print("hello")
  func Test2():
  print("world")
