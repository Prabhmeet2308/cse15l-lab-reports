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


All the ones you see above, the test case were in the correct format of `[]()`. However, depeneding on how the link was written, the downloaded Markdown would somtimes not print, while my Markdown printed everything regardless. For example `test-file 567` was: 

<img width="663" alt="Screen Shot 2022-06-02 at 10 55 39 AM" src="https://user-images.githubusercontent.com/103228539/171695624-2720d551-c325-4bf4-bf26-0718b81b0f8b.png">

And here are the differences in the results:

<img width="975" alt="vimdiff3" src="https://user-images.githubusercontent.com/103228539/171695760-8d457130-45e8-43be-97b1-f1559bc4475b.png">

I was supoosed to not print anything, but my Markdown only recognizes the correct format so it prints it as a link. This would be the common problem seen throughout the lab.

## Conclusion

This then concluded our 9th CSE15L lab on using a script to run many files and comparing two implementations
