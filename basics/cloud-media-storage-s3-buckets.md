# Cloud Media Storage (S3 Buckets)

There are plenty of cloud storage providers that support the AWS S3 bucket hosting.&#x20;

AWS S3 has 99.999% SLA, but also very very expensive. Don’t use it.

* [Amazon Simple Storage Service (S3)](https://aws.amazon.com/s3/)
* [Digital Ocean Spaces](https://www.digitalocean.com/products/spaces)
* [Linode Object Storage](https://www.linode.com/products/object-storage/)
* [Vultr Object Storage](https://www.vultr.com/products/object-storage/)
* [Exoscale Simple Object Storage (SOS)](https://www.exoscale.com/object-storage/)
* [OVH Object Storage](https://www.ovhcloud.com/en-au/public-cloud/object-storage/)
* [Wasabi Cloud Storage](https://wasabi.com/s3-compatible-cloud-storage/)&#x20;
* [Backblaze Cloud Storage](https://www.backblaze.com/b2/cloud-storage.html)
* [Jortage Communal Cloud](https://jortage.com/) (huge fan of this service for US instances)
* Bunny.net Cloud Storage (coming 2023)

## Recommendations

* Just try to find one in your region… not a lot “tuning” that can be done on this front.
* I'd recommend putting a Media Subdomain (https://media.aus.social) or similar to front your traffic. [Read about that here](cloud-media-storage-s3-buckets/media-subdomain.md).

### AWS S3

Do not for any reason use AWS S3... they charge you for storage and upload/download.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption><p>I was using AWS S3, and once more than a few thousand people joined... it went from $30 to $1000s a month for something Wasabi charges $10</p></figcaption></figure>

### Wasabi

I'm using Wasabi, because they are very cheap. They have a history of outages in their primary regions, but in Sydney, I haven't experienced any issues with their service (as of writing).

