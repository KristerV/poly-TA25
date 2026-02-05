logi arvutisse enda kontoga!!
meil tuleb 3 hindelist projekti, viimane kõige suurem. Projektide vastamine on suuliselt ja detailne. Kes on AI-ga teinud jääb üli lihtsasti vahele.
AI no go, sellega sa ei õpi. Kui ei tea mida teha, Googelda.

### arvuti setup

install sublime text
install git
github.com konto ja uus repo nimega 'cookie-clicker'

### projekt gitist alla ja muudatused üles

git clone https                <- toob projekti arvutisse
cd sinu-projekti-nimi          <- läheb projekti kausta
(sublimes File - Open Folder - projekti kaust)
(tee uus fail index.html projekti sisse mingi sisuga)
(ava index.html browseris, näed oma sisu)
git status                     <- index.html peaks olema punane
git add index.html             <- tahan faili committida
git status                     <- index.hmtl on roheline
git commit -m "basic index html" <- salvestab faili ajalikku
(kui jäid editori kinni trüki täpselt :wq)
git status                     <- index.html kadunud
git log                        <- näed oma tehtud committi
(vajuta 'q', et välja saada logist)
git push                       <- saadad githubi oma projekti ajaloo
(vaata kas GitHubi repos näed oma index.html faili)
