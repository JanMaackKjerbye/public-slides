---
marp: true
footer: ![w:150 opacity:1 brightness:4](https://www.os2.eu/web/image/website/1/logo/OS2%20%E2%80%93%20Offentligt%20digitaliseringsf%C3%A6llesskab?unique=8a4ead6)
theme: uncover
class:
 - invert
headingDivider: 2 
paginate: false
---


# ⚖️ [Deployment](https://github.com/OS2compliance/)
![bg blur:2px saturate:0.75 hue-rotate:700deg brightness:0.4](https://images.pexels.com/photos/4779729/pexels-photo-4779729.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)

Ensartet, best-practise baseret deployment repositories i så mange produkter som muligt.
<!-- transition: cube -->


#
<!-- header: "⚖️ [OS²compliance](https://github.com/OS2compliance/)" -->
![bg left:56% 100% opacity:0.7 brightness:0.88](../img/compliance_insight.png)
TRANSPARENT SKABELONBASERET UDVIKLING
###### **🎟️ Alle ændringer er tydelige og stemples med dato, udvikler og formål**

#
<!-- theme: default -->

├── orchestrated-deployment
│   ├── README.md
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   └── .env-example
└── local-deployment
    ├── README.md
    ├── Dockerfile
    ├── docker-compose.yaml
    └── .env-example