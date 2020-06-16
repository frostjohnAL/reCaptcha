# Steps to switch from reCaptcha to Arkose Enforcement Challenge

1. Read over our Developer Guides for Standard setup and Server-side 
2. Private and Public key pair
3. Client-Side integration
4. Server-Side integration

## Developer Guide
Here is our external facing [Developer Guide](https://arkoselabs.atlassian.net/wiki/spaces/DG/overview) which includes the [Standard Setup](https://arkoselabs.atlassian.net/wiki/spaces/DG/pages/214176229/Standard+Setup)

## Keys
Your keys which will be shown in the dashboard.arkoselabs.com for both public and private. If you do not have any keys please reach out to your Sales Rep or Sales Engineer. 

## Client Side Integration
```sh
<script src="https://www.google.com/recaptcha/api.js" async defer></script>
```
to 
```sh
<script src="//client-api.arkoselabs.com/v2/INSERT_PUBLIC_KEY/api.js" data-callback="setupEnforcement" async defer></script>
```
Update public key from the Arkose dashboard


## Server Side Integration
```sh
private_key = "INSERT_PRIVATE_KEY";
```
Update private key from the Arkose dashboard

Response token





