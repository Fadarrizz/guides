---
title: File Handling
---
## File Handling

In C language, we use a structure <b>pointer of file type</b> to declare a file.
 
<pre class="c">FILE <b>*fp</b>;
</pre>
  
#### More Information:

C provides a number of functions that helps to perfrom basic file operations. Following are the functions:

<table class="table table-bordered table-striped">
<tbody><tr><th>Function</th><th>description</th></tr>
<tr><td>fopen()</td><td>create a new file or open a existing file</td></tr>
<tr><td>fclose()</td><td>closes a file</td></tr>
<tr><td>getc()</td><td>reads a character from a file</td></tr>
<tr><td>putc()</td><td>writes a character to a file</td></tr>
<tr><td>fscanf()</td><td>reads a set of data from a file</td></tr>
<tr><td>fprintf()</td><td>writes a set of data to a file</td></tr>
<tr><td>getw()</td><td>reads a integer from a file</td></tr>
<tr><td>putw()</td><td>writes a integer to a file</td></tr>
<tr><td>fseek()</td><td>set the position to desire point</td></tr>
<tr><td>ftell()</td><td>gives current position in the file</td></tr>
<tr><td>rewind()</td><td>set the position to the begining point</td></tr>
</tbody></table>

## Opening a File of Creating a File

The ```fopen()``` function is used to create a new file or to open an existing file.

#### General Syntax:

<pre class="c">*fp = FILE <b>*fopen</b>(const char <i>*filename</i>, const char <i>*mode</i>);
</pre>

Here <b>filename</b> is the name of the file to be opened and <b>mode</b> specifies the purpose of opening the file. Mode can be of following types:

<b>*fp</b> is the FILE pointer (```FILE *fp```), which will hold the reference to the opened (or created) file.

<table class="table table-bordered table-striped">
<tbody><tr><th>mode</th><th>description</th></tr>
<tr><td>r</td><td>opens a text file in reading mode</td></tr>
<tr><td>w</td><td>opens or create a text file in writing mode.</td></tr>
<tr><td>a</td><td>opens a text file in append mode</td></tr>
<tr><td>r+</td><td>opens a text file in both reading and writing mode</td></tr>
<tr><td>w+</td><td>opens a text file in both reading and writing mode</td></tr>
<tr><td>a+</td><td>opens a text file in both reading and writing mode</td></tr>
<tr><td>rb</td><td>opens a binary file in reading mode</td></tr>
<tr><td>wb</td><td>opens or create a binary file in writing mode</td></tr>
<tr><td>ab</td><td>opens a binary file in append mode</td></tr>
<tr><td>rb+</td><td>opens a binary file in both reading and writing mode</td></tr>
<tr><td>wb+</td><td>opens a binary file in both reading and writing mode</td></tr>
<tr><td>ab+</td><td>opens a binary file in both reading and writing mode</td></tr>
</tbody></table>

## Closing a file

The ```fclose()``` function is used to close an already openend file.

#### General Syntax:
<pre class="c">int <b>fclose</b>( FILE <i>*fp</i> );
</pre>

Here fclose() function closes the file and returns <b>zero</b> on success, or <b>EOF</b> if there is an error in closing the file. This <b>EOF</b> is an constant defined in the header file <b>stdio.h</b>

