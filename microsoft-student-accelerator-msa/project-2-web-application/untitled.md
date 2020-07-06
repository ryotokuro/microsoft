# Designing the Header

## The editing interface

So the editing interface pretty much looks like this:

![Wordpress website editing interface](../../.gitbook/assets/image%20%2867%29.png)

It's a sidebar on the left where you can control some things about different elements on your page. It's here where you upload assets into blocks that are pre-defined. As you can see, I need a logo and a site icon \(favicon\) which will be displayed on the navigation bar and on the page tab respectively.

![Site icon preview](../../.gitbook/assets/image%20%2856%29.png)

So thanks to the assets collected previously, I can simply insert those into here and Wordpress will show me how they look. What's neat is that I can customise the size of the logo displayed on the page using the slider - and in this case I've chosen 96px \(for now\) as its a nice power of 2 and sits cleanly on my header.

![Microsoft logo on the page header](../../.gitbook/assets/image%20%2842%29.png)

Moreover, what's even nicer is that Wordpress lets you customise according to screen size, so there's some in-built media queries checking how you're accessing the website; whether you're on desktop or mobile meaning you can customise how the site appears to support different devices.

![Mobile preview of website](../../.gitbook/assets/image%20%2848%29.png)

This means I can adjust the logo size for mobile devices, or even use a different variant of the logo. Moreover, the layout changes to suit for touch and scrolling using your hands, designing a better experience for different users.

