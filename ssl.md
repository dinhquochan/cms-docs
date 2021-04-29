# SSL

- [Install SSL certificate on your hosting/VPS](#install-ssl-certificate-on-your-hostingvps)
- [Redirect http to https](#redirect-http-to-https)

<a name="install-ssl-certificate-on-your-hostingvps"></a>
## Install SSL certificate on your hosting/VPS

You need to install an SSL certificate on your hosting/VPS first. You can purchase an SSL certificate or use free SSL, for example Let's Encrypt.

<a name="redirect-http-to-https"></a>
## Redirect http to https

- Step 1: Change in .env `APP_URL=http://domain.com` to `APP_URL=https://domain.com`.
- Step 2:
    - Option 1: Add to **.env** `ENABLE_HTTPS_SUPPORT=true`.
    - Option 2: Add to **.env**:
      ```bash
        FORCE_SCHEMA=https
        FORCE_ROOT_URL=https://domain.com  
        ENABLE_HTTPS_SUPPORT=false
      ```
If it doesn't work, you have to config it in .htaccess or Nginx config.