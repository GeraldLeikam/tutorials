# Guide -> Install ownCloud Server on a HcloudServer Full
 
## Step1: Creating a server at Hetzner HCloud
Create a cloud server at Hetzner hCloud with Ubuntu 20.04 operating system. [Read more about Cloud Server Creation]
## Step2: Obtaining a Fully Qualified Domain Name (FQDN)
Obtain an FQDN and assign it to your server. I prefer creating a subdomain on Cloudflare for this purpose. [Read more about how to do it with Cloudflare here]
## Step3: Install ownCloud Server
Install the ownCloud server software on the server from step 1. [Read more about install ownCloud Server]
## Step4: Secure servers with SSL and let's encrypt
Apply for a Let's Encrypt certificate for your server and redirect all traffic to port 443. [Read more about applying a let's encrypt certificate]


[Hetzner Cloud Account]: https://console.hetzner.cloud/projects
[Read more about Cloud Server Creation]: https://github.com/GeraldLeikam/tutorials/blob/master/hetzner/setup_a_cloud_server.md
[Read more about install ownCloud Server]: https://github.com/GeraldLeikam/tutorials/blob/master/ownCloud/install_owncloud_20.04_quick.md
[Read more about how to do it with Cloudflare here]: https://github.com/GeraldLeikam/tutorials/blob/master/cloudflare/create_a_new_subdomain.md
[Read more about applying a let's encrypt certificate]: https://github.com/GeraldLeikam/tutorials/blob/master/let's_encrypt/applying_a_lets_encrypt_certificate.md