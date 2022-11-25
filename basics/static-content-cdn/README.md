# Static Content CDN

This is one of the most recommended steps and should be taken by all admins regardless of size.

## Why?

Using a CDN for static files will take pressure off the nginx/puma webserver when serving commonly available files like JS, CSS, SVG etc, and allows your web server to purely focus on the dynamic important stuff.

## Example

I'm running bunny.net CDN, and it's caching more than 95% of the static traffic. Which has dropped my CPU usage massively, and improved the \`end user\` experience.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
