---
layout: post-full
title: Rails Beginer Cheat Sheet
---


  <div class="container ">
    <section id="main-content">
      <h1>Cheat Sheet Conventions</h1>

<p>
  <strong>Bold</strong> words are what is really important e.g.
  the command and concept shown in the usage category. In the code usage and
  example columns these highlight the main part of the concept, like this:
  <code>general_stuff<strong>.concept</strong></code>.
  In the same columns <code><em>italic_words</em></code> mark the
  arguments/parameters of a command/method.
</p>

<p>
  However <em>italic words</em> in the descriptions or general text denote
  more general concepts or concepts explained elsewhere in this cheat
  sheet or in general.
</p>

<h1 id="console">Console Basics</h1>

<p>
  The console (also called <em>command line, command prompt or
  terminal</em>) is just another way of interacting with your computer.
  So you can basically do anything with it that you could also do with
  your graphical desktop user interface. This sections contains a couple
  of examples.
</p>

<p>
  For the different operating systems <strong>starting the console</strong>
  differs.
</p>

<ul>
  <li><strong>Windows:</strong> Open the start menu and search for
    command prompt. Alternatively choose <em>execute</em> and enter
    <em>cmd</em>.</li>
  <li><strong>Mac:</strong> Open Spotlight, type <em>terminal</em>, and
    start that program.
  </li>
  <li><strong>Linux:</strong> The terminal should be one of the main
    options once you open the main menu of your distribution. Otherwise
    search for <em>terminal</em> if your distribution has such an option
    or look under Accessories.
  </li>
</ul>

<table class="table table-striped">
  <tbody><tr>
    <th class="concept">Concept</th>
    <th class="usage">Usage</th>
    <th class="example">Examples</th>
    <th class="description">Description</th>
  </tr>
  <tr>
    <td>Change directory</td>
    <td>
      <code><strong>cd</strong> <em>directory</em></code>
    </td>
    <td>
      <p><code>cd my_app</code></p>

      <p><code>cd my_app/app/controllers</code></p>
    </td>
    <td>Changes the directory to the specified directory on the
      console.
    </td>
  </tr>
  <tr>
    <td>List contents directory</td>
    <td>
      <p><code><strong>ls</strong> <em>directory</em></code></p>

      <p><code>Windows: <strong>dir</strong> <em>directory</em></code>
      </p>
    </td>
    <td>
      <p><code><strong>ls</strong></code></p>

      <p><code><strong>ls</strong> <em>my_app</em></code></p>
    </td>
    <td>Shows all contents (files and folders) of the directory.
      If no directory is specified shows the contents of the
      current directory.
    </td>
  </tr>
  <tr>
    <td>Directory you are currently in</td>
    <td><code><strong>pwd</strong></code></td>
    <td><code><strong>pwd</strong></code></td>
    <td>Shows the full path of the directory you are currently
      in. E.g. /home/tobi/railsgirls
      <br>
      A note on filenames: if a file or directory name starts with a slash / as in the output of pwd above, it is an absolute filename specifying the complete filename starting at the root of the current file system (e.g. hard disk). If the slash (/) is omitted, the file name is relative to the current working directory.
    </td>
  </tr>
  <tr>
    <td>Create a new directory</td>
    <td><code><strong>mkdir</strong> <em>name</em></code></td>
    <td>
      <p><code><strong>mkdir</strong> <em>rails</em></code></p>
      <p><code><strong>mkdir</strong> <em>fun</em></code></p>
    </td>
    <td>
      Creates a directory with the given name in the folder you are currently
      in.
    </td>
  </tr>
  <tr>
    <td>Delete a file</td>
    <td>
      <p><code><strong>rm</strong> <em>file</em></code></p>

      <p><code>Windows: <strong>del</strong> <em>file</em></code>
    </p></td>
    <td>
      <p><code><strong>rm</strong> <em>foo</em></code></p>
      <p><code><strong>rm</strong> <em>index.html</em></code></p>
      <p><code><strong>rm</strong> <em>pictures/old_picture.jpg</em></code></p>
    </td>
    <td>
      <p>Deletes the specified file. Be <strong>extra cautious</strong> with this
      as it would be too bad to delete something you still need :-(</p>
      <p>
        You can simply specify the name of a file of the directory you are
        currently in. However you can also specify a path, this is shown in the
        third example. There we delete the <em>old_picture.jpg</em> file from
        the <em>pictures</em> folder.
      </p>
    </td>
  </tr>
  <tr>
    <td>Delete a directory</td>
    <td>
      <p><code><strong>rm -r</strong> <em>folder</em></code></p>

      <p><code>Windows: <strong>rd</strong> <em>folder</em></code>
    </p></td>
    <td>
      <p><code><strong>rm -r</strong> <em>stuff_i_dont_need</em></code></p>
      <p><code><strong>rm -r</strong> <em>stuff_i_dont_need/</em></code></p>
      <p><code><strong>rm -r</strong> <em>old_application</em></code></p>
    </td>
    <td>
      <p>Deletes the specified folder <strong>and all of its contents</strong>.
        So please be <strong>super cautious</strong> with this! Make sure that
        you do not need any of the contents of this folder any more.
      </p>
      <p>
        So why would you want to delete a whole folder? Well maybe it was an old
        application that you do not need anymore :-)
      </p>
    </td>
  </tr>
  <tr>
    <td>Starting a program</td>
    <td><code><strong>program</strong> <em>arguments</em></code></td>
    <td>
      <p><code><strong>firefox</strong></code></p>

      <p><code>
        <strong>firefox</strong> <em>railsgirlsberlin.de</em></code>
      </p>

      <p><code><strong>irb</strong></code></p>
    </td>
    <td>Starts the program with the given name and arbitrary arguments
      if the program takes arguments. Firefox is just one example. Starting
      Firefox without arguments just opens up Firefox. If you give it an
      argument it opens the specified URL.
      When you type in <code>irb</code> this starts <em>interactive ruby</em>.
    </td>
  </tr>
  <tr>
    <td>Abort the program</td>
    <td>Press <strong>Ctrl + C</strong></td>
    <td>-</td>
    <td>This will abort the program currently running in the terminal.
      For instance this is used to shut down the Rails server.
      You can also abort many other related tasks with it, including:
      bundle install, rake db:migrate, git pull and many more!
    </td>
  </tr>
