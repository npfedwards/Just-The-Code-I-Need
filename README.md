Just The Code In Need (JTCIN) is a simple LESS/CSS framework.

The idea behind the framework is that you don't necessarily want all the code that comes with your chosen framework. You might not use an element spanning 15 columns for example.

JTCIN is designed to be compiled before it reaches the client side providing you with a single CSS file to provide the user.

## What do I do?

JTCIN lets you decide how many columns you want to use, and what page sizes you want to provide your user. Currently included are 16 column grids for 720,960,1168 and 1360. To create your own size, create a LESS file with the following

	@columns: 16; //Current max 16
	@colwidth: 50; //(@colwidth + @gutter) * @columns is your page width.
	@gutter: 10; 

	@import "boilerplate"; //Contains the boilerplate code always required
	@import "columns"; //Contains the columns
	@import "style"; //Just for your code

To remove the columns you won't be using from your final css, open `columns.less` and comment out the columns you don't want (this will permeate all your grids). LESS accepts `\\single line` comments.

### Compile it

I use LESS.app. There's a bunch of other apps around like SimpLESS, and a bunch of other ways to compile, check www.lesscss.org

## Bugs

Hit the issues to flag bugs, or even better, flag it and then fork it and fix it!