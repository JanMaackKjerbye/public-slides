---
marp: true
footer: ![w:200 invert](../img/OS2_logo_cmyk.svg)
theme: uncover
transition: reveal
class: 
 - invert
 
headingDivider: 1
paginate: false
---
#
![bg sepia:0.2 brightness:0.7](../img/Arkitektur.gif)
#### Jan Maack Kjerbye
###### 💼 Enterprise Arkitekt
###### ✉️ jan@os2.eu

# 📊 **BUSINESS INTELLIGENCE**
###### Hvilke arbejdsgange og opgaver forventes det at et "BI system" understøtter?
![bg bg blur:1px brightness:0.3](https://images.pexels.com/photos/577210/pexels-photo-577210.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)

# **FUNDAMENTET**
### DATAINDSAMLING
![bg blur:1px brightness:0.4](https://images.unsplash.com/photo-1518181835702-6eef8b4b2113?q=80&w=1740&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)


###### 📜 Er "BI" prioriteret som et strategisk initiativ i organisationen?

###### 👑 Er der topledelses mandat til arbejdet med at tilgå de nødvendige data?


# **DAGLIGDAGEN - DRIFT**
![bg blur:1px brightness:0.6](https://images.unsplash.com/photo-1485216983937-749292830fcf?q=80&w=1796&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

##### Forventes dataindhentning, validering og overvågning at indgå som en del af et "BI System"?
##### Er der sikret ressourcer og kompetencer til at løse denne opgave?

# **ROLLER**

Data Manager
Data Engineer
Data Scientist


#
![blur:6px bg brightness:0.8](https://images.unsplash.com/photo-1504164996022-09080787b6b3?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

<div class="mermaid">
%%{init: {'theme': 'dark', 'themeVariables': { 'fontSize': '12px', 'fontFamily': 'monospace'}}}%%

graph TD
 A[(source..)] & B[(source..)] & C[["\nsource..\n_"]]-.->D
    subgraph M[MANAGEMENT....] 
    Metrics.
    Access.
    Schedules..
    Events.
    end
    subgraph K[PIPELINE... ]
        D("Ingest..")-.->
         F[(Store..)]-.->       
        E[Transform....]-.->F-.->An([Analyze...]) & ML.-.->F
    end
    subgraph ASH[VIEW..]
    REP[["\n Report..\n."]]
    Dashboard....
    end
An==>ASH
M-.-K
classDef default fill:#13294B;

</div>