</tbody></table>


<h1 id="ruby">Ruby Basics</h1>

<p>
  Ruby is the programming language Ruby on Rails is written in. So most
  of the time you will be writing Ruby code. Therefore it is good to
  grasp the basics of Ruby. If you just want to play with Ruby, type
  <strong>irb</strong> into your console to start interactive ruby. There
  you can easily experiment with Ruby. To leave irb, type
  <strong>exit</strong>.
</p>

<p>
  This is just a very small selection of concepts. This is especially
  true later on when we talk about what Arrays, Strings etc. can do.
  For more complete information have a look at
  <a href="http://ruby-doc.org/">ruby-doc</a> or search with your favorite
  search engine!
</p>

<h2 id="ruby-concepts">General concepts</h2>
<table class="table table-striped">
<tbody><tr>
  <th class="concept">Concept</th>
  <th class="usage">Usage</th>
  <th class="example">Examples</th>
  <th class="description">Description</th>
</tr>
<tr>
  <td>Comment</td>
  <td>
    <code><strong>#</strong> <em>Comment text</em></code>
  </td>
  <td>
    <p>
      <code><strong>#</strong> <em>This text is a comment</em></code>
    </p>

    <p>
      <code>some.ruby_code <strong>#</strong> A comment</code>
    </p>

    <p>
      <code><strong>#</strong> some.ignored_ruby_code</code>
    </p>
  </td>
  <td>
    Ruby ignores everything that is marked as a comment. It does not try
    to execute it. Comments are just there for you as information.
    Comments are also commonly used to <em>comment out code</em>. That
    is when you don't want some part of your code to execute
    but you don't want to delete it just yet, because you are trying
    different things out.
  </td>
</tr>
<tr>
  <td>Variables</td>
  <td>
    <code><strong>variable =</strong> <em>some_value</em></code>
  </td>
  <td>
<pre><code><strong>name =</strong> <em>"Tobi"</em>
<strong>name</strong> # =&gt; "Tobi"</code></pre>
<pre><code><strong>sum =</strong> <em>18 + 5</em>
<strong>sum</strong> # =&gt; 23</code></pre>
  </td>
  <td>
    With a variable you tell Ruby that from now on you want to refer to
    that value by the name you gave it. So for the first example, from
    now on when you use <em>name</em> Ruby will know that you meant
    <em>"Tobi"</em>.
  </td>
</tr>
<tr>
  <td>Console output</td>
  <td>
    <code><strong>puts</strong> <em>something</em></code>
  </td>
  <td>
    <p><code><strong>puts</strong> <em>"Hello World"</em></code></p>

    <p><code><strong>puts</strong> <em>[1, 5, "mooo"]</em></code></p>
  </td>
  <td>
    Prints its argument to the console. Can be used in Rails apps
    to print something in the console where the server is running.
  </td>
</tr>
<tr>
  <td>Call a method</td>
  <td>
    <code>object<strong>.method</strong><em>(arguments)</em></code>
  </td>
  <td>
    <p><code>string<strong>.length</strong></code></p>

    <p><code>
      array<strong>.delete_at</strong><em>(2)</em>
    </code></p>

    <p><code>string<strong>.gsub</strong><em>("ae", "ä")</em></code></p>
  </td>
  <td>
    <p>Calling a method is also often referred to as
      <em>sending a message</em> in Ruby. Basically we are sending an
      object some kind of message and are waiting for its response.
      This message may have no arguments or multiple arguments, depending
      on the message.
      So we kindly ask the object to do something or give us some
      information.
      When you "call a method" or "send a message" something happens. In the
      first example we ask a String how long it is (how many
      characters it consists of). In the last example we substitute all
      occurrences of "ae" in the string with the German "ä".</p>

    <p>
      Different kinds of objects (Strings, Numbers, Arrays...)
      understand different messages.
    </p>
  </td>
</tr>
<tr>
  <td>Define a method</td>
  <td>
<pre><code><strong>def</strong> <em>name(parameter)</em>
  <em># method body</em>
<strong>end</strong></code></pre>
  </td>
  <td>
<pre><code><strong>def</strong> <em>greet(name)</em>
  <em>puts "Hi there " + name</em>
<strong>end</strong></code></pre>
  </td>
  <td>
    <p>Methods are basically reusable units of behaviour. And you can
      define them yourself just like this. Methods are small and focused
      on implementing a specific behaviour.</p>

    <p>
      Our example method is focused on greeting people.
      You could call it like this: <code>greet("Tobi")</code>
    </p>
  </td>
</tr>
<tr>
  <td>Equality</td>
  <td><code>object <strong>==</strong> other</code></td>
  <td>
    <p><code>true <strong>==</strong> true # =&gt; true</code></p>

    <p><code>3 <strong>==</strong> 4 # =&gt; false</code></p>

    <p><code>"Hello" <strong>==</strong> "Hello" # =&gt; true</code></p>

    <p><code>"Helo" <strong>==</strong> "Hello" # =&gt; false</code></p>
  </td>
  <td>
    With two equal signs you can check if two things are the
    same. If so, <code>true</code> will be returned; otherwise, the result
    will be <code>false</code>.
  </td>
