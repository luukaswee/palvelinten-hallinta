# h1 - Viisikko

x. Run Salt Command Locally -tekstissä on mielestäni selkeä ja yksinkertainen ohjeistus. Erityisesti minulle, joka joutuu välillä lukemaan ohjeita useaan kertaan, jos kyseessä on uusi ja itselleni vieras asia, tämä vaikuttaa hyvältä. https://terokarvinen.com/2021/salt-run-command-locally/

Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux -artikkelissa käydään myös helposti luettavasti läpi, mitä Master ja Slave ovat sekä kuinka niiden toimintaa voi kokeilla. https://terokarvinen.com/2018/03/28/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/

Raportin kirjoittaminen -artikkeli on hieman vanhempi kuin muut, mutta edelleen erittäin ajankohtainen. Siinä on myös esimerkkiraportteja, joita muut opiskelijat ovat tehneet eri toteutuksilla. Näiden avulla voin nähdä konkreettisen esimerkin siitä, kuinka raportti tulisi rakentaa. Koitan itse vielä olla todella varovainen ja tarkka lähteiden kanssa sekä myös ettei vahingossakaan tule sepitettyä mitään. https://terokarvinen.com/2006/06/04/raportin-kirjoittaminen-4/

a. Tehty ilman isompia ongelmia!
b. Asennan nyt Salt Debianin Linux Virtual koneeseeni. En saanut asennettua kokonaan valmiiksi. Aloitin seuraamalla ohjeita kohdasta 1. sivulta https://docs.saltproject.io/salt/install-guide/en/latest/topics/install-by-operating-system/linux-deb.html 
Sain kaksi ensimmäistä kohtaa suoritettua

# Ensure keyrings dir exists
mkdir -p /etc/apt/keyrings

# Download public key
curl -fsSL https://packages.broadcom.com/artifactory/api/security/keypair/SaltProjectKey/public | sudo tee /etc/apt/keyrings/salt-archive-keyring.pgp

Kun koitin sitten # Create apt repo target configuration
curl -fsSL https://github.com/saltstack/salt-install-guide/releases/latest/download/salt.sources | sudo tee /etc/apt/sources.list.d/salt.sources
sain ilmoituksen "The following signatures couldnt be verified beacause the public key is not available: NO_PUBKEY 64CBBC8173D76B3F . 

Koitin kohtaa vielä uudestaan mutta sain sman ilmoituksen. En ymmärrä mikä voisi olla tässä tällä hetkellä vialla. Koitin asentaa Salt Stack Masteria ja Slavea vielä erillisen ohjeen mukaan https://terokarvinen.com/2018/03/28/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/ mutta tässä sain ilmoituksen vain että unable to locate package salt-master . Sama kävi myös kun koitin Slaven asennusta.
Uskon tämän nyt johtuvan siitä että joku on mennyt siis pieleen Create apt repo target configuration kohdassa.
c. ja d. kohtia en saa vielä tehtyä koska en ole saanut asennusta tehtyä vielä oikein, mutta tulen tekemään kun tiedän mitä tein väärin ja miten korjaan tekemäni.

lähteet ja ohjeet:
https://terokarvinen.com/2021/salt-run-command-locally/
https://docs.saltproject.io/salt/install-guide/en/latest/topics/install-by-operating-system/linux-deb.html
https://terokarvinen.com/palvelinten-hallinta/ (H1 tehtävänanto)
https://terokarvinen.com/2006/06/04/raportin-kirjoittaminen-4/
