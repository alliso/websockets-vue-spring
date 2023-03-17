
# Table of Contents

1.  [Description](#orgb9decc9)
2.  [Launch the project](#orgcd470e5)
3.  [Websockets in Spring Boot](#org529b474)
    1.  [Project setup](#orgdd0d822)
    2.  [Followed tutorials](#orgae4f1fa)
    3.  [Own notes](#orgfa5164d)
    4.  [Future researches](#org82b5c56)
4.  [Websockets in Vue](#org79065f6)
    1.  [Project setup](#orgec8cc77)
    2.  [Followed tutorials](#orga771c67)
    3.  [Own notes](#org55227a9)
    4.  [Future researches](#orgc87c326)
5.  [Docker compose](#org6439797)


<a id="orgb9decc9"></a>

# Description

Project to test websocket communication between Vue and Spring Boot.


<a id="orgcd470e5"></a>

# Launch the project

Go to the main folder of the project and execute.

    docker compose up -d


<a id="org529b474"></a>

# Websockets in Spring Boot


<a id="orgdd0d822"></a>

## Project setup

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-right" />

<col  class="org-left" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Project</th>
<th scope="col" class="org-left">Language</th>
<th scope="col" class="org-right">Spring Boot</th>
<th scope="col" class="org-left">Packaging</th>
<th scope="col" class="org-right">Java</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Maven</td>
<td class="org-left">Java</td>
<td class="org-right">3.0.4</td>
<td class="org-left">Jar</td>
<td class="org-right">17</td>
</tr>
</tbody>
</table>


<a id="orgae4f1fa"></a>

## Followed tutorials

- [Java in use tutorial](https://www.javainuse.com/spring/boot-websocket)


<a id="orgfa5164d"></a>

## Own notes

-   Remember to set allowed origins.


<a id="org82b5c56"></a>

## Future researches

- [ ] Websockets with Stomp


<a id="org79065f6"></a>

# Websockets in Vue


<a id="orgec8cc77"></a>

## Project setup

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">Node</th>
<th scope="col" class="org-right">Vue</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">19</td>
<td class="org-right">2.6.12</td>
</tr>
</tbody>
</table>


<a id="orga771c67"></a>

## Followed tutorials

- [Fireship websockets and beyond video](https://www.youtube.com/watch?v=1BfCnjr_Vjg)


<a id="org55227a9"></a>

## Own notes


<a id="orgc87c326"></a>

## Future researches

- [ ] Socket.io


<a id="org6439797"></a>

# Docker compose

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-right" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Service</th>
<th scope="col" class="org-left">Image</th>
<th scope="col" class="org-right">Ports</th>
<th scope="col" class="org-left">Volumes</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">frontend</td>
<td class="org-left">maven:3.8.5-openjdk-17</td>
<td class="org-right">5173:5173</td>
<td class="org-left">./frontend:/usr/src/app</td>
</tr>


<tr>
<td class="org-left">backend</td>
<td class="org-left">node:19</td>
<td class="org-right">8080:8080</td>
<td class="org-left">./backend:/usr/src/app</td>
</tr>
</tbody>
</table>

