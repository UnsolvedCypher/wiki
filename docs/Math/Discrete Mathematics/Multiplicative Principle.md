# The Multiplicative Principle

## The Basics

The multiplicative principle is an important part of combinatorics. It has to do with combinations of events or conditions. When there are $a$ possibilities of one thing and $b$ of another, there are $a*b$ possibilities when the two things are combined. A few examples:

If there are 2 types of burgers (cheeseburger or veggie burger) and two drinks (soda or water), there are $2*2 = 4$ combinations of meals, assuming a meal is a burger with a drink. You can think through this example- you start with two choices, cheeseburger or veggie burger. Then, for each choice, you can choose one of two drinks.

This example can be expanded. Say there are 4 entrees, 3 drinks, and 5 desserts. If a meal consists of an entree, drink, and dessert, then you can have $4*3*5 = 60$ different meals. Again, you can think through this example- you start by choosing one of four entrees, then for each entree you can have 3 different drinks, so $4*3 = 12$ entree-drink combinations. Then, for each of these combinations, you can choose from 5 desserts, so you have $12*5=60$ total options.

The general rule is that for $a^b$, a is the number of possibilities, and then b is how many times something could occur.

## Repetition

Often times, you will need to multiply by the same number repeatedly. This is the same as raising the first number to the number of times you want to multiply by it. For example, you have 9 flavors of ice cream to choose from. If 22 people are ordering, how many possible sequences of orders could there be?

You would have to write out $9*9*9*9...$  22 times. Instead, you can simply write $9^{22}$.

Similarly, if you have 22 people ordering but the first 12 can choose from 9 flavors while the next 10 must choose from 4, you would have $9^{12}*4^{10}$, which is the same as $9*9*9*9*9*9*9*9*9*9*9*9*4*4*4*4*4*4*4*4*4*4$.

## Multiple Cases

Not all problems with the multiplicative involve simply multiplying all of the numbers. Consider a problem where you have four entrees, three drinks, and 5 desserts. A meal is *either* an entree and a drink, or an entree and a dessert. You can try to set up the problem with this using only multiplication, but it won't work.

You have to consider both cases: there a $4*3 = 12$ entree-drink combinations, and $4*5=20$ dessert combinations. Thus, we have $12+20 = 32$ cases that satisfy our criteria. In general, you're using multiplication to make combinations, while you're using addition to add together different possible combinations.

Here's another example: a password consists of either 12 letters, 24 digits, or 9 letters followed by 8 digits. Remember, there are 26 letters and 10 digits. So, we have:

- $26^{12}$ for the first case (26 letters in the alphabet, and we're using 12 of them)
- $10^{24}$ for the second case (10 digits, and we're using 24 of them)
- $26^9*10^8$ for the last case (26 letters being used 9 times, and then 10 letters being used 8 times)

So, we just add them together to get the answer!