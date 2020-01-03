# Infinite recursive shape

The idea is to create a recursive function to draw boxes inside each other in array from 3 different variables
`width` `height` and `padding`

## Technology used

I used `create react app` for the UI and I used `Jest` for testing the function and `travis` for CI/CD
I created 2 function for draw function in `draw.js` file I used different techniques for that one is recursion and the second solution is AB|CD or mirroring the array.

## Installation

cd project directory, and run:

`git clone git@github.com:schand143/infinite-recursive-shape.git`
`cd infinite-recursive-shape`
`npm install`
`npm start`

<!-- `npm && npm start` -->

## Testing

Test only run on the draw() function matching data from `JSON` file to check the value given toward the result of the function.

I created the function inside an `object` so I can run deep testing on it as recursive function calls itself directly it is not possible to spy on those calls since they refer directly to the function.

In order to spy on recursive calls they must refer to functions that can be spied on. Fortunately, this is possible by two ways either by wrapping the function inside object or by importing a recursive function back into its own module and use the imported function for the recursion

so I chooses the first option to run the jest.

to run the testing
`npm test`

## First Solution

The first solution I used Array.from to get the `width` of the array and the `height` of the array and then create every row in the array separately.

so the idea in any recursion function is to put the base case so my main base case is to check if the width and height less than or equal to zero then stop the function.

then checking on the height if it less than 2 draw the last row

then I have 2 returns after than the main one which will have the recursion after subtracting the padding after adding 2 to it to count the edges.

the the second return is happen only to draw the last box inside the array.
you can see more details on the `draw.js` file.

### The Big O

### Screen shots

1.  `Width: 40, Height:60, padding: 4)`

![Screen Shot 1](Screenshot1.png?raw=true "Screen Shot 1")

2.  `(Width: 30, Height:50, padding: 6)`

![Screen Shot 2](Screenshot2.png?raw=true "Screen Shot 2")

4.  `(Width: 40, Height:80, padding: 60)`

![Screen Shot 3](Screenshot3.png?raw=true "Screen Shot 3")

## My Activities

### <a href="https://schand143.github.io/My-Portfolio/">My Portfolio</a>
