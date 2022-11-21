# Cloud Servers (VMs)

VMs are generally pretty “affordable” these days.. But if you’re planning to scale to thousands of concurrent people on your instance, you will likely find yourself having multiple VMs.

Our goal with this guide is to optimise the VMs to run as high performance as possible on hopefully the smallest instances we can use.

## Example:&#x20;

Aus.Social currently has 4 VMs:

* PostgreSQL and Redis : 4 CPU / 8 GB VM
* ElasticSearch : 2 CPU / 4 GB VM
* Sidekiq : 6 CPU / 16 GB VM
* Nginx: 2 CPU / 4GB VM
* Puma/Streaming : Two x 4 CPU / 8 GB VM

This setup will allow me to increase the VMs as required but is currently running at around 50% utilisation on the Nginx / web server when hosting 10,000\~ active users (with average on and off usage).

\
