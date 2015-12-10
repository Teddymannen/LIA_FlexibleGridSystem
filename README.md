# LIA_FlexibleGridSystem
_Flexible GS is made by Teddy Fredricson during his internship at BTH([Blekinge Tekniska Högskola](http://www.bth.se/))._

It is made with inspiration from

[Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid)

[CSS3 Flexbox - LESS Mixins](https://gist.github.com/jayj/4012969)

[Tyler Tate's Semantic GS](http://tylertate.github.io/semantic.gs/)

any many other systems found online.

The system uses the power of SASS to create a Semantic Grid System with Flexbox.


###Tutorial to the Grid System:
(first of all, you might want to check out [a guide to flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/), a really good website that explains the basic usage of Flexbox)

1. The first thing you might want to do is download Ruby(unless you're on a mac, then it should be installed already) from [Ruby Installer](http://rubyinstaller.org/downloads/).
2. Then in the ruby folder, run "Start Command Prompt with Ruby". Go to the directory where you have your files(with 'cd [path]') and install Sass: "gem install sass"
3. To compile the input-file you either write "sass input.scss output.css" to make your 'input.scss'-file compiled to 'output.css' or you write "sass --watch input.scss:output.css" to make Sass watch the file until you tell it to stop. (more information here: [SASS Reference](http://sass-lang.com/documentation/file.SASS_REFERENCE.html))
4. Now you can start using the Grid System.

To begin with, to make a div-tag a flexbox container, you include one of the following mixins inside the brackets:

#####@include flex-row

#####@include flex-col

#####@include flex-row-reverse

#####@include flex-col-reverse

Depending on how you want the container to display its items.

#####@include col(x, y)
Decides how wide a specific element should be, where x is the width of the column(depending on the value of y, standard is 12).

_Note: only values for x are mandatory but if you want to play around with more specific results you can still add a second value that will override the standard._

#####@include col-offset(x, y)
Moves the element away from the left side in the x-axis.

_Note: only values for x are mandatory._

#####@include justify-content(x)
Values for x are flex-start(standard), flex-end, center, space-between, space-around.

#####@include align-items(x)
Values for x are flex-start, flex-end, center, baseline, stretch(standard).

#####@include order(x)
Put integer values as x to change the display order of items (useful when working with responsive websites).

#####@include align-self(x)
Values for x are auto(standard), flex-start, flex-end, center, baseline, stretch.
