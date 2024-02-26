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
LØST KOBLET STYRING AF DEVICES
![bg blur:2px brightness:0.5](../img/sigmund-B-x4VaIriRc-unsplash.jpg)


# Sænke barren for bidrag

Letforståeligt format
###### Deklarative formater er mere læsbare end scripts, hvilket kan gøre det nemmere for nye medlemmer af dit team at forstå og bidrage

###### Deklarative formater er nemmere at vedligeholde end scripts, da de ikke kræver kendskab til de specifikke kommandoer eller scriptingsprog

## Eksempel

YAML / Ansible
```yaml 

- hosts: localhost
  tasks:
    - name: Ensure directory exists and create it if it doesn't
      ansible.builtin.file:
        path: /path/to/directory
        state: directory
        owner: username
        group: groupname
        
```
##
<!--_header: "bash" -->
```bash 
#!/bin/bash

# Define the directory to be created
DIR="/path/to/directory"

# Define the log file
LOGFILE="/path/to/logfile.log"

# Define the user and group
USER="username"
GROUP="groupname"

# Function to check if a directory exists
function check_dir() {
    if [ -d "$1" ]; then
        echo "Directory $1 exists."
        return 0
    else
        echo "Directory $1 does not exist." >&2
        echo "$(date): Directory $1 does not exist." >> $LOGFILE
        return 1
    fi
}

# Function to create a directory
function create_dir() {
    mkdir -p "$1"
    if [ $? -eq 0 ]; then
        echo "Directory $1 created successfully."
        chown $USER:$GROUP "$1"
        chmod 755 "$1"
        return 0
    else
        echo "Failed to create directory $1." >&2
        echo "$(date): Failed to create directory $1." >> $LOGFILE
        return 1
    fi
}

# Function to check permissions
function check_permissions() {
    if [ -w "$(dirname "$1")" ]; then
        echo "Write permission is granted on the parent directory."
        return 0
    else
        echo "Write permission is not granted on the parent directory." >&2
        echo "$(date): Write permission is not granted on the parent directory." >> $LOGFILE
        return 1
    fi
}

# Check permissions
check_permissions $DIR
if [ $? -eq 0 ]; then
    # Check if the directory exists
    check_dir $DIR
    if [ $? -ne 0 ]; then
        # If the directory does not exist, create it
        create_dir $DIR
    fi
fi

```

##
![bg blur:2px brightness:0.3 sepia:0.7](https://images.unsplash.com/photo-1573030889348-c6b0f8b15e40?q=80&w=2675&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
### :recycle: **Genbrug & Standardisering**
###### 📦 Eksisterende, velprøvet og pålidelig løsning
###### 🌐 Anvendt og trykprøvet af tusindvis af internationale organisationer
###### 🧑‍🤝‍🧑🧑🏻‍🤝‍🧑🏾 Konstant forbedret og vedligholdt af et globalt community af udviklere

##
![bg blur:4px brightness:0.4 sepia:0.7](https://images.pexels.com/photos/5805485/pexels-photo-5805485.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)
### Ensartedhed & forudsigelighed

###### **Reduktion af fejl og uforudsete konsekvenser**
###### Deklarativt format beskriver det ønskede slutresultat, ikke de trin, der skal tages for at nå det.

###### **Idempotens**
###### Jobs kan køre flere gange uden at ændre resultatet efter den første succesfulde kørsel.

# Sikkerhed
 ‘Desired state’ metoder gør det nemt at vende tilbage til en kendt god tilstand, hvis noget går galt. Dette kan reducere risikoen for nedetid og data tab, hvilket kan forbedre virksomhedens sikkerhed og compliance.

# Bygget til fremtiden
 Klar til automatisering
 Portabilitet og interoperabilitet:
 investerer I i en metode, der er moderne, populær og understøttet af et stort community. Dette kan hjælpe med at sikre, at jeres konfigurationsstyring forbliver relevant og effektiv i fremtiden.

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
