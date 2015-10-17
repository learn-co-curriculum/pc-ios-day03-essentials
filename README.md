# Essentials!

##Arrays
Arrays are one type of list that can be used to group and organize multiple pieces of data.  

+ Array == an ordered list that can be visualized as a two-column table. Left column is the index and the right column is the thing you're listing (Draw on board, using bucket list as an example):

| Index | Bucket List Item |
| --- | --- |
| 0 | Go sky diving | 
| 1 | Visit Antarctica |
| 2 | Climb Mt. Everest |

+ Notice that the index starts at 0. This is a quirk about data structures in computer science that you just have to memorize.
+ So how do we translate this table into code?
  + `["Danny", "Lyel", "Victoria", "Vanessa"]`
  + Remember that the names are data so must be in quotes as strings.
  + We use square brackets to denote an array.
  + We don't explicitly write the index anywhere. (show the index above each item on the board)
+ Assign the array to a variable so that when we call the variable name, we have the array returned to us.
+ Have students create their own bucket list array of their choice and assign it to a variable.

ACCESSING ITEMS IN AN ARRAY
+ What if I want to get the third item listed in my array?
+ We access items in an array using the brackets and the index of the thing you want.
  + `names[3]` will give me what? (the fourth item). how do I get the third item?
  + 
ASSIGNING ITEMS
+ So what if we want to change one of the items in the array?
`names[2] = "Joe"` will re-assign the third item in the array to Joe.

ADD AND REMOVE ITEMS
+ We can also add and remove items from an array.
+ `names.push("Alfred")` will add an item with the contents of the argument to the end of the array it is called on. You can also use `<<` like so: `names << "Alfred"`.
+ `names.pop` will remove the last item in an array.
+ `names.delete_at(3)` will delete the item at index 3.
+ `names.insert(2, "Dan")` will insert the item at the index you specify in the first argument.
+ Here are some other cool methods: .length, .reverse, .sample, .sort
+ [Mini-Lab: Manipulating arrays](https://GitHub.com/learn-co-curriculum/hs-manipulating-arrays-mini-lab) (start with array and then have 10 instructions, what does array look like at the end?)
  + Answer: `["Peru", "Laos", "Chad", "Cuba", "Togo", "Iraq", "Iran", "Mali", "Oman", "Fiji"]`

##Dictionaries
+ Hashes are the second data structure we're going to talk about. 
+ Hashes give context to data (a bunch of ages without names to associate them with mean nothing), it's a additional data dimension. 
+ They are like two column tables. The difference is that for an array the left side of the column is the index, for hashes there is no numbered index, but there is another piece of data on the left side of the table, called the **key**.

####Hash

| Key | Value |
| --- | --- |
| "Danny" | "December 3" | 
| "Victoria" | "December 2" |
| "Vanessa" | "September 16" |

####Array Example for Comparison
 
| Index | Item |
| --- | --- |
| 0 | "Danny" |
| 1 | "Victoria" |
| 2 | "Vanessa" |

+ We use hashes when we have a piece of data tied to another piece of data. We call this a key-value pair. The key in a hash has to be unique, because it's how we access values from the hash. 
+ We write a hash like this: `names_hash = { "Danny" => "December 3", "Victoria" => "December 2" }`

ACCESSING DATA IN A HASH
+ Now we don't have indices, but we have keys. Given what we know about arrays, how do you think we'd access a value from a hash?
  + `names_hash["Danny"]` returns `"December 3"`
+ Knowing what we know about arrays, how would we change a key-value pair's value?
  + `names_hash["Victoria"] = "December 1"`
+ To add a new key-value pair we use the same syntax:
  + `names_hash["Lyel"] = "April 1st"`
+ To delete we use `names_hash.delete("Lyel")` to remove the pair.
+ Sometimes we use a data type called a symbol for the key in a hash. Symbols are unique, which means that they can only exist once in Ruby code, which is convenient because keys in a hash are unique. (CS - one to one/many relationships?) A symbol is made up of a colon (:) and a set of characters. Let's create a new hash, but use symbols instead of strings for the keys.
+ Hash methods to look at: .values, .keys, .length, .include?

ITERATING THROUGH HASHES
+ Let's learn about iteration in hashes, just like we did for arrays. For arrays we only wanted to loop through and do something to the value, but since a hash has a pair of data, we can use them both with `.each`. Say I want to print a string for each key-value pair that reads: `"#{name} has a birthday on #{birth_date}`.  We do this with the `.each` method: 

######OPTIONAL:  Allow students at this point to write out the .each method on their whiteboards.

```ruby
names_hash.each do |key, value|
    puts "#{key} has a birthday on #{value}.
  end
```
+ We can replace the key and value placeholders with anything we want, these are just placeholders. Just remember that the first one is for the key and the second is always representing the value.
+ [Iteration with hashes Mini-Lab](https://GitHub.com/learn-co-curriculum/hs-hash-iteration-mini-lab)

NESTED DATA STRUCTURES *This material is bonus - think of it as nice-to-have*
+ Hashes and Arrays can occur inside of other hashes and arrays. How do we pull individual items out if this is the case?
```ruby
salad_ingredients = [
      ["romaine", "kale", "spring mix"],
      ["tomatoes", "avocado", "beets"],
      ["vinaigrette", "ranch", "ginger-soy"]
    ]
```
This data would be much better represented as a hash (explain why). Can you help me convert it?
```ruby
salad_ingredients ={ 
  :lettuce => ["romaine", "kale", "spring mix"],
  :veggie => ["tomatoes", "avocado", "beets"],
  :dressing => ["vinagrette", "ranch", "ginger-soy"] 
}
```

##Random Function
