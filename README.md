# Box Model Dorm Posters Design
#### _Remixed from the Flatiron School_

<img src="https://s3.amazonaws.com/after-school-assets/posters.jpg" alt="Posters" align="right" width="300" hspace="10">

You can tell a lot about a person by the posters they choose to buy and hang on their wall. I mean, that's commitment. You not only have to spend money, but you have to look at it every single day. 

This becomes really important as you start to select your roommate for college. You have to live with this person (and their posters) every day for a full year.

## Let's Get Started

### Step 0: Setting up our workspace
* Fork and clone this repository
* Open `index.html` and preview it.
* You'll notice that the site is just a mess of images on a grey and white screen. You'll notice several posters: Audrey Hepburn, Beyoncé, Michael Jordan, New York, Picasso, Andy Warhol, and Woody Allen. The goal is to arrange each posted neatly and add a snazzy frame.You're going to be responsible for arranging the posters nicely on the wall and framing them.
* You'll code your solution in `style.css`. Go ahead and open that file.
* Now that you have `index.html`, `style.css`, and the **preview** of `index.html` open, drag `style.css` **right** and **down** like the image below:  

<img src="http://i.imgur.com/zgTSZO2.png">
You can also click on the word `Workspace` on the left for more room.  Now your workspace should look like this:
<img src="http://i.imgur.com/Xsq9DHK.png">


### Step 1: "The Classy Roommate"

<img id="audrey"  src="https://s3.amazonaws.com/after-school-assets/audrey-poster.jpg" alt="Audrey Hepburn" align="right" width="100px" hspace="10">

If you look inside of `index.html`, you'll notice this image is already in the HTML, with the ID `audrey`. We can use this ID as our CSS selector. 

First, we need to center the image. Copy the following code and paste it inside of `style.css` right after the comment `/*"The Classy Roommate"*/`:

```css
#audrey {
  margin-left: auto;
  margin-right: auto;
  display: block;
}
```

`margin` is responsible for the space around the image we're styling. You can think of it as the space between pieces of content. In the case of the Audrey poster, we're talking about the space between the sides of the grey box and the poster. If we want the image to be centered, we want the same margin on the left and the right. `margin-left` and `margin-right` are two CSS properties that we set to `auto` meaning it will automatically center the image.

`display: block;` means that the image will take up the entire width of the grey box. Nothing can fill in next to it. Without the `display: block;`, we wouldn't have a margin to the left, because by default, images will fill in next to each other.

And now to add the border:

```css
  /*Add this line to your CSS!*/
  border: 15px solid red;
```

`border: 15px solid red` means that our border around the image will be 15px wide, will be a solid line, and will be red in color.


### Step 2: "The Neurotic New Yorker"

<img src="https://s3.amazonaws.com/after-school-assets/woody-poster.jpg" align="right" width="100px" hspace="10">
<img src="https://s3.amazonaws.com/after-school-assets/newyork-poster.jpg" align="right" width="100px" hspace="10">

For these two posters, we want to frame them individually, but have the frames be the same size. Currently the Woody Allen poster is 171 x 253 pixels and the NYC poster is 236 x 364 pixels. If we want the frame to be the same size around both posters, we have to increase the size around the Woody Allen Poster, but inside the frame.  This is called `padding`, and we're going to use it to add space between the content and the border.  

If we want this image to be 236px wide, we need to add `32.5px` of padding to the right and the left. This number comes from finding the difference in the width of the two pictures and then dividing by 2 (half for the left, half for the right).

In order to make the image `364px` tall, we need to add `55.5px` of padding to the bottom and the top.

Luckily, we can give `padding` 1-4 inputs, and here's how it will use 1/2/3/4 numbers.
```css
(1 input)  padding: all;
(2 inputs) padding: top/bottom left/right;
(3 inputs) padding: top left/right bottom;
(4 inputs) padding: top right bottom left;
```

_(The same applies to_ `margin` _)_  
For an in-depth explanation, [read more here](http://www.w3schools.com/cssref/pr_margin.asp).

Use the ID selector for `woody` to style the Woody Allen poster. Underneath the comment `/*"The Neurotic New Yorker"*/`:
* Set the top and bottom padding `55.5px` and the left/right padding to `32.5px`.  You should be able to do this in one declaration (as explained above).
* Set the `background-color` to `white`.  This will fill in the background so that the padding has color.  
Voila! Looks pretty nice, eh?


And now we need to set the border - again `border: 15px solid red;`. You can change up the value of the border property to be smaller pixels in width, or dashed in style, or even purple in color! 

And now for the New York City poster, we just need to add a border. Select the element with ID `newyork` and give it the same border as `woody`.

If we wanted to _properly_ center these images on the wall, we'd need `relative` and `absolute` positioning (we'll learn that later). For now, center the images as best you can by using `margin`.  Try to get it to look something like this:
<img src="http://i.imgur.com/M4PIi9x.png">

### Step 3: "The Art History Major"

<img src="https://s3.amazonaws.com/after-school-assets/picasso-poster.jpg" align="right" width="100px" hspace="10">
<img src="https://s3.amazonaws.com/after-school-assets/warhol-poster.jpg" align="right" width="100px" hspace="10">

For this one, we need to resize the images so that they fit on the wall, and then frame them together in one big frame.

First, let's resize the images using the `height` css property. Copy and paste the following code inside of `style.css` underneath the `/*"The Art History Major"*/` comment:

```css
#warhol {
  height: 300px;
}

#picasso {
  height: 300px;
}
```

Now, our images are the same height and fit on the wall properly! Next up, we need to put a frame around both images. We can't just add a border to each poster, because that would frame them separately. If you look at `index.html`, you'll notice that both `img` tags are nested inside of a `div` with the class `double`.

That class is what we want to use as our CSS selector and apply styling to.
* Set a 20px wide, solid navy border around both images using the `border` property. 
* Use `text-align:center;` to center our image. Yes, this technically works even though we're not centering text, but we'll get to advanced positiong later.  Right now we're just focusing on margin/padding/borders.
* Set the `background-color` to `white` to give our posters a matte. Without it, we would see the grey between the images and the border.

The result should look like this:
<img src="http://i.imgur.com/nECafAF.png">

### Step 4: "Pop Culture Fanatic"

<img src="https://s3.amazonaws.com/after-school-assets/michael-jordan-poster.jpg" align="right" width="100px" hspace="10">
<img src="https://s3.amazonaws.com/after-school-assets/beyonce-poster.jpg" align="right" width="100px" hspace="10">

For these posters, we want to stack them on top of each other, center them, and add a unique border to each one.

First, we need to resize both images. Copy and paste the following code inside of `style.css` underneath the comment `
/*"Pop Culture Fanatic"*/`:

```css
#mj {
  height: 200px;
}

#beyonce {
  height: 200px;
}
```
As for the rest, well, you're on your own. But keep adding CSS until those images look like this: 
<img src="http://i.imgur.com/W580Rct.png">

### All done?
That means YOU are ready for college!  Here's a little HTML/CSS extension: add your OWN wall at the bottom with your own pictures.  Make sure they fit your personality!

### Additional Resources

1 [Mozilla Developer Network Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)

2 [W3C Schools Box Model](http://www.w3schools.com/css/css_boxmodel.asp)

3 [CSS Box Model Tricks](https://css-tricks.com/the-css-box-model/)




