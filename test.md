##TIL
CSS can be a cruel mistress. CSS is salty, unforgiving, and downright nonsensical at times. But there are other times when you get a peek behind the curtain and you are able to connect the dot which previously evaded you like a sasquatch.

So I was running into an issue today (all day everyday, amiright?). There was an image that I was displaying on the front end that was actually just a div with a background-image applied to it with CSS. This works great for me when I want total control over the dimensions of an image since I can just apply `background-size: cover;` and get the box to do what I want without worrying about the image too much. Where I ran into my issue was needing to apply alt text dynamically. Since it was essentially just a `<div>` element, WordPress won't recognize it and therefore, won't give it that beautiful SEO-rich alt-text. I still needed control over the element but it also needed to be an `<img>`. 

###The Solution?
What I learned is that you can have your cake and eat it too, with a little css property called `object-fit`. This was a life-saver. I simply did this:

```
img.image-frame.mobile {
    object-fit: cover;
}
```
This gave me the power of the background properties, with the recognition of the image element! Aside from some minor padding tweaks that I had to do after the fact, this solution worked perfectly.

The perceived danger that one is faced with when revealing the things they learn is that they will actually be revealing their ignorance.