</tr>
<tr>
  <td>Inequality</td>
  <td><code>object <strong>!=</strong> other</code></td>
  <td>
    <p><code>true <strong>!=</strong> true # =&gt; false</code></p>

    <p><code>3 <strong>!=</strong> 4 # =&gt; true</code></p>
  </td>
  <td>
    Inequality is the inverse to equality, e.g. it results in
    <code>true</code> when two values are not the same and it results
    in <code>false</code> when they are the same.
  </td>
</tr>
<tr>
  <td>Decisions with if</td>
  <td>
<pre><code><strong>if</strong> <em>condition</em>
  # happens when true
<strong>else</strong>
  # happens when false
<strong>end</strong>
</code></pre>
  </td>
  <td>
<pre><code><strong>if</strong> <em>input == password</em>
  grant_access
<strong>else</strong>
  deny_access
<strong>end</strong>
</code></pre>
  </td>
  <td>
    <p>With if-clauses you can decide based upon a <em>condition</em>
      what to do. When the condition is considered true, then the code
      after it is executed. If it is considered false, the code after
      the "else" is executed.</p>

    <p>
      In the example, access is granted based upon the decision if a
      given input matches the password.
    </p>
  </td>
</tr>
<tr>
  <td>Constants</td>
  <td><code><strong>CONSTANT =</strong> <em>some_value</em></code></td>
  <td>
<pre><code><strong>PI = 3.1415926535</strong>
<strong>PI</strong> # =&gt; 3.1415926535</code></pre>
<pre><code><strong>ADULT_AGE</strong> = 18
<strong>ADULT_AGE</strong> # =&gt; 18</code></pre>
  </td>
  <td>
    Constants look like variables, just in UPCASE. Both hold
    values and give you a name to refer to those values. However while
    the value a variable holds may change or might be of an unknown
    value (if you save user input in a variable) constants are
    different. They have a known value that should never change. Think
    of it a bit like mathematical or physical constants. These don't
    change, they always refer to the same value.
  </td>
</tr>
</tbody></table>

<h2 id="ruby-numbers">Numbers</h2>

<p>
  Numbers are what you would expect them to be, normal
  numbers that you use to perform basic math operations.
</p>

<p>
  More information about numbers can be found in the
  <a href="http://ruby-doc.org/core-2.0/Numeric.html">ruby-doc of Numeric</a>.
</p>

<table class="table table-striped">
  <tbody><tr>
    <th class="concept">Concept</th>
    <th class="usage">Usage</th>
    <th class="example">Examples</th>
    <th class="description">Description</th>
  </tr>
  <tr>
    <td>normal Number</td>
    <td><code><strong>number_of_your_choice</strong></code></td>
    <td>
      <p><code><strong>0</strong></code></p>

      <p><code><strong>-11</strong></code></p>

      <p><code><strong>42</strong></code></p>
    </td>
    <td>
      Numbers are natural for Ruby, you just have to enter them!
    </td>
  </tr>
  <tr>
    <td>Decimals</td>
    <td><code><strong>main.decimal</strong></code></td>
    <td>
      <p><code><strong>3.2</strong></code></p>

      <p><code><strong>-5.0</strong></code></p>
    </td>
    <td>
      You can achieve decimal numbers in Ruby simply by adding a point.
    </td>
  </tr>
  <tr>
    <td>Basic Math</td>
    <td>
      <code>n <strong>operator</strong> <em>m</em></code>
    </td>
    <td>
      <p><code>2 <strong>+</strong> <em>3</em> # =&gt; 5</code></p>

      <p><code>5 <strong>-</strong> <em>7</em> # =&gt; -2</code></p>

      <p><code>8 <strong>*</strong> <em>7</em> # =&gt; 56</code></p>

      <p><code>84 <strong>/</strong> <em>4</em> # =&gt; 21</code></p>
    </td>
    <td>
      In Ruby you can easily use basic math operations.
      In that sense you may use Ruby as a super-powered calculator.
    </td>
  </tr>
  <tr>
    <td>Comparison</td>
    <td>
      <code>n <strong>operator</strong> <em>m</em></code>
    </td>
    <td>
      <p><code>12 <strong>&gt;</strong> <em>3</em> # =&gt; true</code></p>

      <p><code>12 <strong>&lt;</strong> <em>3</em> # =&gt; false</code></p>

      <p><code>7 <strong>&gt;=</strong> <em>7</em> # =&gt; true</code></p>
    </td>
    <td>
      <p>Numbers may be compared to determine if a number is bigger or smaller
        than another number. When you have the age of a person saved in the
        <code>age</code> variable you can see if that person is considered
        an adult in Germany:</p>

      <p><code>age &gt;= 18 # true or false</code></p>
    </td>
  </tr>
</tbody></table>

<h2 id="ruby-strings">Strings</h2>

<p>
  Strings are used to hold textual information. They may contain
  single characters, words, sentences or a whole book. However you may
  just think of them as an ordered collection of characters.
</p>

<p>
  You can find out more about Strings at the
  <a href="http://ruby-doc.org/core-2.0/String.html">ruby-doc page about
    Strings</a>.
</p>

