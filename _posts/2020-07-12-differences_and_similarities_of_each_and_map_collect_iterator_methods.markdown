---
layout: post
title:      "Differences and Similarities of Each and Map/Collect Iterator Methods"
date:       2020-07-12 21:36:09 +0000
permalink:  differences_and_similarities_of_each_and_map_collect_iterator_methods
---

To fully understand the role of Iterators, you must first understand each of the elements that are supported and in direct relation to the use of Iteration in programming. Iterators are supported by collections. Collections are the objects which store a group of data members. These collections can be Arrays and Hashes which are the most common, as well as Sets, Structs, and OpenStructs, but we will not be focusing on those in this post. Iterators themselves are methods which exist in numerous coding languages. These methods are essential to returning elements of a collection one after another. The word “iterate” is a verb, meaning: “to say or do again or again and again” according to Webster’s dictionary. This basically tells us exactly what iterators do within programming as well. 

There are several Iterator methods that perform different and similar functions in programming. Specifically, I would like to discuss the differences and similarities of Each Iterator method and Map/Collect Iterator method. 


The Each Method:

The Each Iterator method returns all of the elements of an Array or Hash returning each value one by one. This method iterates though each element and makes the changes we tell it to for our output, however it still returns the original array or hash.

The Syntax looks like this:

```
collection.each do |variable_name|

   # code to be iterate
	 
end
```

So for example, using Each, this code:

```
a = ['A', 'B', 'C', 'D', 'E'] 
  
a.each do |arr| 
   
    puts arr 
      
end
```

would have this output:

```
A
B
C
D
E
```

and returns:

```
['A', 'B', 'C', 'D', 'E'] 
```

The Map/Collect Method:

Map and Collect refer to the exact same method. It is essentially up to the user to decide whether they'd like to use '.map' or '.collect' in their code.

I prefer using '.collect' therefor I will be refering the the method as the Collect method.

The Collect Iterator method returns all of the elements of a collection regardless of whether it is an Array or Hash; this method also need not always be associated with a block. A unique feature of this method is that it gives us a new collection of elements based on the results of our output. That new collection is commonly a new Array or Hash.

The Syntax looks like this: 

```
Collection = collection.collect{ |variable_name| }

# code to be iterate	 
```

So for example, using Collect, this code:

```
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

b = a.collect{ |y| (5 * y) }

puts b 
```

would have this output:

```
5
10
15
20
25
30
35
40
45
50
```

and returns:

```
[5, 10, 15, 20, 25, 30, 35, 40, 45, 50]
```

Now that I have explained each method and shown examples of how they are used. I'd like to break down specifically what their similarities and differences are in order to sum up this blog post. Being that both of these methods are Iterators, they perform a very similar function in how they ouput collections of elements. Their differences are that Each is used specifically when returning elements of an Array or Hash and is commonly associated with a block. Each also always returns the original array or hash. Map/Collect can be used on any collection of elements, does not need to be associated with a block, and also returns a new collection of elements.

It is also important to understand when it is beneficial to use both of these methods. Both Each and Collect are helpful methods for iterating when you want to make changes that affect each element in an array, hash or other collection type. If you want your code to return a new collection you should use Map/Collect and if not, use Each. 

Writing this post has definitely helped me reach a better understanding of Iteration and Iterator methods, so I hope this is helpful to other programmers as well.

