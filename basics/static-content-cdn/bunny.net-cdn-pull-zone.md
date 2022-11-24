# Bunny.net CDN (Pull Zone)

## Stage 1: Setup Pull Zone&#x20;

### 1) Add new pull zone in Bunny.net

### 2) Create a unique name for the pullzone&#x20;

Example: `mastodoninstancestatic` or similar.

<figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

### 3) Select `Origin Type URL`

### 4) Update **Origin URL**

Place the original FQDN of your instance in the Original URL.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### 5) Select your regions to replicate data

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

### 6) Add new Pull zone

## Stage 2: Configure Pull Zone.

### 1) Force SSL

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

### 2) Setup SafeHop (retries on failures)

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### 3) Add additional Headers (CORS)

Add \`,js, gz\` to the Extension list.

Example: \`eot, ttf, woff, woff2, css, js, gz\`

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

## Stage 3: Configure Mastodon and NGINX

### 1) NGINX Headers

Add **`Access-Control-Allow-Origin`** header to nginx all locations.\
Example: `add_header Access-Control-Allow-Origin "https://aussocialstatic.b-cdn.net";`

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>These paths are heavily used for static files... but the header might be required in multiple locations in the nginx conf</p></figcaption></figure>

### 2) Mastodon .env

Add `CDN_HOST` to .env.production&#x20;

Example: `CDN_HOST=https://aussocialstatic.b-cdn.net`

### 3) Reload nginx and restart mastodon.

## Troubleshooting

The OCR (Optical character recognition) might fail if you missed gz from the extension list.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

## Notes

Do we need to add to svg to the CORs?

