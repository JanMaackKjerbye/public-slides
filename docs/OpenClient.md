---
marp: true
footer: ![w:150 opacity:1 brightness:3 ](https://www.os2.eu/web/image/website/1/logo/OS2%20%E2%80%93%20Offentligt%20digitaliseringsf%C3%A6llesskab?unique=8a4ead6)
---
<!--
theme: uncover
transition: dissolve
class:
 - invert
headingDivider: 2 
paginate: false
-->

### OS²OpenClient
<!--_footer: "" -->
<!--_header: ![w:240 opacity:0.9 brightness:2 ](https://www.os2.eu/web/image/website/1/logo/OS2%20%E2%80%93%20Offentligt%20digitaliseringsf%C3%A6llesskab?unique=8a4ead6) -->
LØST KOBLET STYRING AF LINUX DEVICES
![bg blur:2px brightness:0.5](../img/sigmund-B-x4VaIriRc-unsplash.jpg)


#
🏗️ ARKITEKTUR OPLÆG
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

<pre class="mermaid">

graph TB

semaphore(&amp#x1F619 ManagementUI- ansible-semaphore);

subgraph NUC
debarm("`**OS²OpenClient** debian_x64`")-.-
app2("`**Chromium browser** kiosk_mode`")
end


subgraph RPi
debx64("`**OS²OpenClient** debian_armx64`")-.-
app1("`**Chromium browser** kiosk_mode`")
end

subgraph Backend
configman("`**OS²Konfiguration** *github.com/  ansible*`");
netboot("`**OS²Deploy** *github.com/ netboot.xyz*`");
end

configman<-->semaphore
configman--ssh-->RPi & NUC

</pre>

#
### 🔧 ANSIBLE
###### Agentless automatisk konfiguration og udrulning

![bg left:18% brightness:0.3 blur:1px](https://spacelift.io/_next/image?url=https%3A%2F%2Fspaceliftio.wpcomstaging.com%2Fwp-content%2Fuploads%2F2022%2F02%2F54.ansible.png&w=1920&q=100)

   - [80 contributors - 7700 stars](https://github.com/ansible)
   - [Getting started](https://docs.ansible.com/ansible/latest/getting_started/index.html)
   - [Beginner Tutorial](https://spacelift.io/blog/ansible-tutorial)
   - [Desktop Automation examples](https://beta-galaxy.ansible.com/ui/collections/?page_size=10&view_type=null&keywords=desktop&page=1)



##
### 🔮 SEMAPHORE
![bg right:54% brightness:0.6 blur:1px w:640](../img/semaphore.gif)
 - [Modern Web UI](https://www.ansible-semaphore.com/)


# 💽 OS Deployment
###### nebootxyz

![bg left:38% brightness:0.4 blur:2px](../img/lucian-alexe-yh0UtueiZ-I-unsplash.jpg)

https://netboot.xyz/
