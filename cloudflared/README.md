<p align="center">
  <a href="https://hub.docker.com/r/erisamoe/cloudflared">
    <img src="https://cdn.svgporn.com/logos/cloudflare.svg" alt="Cloudflare logo" title="Cloudflared" width="350"/>
  </a>
<p/>

# Chart requisites

1. You need to create a named Argo tunnel. In order to create one, you will need a Cloudflare account and the `cloudflared` utility.
2. Once you have a Cloudflare account and the `cloudflared` utility run `cloudflared tunnel login` to get a login certificate for your account and domain to start using `cloudflared`.
3. Create a named tunnel for your hostname using `cloudflared`, you can follow the documentation steps [here](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/create-tunnel).
4. A secret JSON file will be generated after the creation of your tunnel. That file need to be renamed to `creds.json` and copied to the secrets folder to allow the container to control the tunnel.
5. Once everything is ready, you need to go to your Cloudflare account and create a CNAME record with your domain pointing to the tunnel `<UUID>.cfargotunnel.com`.
