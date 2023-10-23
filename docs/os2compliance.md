---
marp: true
footer: ![w:150 opacity:1 brightness:4](https://www.os2.eu/web/image/website/1/logo/OS2%20%E2%80%93%20Offentligt%20digitaliseringsf%C3%A6llesskab?unique=8a4ead6)
---
<!--
theme: uncover
transition: dissolve
class:
 - invert
headingDivider: 2 
paginate: false
-->

## OS²compliance ![bg l40% blur:2px brightness:0.6](https://images.pexels.com/photos/1383416/pexels-photo-1383416.jpeg)
:small_blue_diamond:
###### REPO SETUP OCT 2023

## **STRATEGISK FUNDAMENT**
![bg brightness:0.4](https://images.pexels.com/photos/18624136/pexels-photo-18624136/free-photo-of-bygning-gangbro-korridor-entre.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)
#### Talentudvikling:small_blue_diamond:Rammeskabelse
#### Åbenhed:small_blue_diamond:Ejerskab


## **TALENTUDVIKLING**
#### *Styrkelse og ensartethed af:*


 Organisering:small_blue_diamond:Værktøjskasse:small_blue_diamond:Dokumentation:small_blue_diamond:Samararbejdsmetoder:small_blue_diamond:Transparens
![bg l40% blur:2px brightness:0.3](https://images.pexels.com/photos/4482012/pexels-photo-4482012.jpeg?auto=compress)

## **RAMMMESKABELSE**

#### *Operationalisering af processer og metoder*
 Automatsering:small_blue_diamond:Ensartethed
 Flerleverandør samarbejde
![bg l40% blur:2px brightness:0.3](https://images.pexels.com/photos/3184660/pexels-photo-3184660.jpeg)

##
#### 🫱🏾‍🫲🏼 CONTRIBUTING.md
![bg brightness:0.4](https://images.pexels.com/photos/461049/pexels-photo-461049.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)
###### ⭐ Issues trackes i GitHub 
###### ⭐ Commits og PRs linkes til issues
###### ⭐ Flow: issue->branch->commit/PR 
###### ⭐ Conventional Commits
<!--Eksempler:

chore: update project dependencies #3456

fix: resolve null reference exception in data processing module #1234

feat: implement typeahead in the product catalog search functionality #7890 -->

## 
#### ☸️ STYRING
![bg blur:1px brightness:0.6](https://images.pexels.com/photos/1416649/pexels-photo-1416649.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)
###### ⭐ Epics samler issues og ligger i GitHub - kan synces til Jira
###### ⭐ Hvis arbejdet bliver for tungt kan der investeres i automatisk synkronisering.
<!-- Store features med mange underopgaver labeles som Epics og og kan holdes alene i GitHub Issues eller hvis der ønskes Epic issues spejlet i Jira til projektstyring, kan det gøres manuelt.

Der kan også vælges GitHub Projects til styring.

Hvis arbejdet bliver for tungt kan der investeres i automatisk synkronisering.-->

#
![bg blur:1px brightness:0.3](https://images.pexels.com/photos/5428833/pexels-photo-5428833.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)
###### ❓ Er der lavet Dockerfiler?
##### ❓ CI/CD: Bliver der bygget images automatiskt med github actions?
❓ Er der lavet en docker-compose til udvikling/demo/test?
❓ Placeres integrationer i eget repo
❓ Kan de køre løskoblet som standalone services med standard snitflader?