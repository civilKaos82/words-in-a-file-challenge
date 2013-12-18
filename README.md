# Words In A File 
 
##Learning Competencies 

##Summary 

 You can use Ruby to read from and write to files.
  
In this challenge, you will parse a file and then print out data about the contents of the file.

This challenge was inspired by [this exercise](http://programmingpraxis.com/2009/03/10/word-frequencies/) from [Programming Praxis](http://programmingpraxis.com/).

## Objectives

### Parse the file

Write a program that takes a filename and a parameter `n` and prints the `n` most common words in the file, and the count of their occurrences, in descending order.

The source file is provided in the original gist.

Sample interface:

```ruby
most_common_words('some_file.txt', 3)  # prints => 
> 'apples': 18 occurrences
> 'oranges': 13 occurrences
> 'melons': 9 occurrences
```


### Build a filter

Your results most likely included a lot of little words such as `a`, `the`, `and`, etc.  
      
Rewrite your program to filter out the noise so that your results paint a more accurate picture of the data in the file, i.e. it only counts "non-trivial" words like nouns and verbs, not prepositions or conjunctions.


### Pick a new file and get creative

Use your program to parse another file of your choice.  (If you want to get creative, try using a funky [ipsum generator](http://wpmu.org/12-lorem-ipsum-generators-that-make-dummy-text-more-fun/).
      
Modify your program to display other data about the file.  What are the least used words?  The longest sentences?  How many words?
      
Get creative and build other ways to parse the data.  Write up a blog post and share your results!
 

##Releases
###Release 0 

##Optimize Your Learning 

##Resources