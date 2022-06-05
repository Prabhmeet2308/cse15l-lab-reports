# CSE15L Week 10 Lab Report
This is the Lab Report for Week 10 of CSE15L, due on the 5th of June, 2022. In this lab we were experimented with the many tests provided for usunder the test-files/ folder, and comparing the results.

## Beginning Process

We were first given access to this [github repository](https://github.com/nidhidhamnani/markdown-parser), in which we used `git clone` to put it into our `ieng`. We then ran the `make test` command, and although most there were some failures, all of it compiled. 

Now to test all the tests in the `test-files` folder we ran the `time bash script.sh`. Then, to make it more create as to which test each result came from, in `script.sh` we added the line `echo "Test file name is: ${file}"` where now if we ran it would also print the title of the file along with the result. 

However, showing the outpot in terminal was time consuming so we used the command `bash script.sh > results.txt` which would make the file `results.txt` with the entire output there.

Then use `cp -r cse15lsp22-markdown-parser/test-files my-markdown-parser/` and `cp cse15lsp22-markdown-parser/script.sh my-markdown-parser/` to copy the files from the repository you just copied from that day's lab into your own repository. Then run `bash script.sh > results.txt` again, but in your own respository to get the results of the test files when it runes on your Markdown File.

Finally , use the command `$ vimdiff my-markdown-parser/results.txt cse15lsp22-markdown-parser/results.txt` to use vimdiff to compare the 2 result files to see the differences between the results.

## Vimdiff 

A pattern that can be seen throughout the results is that my Markdown-Parse had extra results while the downloaded Markdown-Parser had just `[]`. 

![vimdiff results](https://user-images.githubusercontent.com/103228599/172040087-d623b209-bc7a-463e-b956-d8369cdccf7d.jpeg)


All the ones you see above, the test case were in the correct format of `[]()`. However, depeneding on how the link was written, the downloaded Markdown would not print, while my Markdown printed everything regardless.

### Expected Output  

![WhatsApp Image 2022-06-05 at 12 28 52 AM](https://user-images.githubusercontent.com/103228599/172040356-a11e38e0-e827-457f-80b6-69665f21930f.jpeg)

[link for test-file 507](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/507.md)

The links printed for test 506 and 508 are vald that is my markdown parse is working correctly whereas there is a bug in the given markdown-parser.
For test 507 there are 2 set of double quoatations which make it an invalid link which my my markdown-parse did not recognize as a condition.


![WhatsApp Image 2022-06-05 at 12 43 17 AM](https://user-images.githubusercontent.com/103228599/172040758-8a0c51b5-7e9a-416e-8525-012b49f9993c.jpeg)

A condition should be added after this to check if there are 2 sets of double quotation within the link and if the link pass the test it should add it to toreturn.


## Conclusion

This then concluded our 9th CSE15L lab on using a script to run many files and comparing two implementations
