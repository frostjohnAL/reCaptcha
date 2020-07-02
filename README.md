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

You're likely using a reCaptcha library but Arkose does not provide a stand alone library. There is however sample code provided [here](https://github.com/frostjohnAL/StandardSetup/blob/master/validate-token-v3.php).

#### Private Key
Update `secret key` to the Arkose Labs `private key` located in your [dashboard](https://dashboard.arkoselabs.com/)


#### Replace parameter
`g-recaptcha-response` becomes the `Session_token`ie verification


#### Update POST URL
Make a POST request to the Verify Endpoint and include a session token containing the value of the response.token from the response object.

```sh
https://www.google.com/recaptcha/api/siteverify
``` 
to 
```sh
https://verify-api.arkoselabs.com/api/v3/verify/
```



