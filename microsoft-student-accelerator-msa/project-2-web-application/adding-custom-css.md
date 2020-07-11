# Adding custom CSS

So with Elementor Page Builder I have to **pay to add my own custom CSS**. That's kind of a bummer - so I'll be editing custom CSS through the default editor that exists on the side panel.

![Additional CSS options](../../.gitbook/assets/image%20%28119%29.png)

In order to overwrite some of the default theme settings, I'll have to mark some fields as **`!important`** to make sure my changes go through intentionally.

![CSS test changes](../../.gitbook/assets/image%20%28128%29.png)

## Fixing the ridiculous headers

So I've had this annoying bug with the headers for a while now where h2 takes like the whole viewport length. To figure out why this is occuring, I dug into the source code. Initially I suspected it was because the **`padding`** of the content container was so big, but actually it turned out to be the **`line-height`** that was causing the issue.

![Giant space being taken up by h2](../../.gitbook/assets/image%20%28125%29.png)

![CSS for h2](../../.gitbook/assets/image%20%28118%29.png)

Now that I think about it, it probably was caused my me messing with the default header settings, so I might not need custom CSS here. I'll go dig into the settings and see how to resolve it but here it is if it ever comes up again.

**Update**: yep I found it.

![](../../.gitbook/assets/image%20%28114%29.png)



