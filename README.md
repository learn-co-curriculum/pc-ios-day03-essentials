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

##Random Function
