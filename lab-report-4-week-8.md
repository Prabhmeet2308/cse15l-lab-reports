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
![WhatsApp Image 2022-05-22 at 9 20 31 PM](https://user-images.githubusercontent.com/103228599/169742776-5eb5e8cc-5667-4aeb-b521-0d0a190baf56.jpeg)

### Their Repo Output
![WhatsApp Image 2022-05-22 at 10 00 42 PM](https://user-images.githubusercontent.com/103228599/169746848-8d2abe62-7ed9-46c3-b75c-de8a741ddea4.jpeg)

### Fix
The main problems arrises when the back ticks are used. So creating method to 
deal with the code blocks. We would want to ignore anything in a code block.
So creating a method that removes actual code segments/block from the getLinks 
method, being careful to no remove ones like the [another link](`google.com)` 
example because it doesn't actually function as a code segment because of the 
brackets.


## Snippet 2
### Expected
![WhatsApp Image 2022-05-22 at 9 46 46 PM](https://user-images.githubusercontent.com/103228599/169745345-8da3cba7-37a6-4d48-8f04-f3f581bcf35a.jpeg)

There are 3 links: `nested link`, `a nested paranthesized url`, and `some escaped [ bracket ]`

**MarkdownParse:** [a.com, a.com(()), example.com]

### Tester
Gets the path of file, then it reads the file. Then it runs the getLinks method 
on the file. Following that it makes a list of the expected output. Then tests 
if they are equivalent

![WhatsApp Image 2022-05-22 at 9 09 14 PM (1)](https://user-images.githubusercontent.com/103228599/169741776-44cba3d0-6ae7-4a51-a208-4774631438ee.jpeg)

### My Repo Output

![WhatsApp Image 2022-05-22 at 9 20 31 PM (1)](https://user-images.githubusercontent.com/103228599/169742793-88bb12f3-0f9c-4620-a433-a90921938917.jpeg)

### Their Repo Output
![WhatsApp Image 2022-05-22 at 10 00 42 PM (1)](https://user-images.githubusercontent.com/103228599/169746873-cf905cd4-0ffb-4004-ba7b-d6cd04556030.jpeg)

### Fix
The main problem with snippet 2 is the parantheses inside the link, which we 
would need to include a way to deal with the parantheses within the link by 
either counting them the way markdown likely does (with a stack data
structure) in order to keep track of the parentheses.

## Snipet 3
### Expected
![WhatsApp Image 2022-05-22 at 9 47 00 PM](https://user-images.githubusercontent.com/103228599/169745360-f29fc994-662e-48e9-86a3-7224e696c556.jpeg)

There is 3 links: `this title text is really long and takes up more than one line and has some line breaks`, `https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedu` (this one doesn't use the markdown formatting it's just a link), `this link doesn't have a closing parenthesis for a while` 

**MarkdownParse:** [https://www.twitter.com, https://cse.ucsd.edu/]

### Tester
Gets the path of file, then it reads the file. Then it runs the getLinks method 
on the file. Following that it makes a list of the expected output. Then tests 
if they are equivalent

![WhatsApp Image 2022-05-22 at 9 09 14 PM (2)](https://user-images.githubusercontent.com/103228599/169741783-96aba29a-0ed9-4440-93d5-a4d249abd644.jpeg)

### My Repo Output
![WhatsApp Image 2022-05-22 at 9 20 31 PM (2)](https://user-images.githubusercontent.com/103228599/169742824-fc4f25c8-e518-4051-96d7-4f4e25768cc6.jpeg)


### Their Repo Output
![WhatsApp Image 2022-05-22 at 10 00 42 PM (2)](https://user-images.githubusercontent.com/103228599/169746885-7b91e07b-2d78-4e5e-b664-a03b140b1558.jpeg)

### Fix
The main problems is dealing with new lines (\n) so when creating the list of
links it should not allow for new line charaters. Long with a way to ensure
that the problem with the cse link is solved as well and read as a link. That 
problem probably arrises because of the github link doesn't have a end parantheses
which throws everything off for the rest of the file so a way to reset in case 
of a mistype like this.
