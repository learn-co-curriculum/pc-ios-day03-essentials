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
+ So how do we translate this table into code in Swift?
  + var name_array = `["Danny", "Lyel", "Victoria", "Vanessa"]`
  + Remember that the names are data so must be in quotes as strings.


ACCESSING ITEMS IN AN ARRAY
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
+ Hashes give context to data (a bunch of ages without names to associate them with mean nothing), it's an additional data dimension. 
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
