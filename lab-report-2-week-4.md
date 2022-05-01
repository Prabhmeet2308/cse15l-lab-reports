# Lab report 2
For lab report 2 we worked together with our group to debug and improve a program by making 3 changes to it.
## Orignal Code 
<img width="818" alt="Screenshot 2022-04-24 at 9 41 07 PM" src="https://user-images.githubusercontent.com/103228599/165022049-717b6546-3e90-4c25-aa86-0ce8349af3c0.png">

## Updates made in the file
* **Change one**- Adding if condition for each bracket and parenthesis which breaks if not found(-1)
 ![WhatsApp Image 2022-04-24 at 9 54 02 PM](https://user-images.githubusercontent.com/103228599/165023226-cfddc9f7-af29-4bf0-9677-29f980072795.jpeg)
* **Change two**- Adding if statement in main to avoid no input or file with no input
   <img width="661" alt="Screenshot 2022-04-24 at 10 15 26 PM" src="https://user-images.githubusercontent.com/103228599/165024843-8e05956a-57f8-4d8e-9c52-e00c9c90aa56.png">
   <img width="588" alt="Screenshot 2022-04-30 at 8 20 45 PM" src="https://user-images.githubusercontent.com/103228599/166130778-bbe0796a-c1f2-496d-a13f-e0fb9cca95a9.png">


* **Change three**- Adding if statement to insure no invalid characters are present in the list
  <img width="1023" alt="Screenshot 2022-04-24 at 10 09 55 PM" src="https://user-images.githubusercontent.com/103228599/165024425-2f64c88a-7800-4eaa-be79-7a259e934b08.png">
  
  
## Error Inducing Test file

 **Change 1**- Since the first link started but never ended the it was stuck in an infinite loop which made us add if loops to break if parameter not found
 
 [myfile.md](https://github.com/Prabhmeet2308/markdown-parser/blob/main/myfile.md)
 
 **Change 2**- It was an error which was made to insure a file was inputted no error inducing test file
 
 **Change 3**- The program doesn't make sure that the link exist one. We wanted to improve on one factors to remove invalid links is links which cotain characters that cannot be used in a link like \[ \] { }
 
 [myfile2.md](https://github.com/Prabhmeet2308/markdown-parser/blob/main/myfile2.md)

## Symptoms of the Errors

* **Error before Change 1**

  <img width="714" alt="Screenshot 2022-04-24 at 10 49 34 PM" src="https://user-images.githubusercontent.com/103228599/165028124-c397b976-46bc-4599-8683-fad0705b57a5.png">
* **Error before change 2**

  <img width="814" alt="Screenshot 2022-04-24 at 10 50 48 PM" src="https://user-images.githubusercontent.com/103228599/165028274-0e997a44-5eb0-4bf7-b913-9da29c7d62e9.png">
* **Error before change 3**


  <img width="567" alt="Screenshot 2022-04-24 at 10 53 28 PM" src="https://user-images.githubusercontent.com/103228599/165028566-48066b9d-86a5-40b0-8c0d-36ff40b40429.png">

## About the Errors
### Error 1: Incomplete Links
**Bug:** The code lacked a way to deal with a situation when a link started but did not end or the brackets were not in the link sequence

**Symptom:** The symptom was an error message not allowing for the code to compile with a StringIndexOutOfBoundsException


### Error 2: No arguments provided
**Bug:** The code lacked a way to deal with a situation if no argument was provided to getlinks method

**Symptom:** The symptom was an error message not allowing for the code to compile with a ArrayIndexOutOfBoundsException


### Error 3: Invalid links
**Bug:** The code does not filter invalid links

**Symptom:** Does not remove invalid links which contain invalid characters from the list of links



 
