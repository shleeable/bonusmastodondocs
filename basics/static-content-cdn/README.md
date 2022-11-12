# Static Content CDN

This is one of the most recommended steps and should be taken by all admins regardless of size.

## Why?

Using a CDN for static files will take pressure off the nginx/puma webserver when serving commonly available files like JS, CSS, SVG etc, and allows your web server to purely focus on the dynamic important stuff.

## Example

I'm running bunny.net CDN, and it's caching more than 90% of the static traffic. Which has dropped my CPU usage massively.

![](https://lh5.googleusercontent.com/ucfgaozaJzDk6s35KCfdgrV-lJMT3k4Vc99BDNAx1K3\_PVg977mIHzuAMg-Vg\_Ji7Khtgln9LXRgQu1dEvJr7sK1kgNf7YcHoM9cT9vXVyyTbf9vOAoLMZUp292WDEzkNw6IfJdCOaiE98TkeJC7l2sksOGsTnNV5rcB4hzfzJCnICquE7Te-UrOzLejzw)
