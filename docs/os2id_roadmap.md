---
marp: true
footer: ![w:150 opacity:1 brightness:4](https://www.os2.eu/web/image/website/1/logo/OS2%20%E2%80%93%20Offentligt%20digitaliseringsf%C3%A6llesskab?unique=8a4ead6)
theme: uncover
class:
 - invert
headingDivider: 2 
paginate: false
---

# 🪪 [OS²ID](https://github.com/OS2lab/OS2ID)
<!-- _header: "" -->
Fælles identitessikkerhed baseret på åbne standarder
![blur:1px bg auto brightness:0.5](https://images.unsplash.com/photo-1585079374502-415f8516dcc3)


# 
<!-- _header: "🪪 [OS²ID](https://github.com/OS2lab/OS2ID)" -->
![blur:1px bg left:55% brightness:1.3](https://images.unsplash.com/photo-1585079374502-415f8516dcc3)
#### **BASERET PÅ EKSISTERENDE KOMPONENTER**

###### ♻️ Klar til genbrug
###### 🔮 Bygget til fremtiden
###### 💝 Delegeret vedligehold
<!--
###### 🎁 **Et NIS2 understøttende bidrag fra OS²** 
Bygger på standard teknologier (JWT OpenIDconnect) og

(Upstream first) - Baseret på upstream komponenten Authentik = delegeret vedligehold

Klar til genbrug (Open by default, Open Standards)
kan anvendes i andre os2produkter som authentication/authorization komponent istedet for at alle produkter laver sin egen integration til f.eks FK. og senere statens IT?

###### 🕋 Afgrænset kerne (Minimum viable Product) Kun basal login flow understøttes i PoC
 - Hvor langt kan man komme på 14 (arbejds)dage 100 timer - deraf 30 til at lave dokumentations arbejde på KOMBIT delen. KOMBIT er tung og svært at tilegne sig, så vi investerer i en mere simpel dokumentation til leverandørerne.


-->
# ROADMAP
#### **PoC - Demo - Customer0**
<!-- _header: "🪪 [OS²ID](https://github.com/OS2lab/OS2ID)" -->
![blur:9px bg brightness:0.9](https://images.unsplash.com/photo-1585079374502-415f8516dcc3)

<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

<div class="mermaid">

gantt
    title OS2id
    dateFormat  YYYY-MM-DD
    section Code
    Kickoff           :a1, 2023-11-16, 14d
    PoC    :b1, 2023-12-01, 2024-02-10
    Demo :c1, 2024-03-01, 130d
    section Docs
    Getting started :d1, 2023-12-01, 2024-02-10

</div>

#
<div class="mermaid">

%%{init: { 'gitGraph': { 'mainBranchName': 'Cloud 0'}} }%%
gitGraph
    commit id: "Google Borg 2003"
    commit id: "Amazon EC2 2006"
    branch "Cloud 1.0"
    commit id:"DevOps 2005"
    checkout "Cloud 0"
    commit id:"Microsoft Azure 2010"
    checkout "Cloud 1.0"
    commit id:"Google App Engine 2008"
    commit id:"12 Factor App 2011"
    commit id:"Docker 2013"
    branch "Cloud 2.0"
    commit id:"Google Kubernetes 2014"
    commit id:"CNCF 2015"

<div>

# LETS DIVE IN

![bg](../img/dive_in.webp)
