---
layout: default
---


<div class='container'>
<h1 class='display-1 text-center'>C++</h1>
<h3>Resources</h3>
<ul>
<li><a href='https://www.geeksforgeeks.org/c-plus-plus/'>GeeksforGeeks</a></li>
<li><a href='https://www.w3schools.com/cpp/default.asp'>W3Schools</a></li>
<li><a href='https://www.codecademy.com/learn/learn-c-plus-plus'>Codecademy</a> (Personally not a huge fan)</li>
</ul>

<h3>Why C++?</h3>
<p>C++ is entering its 36th year strong, with many features being added in the last decade (lambdas, auto, smart pointers). But why hasn't C++ gone the way of the dinosaur? That's becuse C/C++ is fast... <i>really</i> fast. The language gives almost full control to the programmer, giving you direct access to memory, full control of pointers, and even lets you write inline assembly (pretty much the lowest level human readable language possible). However, with great power comes great responsibility: It's up to the programmer to manage references, dynamically allocated memory, and all sorts of other things.</p>
<h5 class="text-center" style="color: whitesmoke">
"C makes it easy to shoot yourself in the foot; C++ makes it harder, but when you do it blows your whole leg off."<br>- Bjarne Stroustrop, creator of C++
</h5>
<h3>Getting Started</h3>
<h4>Installation</h4>
<p>To start off, you're going to need a C++ compiler. If you're on Mac, I recommend Clang (comes bundled with XCode) or GCC (the GNU compiler, highly recommend). If you're on Windows, you can try downloading <a href="https://code.visualstudio.com/docs/languages/cpp#_example-install-mingwx64">MinGW-x64</a>, but I personally prefer <a href="https://docs.microsoft.com/en-us/windows/wsl/install">WSL</a> because Linux makes a bunch of stuff easier. If you're on Linux, I'm going to recommend GCC again, which can be downloaded with a good 'ol <kbd>$ sudo apt install build-essential</kbd>. If you're on Chromebook, do not despair! You can get up and running with <a href="https://replit.com/site/ide">repl.it</a> in no time.
</p>

<h4>Obligatory "Hello, World!"</h4>

<div class="col-4">
<pre><code>#include &lt;iostream&gt;

int main() {
    std::cout &lt;&lt; "Hello, world!\n";
    return 0;
}</code></pre>
</div>

<p>There's quite a bit to break down here. Most obvious is the <kbd><code>#include &lt;iostream&gt;</code></kbd> business. The <kbd><code>#</code></kbd> is for a <i>preprocessor directive</i>, which is basically a command for the compiler, and <kbd><code>#include</code></kbd> is one such directive that imports a <i>header file</i> into your code. It's actually a lot more low-tech than it looks: The compiler literally copy-pastes the contents of <kbd><code>&lt;iostream.h&gt;</code></kbd> into your code, and then compiles the whole thing (the <kbd>.h</kbd> is for header file).

<br><br>
&emsp;"Ok, well, where did this 'iostream.h' file come from?" you might ask.<br><br>Every installation of a C++ compiler comes bundled with a version of the <i>standard <small>template</small> library</i> (STL). The standard library is a collection of useful algorirthms, containers and other stuff that makes life a lot easier, like <kbd><code>&lt;iostream&gt;</code></kbd> for I/O. The implementation of the STL is totally up to the compiler vendor, but all implementations have the exact same function/class names and all the algorithms are guarateed to run with a certain time and space complexity. In other words, <em>don't worry about it</em>.

<br><br>
The next thing to tackle is this <kbd><code>int main()</code></kbd> function. <kbd><code>main()</code></kbd> might be familiar to you already, but if it's not the main function acts as the entry point to your program. If all roads lead to Rome, all your code has to lead back to main(), otherwise it will never run! The second part of this that may not make as much sense is the <kbd><code>int</code></kbd> return type... You probably guessed that 'int' is the type that stands for 'integer', but wait... Java's main doesn't return anything, so why the int? The int is an <i>exit code</i> which lets whatever called the C/C++ program know if it succeeded or failed, kinda like how 404 is an HTTP status code that means 'resource not found'. To make a long story short, returning a 0 means the program ran successfully and anything else means it failed, so 99% of the time you can just slap a <kbd><code>return 0;</code></kbd> at the end of your code and be fine.
</p>

<div class="col-4">
<pre><code class="language-plaintext"> | return type goes here
 v
int main() &lt;- function arguments go in here
      ^
      | function name goes here</code></pre>
</div>

<br>
<p>
Now we're at the meat and potatoes of the program. <kbd><code>std::cout</code></kbd> is data stream from <kbd><code>&lt;iostream&gt;</code></kbd> and the Standard Library which I talked about earlier. You can read about it <a href='https://www.geeksforgeeks.org/cout-in-c/'>more</a> if you're interested, but honestly the details aren't too important. You just need to know that this is how you print stuff to the screen (cout) and recieve user input to your program (cin). The <kbd><code>std</code></kbd> is called a namespace, which you also don't really have to worry about now, but a lot of people put <kbd><code>using namespace std;</code></kbd> at the top of their program, which means that you don't have to prepend stuff from the STL with <kbd><code>std</code></kbd>.
</p>

<div class="col-4">
<pre><code>#include &lt;iostream&gt;
using namespace std; // this is new

int main() {
    // no more std::
    cout &lt;&lt; "Hello, world!\n";
    return 0;
}</code></pre>
</div>

<br>
<p>
The <kbd>&lt;&lt;</kbd> falls into the same 'hand-wavey' category as cout, but it's basically how you read/write to a stream (how you print stuff). <kbd>"Hello, world!"</kbd> is probably pretty self explnatory, but in case you haven't seen <kbd>\n</kbd> before, its an escape code that means newline.
<br><br>
Phew! That was a lot to get through. Maybe take 5, get some water or something.
<br>
In all honesty, there's no way I can teach C++ better than one of the websites listed at the top. Buuuut I and many hack club members have experience with C++, so asking us for help is not a bad idea. Probably pretty infeasible for me to write a whole C++ tutorial though.
</p>



</div>

{% include syntax-highlighter.html %}