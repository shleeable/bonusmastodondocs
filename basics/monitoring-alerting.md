# Monitoring / Alerting

## Basic Monitoring

I'm running a monitoring service called statuscake.com to test my mastodon endpoints every 5 minutes and respond that the services are all online.

* https://aus.social/about
* https://aus.social/api/v1/instance
* https://aus.social/api/v1/streaming/health

These 3 endpoints should give a pretty basic amount of coverage for the internet facing Puma and NodeJS endpoints.&#x20;

I've connected statuscake up to my mobile, and get push notifications sent to my phone when one of these tests fail.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

## Advanced Monitoring (metrics)

You can investigate using promethius and other dashboards to display real time and historical details from your instance.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>tyr@pettingzoo.co example dashboard</p></figcaption></figure>

## APM (application performance monitoring)

There are more advanced monitoring tools that offer insight into the actual application low level code.&#x20;

I'd recommend investigating the different APM (application performance monitoring) tooling.

* NewRelic
* Sentry.io

