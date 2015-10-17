# Essentials!

##Arrays
Arrays are one type of list that can be used to group and organize multiple pieces of data.  You can ordered list that can be visualized as a two-column table. Left column is the index and the right column is the thing you're listing.  For example, imagine a bucket list:

| Index | Bucket List Item |
| --- | --- |
| 0 | Go sky diving | 
| 1 | Visit Antarctica |
| 2 | Climb Mt. Everest |

+ Notice that the index starts at 0. This is a quirk about data structures in computer science that you just have to memorize.
+ So how do we translate this table into code in Swift?
  + var bucket_list = `["Go sky diving", "Visit Antartica", "Climb Mt. Everest"]`

ACCESSING ITEMS IN AN ARRAY
+ We access items in an array using the brackets and the index of the thing you want.
If we want to get to the second element in 'bucket_list' we can say
`bucket_list[1]`
  + 
ASSIGNING ITEMS
+ So what if we want to change one of the items in the array?
`bucket_list[2] = "take a nap"` will re-assign the third item in the array to 'take a nap'.

ADD AND REMOVE ITEMS
+ We can also add and remove items from an array.
+ `bucket_list.append("graduate from Flatiron")` will add an item with the contents of the argument to the end of the array it is called on. 
+ `bucket_list.removeAtIndex[1]` will delete the item at index 1.

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