<table class="table table-striped">
  <tbody><tr>
    <th class="concept">Concept</th>
    <th class="usage">Usage</th>
    <th class="example">Examples</th>
    <th class="description">Description</th>
  </tr>
  <tr>
    <td>Create</td>
    <td>
      <p><code><strong>'</strong>A string<strong>'</strong></code></p>
    </td>
    <td>
      <p><code><strong>'</strong>Hello World<strong>'</strong></code></p>

      <p><code><strong>'</strong>a<strong>'</strong></code></p>

      <p><code>
        <strong>'</strong>Just characters 129 _!$%^<strong>'</strong>
      </code></p>

      <p><code><strong>''</strong></code></p>
    </td>
    <td>
      A string is created by putting quotation marks around a
      character sequence. A <a href="https://github.com/bbatsov/ruby-style-guide/">Ruby style guide</a>
      recommends using single quotes for simple strings.
    </td>
  </tr>
  <tr>
    <td>Interpolation</td>
    <td>
      <p><code><strong>"</strong>A string and an #{expression}<strong>"</strong></code></p>
    </td>
    <td>
      <p><code><strong>"</strong>Email: #{user.email}<strong>"</strong></code></p>

      <p><code><strong>"</strong>The total is #{2 + 2}<strong>"</strong></code></p>

      <p><code><strong>"</strong>A simple string<strong>"</strong></code></p>
    </td>
    <td>
      You can combine a string with a variable or Ruby expression using double quotation marks.
      This is called "interpolation." It is okay to use double quotation marks around a simple
      string, too.
    </td>
  </tr>
  <tr>
    <td>Length</td>
    <td><code>string<strong>.length</strong></code></td>
    <td>
      <p><code>"Hello"<strong>.length</strong> # =&gt; 5</code></p>

      <p><code>""<strong>.length</strong> # =&gt; 0</code></p>
    </td>
    <td>
      You can send a string a message, asking it how long it is and it
      will respond with the number of characters it consists of. You could
      use this to check if the desired password of a user exceeds the
      required minimum length. Notice how we add a comment to show the
      expected result.
    </td>
  </tr>
  <tr>
    <td>Concatenate</td>
    <td><code>string <strong>+</strong> <em>string2</em></code></td>
    <td>
<pre><code>"Hello " <strong>+</strong> <em>"reader"</em>
# =&gt; "Hello reader"</code></pre>
      <p><code>"a" <strong>+</strong> <em>"b"</em> <strong>+</strong>
        <em>"c"</em>
        # =&gt; "abc"</code></p>
    </td>
    <td>Concatenates two or more strings together and returns the result.</td>
  </tr>
  <tr>
    <td>Substitute</td>
    <td>
<pre><code>string<strong>.gsub</strong><em>(a_string,
substitute)</em></code></pre>
    </td>
    <td>
<pre><code>"Hae"<strong>.gsub</strong><em>("ae", "ä")
# =&gt; "Hä"</em></code></pre>
<pre><code>"Hae"<strong>.gsub</strong><em>("b", "ä")
# =&gt; "Hae"</em></code></pre>
<pre><code>"Greenie"<strong>.gsub</strong><em>("e", "u")
# =&gt; "Gruuniu"</em></code></pre>
    </td>
    <td><em>gsub</em> stands for "globally substitute". It substitutes all
      occurrences of <code>a_string</code> within the string with
      <code>substitute</code>.</td>
  </tr>
  <tr>
    <td>Access</td>
    <td>
      <code>
        string<strong>[</strong><em>position</em><strong>]</strong>
      </code>
    </td>
    <td>
      <code>
        "Hello"<strong>[</strong><em>1</em><strong>]</strong> # =&gt; "e"
      </code>
    </td>
    <td>
      Access the character at the given position in the string. Be aware
      that the first position is actually position <em>0</em>.
    </td>
  </tr>
</tbody></table>


<h2 id="ruby-arrays">Arrays</h2>

<p>
  An array is an ordered collection of items which is indexed by numbers.
  So an array contains multiple objects that are mostly related to each
  other. So what could you do? You could store a collection of the names
  of your favorite fruits and name it <em>fruits</em>.
</p>

<p>
  This is just a small selection of things an Array can do. For more
  information have a look at the
  <a href="http://ruby-doc.org/core-2.0/Array.html">ruby-doc for Array</a>.
</p>

<table class="table table-striped">
  <tbody><tr>
    <th class="concept">Concept</th>
    <th class="usage">Usage</th>
    <th class="example">Examples</th>
    <th class="description">Description</th>
  </tr>
  <tr>
    <td>Create</td>
    <td>
      <code><strong>[</strong><em>contents</em><strong>]</strong></code>
    </td>
    <td>
      <p><code><strong>[]</strong></code></p>

      <p><code>
        <strong>[</strong><em>"Rails", "fun", 5</em><strong>]</strong>
      </code></p>
    </td>
    <td>Creates an Array, empty or with the specified contents.</td>
  </tr>
  <tr>
    <td>Number of elements</td>
    <td>
      <code>array<strong>.size</strong></code>
    </td>
    <td>
      <p><code>[]<strong>.size</strong> # =&gt; 0</code></p>

      <p><code>[1, 2, 3]<strong>.size</strong> # =&gt; 3</code></p>

      <p><code>["foo", "bar"]<strong>.size</strong> # =&gt; 2</code></p>
    </td>
    <td>Returns the number of elements in an Array.</td>
  </tr>
  <tr>
    <td>Access</td>
    <td>
      <code>
        array<strong>[</strong><em>position</em><strong>]</strong>
      </code>
    </td>
    <td>
