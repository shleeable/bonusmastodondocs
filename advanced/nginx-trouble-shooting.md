# NGINX Trouble Shooting

## Not enough worker processes

* Keep your eyes on the /var/log/nginx/errors.log\
  Problem: Not enough worker processes (Tells you the problem/solution)

Solution: Increase worker processes.

<figure><img src="https://lh5.googleusercontent.com/yxQhZHfmUkqmxOYtkhwAhRc3PKSw6XZd9t34Fqw5wk_6BkE9Yn9_ZvqqPhwzD9vobUHJpd6mKP9uwWbHJfSZCGnQ4Amu39AKkXVorEVxhXgIMkeu0GGBE5L_PIIQ0Gr3ClHj8-fHEpONXuHa2cvNjWmgKHt5me2N6WpI3K3QlWFp0gmjZ4v4mJoMJuyAkg" alt=""><figcaption></figcaption></figure>

## cache file has too long header

* `2022/11/30 08:18:38 [crit] 1392615#1392615: *4208360 cache file "/var/cache/nginx/8/aa/d974f05ff7f54ab0f4b21dbba7861aa8" has too long header, client: x.x.x.x, server: aus.social, request: "GET /api/v1/instance HTTP/2.0", host: "X.social"`

Solution: ??\


## Monitor the active connections

* Consider installing the status module to keep an eye on the active connections.

<figure><img src="https://lh5.googleusercontent.com/VjAazCLQ70bmYsz4bywwbv1rK2-nRx7j7KOVHN0l76524vVCj6A9NLUQq2xdZGdQmS0jilHF_6cFe5jJk5x_iF0P7SoSfVl-h4-7v0C5PVDoe9IemkfrAxEnhqXgoQMKfPsIjlgqqE_dxo1PoTAbG2NtPNrQuWtzOgiqxibuFBoC64hlnspwalYCvobF9w" alt=""><figcaption><p>Output of https://x.com/nginx_status</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>Code Block from my instance conf</p></figcaption></figure>

* TODO: Investigate the Nginx virtual host traffic status module\
  [https://github.com/vozlt/nginx-module-vts](https://github.com/vozlt/nginx-module-vts)
