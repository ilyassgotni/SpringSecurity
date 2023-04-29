<h2>Gestion des Patient avec Spring Security 6</h2>

<p>• Spring Security a une architecture conçue pour séparer l'authentification de
l'autorisation et offre des stratégies extensibles pour les deux. <br>
• Spring Security est un module de Spring qui permet de sécuriser les
applications Web. <br>
• Spring Security configure des filtres (springSecurityFilterChain) qui permet
d’intercepter les requêtes HTTP et de vérifier si l’utilisateur authentifié dispose
des droits d’accès à la ressource demandée. <br>
• Les actions du contrôleur ne seront invoquées que si l’utilisateur authentifié
dispose de l’un des rôles attribués à l’action. <br>
• Spring Security peut configurer les rôles associés aux utilisateurs en utilisant
différentes solution (inMemory, JDBC, UserDetails, etc..)</p>

<h3>- InMemory Authentication method :</h3>
<img src="Screenshots/securityConfig.PNG" alt="">
<h4>Protection des methodes avec l'annotation "@PreAuthorize".</h4>
<img src="Screenshots/preauthorize.PNG" alt="">


<h3>- JDBC Authentication method :</h3>
<h4>JDBC Bean permettant la connexion avec la base de données via l'objet dataSource.</h4>
<h4>La Création des users avec leurs roles au démarrage de l'application via le JDBC Bean crée.</h4>
<img src="Screenshots/jdbc.PNG" alt="">
<h4>Le Fichier schema.sql contenant les requêttes permettant la création des tables users et authorities et un index sur leurs colonnes.</h4>
<img src="Screenshots/schema.PNG" alt="">
<h4>Pour que Spring crée les tables users et roles á partir du fichier schema.sql, il faut la préciser dans application.properties.</h4>
<img src="Screenshots/spring.PNG" alt="">


<h3>- UserDetails Authentication method :</h3>
<h4>L'entité User :</h4>
<img src="Screenshots/entiteUser.PNG" alt="">
<h4>L'entité Role :</h4>
<img src="Screenshots/entiteRole.PNG" alt="">

<h4>L'interface UserRepository :</h4>
<img src="Screenshots/userRepo.PNG" alt="">

<h4>L'interface UserService :</h4>
<img src="Screenshots/UserHH.PNG" alt="">



<h4>La Création des users et des roles et affecter les roles au users.</h4>
<img src="Screenshots/creationUsers.PNG" alt="">

<h4>L'implémentation de l'interface UserDetailsService :</h4>
<img src="Screenshots/UserDetailService.PNG" alt="">
<h4>Il faut configurer aussi le fichier application.properties.</h4>
<img src="Screenshots/configFile.PNG" alt="">
<h2>Captures d'écrans des interfaces</h2>
<h4>Login</h4>
<img src="Screenshots/login.PNG" alt="">
<h4>Acceuil</h4>
<img src="Screenshots/Acceuil.PNG" alt="">
<h4>Ajouter Patient</h4>
<img src="Screenshots/form.PNG" alt="">
<h4>Modifier Patient</h4>

![editPatient.PNG](Screenshots%2FeditPatient.PNG)