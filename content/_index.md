+++
title = "My presentation"
outputs = ["Reveal"]
[reveal_hugo]
theme = "black"
+++

# ------------------
# Solution d’analyse LAN/WAN

#####################
<section data-background-video="Blurred.mp4" data-background-video-loop="loop">
</section>

---

# Objectif de la solution

- {{% fragment %}} Avoir une remontée des informations du trafic réseau centralisée et sécurisée {{% /fragment %}}
- {{% fragment %}} Visualiser les données avec des graphiques pour une lecture simple et efficace {{% /fragment %}}
- {{% fragment %}}Pouvoir prendre en main le système à distance grâce à une interface simple et intuitive{{% /fragment %}}
- {{% fragment %}}Utilisation d’outils libres et gratuits{{% /fragment %}}

---

# Présentation des éléments :

- {{% fragment %}}Docker / Portainer.io{{% /fragment %}}
- {{% fragment %}}NTOPNG{{% /fragment %}}
- {{% fragment %}}Grafana{{% /fragment %}}
- {{% fragment %}}Elasticsearch{{% /fragment %}}
- {{% fragment %}}Kibana{{% /fragment %}}
- {{% fragment %}}Xampp{{% /fragment %}}

---
{{% section %}}
# Docker

<section>
<img src="http://www.loligrub.be/blog/wp-content/uploads/2017/01/docker_logo.png" style="width:210px;height:150px">
</section>

<section>	
	<ul>
		<li>Open source</li>
		<li style="text-align: justify;">Docker est une plateforme de virtualisation par conteneur. Son but est de permettre d'empaqueter une application pour la rendre facilement déployable et exécutable sur tout hôte Docker, dans un conteneur </li>
	</ul>
</section>

---

# Docker

<img src="https://xataz.developpez.com/tutoriels/utilisation-docker/images/image-1.png" >


---

# Portainer io 

Portainer est une application qui permet de gérer via une interface graphique un environnement docker 
<img src="https://portainer.io/images/screenshots/portainer-docker-dashboard.jpg" >

{{% /section %}}

---

# NTOPNG

<img src="https://www.poftut.com/wp-content/uploads/2017/11/img_5a016c5f36ba5.png"  style="width:210px;height:110px" >
<p style="text-align: justify;"> NTOP (Network TOP) est un outil libre de supervision réseau. C'est une application qui capture et analyse les trames d'une interface donnée, et permet d'observer une majeure partie des caractéristiques du trafic (entrant et sortant) </p>

---

# Grafana

<img src="https://www.neteye-blog.com/wp-content/uploads/2017/12/Grafana.png" >
<p style="text-align: justify;"> Grafana est un logiciel libre qui permet la visualisation et la mise en forme de données métriques. Il permet de réaliser des tableaux de bord et des graphiques depuis plusieurs sources. Grafana dispose d’un plugin NTOP qui permet d’intégrer facilement les mesures acquises par celui-ci </p>



---

# Elasticsearch + Kibana

<p style="text-align: justify;"> ElasticSearch est la base de données et le moteur d’indexation, et Kibana l'interface graphique utilisée pour afficher les données. Comme ntopng est capable d'exporter nativement des données dans ElasticSearch, nous n'avons pas besoin d'utiliser LogStash. </p>


---

# Xampp - Apache + MariaDB + PHP + Perl

<p style="text-align: justify;"> Xampp est un ensemble de logiciels permettant de mettre en place un serveur Web en local </p>


---
{{% section %}}

# Infrastructure

<img src="https://i.imgur.com/511G9qH.png" >


---

# Infrastructure

<img src="https://i.imgur.com/BNIhSl8.png" >

{{% /section %}}

---

<script id="asciicast-9XieppEm4YY9DCnhpbIPKPEX2" src="https://asciinema.org/a/9XieppEm4YY9DCnhpbIPKPEX2.js" async></script>


---

# Lancement NTOPNG

<pre><code>
ntopng -F “es;<ES Index Type>;<ES Index Name>;<ES URL>;<ES pwd>”
	</code></pre>
<pre><code>
ntopng -F “es;flows;ntopng-%Y.%m.%d;http://XYZ:9200/_bulk;”
	</code></pre>
	
---

# Démo

http://10.135.224.126:41062/www/

---

# Conclusion

- {{% fragment %}}Déploiement chez un client ?{{% /fragment %}}
- {{% fragment %}}Accès aux données{{% /fragment %}}

---

{{< slide id="hello" background="#FFF" transition="zoom" transition-speed="fast" >}}

# FIN

---



contact: matthias.bricard@axians.com