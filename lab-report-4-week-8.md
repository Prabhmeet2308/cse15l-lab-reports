# Lab Report 4

[My Markdown Repo](https://github.com/Prabhmeet2308/markdown-parser)

[Other Group Markdown Repo](https://github.com/ehsly/markdown-parser)

## Snippet 1
### Expected
<img width="390" alt="Screenshot 2022-05-22 at 9 03 12 PM" src="https://user-images.githubusercontent.com/103228599/169741109-14841253-7abc-4a2f-8e49-72c7ced38408.png">

There is 1 link: `another link`

**MarkdownParse:** [&#96;google.com]

### Tester
Gets the path of file, then it reads the file. Then it runs the getLinks method 
on the file. Following that it makes a list of the expected output. Then tests 
if they are equivalent

![my repo tester 1](https://user-images.githubusercontent.com/103228599/169741609-8476925e-055c-4e06-9b5f-aeeb967d5ee9.jpeg))

### My Repo Output
![WhatsApp Image 2022-05-22 at 9 09 14 PM](https://user-images.githubusercontent.com/103228599/169742593-4f4a9185-7d5b-448b-9324-70dac0034990.jpeg)

### Their Repo Output
![theirop1](report4-snips/theirFail1.png)

### Fix
The main problems arrises when the back ticks are used. So creating method to 
deal with the code blocks. We would want to ignore anything in a code block.
So creating a method that removes actual code segments/block from the getLinks 
method, being careful to no remove ones like the [another link](`google.com)` 
example because it doesn't actually function as a code segment because of the 
brackets.


## Snippet 2
### Expected
![exp snip 2](report4-snips/Screenshot%202022-05-21%20142857.png)

There are 3 links: `nested link`, `a nested paranthesized url`, and `some escaped [ bracket ]`

**MarkdownParse:** [a.com, a.com(()), example.com]

### Tester
Gets the path of file, then it reads the file. Then it runs the getLinks method 
on the file. Following that it makes a list of the expected output. Then tests 
if they are equivalent

![WhatsApp Image 2022-05-22 at 9 09 14 PM (1)](https://user-images.githubusercontent.com/103228599/169741776-44cba3d0-6ae7-4a51-a208-4774631438ee.jpeg)

### My Repo Output

![WhatsApp Image 2022-05-22 at 9 09 14 PM (1)](https://user-images.githubusercontent.com/103228599/169742614-a02ab104-f2d6-475b-a496-1f81a36804b5.jpeg)

### Their Repo Output
![theirop2](report4-snips/theirFail2.png)

### Fix
The main problem with snippet 2 is the parantheses inside the link, which we 
would need to include a way to deal with the parantheses within the link by 
either counting them the way markdown likely does (with a stack data
structure) in order to keep track of the parentheses.

## Snipet 3
### Expected
![exp snip 3](report4-snips/Screenshot%202022-05-21%20143254.png)

There is 3 links: `this title text is really long and takes up more than one line and has some line breaks`, `https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedu` (this one doesn't use the markdown formatting it's just a link), `this link doesn't have a closing parenthesis for a while` 

**MarkdownParse:** [https://www.twitter.com, https://cse.ucsd.edu/]

### Tester
Gets the path of file, then it reads the file. Then it runs the getLinks method 
on the file. Following that it makes a list of the expected output. Then tests 
if they are equivalent

![WhatsApp Image 2022-05-22 at 9 09 14 PM (2)](https://user-images.githubusercontent.com/103228599/169741783-96aba29a-0ed9-4440-93d5-a4d249abd644.jpeg)

### My Repo Output
![WhatsApp Image 2022-05-22 at 9 09 14 PM (2)](https://user-images.githubusercontent.com/103228599/169742624-deb0a743-3419-4df9-a543-0ea7c3167a86.jpeg)

### Their Repo Output
![myop3](report4-snips/theirFail3.png)

### Fix
The main problems is dealing with new lines (\n) so when creating the list of
links it should not allow for new line charaters. Long with a way to ensure
that the problem with the cse link is solved as well and read as a link. That 
problem probably arrises because of the github link doesn't have a end parantheses
which throws everything off for the rest of the file so a way to reset in case 
of a mistype like this.
