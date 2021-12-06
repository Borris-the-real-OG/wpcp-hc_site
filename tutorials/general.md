---
layout: default
---


<div class='container'>
<h1 class='display-1 text-center'>General Skills</h1>

<p>Here's a list of stuff you should probably know. I'm not going to reinvent the wheel here, but instead compile a list of resources I think are good.</p>

<h3>Linux</h3>
<h5><i>Worth learning?</i></h5>
<p>100% learn Linux (at least the basics). This is useful 11/10 times unless you live & breathe C#. Even then you should still learn it.</p>
<h5>Resources</h5>
<ul>
<li><a href="https://linuxjourney.com/">Linux Journey</a></li>
<li><a href="https://replit.com/">repl.it</a> for Chromebook users (if you have a better online terminal, let me know!)</li>
<iframe id='linux_player' width="560" height="315" src="https://www.youtube-nocookie.com/embed/ZtqBQ68cfJc" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<p class='text-muted'><i><a href='https://www.freecodecamp.org/'>freeCodeCamp</a> has all sorts of good tutorials and videos covering a wide range of topics... I especially liked their web development courses.</i></p>
<p>This is a good tutorial for commonly used Linux commands. It's quite long, but I recommend beginners only watch through <kbd><code>head</code></kbd>.</p>
</ul>

<h3>Git</h3>
<h5><i>Worth learning?</i></h5>
<p>Probably, yes. You can definitely get by without this because most students work independently, but there are a lot of merits to easily uploading your code to the cloud and being able to bounce around the version history. This website is actually hosted on Github and is one big ol' Git repository! I'm going to add some activities in the repo later, but for now I recommend checking out the resources.</p>
<h5>Resources</h5>
<ul>
<li><a href='https://git-scm.com/'>Git</a></li>
<li><a href='https://learngitbranching.js.org/'>Learn Git Branching</a></li>
<li><a href='https://github.com/jlord/git-it-electron/releases'>Git-it</a></li>
<li><a href='https://www.git-tower.com/learn/git/ebook/'>Git Tower Git guide</a></li>
</ul>


<h3>Scripting Languages</h3>
<h5><i>Worth learning?</i></h5>
<p>Definitely. IMO you should know at least one scripting language as your multi-tool to quickly do random programming tasks when you don't need to heavily optimize your code or work on a really low level. A good chunk of CTF challenges practically <i>require</i> the use of Python and <kbd><code>pwntools</code></kbd>... Seriously, this is how easy it is to connect to a web server with <kbd><code>pwntools</code></kbd>:</p>

<div class="col-4">
<pre><code>from pwn import *
conn = remote(SERVER_ADDRESS, PORT)
# receive a line from the server
conn.recvline()
# receive input until a target string
conn.recvuntil('Success! Flag is ')
# send input
conn.send('Hello world!\r\n')
conn.close()

#///////////////////

listener = listen(1234)
server = listener.wait_for_connection()
server.recv()
</code></pre>
</div>
<p class='text-muted'><i><a href='https://es7evam.gitbook.io/security-studies/exploitation/sockets/03-connections-with-pwntools'>Source</a></i></p>
<p>The other big contenders for scripting languages are Perl and Ruby. Perl had its heyday in the '90s as the "Swiss-Army chainsaw" of programming languages, but Python can do pretty much anything Perl can do (I do like Perl regex better, though). Ruby is still relevant because of its killer app <a href='https://rubyonrails.org/'>Ruby on Rails</a>, but I haven't seen a lot of use outside of that. Also, JavaScript is not <i>really</i> a scripting language in the traditional sense, but you should still learn Javascript because it's what the internet is built on.</p>
<h5>Resources</h5>
<ul>
<li><a href='{{ site.baseurl }}/tutorials/python.html'>WPCP Hack Club Python guide</a></li>
<li><a href='https://docs.pwntools.com/en/stable/'>pwntools</a></li>
</ul>

<h3>Docker</h3>
<h5><i>Worth learning?</i></h5>
<p>Fully? Depends on what you want to do, but really you just need to kind of know how Docker works. Docker is containerization software that packs your code/project into packages called containers which can communicate with each other but are ultimately separate. Docker is great for deploying code to the cloud, parallelized computing, or just having a consistent workspace across machines.</p>

<h5>Resources</h5>
<ul>
<li><a href='https://www.docker.com/'>Docker</a></li>
</ul>

<h2>WIP:</h2>
<ul>
<li>Volatility3</li>
<li>GDB</li>
<li>Ghidra</li>
<li>JavaScript for CTF</li>
<li>Algorithms</li>
</ul>


</div>

{% include syntax-highlighter.html %}