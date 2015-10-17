# Essentials!

##Arrays
Arrays are a type of list that can be used to group and organize multiple pieces of data.  You can ordered list that can be visualized as a two-column table. Left column is the index and the right column is the thing you're listing.  For example, imagine a bucket list:

| Index | Bucket List Item |
| --- | --- |
| 0 | Go sky diving | 
| 1 | Visit Antarctica |
| 2 | Climb Mt. Everest |

+ Notice that the index starts at 0. This is a quirk about data structures in computer science that you just have to memorize.
+ So how do we translate this table into code in Swift?
  + var bucket_list = `["Go sky diving", "Visit Antartica", "Climb Mt. Everest"]`

**Accessing an item in an array**
+ We access items in an array using the brackets and the index of the thing you want.
If we want to get to the second element in 'bucket_list' we can say
`bucket_list[1]`
  + 
*Assigning items**
+ So what if we want to change one of the items in the array?
`bucket_list[2] = "take a nap"` will re-assign the third item in the array to 'take a nap'.

**adding and removing items**
+ We can also add and remove items from an array.
+ `bucket_list.append("graduate from Flatiron")` will add an item with the contents of the argument to the end of the array it is called on. 
+ `bucket_list.removeAtIndex[1]` will delete the item at index 1.

##Dictionaries
Dictionaries are also a type of list and can be thought of as two-column tables. The difference is that for an array the left side of the column is the index, for dictionaries there is no numbered index, but there is another piece of data on the left side of the table, called the **key**, while the data on the right are called **values**

####Dictionaries

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

We use ditionaries when we have a piece of data tied to another piece of data. We call this a key-value pair. The key in a dictionary has to be unique, because it's how we access values from the hash. 

We initialize a dictionary like this: `var names_dict = [String: String]()`
We write a dictionary like this: `names_dict = [ "Danny": "December 3", "Victoria": "December 2" ]`

**Accessing data in a dictionary**
+ Now we don't have indices, but we have keys. Given what we know about arrays, how do you think we'd access a value from a dictionary?
  + `names_dict["Danny"]` returns `"December 3"`
+ Knowing what we know about arrays, how would we change a key-value pair's value?
  + `names_dict["Victoria"] = "December 1"`
+ To add a new key-value pair we use the same syntax:
  + `names_dict["Lyel"] = "April 1st"`
+ To delete we use `names_dict.removeAtKey("Lyel")` to remove the pair.


