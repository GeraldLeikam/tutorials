# Guide -> Create a subdomain with Cloudflare

## Prerequisites
- A Server with a static IPv4 address
- A [cloudflare] Account
## Step1: Login
Log in to your Cloudflare account
## Step2: Select Account
Select the appropriate account for you.
## Step3: Select Domain
Select the appropriate domain for you.
## Step4: Add DNS Entry
Select "DNS" on the left side, and then click on "Add Record" on the right side. Choose the type. (Typically, we use IPv4, so we will use the value "A" for that.) Enter the name of the subdomain. Please note that this is an example, but if you specify the name as "ultra-sonic-super-cloud", your server will be accessible at the FQDN "ultra-sonic-super-cloud.your-domain.com". Enter the IP address of your server under "IPv4 Address". Then set the Proxy Status to "DNS only" and click on "Save".
## Step4: Finalize
Your server should now be accessible under the subdomain you entered. If this is not the case, please check if the server has a firewall that may be blocking external access. If you are using a server from Hetzner hCloud, also check if there is a firewall configured on the server. Additionally, verify if the desired service is running on the server. If you have ruled out all of these possibilities, please double-check your settings in Cloudflare to ensure they are correctly configured. In rare cases, it may take a few minutes for the server to be accessible via its FQDN.

[cloudflare]: https://dash.cloudflare.com/login