<pre><code>array = ["hi", "foo", "bar"]
array<strong>[</strong><em>0</em><strong>]</strong> # =&gt; "hi"
array<strong>[</strong><em>2</em><strong>]</strong> # =&gt; "bar"</code></pre>
    </td>
    <td>As an Array is a collection of different elements, you often want
      to access a single element of the Array.
      Arrays are indexed by numbers so you can use a number
      to access an individual element. Be aware that the
      numbering actually starts with "0" so the first element
      actually is the 0th. And the last element of a three element
      array is element number 2.
    </td>
  </tr>
  <tr>
    <td>Adding an element</td>
    <td>
      <code>array <strong>&lt;&lt;</strong> <em>element</em></code>
    </td>
    <td>
<pre><code>array = [1, 2, 3]
array <strong>&lt;&lt;</strong> <em>4</em>
array # =&gt; [1, 2, 3, 4]
</code></pre>
    </td>
    <td>
      Adds the element to the end of the array,
      increasing the size of the array by one.
    </td>
  </tr>
  <tr>
    <td>Assigning</td>
    <td>
      <code>array<strong>[</strong><em>number</em><strong>] =
      </strong> <em>value</em></code>
    </td>
    <td>
<pre><code>array = ["hi", "foo", "bar"]
array<strong>[</strong><em>2</em><strong>] =</strong> <em>"new"</em>
array # =&gt; ["hi", "foo", "new"]</code></pre>
    </td>
    <td>Assigning new Array Values works a lot like accessing
      them; use an equals sign to set a new value. Voila!
      You changed an element of the array! Weehuuuuu!
    </td>
  </tr>
  <tr>
    <td>Delete at index</td>
    <td><code>
      array<strong>.delete_at</strong><em>(i)</em>
    </code></td>
    <td>
<pre><code>array = [0, 14, 55, 79]
array<strong>.delete_at</strong><em>(2)</em>
array # =&gt; [0, 14, 79]
</code></pre>
    </td>
    <td>
      Deletes the element of the array at the specified index. Remember
      that indexing starts at 0. If you specify an index larger than the
      number of elements in the array, nothing will happen.
    </td>
  </tr>
  <tr>
    <td>Iterating</td>
    <td>
      <code>array<strong>.each</strong> <em>do |e| .. end</em></code>
    </td>
    <td>
      <p><code>
        persons<strong>.each</strong> <em>do |p| puts p.name end</em>
      </code></p>

      <p><code>
        numbers<strong>.each</strong> <em>do |n| n = n * 2 end</em>
      </code></p>
    </td>
    <td>
      <p>
        "Iterating" means doing something for <em>each</em> element
        of the array. Code placed between <em>do</em> and <em>end</em>
        determines what is done to each element in the array.
      </p>

      <p>
        The first example prints the name of every person in the array to
        the console. The second example simply doubles every number of a
        given array.
      </p>
    </td>
  </tr>
</tbody></table>

<h2 id="ruby-hashes">Hashes</h2>

<p>
  Hashes associate a <em>key</em>  to some <em>value</em>. You may then retrieve the value based upon its key.
  This construct is called a <em>dictionary</em> in other languages, which is appropriate
  because you use the key to "look up" a value, as you would look up a definition for
  a word in a dictionary. Each key must be unique for a given hash but values can be repeated.
</p>

<p>
  Hashes can map from anything to anything! You can map from Strings to
  Numbers, Strings to Strings, Numbers to Booleans... and you can mix
  all of those! Although it is common that at least all the keys are of
  the same class. <em>Symbols</em> are especially common as keys. Symbols
  look like this: <code>:symbol</code>. A symbol is a colon followed by some
  characters. You can think of them as special strings that stand for
  (symbolize) something! We often use symbols because
  Ruby runs faster when we use symbols instead of strings.
</p>

<p>Learn more about hashes at
  <a href="http://www.ruby-doc.org/core-2.0/Hash.html">ruby-doc</a>.
</p>

<table class="table table-striped">
  <tbody><tr>
    <th class="concept">Concept</th>
    <th class="usage">Usage</th>
    <th class="hash-example">Examples</th>
    <th class="description">Description</th>
  </tr>
  <tr>
    <td>Creating</td>
    <td><code>
      <strong>{</strong>key <strong>=&gt;</strong> value<strong>}</strong>
    </code></td>
    <td>
      <p><code>
        <strong>{</strong>:hobby <strong>=&gt;</strong>
        "programming"<strong>}</strong>
      </code></p>
<pre><code><strong>{</strong>42 <strong>=&gt;</strong> "answer", "score" <strong>=&gt;</strong> 100,
 :name <strong>=&gt;</strong> "Tobi"<strong>}</strong>
</code></pre>
    </td>
    <td>
      You create a hash by surrounding the key-value pairs with curly
      braces. The arrow always goes from the <em>key</em> to the
      <em>value</em> depicting the meaning: <em>"This key points to this
      value."</em>. Key-value pairs are then separated by commas.
    </td>
  </tr>
  <tr>
    <td>Accessing</td>
    <td><code>hash<strong>[</strong>key<strong>]</strong></code></td>
    <td>
<pre><code>hash = {:key =&gt; "value"}
hash<strong>[</strong>:key<strong>]</strong> # =&gt; "value"
hash<strong>[</strong>foo<strong>]</strong> # =&gt; nil
</code></pre>
    </td>
    <td>
      Accessing an entry in a hash looks a lot like accessing it in
      an <em>array</em>. However with a hash the key can be anything, not
      just numbers. If you try to access a key that does not exist, the
      value <code>nil</code> is returned, which is Ruby's way of saying
      "nothing", because if it doesn't recognize the key it can't return
      a value for it.
    </td>
  </tr>
  <tr>
    <td>Assigning</td>
    <td>
      <code>hash<strong>[</strong>key<strong>] =</strong> value</code>
    </td>
    <td>
