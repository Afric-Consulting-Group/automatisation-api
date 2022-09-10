# Total.js Flow

- [Website](https://www.totaljs.com/flow/)
- [__Documentation__](https://docs.totaljs.com/flow10/)
- [Chat support](https://platform.totaljs.com/?open=messenger)
- [Join __Total.js Telegram__](https://t.me/totalplatform)
- [Support](https://www.totaljs.com/support/)

__Requirements__:

- Total.js 4 - `$ npm install total4`

__Run__:

```
npm run start
```
or directly using node executable (port is optional, default 8000)
```
node index.js <port>
```
__Sitemap (Routes)__

`/`                      ----> `Espace de validation`


`/flow`                 ----> `Espace technique de maintenance et de programmation visuelle`

`/evenements`           -----> `Espace de validation service foot`



__Docker__:

```bash
docker pull totalplatform/flow
docker run -p 8000:8000 totalplatform/flow
````

# Documentation

## Introduction globale
Afric Consulting Group est une entreprise specialisee dans la conception, la creation et la maintenance des services a valeurs ajoutees SVA (SVI, KIOSQUE MOBILE, CENTRE D'APPEL, USSD, SMS etc) pour les operateurs de telephonie mobile.Cette application intervient specifique dans le cadre des service KIOSQUE MOBILE. L'entreprise dispose d'une equipe de mise a jours des contenus de kiosque et cette application servira a automatiser les differentes taches repetives des agents de mise a jour.

## L'objectif de l'application.
Le but principal de l'application est d'aider les agents de mise a jour dans leurs taches quotidiennes. La methode traditionnelle de mise a jour consitait a aller sur internet, parcourrir des dizaines de sites web, collecter les informations ou contenus, les trier, les analyser, les mettre sous format SMS, et les preparer au mieux pour etre diffuses a des millions d'abonnes des differents operateurs de telephonie mobile (TELECEL FASO, MOOV AFRICA BURKINA, MOOV AFRICA BENIN, MOOV AFRICA MALI). Ces taches sont repetives, fatiguantes et prennent enormement du temps si bien que la qualite et la quantite baisse au fil du temps. L'objectif donc de l'application est d'automatiser au maximum les differentes taches afin de faciliter la vie des agents de mise a jours et eventuellement avoir du temps et de l'energie pour d'autres inovations.

## Fonctionnement global
D'une part l'application consomme des API REST disponible sur internet afin de recuperer periodiquement les informations, les trier, les formater et conserver en base de donnee selon la logique business du service kiosque mobile.
D'autre part, l'application se sert du [__DATA SCRAPING__](https://www.rgdesign.fr/blog/web-scraping/) pour les sites qui n'ont pas d'API.

## Outils et dependances de programmation
- [__Total.js platform__](https://www.totaljs.com)
 
  Total.js Platform est une collection de bibliothèques JavaScript, de composants d'interface utilisateur, de pratiques et d'applications complètes écrites en JavaScript pur, la plupart du temps sans dépendances. Gratuit et open source. La chose amusante de total.js est que pour concevoir une application, tout ceux dont vous avez besoin c'est de faire une seule fois `npm install total4` et vous avez tout pour faire votre application. Grace a sa [__documentation__](https://docs.totaljs.com) tres riche et detaillee, il est tres facile et rapide de concevoir son siteweb. Si vous aimez apprendre par les videos, [__Cette serie de video youtube__](https://www.youtube.com/watch?v=De-PZ7UQH_s&list=PL0TUP_nW6cmTguY8FsxFzm3cN-cPIJGAS&index=4) va vous etre util (N'oubliez pas de vous abonner, de liker et de partager 👨🏽‍💻😁🥳😅👨🏽‍💻).

- [__Total.js flow 10+__](https://www.totaljs.com/flow)

  Total.js flow est une application de programmation visuelle construite au dessus de total.js. Sa [__documentation__](https://docs.totaljs.com/flow) est aussi tres riche et detaillee. Si c'est votre premiere fois d'entendre parler de la programmation visuelle et de total.js FLOW 10, alors [__Cette serie de video youtube__](https://www.youtube.com/playlist?list=PL0TUP_nW6cmSA-QsjzgHTOfIRxHf0M4xk) va aussi vous aider.  (N'oubliez pas egalement de vous abonner, de liker et de partager 👨🏽‍💻😁🥳😅👨🏽‍💻).
  
  <a href="https://ibb.co/CQGRtBg"><img src="https://i.ibb.co/SBCFxNb/Screenshot-at-2022-09-10-10-36-48.png" alt="Screenshot-at-2022-09-10-10-36-48" border="0"></a>
  
- [__Cheerio.js__](https://cheerio.js.org/)

  Cheerio est une librairie javascript qui facilite le DATA SCRAPING. A l'interieur de totaljs flow nous avons un composan qui porte son nom. Son fonctionnement est comme suite il prend en entree un document HTML et retourne une instance de Jquery de ce document HTML permettant ainsi de manipuler a volonte et de recuperer les ressources textes de ce document HTML.  Si c'est votre premiere fois d'entendre parler de cheerio alors [__Cette video youtube__](https://www.youtube.com/watch?v=-e_QdRIKzYo) vous sera utile.

  
## Exemple d'automatisation par API

### Meteo et Actualites

- Meteo 

  Dans le cas de la meteo nous avons utilise comme API [__Open wheather__](https://openweathermap.org/api). Il faut noter aussi que l'API utilise les coordonnees geographique de [__Google Maps__](https://www.google.com/maps/d/viewer?mid=1_FHxOZC_HTtuUvdI5ls43mkUR4s&ie=UTF8&hl=fr&msa=0&ll=12.849293000000007%2C-1.549071999999998&spn=1.231767%2C2.087402&z=9&om=1) pour pouvoir envoye les informations specifique a l'endroit voulu
  
  <a href="https://ibb.co/JQCRJ4X"><img src="https://i.ibb.co/GTFvSLg/Screenshot-at-2022-09-10-11-01-21.png" alt="Screenshot-at-2022-09-10-11-01-21" border="0"></a>

- Actualites

  Dans le cas des actualites nous avons utilise comme API [__Mediastack__](https://mediastack.com/documentation) pour recuperer les informations en temps reel sur les actualites du momde plus precisement celles des pays de la zone UEMOA
  
  <a href="https://ibb.co/2dXsHgz"><img src="https://i.ibb.co/yqLY7Wz/image.png" alt="image" border="0"></a>
  
  
## Exemple d'automatisation par DATA SCRAPING

### PMU et Horoscope

- PMU

  Dans le cas de PMU nous avons deux sites principalement sur lesquels nous collectons les donnees avec le data scraping a savoir [__Turf-fr__](https://www.turf-fr.com/)

<a href="https://ibb.co/hWcJR9x"><img src="https://i.ibb.co/swCdvRp/image.png" alt="image" border="0"></a>

et [__Canalturf__](https://www.canalturf.com/)

<a href="https://ibb.co/BnkXcDK"><img src="https://i.ibb.co/8YkWN34/image.png" alt="image" border="0"></a>

- Horoscope

  Dans le cas de Horoscope nous faisons le data scrapingsur le site de [__Asiaflah__](https://www.asiaflash.com/) pour la collecte des donnees en fonction d'horoscope (Amour, Famille ....) ou de type d'horoscope (belier, balance ....)
  
  <a href="https://ibb.co/Xzf1w8w"><img src="https://i.ibb.co/wKZVvsv/image.png" alt="image" border="0"></a>
  
