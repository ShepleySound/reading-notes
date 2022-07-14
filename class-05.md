# Class 05

## HTML Media

1. What is a real world use case for the `alt` attribute being used in a website?  
The `alt` attribute is typically used on an `<img>` element. If an image cannot be displayed for any reason (such as a slow internet connection, or a broken link) then the text provided in the `alt` attribute will be displayed instead.
2. How can you improve accessibility of images in an HTML document?  
Using an `alt` attribute will allow screen readers to read out something in place of the image. `<figure>` and `<figcaption>` can also be used to provide a description for whatever is inside of `<figure>` that is semantically linked.
3. Provide an example of when the figure element would be useful in an HTML document.  
Items such as images or charts can be wrapped in a `<figure>` element alongside a `<figcaption>` to easily provide a semantically linked caption/description to the item.
4. Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.  
A gif can be a still image or a moving picture. They don't take long to load, so if your internet is slow then you can still look at them, but they might look grainy or pixelated.   
An svg deals with vector graphics. It's good for buttons and text, since you can zoom in on it as much as you want and it will never look pixelated.
5. What image type would you use to display a screenshot on your website and why?  
Almost all currently used browsers support WebP, so I would probably use that. Depending on what it is a screenshot of, detail might be important. A JPEG might not have the detail required, but a PNG can be relatively large in file size.

# Learn CSS

1. Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.  
Foreground color sets the color of words on a page. Background color sets the color of the space behind text or images. Since things on a page are separated out into boxes, different things can have different background colors. So you can set a background color for the entire page, and then set background colors for individual boxes inside the page.
2. Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?  
I would go through a tool like coolors.co or paletton.com and have them choose a color palette that they like. To start, I might style the backgrounds of individual posts in a card style using the newly chosen primary color, and then apply the newly chosen secondary color to headings on the page, or the backgrounds of the header and footer.
3. What should you consider when choosing fonts for an HTML document?  
The tone of the page should be considered. A serious article or blog should probably use a more standard font that is easily readable. Large headings can be given a more "unique" font. A page for a game or something less serious might use a more stylized font, but small paragraph-style text should still be easily readable.
4. What do font-size, font-weight, and font-style do to HTML text elements?  
   - `font-size` changes the size of the text.
   - `font-weight` changes the boldness, or weight, of text.
   - `font-style` applies different italic or oblique (slanted) styles to text.
5. Describe two ways you could add spacing around the characters displayed in an h1 element.  
The `letter-spacing` property lets you set spacing between each character in a word. Depending on information stored inside the font, the `font-kerning` property can also alter the spacing between characters to make words look more uniform and easier to read.


