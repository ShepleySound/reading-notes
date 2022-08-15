# Class 11

## Video and Audio Content

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.  
Not only have new features, such as `<video>` and `<audio>` elements and new JavaScript API's, been added, but the average bandwidth that each user browsing the web has access to has increased dramatically. This means that creators can focus more on the content of their video and audio rather than worrying about the deeply technical issues of heavy compression and efficient storage use.
2. Describe the use of the `src` and `controls` attributes in the `<video>` element.  
`src` acts the same as in the `<img>` element, in that it describes a path to the video to embed. `controls` adds controls to the video or audio playback. This can be the default controls provided by the browser, or can be built using JavaScript.
3. Why is it important to have fallback content inside the `<video>` element?  
The fallback content in `<video>` has a different purpose from the `alt` property on the `<img>` element. It provides a fallback for browsers that do not support the video type. Sometimes it is a direct link to the video file.
4. Write a very short story where `<audio>` and `<video>` are characters.  

A long, long time ago, the ancient powers **Flash** and **Silverlight** dominated the land of web design. None could display moving pictures or listen to the sweet sounds of music without using these powers, or else by delving into dark, esoteric magiks.  

But one day, the ruler of the land perished, and a new monarch raised in his place - **HTML5**. This new king raised knights to his service, Sir `<video>` and Sir `<audio>`. These knights were given singular tasks, to aid in the banishment of the now greater power, **Silverlight**, by providing all with the power to move pictures and play sounds. 

While these knights did not single-handedly defeat these ancient powers, but they were instrumental in providing the kingdom's subjects something even more powerful - Hope. Hope that the kingdom could happily exist in a world without magic.

## A Complete Guide To Grid

1. How does Grid layout differ from Flex?  
Grid is built with 2-dimensional layout in mind, whereas Flex is *really* good at 1-dimensional layout. Flex is still very usable for 2-dimensional layout, though! One of Grid's biggest advantages is its ability to control the size of containers while remaining responsive, giving the creator some pretty powerful options in laying out a page with many different elements.
2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.  
A grid container is an element with the property `display: grid;`. This turns its immediate children into grid items. These grid items are layed out according to the grid's column and row rules. Grid lines are the lines that divide the grid items, and they outline the structure of the grid.

## Responsive Images

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?  
Without planning for responsiveness in images, weird things can happen when the screen size changes. For example, an image that is meant to be short header image could have its height increased dramatically on a thinner, mobile-like screen. This would make looking at the important content difficult for the user.
2. Define the following <img> attributes `srcset` and `sizes`. Write an example of how they are used.  
`srcset` provides different images for the browser to choose between. `sizes` provides a set of media conditions, or screen widths, and tells the browser which image size would be best to use depending on those conditions. Depending on the matching item in the `sizes` list, the browser will load the image in the `srcset` list with the same size, or the first image that is bigger than the given slot size.
3. How is `srcset` more helpful for responsive images than CSS or JavaScript?  
`srcset` gives a built-in way to create responsive images, and since HTML is loaded before CSS and JavaScript, it allows the browser to *reserve the appropriate amount of space*. It is harder to make CSS and JavaScript tell the browser to reserve this space, as they are loaded after these decisions happen.<br>
This is really helpful, because it helps to prevent the annoying behavior of having the page load the HTML, reserve a small size for an image, and then pushing all of the loaded text content when the large image finally loads. This behavior can be seen a lot with slow-loading ads, and it's one of the most annoying things in web design as a user.
