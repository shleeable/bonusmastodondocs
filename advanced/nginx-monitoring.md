# NGINX Monitoring

*   Keep your eyes on the /var/log/nginx/errors.log\
    Example: Not enough worker processes (Tells you the problem/solution)\


    <figure><img src="https://lh5.googleusercontent.com/yxQhZHfmUkqmxOYtkhwAhRc3PKSw6XZd9t34Fqw5wk_6BkE9Yn9_ZvqqPhwzD9vobUHJpd6mKP9uwWbHJfSZCGnQ4Amu39AKkXVorEVxhXgIMkeu0GGBE5L_PIIQ0Gr3ClHj8-fHEpONXuHa2cvNjWmgKHt5me2N6WpI3K3QlWFp0gmjZ4v4mJoMJuyAkg" alt=""><figcaption></figcaption></figure>
* Consider installing the status module to keep an eye on the active connections.

<figure><img src="https://lh5.googleusercontent.com/VjAazCLQ70bmYsz4bywwbv1rK2-nRx7j7KOVHN0l76524vVCj6A9NLUQq2xdZGdQmS0jilHF_6cFe5jJk5x_iF0P7SoSfVl-h4-7v0C5PVDoe9IemkfrAxEnhqXgoQMKfPsIjlgqqE_dxo1PoTAbG2NtPNrQuWtzOgiqxibuFBoC64hlnspwalYCvobF9w" alt=""><figcaption><p>Output of https://x.com/nginx_status</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>Code Block from my instance conf</p></figcaption></figure>

* TODO: Investigate the Nginx virtual host traffic status module\
  [https://github.com/vozlt/nginx-module-vts](https://github.com/vozlt/nginx-module-vts)