<pre><code>hash = {:a =&gt; "b"}
hash<strong>[</strong>:key<strong>] =</strong> "value"
hash # =&gt; {:a=&gt;"b", :key=&gt;"value"}
</code></pre>
    </td>
    <td>
      Assigning values to a hash is similar to assigning values to an
      array. With a hash, the key can
      be a number or it can be a symbol, string,
      number... or anything, really!
    </td>
  </tr>
  <tr>
    <td>Deleting</td>
    <td><code>hash<strong>.delete</strong><em>(key)</em></code></td>
    <td>
<pre><code>hash = {:a =&gt; "b", :b =&gt; 10}
hash<strong>.delete</strong><em>(:a)</em>
hash # =&gt; {:b=&gt;10}
</code></pre>
    </td>
    <td>
      You can delete a specified key from the hash, so that the key and its
      value can not be accessed.
    </td>
  </tr>
</tbody></table>

<h1 id="rails">Rails Basics</h1>

<p>This is an introduction to the basics of Rails. We look at the general
  structure of a Rails application and the important commands used in the terminal.
</p>

<p>
  If you do not have Rails installed yet, there is a
  <a href="http://railsapps.github.io/installing-rails.html">
    well maintained guide by Daniel Kehoe
  </a> on how to install Rails on different platforms.
</p>

<h2 id="rails-folder-structure">The Structure of a Rails app</h2>
Here is an overview of all the folders of a new Rails application, outlining
the purpose of each folder, and describing the most important files.
<table class="table table-striped">
  <tbody><tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>app</td>
    <td>This folder contains your application. Therefore it is the
      <strong>most important folder</strong> in Ruby on Rails and it is
      worth digging into its subfolders. See the following rows.
    </td>
  </tr>
  <tr>
    <td>app/assets</td>
    <td>Assets basically are your front-end stuff. This folder contains
      <em>images</em> you use on your website, <em>javascripts</em> for
      all your fancy front-end interaction and <em>stylesheets</em> for
      all your CSS making your website absolutely beautiful.
    </td>
  </tr>
  <tr>
    <td>app/controllers</td>
    <td>The controllers subdirectory contains the controllers, which
      handle the requests from
      the users. It is often responsible for a single resource type,
      such as places, users or attendees. Controllers also tie together
      the <em>models</em> and the <em>views</em>.
    </td>
  </tr>
  <tr>
    <td>app/helpers</td>
    <td>Helpers are used to take care of logic that is needed in the views
      in order to keep the views clean of logic and reuse that logic in
      multiple views.
    </td>
  </tr>
  <tr>
    <td>app/mailers</td>
    <td>Functionality to send emails goes here.</td>
  </tr>
  <tr>
    <td>app/models</td>
    <td>The models subdirectory holds the classes that model the business
      logic of our application. It is concerned with the things our
      application is about. Often this is data, that is also saved in the
      database. Examples here are a Person, or a Place class with all
      their typical behaviour.
    </td>
  </tr>
  <tr>
    <td>app/views</td>
    <td>
      <p>The views subdirectory contains the display templates that will
        be displayed to the user after a successful request.
        By default they are written in HTML with embedded ruby
        (.html.erb). The embedded ruby is used to insert data from the
        application. It is then converted to HTML and sent to the browser
        of the user. It has subdirectories for every resource of our
        application, e.g. places, persons. These subdirectories contain the
        associated view files.</p>

      <p>Files starting with an underscore (<em>_</em>) are called
        <em>partials</em>. Those are parts of a view which are reused in
        other views. A common example is <em>_form.html.erb</em> which
        contains the basic form for a given resource. It is used in the
        <em>new</em> and in the <em>edit</em> view since creating
        something
        and editing something looks pretty similar.
      </p>
    </td>
  </tr>
  <tr>
    <td>config</td>
    <td>This directory contains the configuration files that your
      application will need, including your database configuration (in
      <em>database.yml</em>) and the particularly important
      <em>routes.rb</em> which decides how web requests are handled.
      The <em>routes.rb</em> file matches a given URL with the
      <em>controller</em> which will handle the request.
    </td>
  </tr>
  <tr>
    <td>db</td>
    <td>Contains a lot of <em>database</em> related files.
      Most importantly the <em>migrations</em> subdirectory, containing
      all your database migration files. Migrations set up your
      database structure, including the attributes of your models. With migrations
      you can add new attributes to existing models or create new models.
      So you could add the <em>favorite_color</em> attribute to your
      Person model so everyone can specify their favorite color.
    </td>
  </tr>
  <tr>
    <td>doc</td>
    <td>Contains the documentation you create for your application. Not
      too important when starting out.
    </td>
  </tr>
  <tr>
    <td>lib</td>
    <td>Short for library. Contains code you've developed that is used in
      your application and may be used elsewhere. For example, this
      might be code used to get specific information from Facebook.
    </td>
  </tr>
  <tr>
    <td>log</td>
    <td>See all the funny stuff that is written in the console where you
      started the Rails server? It is written to your
      <em>development.log</em>. Logs contain runtime information
      of your application. If an error happens, it will be recorded
      here.
    </td>
  </tr>
  <tr>
    <td>public</td>
    <td>Contains static files that do not contain Ruby code, such as error pages.</td>
  </tr>
  <tr>
    <td>script</td>
    <td>By default contains what is executed when you type in the
      <em>rails</em> command. Seldom of importance to beginners.
    </td>
  </tr>
  <tr>
    <td>test</td>
    <td>Contains the tests for your application. With tests you make sure
      that your application actually does what you think it does. This
      directory might also be called <em>spec</em>, if you are using the
      RSpec gem (an alternative testing framework).
    </td>
  </tr>
  <tr>
    <td>vendor</td>
    <td>A folder for software code provided by others ("libraries"). Most
      often, libraries are provided as <em>ruby gems</em> and
      installed using the <em>Gemfile</em>. If code is not available as
      a ruby gem then you should put it here. This might be the case for
      jQuery plugins. Probably won't be used that often in the beginning.
    </td>
  </tr>
  <tr>
    <td>Gemfile</td>
    <td><p>A file that specifies a list of gems that are required to run
      your application. Rails itself is a gem you will find listed in the
      Gemfile. Ruby gems are self-contained packages of code, more generally
      called libraries, that add functionality or features to your application.
      </p>

      <p>If you want to add a new gem to your application,
        add "<strong>gem</strong> <em>gem_name</em>" to your Gemfile,
        optionally specifying a version number. Save the file and then run
        <em>bundle install</em> to install the gem.
      </p>
    </td>
  </tr>
  <tr>
    <td>Gemfile.lock</td>
    <td>This file specifies the exact versions of all gems you use. Because some
      gems depend on other gems, Ruby will install all you need
      automatically. The file also contains specific version numbers.
      It can be used to make sure that everyone within a team is working
      with the same versions of gems. The file is auto-generated.
      <em>Do not edit this file.</em></td>
  </tr>
