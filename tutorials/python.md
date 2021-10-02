---
layout: default
---

<div class='container'>
<h1 class='display-1 text-center'>Python</h1>

<h3>Resources</h3>

<ul>
<li><a href='http://www.pythonlikeyoumeanit.com/'>Python Like You Mean It</a> (Really great if you already know a programming language)</li>
<li><a href='https://www.w3schools.com/python/default.asp'>W3Schools</a></li>
<li>DM George for useful Jupyter notebooks</li>
</ul>

<h3>Getting Started</h3>
<h4>Installation</h4>
<p>
You can download Python for any platform at <a href='https://www.python.org/downloads/'>python.org</a>, but most Unix-based systems will already have Python installed.
</p>
<h4>Hello, World!</h4>

<div class="col-4">
<pre><code>print("Hello, world!")</code></pre>
</div>

<h4>Wait... That was it?!</h4>
<p>
Yep! This is the reason Python is so popular: You trade performance for a massive increase in productivity. While it's true that Python runs orders of magnitude slower than C, if you're smart, you can use Python as a high-level 'glue' and use libraries written in C to do all of the heavy lifting. This is why Python is <b>the</b> go-to lang for machine learning, data science, and even quantum computing. Python is also the de facto scripting language (have you ever used a Perl program?), which is why I strongly recommend learning Python because it is so darn useful and (comparatively) very easy to learn.
</p>


<h3>Concepts</h3>

<h4>Everything is an Object</h4>

<div class="col-4">
<pre><code>&gt;&gt;&gt; type(10)
&lt;class 'int'&gt;
&gt;&gt;&gt; type("bruh moment")
&lt;class 'str'&gt;
&gt;&gt;&gt; type(lambda x: x + 1) # don't worry about this
&lt;class 'function'&gt;
</code></pre>
</div>

<h4>Whitespace Is Important</h4>

<div class="col-4">
<pre><code> x = 1 # notice the single leading space
# IndentationError: unexpected indent

for i in range(10):
    if True:
# ^ 1 tab (pretend it's actually a tab)
        print("Error!")
# ^ 8 spaces
# TabError: inconsistent use of tabs and spaces in indentation
</code></pre>
</div>
<p>
I'm sure this will trip up people from other langs, but whitespace replaces the function of brackets and semicolons. <a href='https://www.youtube.com/watch?v=SsoOG6ZeyUI'>Tabs vs. spaces</a> is its own debate, but I would recommend using a linter that converts all tabs to spaces or vice versa to save yourself some headaches.
</p>

<h4>Classes and Functions</h4>

<div class="col-4">
<pre><code>class Foo:
    x = "Ex" # class (static) variable

    # all methods must use 'self' as a parameter
    def __init__(self): # constructor
        self.bar = 1 # instance (non-static) variable

    def foo(self):
        print("foo the method")

def foo():
    print("foo the function")

foo()
# foo the function
Foo().foo()
# foo the method


# inheritance
class Bar(Foo):
    pass
</code></pre>
</div>

<h3>Libraries</h3>
<p>
It would be a fool's errand for me to try to list every Python library (320k+ on PyPI), but I can at least show you some of the ones you might see floating around. Please note there is <u>considerable</u> overlap between some of these, and your mileage will vary on how useful you will find these. Of course, just because it isn't listed below doesn't mean it isn't useful or popular, either.
</p>

<h4>General</h4>
<ul>
<li>Standard Library
<ul>
<li><a href='https://docs.python.org/3/library/datetime.html'>datetime</a> (<a href='https://docs.python.org/3/library/time.html'>time</a> is more useful for working with epoch)</li>
<li><a href='https://docs.python.org/3/library/argparse.html'>argparse</a></li>
<li><a href='https://docs.python.org/3/library/math.html'>math</a></li>
<li><a href='https://docs.python.org/3/library/random.html'>random</a></li>
<li><a href='https://docs.python.org/3/library/os.html'>os</a></li>
<li><a href='https://docs.python.org/3/library/threading.html'>threading</a></li>
<li><a href='https://docs.python.org/3/library/asyncio.html'>asyncio</a></li>
<li><a href='https://docs.python.org/3/library/urllib.html'>urllib</a></li>
<li><a href='https://docs.python.org/3/library/tkinter.html'>tkinter</a></li>
</ul></li>
<li><a href='https://docs.python-requests.org/en/latest/'>Requests</a></li>
</ul>

<h4>Data Science</h4>
<ul>
<li><a href='https://numpy.org/'>NumPy</a>  (incredibly useful for working with large arrays through <a href='https://stackoverflow.com/questions/1422149/what-is-vectorization'>vectorization</a>)</li>
<li><a href='https://pandas.pydata.org/'>Pandas</a></li>
<li><a href='https://matplotlib.org/'>Matplotlib</a></li>
</ul>

<h4>Machine Learning</h4>
<ul>
<li><a href='https://www.tensorflow.org/'>TensorFlow</a></li>
<li><a href='https://keras.io/'>Keras</a></li>
<li><a href='https://pytorch.org/'>PyTorch</a></li>
<li><a href='https://scikit-learn.org/stable/'>Scikit-learn</a></li>
</ul>


</div>

{% include syntax-highlighter.html %}