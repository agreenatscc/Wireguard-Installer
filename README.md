# Wireguard-Installer
 WireGuard installer for Ubuntu, Debian, Fedora, CentOS, Arch Linux
 
<article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-wireguard-installer" class="anchor" aria-hidden="true" href="#wireguard-installer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>WireGuard installer</h1>
<p><strong>This project is a bash script that aims to setup a <a href="https://www.wireguard.com/" rel="nofollow">WireGuard</a> VPN on a Linux server, as easily as possible!</strong></p>
<p>WireGuard is a point-to-point VPN that can be used in different ways. Here, we mean a VPN as in: the client will forward all its traffic trough an encrypted tunnel to the server.
The server will apply NAT to the client's traffic so it will appear as if the client is browsing the web with the server's IP.</p>
<p>The script supports both IPv4 and IPv6. Please check the <a href="https://github.com/angristan/wireguard-install/issues">issues</a> for ongoing development, bugs and planned features!</p>
<p>WireGuard does not fit your environment? Check out <a href="https://github.com/angristan/openvpn-install">openvpn-install</a>.</p>
<h2><a id="user-content-requirements" class="anchor" aria-hidden="true" href="#requirements"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Requirements</h2>
<p>Supported distributions:</p>
<ul>
<li>Ubuntu</li>
<li>Debian</li>
<li>Fedora</li>
<li>CentOS</li>
<li>Arch Linux</li>
</ul>
<p>I recommend these cheap cloud providers for your VPN server:</p>
<ul>
<li><a href="https://goo.gl/Xyd1Sc" rel="nofollow">Vultr</a>: Worldwide locations, IPv6 support, starting at $3.50/month</li>
<li><a href="https://goo.gl/76yqW5" rel="nofollow">PulseHeberg</a>: France, unlimited bandwidth, starting at €3/month</li>
<li><a href="https://goo.gl/qXrNLK" rel="nofollow">Digital Ocean</a>: Worldwide locations, IPv6 support, starting at $5/month</li>
</ul>
<h2><a id="user-content-usage" class="anchor" aria-hidden="true" href="#usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Usage</h2>
<p>Download and execute the script. Answer the questions asked by the script and it will take care of the rest.</p>
<div class="highlight highlight-source-shell"><pre>curl -O https://raw.githubusercontent.com/agreenatscc/Wireguard-Installer/master/wireguard-install.sh
chmod +x wireguard-install.sh
./wireguard-install.sh</pre></div>
<p>It will install WireGuard (kernel module and tools) on the server, configure it, create a systemd service and a client configuration file.</p>
<p>To generate more client files, run the following:</p>
<div class="highlight highlight-source-shell"><pre>./wireguard-install.sh add-client</pre></div>
<p>Make sure you choose different IPs for you clients.</p>
<p>Contributions are welcome!</p>
</article>