</tbody></table>

<h2 id="rails-commands">Important Rails commands</h2>

<p>
  Here is a summary of important commands that can be used as you develop
  your Ruby on Rails app. You must be in the root directory of your project
  to run any of these commands (with the exception of the <em>rails new</em>
  command). The project or application root directory is the folder containing
  all the subfolders described above (app, config, etc.).
</p>

<table class="table table-striped">
  <tbody><tr>
    <th>Concept</th>
    <th>Usage</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Create a new app</td>
    <td><code><strong>rails new</strong> <em>name</em></code></td>
    <td>Create a new Ruby on Rails application with the given name here.
      This will give you the basic structure to immediately get started.
      After this command has successfully run your application is in a
      folder with the same name you gave the application. You have to
      <em>cd</em> into that folder.
    </td>
  </tr>
  <tr>
    <td>Start the server</td>
    <td><code><strong>rails server</strong></code></td>
    <td>
      <p>You have to start the server in order for your application to
        respond to your requests. Starting the server might take some time.
        When it is done, you can access your application under
        <a href="localhost:3000">localhost:3000</a> in the browser of your
        choice.</p>

      <p>In order to stop the server, go to the console where it is
        running and press <strong>Ctrl + C</strong></p>
    </td>
  </tr>
  <tr>
    <td>Scaffolding</td>
    <td>
      <code><strong>rails generate scaffold</strong>
        <em>name attribute:type</em></code>
    </td>
    <td>
      <p>
        The scaffold command magically generates all the common things needed
        for a new resource for you! This includes <em>controllers, models and views</em>. It
        also creates the following basic actions: create a new resource,
        edit a resource, show a resource, and delete a resource.
      </p>

      <p>That's all the basics you need. Take this example:</p>

      <p><code><strong>rails generate scaffold</strong> <em>product
        name:string price:integer</em></code></p>

      <p>Now you can create new products, edit them, view them and delete
        them if you don't need them anymore. Nothing stops you from
        creating a full fledged web shop now ;-)</p>
    </td>
  </tr>
  <tr>
    <td>Run migrations</td>
    <td><code><strong>rake db:migrate</strong></code></td>
    <td>When you add a new migration, for example by creating
      a new <em>scaffold</em>, the migration has to be applied to your database.
      The command is used to update your database.
    </td>
  </tr>
  <tr>
    <td>Install dependencies</td>
    <td><code><strong>bundle install</strong></code></td>
    <td>If you just added a new gem to your Gemfile you should run bundle
      install to install it. Don't forget to restart your server
      afterwards!
    </td>
  </tr>
  <tr>
    <td>Check dependencies</td>
    <td><code><strong>bundle check</strong></code></td>
    <td>Checks if the dependencies listed in Gemfile are satisfied by currently installed gems
    </td>
  </tr> 
  <tr>
    <td>Show existing routes</td>
    <td><code><strong>rake routes</strong></code></td>
    <td>Shows complete list of available routes in your application.</td>
  </tr>
</tbody></table>

<h2 id="rails-erb">ERB: Embedded Ruby</h2>
<p>
  In your views (that is, under <code>app/views</code> in your Rails app) you
  will find <code>.html.<strong>erb</strong></code> files. <strong>ERB</strong>
  stands for <strong>E</strong>mbedded <strong>R</strong>u<strong>B</strong>y.
  This just means that Rails processes some special tags in those files and
  produces HTML output to send back to the user.
</p>
<p>
  There are two ERB tags that you need to remember:
  <code>&lt;%= <i>ruby_code</i> %&gt;</code> and
  <code>&lt;% <i>ruby_code</i> %&gt;</code>. Notice that the difference is the
  <strong>=</strong> in the first tag.
</p>

