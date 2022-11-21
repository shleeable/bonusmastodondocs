# Introduction

Mastodon requires a server (physical or virtual), and it’s also highly recommended to use an S3 bucket to store all local/remote media.

Any cloud provider should be fine. Try to find something local to your region. I’m in Sydney, so I’m using Linode, and Wasabi because they have Sydney based data centers, and offer good prices.

## Introduction to Scaling

Mastodon is built around multiple pieces of technology, and each of them can be tweaked to improve performance.

Key themes of this document is to highlight bottle necks and allow for scaling. All of these services can be run from a single box, but we HIGHLY recommend splitting them up as you start to scale (as soon as you can afford it).

Firstly, Please read the blogs written by Gargon and the official documentation on scaling. We will be using this as reference.

\
[https://blog.joinmastodon.org/2017/04/scaling-mastodon/\
](https://blog.joinmastodon.org/2017/04/scaling-mastodon/)[https://docs.joinmastodon.org/admin/scaling/](https://docs.joinmastodon.org/admin/scaling/)\
[https://gist.github.com/Gargron/aa9341a49dc91d5a721019d9e0c9fd11](https://gist.github.com/Gargron/aa9341a49dc91d5a721019d9e0c9fd11)

## Mastodon: Piece by Piece

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>High Level diagram of Aus.Social (NOV 2022)</p></figcaption></figure>



<figure><img src="https://lh6.googleusercontent.com/_mWsfCArEKIr4YwIzI5t5X3yEwAa-XgUECQelS135_w6R6g60pAVbWIPuRE9Ob5Jdv2SNSkCIvnYfHDE421CNEyKMvRc5RWbPVgTAo-jc8u0jrE-l3GFW7TtyrB81JpsZHi-2LoU0CzMCm1a3mLLX9aCNDIonb_jtb-PhTUn0HjS9FwU3wp76ledOU9BPw" alt=""><figcaption><p>Generic diagram of a Mastodon Instance</p></figcaption></figure>
