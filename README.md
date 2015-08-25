# Words In A File

## Summary
In this challenge, we're going to use Ruby to read the contents of a file.  We're going to write a method that counts how many times unique words occur in a given file.

Specific details for how our method should behave will be revealed in the *Releases* section of the challenge.  We'll be told how our method should behave.  We'll have to discover how to implement the behavior.  This will involve forming good questions, finding good resources, and reading through documentation.  All of these are skills that we need as developers.

*Note:* This challenge was inspired by an [exercise] from [Programming Praxis].

## Releases
### Release 0: Find the Most Common Words
```ruby
def most_frequent_words(filename, count = 5)
  # Implement method ...
end

most_frequent_words('some_file.txt', 3)
# => { "the" => 35, "I" => 20, "a" => 19 }

most_frequent_words('some_file.txt', 4)
# => { "the" => 35, "I" => 20, "a" => 19, "like" => 10 }
```
*Figure 1*. Determining the three most frequent words in a given file. 

Let's start by writing a basic version of our method.  When we call the method, we'll pass in the file we want to parse and the number of most frequently occurring words we want returned.  The method should count how many times unique words occur in the given file and return the specified number of most frequently occurring words.

A test file has been set up to include a reference to a text file that we can use for testing (see `spec/support/test.txt`).  However, no tests have been written.  We'll need to write them ourselves.


### Release 1: Filter Articles, Conjunctions, Prepositions, etc.
Our results most likely include a lot of words like *a*, *the*, *and*, *of*, etc.  Let's update our method to filter out this noise so that the results are more reflective of the content in the file.  In other words, our method should only count non-trivial words like nouns and verbs, not articles, prepositions, conjunctions, etc.

We'll need to update our test suite to match this behavior.


### Release 2: Refactor for Single Responsibility
For what is our one method responsible?  If we think about what needs to happen for our method to function properly, there is surely more than one step: read in the contents of a file, parse the words from the rest of the characters, keep track of how often a word occurs, find the most frequently occurring, etc.

It's best practice to write methods that do one thing.  Is our method doing just one thing, or does it do more than that?  Let's refactor our method by extracting out the different bits of work into their own methods.

We'll need to make sure that our tests don't break as we refactor.


### Release 3: Code Reuse
Let's add some functionality.  Let's start with a method for returning the least frequent words.  If we've extracted single responsibility methods from our original `most_frequent_words` method, we should be able to reuse them.  After all, the steps should be the same until we actually select the words to return.

Get creative and build other ways to parse the data. How many words are in the file?  How many words occur a specific number of times?


## Resources

[exercise]: http://programmingpraxis.com/2009/03/10/word-frequencies/
[Programming Praxis]: http://programmingpraxis.com/
