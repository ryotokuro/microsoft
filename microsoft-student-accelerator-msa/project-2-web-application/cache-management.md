# Cache Management

For cache management, I'll be using a plugin to store the page information and improve the speed at which my website is served. In this case, I've chosen WP Super Cache to manage the caching easily since it's one of the most popular caching plugins.

![](../../.gitbook/assets/image%20%28165%29.png)

## Caching Settings

To turn on caching, I simply need to select the radio button to turn it on and update the status of the plugin. This sets up the cache following the _recommended settings_ as specified.

![](../../.gitbook/assets/image%20%28166%29.png)

## Testing the Cache

What's great about this plugin is that it even has a test suite to verify that my cache is set-up and working as intended. All the logic is abstracted away and I simply have to hit the button to run the tests and it will output the results of the tests and the HTTP response from loading my website. As you can see, everything works perfectly and my simple cache is set-up nicely.

![](../../.gitbook/assets/image%20%28168%29.png)

## Exploring Advanced Settings

Beyond the basic configuration, I'll be digging in the advanced settings a little to see how the caching works and maybe find some unique settings that would be good for my case. For now I've simply enabled the recommended settings which shouldn't cause too much of an issue - such as **page compresssion** and **304 Browser caching**.

![](../../.gitbook/assets/image%20%28167%29.png)