<table class="table table-striped">
  <tbody><tr>
    <th class="usage">Tag</th>
    <th class="erb-example">Examples</th>
    <th class="description">Description</th>
  </tr>
  <tr>
    <td><code>&lt;%<strong>=</strong> %&gt;</code></td>
    <td><code><strong>&lt;%= @product.price %&gt;</strong></code></td>
    <td>
      It runs the Ruby code and inserts the result to the HTML at that position.
      You can put <em>any kind of Ruby code</em> between <code>&lt;%=</code> and
      <code>%&gt;</code>, for instance, <code>&lt;%= 9 * 3 %&gt;</code> will translate to
      <strong>27</strong> in the page that the user is viewing. However,
      typically this tag is used to display some data from a model, such as the
      price of a product, as shown in the example here.
    </td>
  </tr>
  <tr>
    <td><code>&lt;% %&gt;</code></td>
    <td>
<pre><code><strong>&lt;% if user.admin? %&gt;</strong>
  &lt;p&gt;Hello Admin!&lt;/p&gt;
&lt;% end %&gt;</code></pre></td>
    <td>
      The Ruby code between the delimiters <code>&lt;%</code> and <code>%&gt;</code>
      is run but the result will <strong>not</strong> be inserted at this point
      in the HTML. Therefore these tags are most commonly used for control flow
      structures such as an if statement in the example, or loops.
    </td>
  </tr>
</tbody></table>

<h1 id="editor">Editor tips</h1>

<p>
  When you write code you will be using a text editor. Of course each text
  editor is different and configurable. Here are just some functions and
  their most general short cuts. All of them work in
  <a href="https://sublimetext.com/2">Sublime Text 2</a>. Your editor may
  differ!
</p>

<p>
  The shortcuts listed here are for Linux/Windows. On a Mac you will have
  to replace <em>Ctrl</em> with <em>Cmd</em>.
</p>

<table class="table table-striped">
  <tbody><tr>
    <th>Function</th>
    <th class="shortcut">Shortcut</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Save file</td>
    <td><strong>Ctrl + S</strong></td>
    <td>
      Saves the currently open file. If it was a new file you may also be
      asked where to save it.
    </td>
  </tr>
  <tr>
    <td>Undo</td>
    <td><strong>Ctrl + Z</strong></td>
    <td>
      Undo the last change you made to the current file. Can be applied
      multiple times in succession to undo multiple changes.
    </td>
  </tr>
  <tr>
    <td>Redo</td>
    <td><p><strong>Ctrl + Y</strong></p>

      <p><em>or Ctrl + Shift + Z</em></p></td>
    <td>
      Redo what you just undid with <em>undo</em>, can also be done
      multiple times.
    </td>
  </tr>
  <tr>
    <td>Find in File</td>
    <td><strong>Ctrl + F</strong></td>
    <td>
      Search for a character sequence within the currently open file.
      Hit <em>Enter</em> to progress to the next match.
    </td>
  </tr>
  <tr>
    <td>Find in all Files</td>
    <td><strong>Ctrl + Shift + F</strong></td>
    <td>Search for a character sequence in all files of the project.</td>
  </tr>
  <tr>
    <td>Replace</td>
    <td>
      <p><strong>Ctrl + H</strong></p>

      <p><em>or Ctrl + R</em></p>
    </td>
    <td>
      Replace occurrences of the supplied character sequence with the
      other supplied character sequence. Useful when renaming something.
    </td>
  </tr>
  <tr>
    <td>Copy</td>
    <td><strong>Ctrl + C</strong></td>
    <td>
      Copy the currently highlighted text into the clipboard.
    </td>
  </tr>
  <tr>
    <td>Cut</td>
    <td><strong>Ctrl + X</strong></td>
    <td>Copy the highlighted text into the clipboard but delete it.</td>
  </tr>
  <tr>
    <td>Paste</td>
    <td><strong>Ctrl + V</strong></td>
    <td>
      Insert whatever currently is in the clipboard (through
      <em>Copy</em> or <em>Cut</em>) at the current caret position.
      Can insert multiple times.
    </td>
  </tr>
  <tr>
    <td>New File</td>
    <td><strong>Ctrl + N</strong></td>
    <td>Create a new empty file.</td>
  </tr>
  <tr>
    <td>Search and open file</td>
    <td><strong>Ctrl + P</strong></td>
    <td>
      Search for a file giving part of its name (<em>fuzzy search</em>).
      Pressing <em>enter</em> will open the selected file.
    </td>
  </tr>
  <tr>
    <td>Comment</td>
    <td><strong>Ctrl + /</strong></td>
    <td>
      Marks the selected text as a comment, which means that it will
      be ignored. Useful when you want to see how something behaves or looks
      without a specific section of code being run.
    </td>
  </tr>
</tbody></table>

<h1 id="help">Help: What to do when things go wrong?</h1>

<p>
  Things go wrong all the time. Don't worry, this happens to everyone.
  So keep calm. When you encounter an error, just google the error message.
  For best results, add the keywords "rails" or "ruby". Results from
  <a href="http://stackoverflow.com/questions/tagged/ruby-on-rails?sort=newest">stackoverflow.com</a>
  are often really helpful. Look for those! The most experienced developers do this frequently ;-).
  </p>

<p>
  Here are common mistakes with a little checklist:
</p>

<ul>
  <li>Have you run <em>rake db:migrate</em> to apply the newest database
    migrations?
  </li>
  <li>Have you really saved the file you just changed? Unsaved files are
    often marked in the editor via an asterisk or a point next to their
    name.
  </li>
  <li>If you just added a gem to the Gemfile, have you run <em>bundle
    install</em> to install it?
  </li>
  <li>If you just installed a gem, have you restarted the server?</li>
</ul>

<p>
  Do you need more beginner friendly in depth information about Ruby on Rails?
  We have started to gather free tutorials and learning material on a
  <strong><a href="resources.html">resources</a></strong> page! Please give
  feedback about your
  favorite tutorials and lessons!
</p>

  </div>
