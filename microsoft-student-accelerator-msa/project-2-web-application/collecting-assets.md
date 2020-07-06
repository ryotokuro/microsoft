# Collecting assets

## Favicon

First, the little icon that pops up in the tab that demonstrates the branding of the website. 

![Microsoft website favicon](../../.gitbook/assets/image%20%2839%29.png)

In web development this is called the **`favicon`** and placed in the `<head>` tag as a link. I want the official favicon - so since there's no official repository of Microsoft's website branding resources, I'll just snag it from their website. To do so, I just navigate to one of Microsoft's official websites and go into the source code \(or inspect element\) and **find the .ico file** under the head section.

![Source code for Microsoft&apos;s website](../../.gitbook/assets/image%20%2842%29.png)

So now I'll just save the icon at this [link](https://c.s-microsoft.com/favicon.ico?v2) for use as a favicon for my website. This seems to be appropriate now as it is consistent across Microsoft websites and there doesn't seem to be an official MSA logo that is recognisable outside of AU/NZ. Perhaps I could have a partner logo created on their [official partner website](https://partner.microsoft.com/en-us/marketing/branding) but at the moment for the first iteration of this it doesn't seem likely.

## Microsoft's Logo

Now for Microsoft's Logo. This is quite simple to obtain since it is publicly available on their website so that collaborators are able to use it in their advertising. You can see an example of it being used in the page `<header>` here:

![Microsoft website header and nav](../../.gitbook/assets/image%20%2871%29.png)

Again, I can navigate to their corporate website, dig into the source code and snag it off there or alternatively get the [full-resolution file on their website here](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/logo.aspx).

![](../../.gitbook/assets/image%20%2833%29.png)

## Microsoft Font

For Microsoft's font, again I'll dive into their code, this time looking at their styling \(CSS\) to see what font-family they use. Again, this is pretty simple and consistent - Microsoft like to purely use **Seogoe UI** as their font of choice across all their products. The only difference would be the **different sizes** for hierarchy of text. This can be seen here with `h1` as an example:

![h1 with a size of 46px and using Segoe UI](../../.gitbook/assets/image%20%2872%29.png)

So for reference, I've found all the sizes they like to use and tabulated the data here.

| Level | Size | Weight | Margin | Line Height | Color |
| :--- | :--- | :--- | :--- | :--- | :--- |
| h1 \(Heading 1\) | 46px / 2em | 600 | .67em 0 | 56px | \#000 |
| h2 \(Heading 2\) | 46px | 600 | N/A | 56px | \#000 |
| h3 \(Heading 3\) | 20px | 600 | 37px top | 24px | \#000 |
| Body | 15px | N/A | N/A | N/A | \#000 |
| Anchors/Buttons | 15px | 600 | N/A | 1.3 | \#0067b8 |
| Nav links | 13px | N/A | 1px top | N/A | \#262626 |
| h4 \(Footer head\) | 15px | 600 | N/A | N/A | \#616161 |
| Footer links | 11px | N/A | N/A | 16px | \#616161 |

## Branding Colours

For the website colour palette, we can stick to the default colours \(white, black\). However, if we want any splashes of colour, it would be useful to have the colour codes on deck. [Here we can find the HEX codes for Microsoft's logo](https://brandpalettes.com/microsoft-color-codes/) and also the [MSA branding colours here](https://msa.ms).

| Colour | HEX Code |
| :--- | :--- |
| Microsoft ORANGE | \#F25022 |
| Microsoft GREEN | \#7FBA00 |
| Microsoft BLUE | \#00A4EF |
| Microsoft YELLOW | \#FFB900 |
| Microsoft GREY | \#737373 |
| MSA PURPLE | \#5C2D91 |



