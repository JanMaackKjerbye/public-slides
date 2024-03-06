---
marp: true
footer: ![w:200 invert](../img/OS2_logo_cmyk.svg)
theme: uncover

class: 
 - invert
 
headingDivider: 1
paginate: false
---
#
![bg sepia:0.8 brightness:0.7](../img/Arkitektur.gif)
#### Jan Maack Kjerbye
###### 💼 Enterprise Arkitekt
###### ✉️ jan@os2.eu


# **LOKALE MÅL**
![bg brightness:0.8 sepia:0.1 ](https://images.unsplash.com/photo-1586339949531-a77bdcc85fef?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
####  🩹 Levetidsforlængelse?

#### 🏅 Konkurrencedygtighed?

#### 💸 Besparelser?

#  **FÆLLES MÅL**
![bg brightness:0.9 blur:0.5px](https://images.pexels.com/photos/194094/pexels-photo-194094.jpeg)
####  📈 Udbredelse
#### 🎯 Profesionalisering
#### 💡 Talentudvikling

# **NATIONALE MÅL**
![bg brightness:0.8 blur:1px](https://images.pexels.com/photos/3482442/pexels-photo-3482442.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)

#### 🔀 Sammenhængende it
#### 🧩 Byg til genbrug og forandring
#### 🤝🏻 Flere leverandører

# **INTERNATIONALE MÅL**
![bg brightness:0.7 blur:1px](https://images.unsplash.com/photo-1628313348684-5d75dd67e7c8)
#### 🪢 Interoperability
#### 👑 Soverignity
#### ⬆️ Upstream first
#### 🔌 API first


# **ROADMAP**
<!-- BackgroundColor: white -->
![bg  brightness:0.9](https://images.unsplash.com/photo-1533930086187-0fc58e5a92e2?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

#

```
Udvikling prioriteres til kernefunktionalitet resten løses af åbne standard løsninger
```

```
Standardløsninger leverer færdigudviklet sikkerhed, compliance, skalering ud fra industry best-practice
```
```
Vejen ryddes for interoperabilitet og genbrug via allerede indbyggede åbne integrations standarder
```

```
Vedligeholdelsesbyrden distribueres til bred vifte af profesionelle udviklere i communitiet
```

#

> ..one key reason why open source technology is a great choice. 
> It gives an organization the flexibility to change rapidly. 

![bg brightness:0.5](https://images.unsplash.com/photo-1557318041-1ce374d55ebf?q=80&w=2080&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

# **SIKKERHED**
 *“Given enough eyeballs, all bugs are shallow,”*
###### **-Eric Steven Raymond “The Cathedral and the Bazaar.”**

![bg blur:1.5px brightness:0.9](https://images.unsplash.com/photo-1477281765962-ef34e8bb0967?q=80&w=1933&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
<!-- The message here is that, given a large enough developer/tester base, almost every problem in a piece of software can be identified quickly and the fix will become obvious to someone. This is the benefit of having better software reviewing processes. The review audience of open source software systems is much larger and diverse. This not only makes the software better and more secure, but, in the case of a defect or vulnerability, it also enables finding a fix faster. -->

#
## <!-- fit --> - Aktivitet
![bg](../img/local_contrib.png)
![bg](../img/Upstream_contrib.png)

#

<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

<div class="mermaid">

quadrantChart
    title Activity and engagement
    x-axis Low Engagement --> High Engagement
    y-axis Inactive --> High Activity
    quadrant-1 Contribute
    quadrant-2 Remarket
    quadrant-3 Lifecycle analysis
    quadrant-4 Integrate
    Kong Project: [0.9, 0.9]
    Tyk Project: [0.85, 0.86]
    OSindberetning: [0.51, 0.09]

</div>