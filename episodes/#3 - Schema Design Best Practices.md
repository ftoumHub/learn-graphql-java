When you create your schema is it crucial that you follow some best practices.

With all APIs, it is extremely important to have descriptive names. But, with the 
nature of the graphql schema and evolution, one would argue that it is even more crucial. 

Simply, create a naming convention and place it in a doc :) .

Wrapper types will allow your schema to freely evolve, makes changes in a backwards 
compatible way and we do not need to worry about our clients migrating to new types.

For example, If you have a field "userId", when you decide you require more user 
information, you will typically need to create a new type that contains the userId 
and your new fields. Here we need to deprecate userId and wait until all clients 
migrate over to the new type. Then clean-up userId. If you created a user type from 
the start, you could freely add new fields without planning backwards compatible changes.

It is important to note, this is not a hard rule. Please be pragmatic :)

“Public APIs are forever, ONE chance to get it right. “