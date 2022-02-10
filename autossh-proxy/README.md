<p align="center">
  <a href="https://hub.docker.com/r/jnovack/autossh">
    <img src="https://cdn.svgporn.com/logos/docker.svg" alt="Docker logo" title="jnovack/autossh" width="350"/>
  </a>
</p>

# Description 

The idea of this chart is the same as the Cloudflared one but with non-http applications. 

This chart will generate a tunnel to an instance in AWS, Azure or whatever provider you use to allow you to host different services without openning ports in your router or firewall. Also is great to avoid pointing DNS record to your public IP address.
