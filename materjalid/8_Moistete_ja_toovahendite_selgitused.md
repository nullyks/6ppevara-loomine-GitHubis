# Selgitused kasutatud mõistete ja töövahendite olemuse kohta

## Sisukord

- [CHANGELOG.md fail](#changelogmd-fail)
- [Commit](#commit)
- [GitHub Issues](#github-issues)
- [GitHub Projects](#github-projects)
- [GitHub Releases](#github-releases)
- [Harude liitmine (merge)](#harude-liitmine-merge)
- [Konflikt harude liitmisel (merge conflict)](#konflikt-harude-liitmisel-merge-conflict)
- [Pull](#pull)
- [Pull Request](#pull-request)
- [Push](#push)
- [Repositooriumi Forkimine](#repositooriumi-forkimine)
- [Repositooriumi haru (branch)](#repositooriumi-haru-branch)
- [Repositooriumi kloonimine](#repositooriumi-kloonimine)

## GitHub Issues
GitHub Issues ehk probleemikirjeldused on tööriist, mille abil saab arendustöö käigus üles märkida ideid, ettepanekuid, puudusi või parandamist vajavaid kohti. Iga uus sisuplokk, parandus või täiendus võiks koostöise arenduse puhul alata vastava Issue loomisega. See aitab hoida töövoogu läbipaistvana ja struktureerituna, andes selge ülevaate, mille kallal keegi töötab või millised ideed on veel realiseerimata. Issue ise on lihtne tekstipõhine kirjeldus, millele saab lisada pealkirja, üksikasjaliku selgituse ning soovi korral ka pilte või linke.

Iga Issue on mõnes mõttes nagu ülesanne või mõttevahetuse koht. Sinna saab lisada silte (labels), näiteks „sisu”, „vigade parandus” või „arutelu”, et määratleda, mis tüüpi probleemiga on tegu. Samuti saab määrata vastutaja (assignee), tähtaja või ühendada neid GitHub Projects töölaudadega. See teeb lihtsamaks suuremahulise või mitme inimese koostööl põhineva õppematerjali arendamise juhtimise. Kui mitu inimest töötavad sama materjali kallal, aitab Issues kasutamine vältida kattuvat tööd ja suunata arutelu õigesse kohta.

Lisaks saab iga Issue juurde kirjutada kommentaare. Nii muutub see ka arutelukeskkonnaks, kus õpetajad saavad jagada mõtteid, küsida täpsustusi või teha ettepanekuid. Kui õppematerjali arendaja lahendab Issue juures kirjeldatud probleemi (nt kirjutab uue peatüki või parandab vea), saab ta selle siduda pull requestiga ja lõpuks automaatselt sulgeda. Nii tekib dokumenteeritud ja jälgitav töövoog, mis toetab ka hilisemat versioonihaldust.

## GitHub Projects
GitHub Projects on tööriist, mis võimaldab planeerida, jälgida ja hallata arendusprotsessi. Võimalikud on mitmed visuaalsed vaated, millest õppematerjali loomisel on mugavaim Board, mis sarnaneb Kanban-tahvlile. See aitab õppematerjalide koostajatel näha kogu töövoogu korraga, jaotada ülesanded etappidesse nagu „To Do“, „In Progress“ ja „Done“, ning hoida silma peal, kes millega parajasti tegeleb. Projekte saab kasutada nii individuaalselt kui ka koostöös: iga kaart tahvlil (kaart = üks tööülesanne) võib olla seotud konkreetse Issue või Pull Requestiga.

GitHub Projects toetab nii lihtsat käsitsi haldamist kui ka automatiseerimist. Näiteks saab määrata, et kui Pull Request liidetakse main-harusse, liigub selle kaart automaatselt veergu „Done“. Samuti saab kaartidele lisada tähtaegu, vastutajaid ja silte, et täpsemalt planeerida, kellele ja millal mingi tööülesanne määratud on. 

GitHub Projects ei eelda eraldi paigaldamist ega keerulist seadistust – see on saadaval iga repositooriumi vaates ja seda saab avada ka otselingi [github.com/projects](github.com/projects) kaudu. Projekte saab hallata individuaalselt igas repositooriumis või koondada suuremasse „Organization project“ vaatesse, kui materjale arendatakse näiteks kooli või õppeasutuse ühises GitHub organisatsioonis.
## Pull Request
Pull Request (edaspidi PR) on GitHubi koostöise arenduse keskne tööriist, mille abil tehakse ettepanekuid muudatuste liitmiseks repositooriumi põhiharuga (nt main). Kui keegi arendajatest teeb muudatusi eraldi harus (branch), siis Pull Request võimaldab neid muudatusi teistele nähtavaks teha ja üle vaadata enne, kui need lisatakse ametlikku versiooni. See on oluline kvaliteedikontrolli ja läbipaistvuse tagamiseks: teised arendajad saavad PR-i kaudu tutvuda tehtud muudatustega, kommenteerida, küsida selgitusi või soovitada täiendusi.

Pull Requestiga seotakse tihti ka konkreetne Issue, mida muudatus lahendab (nt märksõnaga Lahendab probleemikirjelduse #3). PR-i avamisel on soovitatav kirjutada lühike, kuid informatiivne kokkuvõte: mida muudeti ja miks see muudatus on vajalik. GitHubi keskkond võimaldab kommentaare jätta nii PR-i üldisesse aruteluvälja kui ka sisu konkreetse rea juurde, mis teeb tagasisidestamise väga paindlikuks.

Kui kõik arendajad on muudatustega nõus, saab PR-i kinnitada (merge). See liidab muudatused põhiharusse ja sulgeb automaatselt seotud Issue, kui PR-is oli sellele viide. Pull Requestid dokumenteerivad kogu arenduse ajaloo – nii on hiljem lihtne näha, kes mida muutis ja miks. Õppematerjalide arenduses võimaldab PR hästi hallata ka õpetajate vahelisi arutelusid sisu ja ülesehituse üle.

## Repositooriumi haru (branch)
Branch ehk haru on GitHubis versioonihalduse töövahend, mis võimaldab arendajatel teha muudatusi repositooriumi sisu kallal eraldi haruna, ilma et see mõjutaks kohe kogu projekti põhiversiooni (nt main haru). Haru loomine tähendab, et saad oma töö teha isoleeritult – näiteks kirjutada uut peatükki, parandada kirjavigu või lisada pilte – samal ajal kui teised arendajad töötavad oma harudes paralleelselt teiste teemade kallal. See aitab hoida repositooriumi põhisisu stabiilsena.

Tüüpiline töövoog algab sellega, et valitakse mõni Issue, seejärel luuakse selle lahendamiseks uus haru (näiteks tmp36-anduri-kasutamine) ja tehakse kõik muudatused just selles harus. Kui töö on valmis, avatakse Pull Request, mille kaudu saab teistega arutada, üle vaadata ja kinnitada, et muudatus sobib liitmiseks põhiharusse. Nii toimib GitHubi harupõhine töökorraldus kui paindlik ja ohutu viis koostööd teha.

Harude kasutamine on mugav õppematerjalide arenduses, kus paralleelselt luuakse mitut erinevat teemat või täiendatakse olemasolevaid osasid. Õpetajad saavad luua igale arendusetapile eraldi haru ja hoida töökorraldus läbipaistva ning loogilise. Ka vigade parandused või kujundusuuendused saab teha omaette harudes.

## Harude liitmine (merge)

Merge ehk harude liitmine on GitHubis protsess, millega ühe haru (nt arendusharu) muudatused liidetakse teise harusse, tavaliselt projekti põhiharusse (main). See tähendab, et kõik muudatused – olgu need uued tekstiosad, parandused või täiendused – viiakse kokku projekti ametliku versiooniga. Merge kasutatakse tavaliselt pärast seda, kui Pull Request on avatud ja muudatused on üle vaadatud ning heaks kiidetud.

Liitmise eesmärk on ühendada töö viljad stabiilsesse versiooni, ilma et vahepealsed eksperimentaalsed või pooleliolevad muudatused segaksid teiste arendajate tööd. Merge toimub enamasti ilma lisatööd vajamata. Kui aga mitmes harus on tehtud samadele failidele vastuolulisi muudatusi, võib tekkida konflikt, mis tuleb käsitsi lahendada. GitHub pakub selleks visuaalseid tööriistu, mis aitavad vaadata, millised muudatused on vastuolus ja võimaldavad valida või ühendada parima tulemuse.

Õppematerjalide arenduse kontekstis tähendab merge näiteks seda, et üks õpetaja on lisanud uue osa tmp36-anduri-kasutamine.md failina ja teine on täiendanud pilte meedia/ kaustas – kui need muudatused on valmis ja kontrollitud, saab need mõlemad liita põhiharusse. Nii tekib samm-sammuline, versioonihalduses jälgitav arendusprotsess, mille igal etapil on säilinud selge jälg, kes ja mida muutis ning millal.

## Konflikt harude liitmisel (merge conflict)

Merge conflict ehk liitmise konflikt tekib siis, kui GitHub ei suuda automaatselt otsustada, millised muudatused peaksid jääma failis kehtima, sest erinevates harudes on samale tekstiosale tehtud vastuolulisi muudatusi. Näiteks kui kaks õpetajat muudavad sama lõiku samas failis, aga erinevalt – üks lisab selgitava lause, teine muudab sama kohta teistmoodi. Tekib konflikt. GitHub ei saa automaatselt valida, kumb versioon peaks lõplikult jääma, ning see tuleb lahendada käsitsi.

Kui konflikt tekib, tähistab GitHub vastava faili sees konfliktse koha spetsiaalsete märgenditega (näiteks <<<<<<<, =======, >>>>>>>), mis näitavad, milline osa pärineb millisest harust. Arendaja peab otsustama, milline versioon säilitada või kas kombineerida erinevad muudatused üheks. Seda saab teha GitHubi veebipõhises redaktoris, käsureal või spetsiaalsete Git-klientide (nt GitHub Desktop või VS Code) abil.

Õppematerjalide koostöisel arendamisel võib eeldada, et konflikte tekib, eriti kui mitu inimest töötavad sama faili kallal. Sellisel juhul on soovitatav enne PR-i liitmist hoida oma haru ajakohasena, tõmmates (pull) muudatused main-harust ja lahendades konfliktid enne, kui need suuremaks kasvavad. Konfliktide käsitlemine võib tunduda keeruline, kuid GitHub pakub selleks samm-sammulisi tööriistu ja visuaalseid juhiseid. Ideaalis peaks koostöise arendamise korraldama viisil, et paralleelselt ei muudeta samu faile. See eeldab vastavaid kokkuleppeid ja ka õppematerjali struktuuri hoidmist piisavalt modullaarsena.

## Repositooriumi Forkimine

Repositooriumi forkimine (ingl fork) on GitHubi toiming, millega luuakse kellegi teise repositooriumist isiklik koopia oma kontole. Forkimine võimaldab teha muudatusi originaalprojekti sisu kallal ilma, et selle algset versiooni kohe muudetaks. Forki kasutatakse eelkõige siis, kui soovitakse panustada avalikku projekti või töötada eraldi koopial, näiteks täiendada olemasolevat õppematerjali või teha sellele oma versioon.

Forkitud repositoorium käitub nagu iga teine GitHubi repo – sinna saab lisada faile, luua harusid, teha pull requeste ja hallata sisu. Kui muudatused on valmis ja soovitakse need saata tagasi algsesse repositooriumisse, saab oma harust avada pull requesti originaalprojekti vastu. Selline töövoog on tavaline siis, kui arendajad ei oma kirjutamisõigust algses repositooriumis, aga soovivad siiski panustada.

Õppematerjalide arenduses võimaldab forkimine näiteks teisel õpetajal võtta aluseks juba olemasolev materjal ja teha sellest kohandatud versioon (nt teise klassiastme või õppekeele jaoks). Samuti saab forkimise abil testida ideid või õpetada õppijatele GitHubi töövoogu, ilma et originaalfailid oleksid ohus.

## Repositooriumi kloonimine

Repositooriumi kloonimine (ingl clone) on toiming, mille käigus kopeeritakse GitHubi repositoorium oma arvutisse, et saaks sellega lokaalselt töötada. See tähendab, et kõik failid, kaustad ja kogu versiooniajalugu laaditakse sinu arvutisse täpselt sellisena, nagu need on GitHubi serveris. Kloonimist kasutatakse siis, kui soovitakse teha sisulisi muudatusi, kirjutada uusi faile või testida koodi/lahendusi ilma veebilehitseja kaudu töötamata.

Kui repositoorium on kloonitud, saab lokaalselt luua harusid, teha muudatusi, versioonihaldust (commit) ja seejärel need muudatused GitHubi tagasi lükata (push). Kloonitud repositooriumis töötamine võimaldab kasutada ka kõiki tekstiredaktoreid ja arenduskeskkondi (nt VS Code), mis teeb õppematerjalide loomisprotsessi palju paindlikumaks ja mugavamaks, eriti kui tuleb hallata mitut faili või lisada keerulisemat struktuuri.

 Kloonimine sobib hästi olukordadeks, kus internetiühendus pole alati tagatud – saad töötada lokaalselt ja lükata muudatused üles alles siis, kui ühendus on taastunud.

## Pull

Pull (täpsemalt git pull) on Git versioonihaldussüsteemi käsk, millega tuuakse muudatused kaug-repositooriumist (nt GitHubist) oma lokaalsesse koopiasse. Kui keegi teine on teinud samas repositooriumis muudatusi (näiteks lisanud uusi faile või täiendusi), siis git pull aitab tagada, et sinu lokaalne versioon on ajakohane. See on eriti oluline koostöösituatsioonides, kus mitu arendajat või õpetajat töötavad sama õppematerjali kallal – enne uute muudatuste tegemist tuleks alati teha pull, et vältida konflikte.

Tehniliselt teeb git pull kaks toimingut järjest: esmalt tõmbab (fetch) muudatused kaug-repositooriumist ning seejärel liidab (merge) need sinu aktiivsesse harusse. Kui sinu lokaalsed failid pole vastuolus tõmmatud muudatustega, toimub liitmine automaatselt. Kui aga samades kohtades on erinevad muudatused, võib tekkida merge conflict, mis tuleb käsitsi lahendada. Regulaarne git pull käivitamine aitab vältida keerukaid konflikte ja tagab, et kõik töötavad ühise, värske sisuga versiooni kallal.

## Push

Push (täpsemalt git push) on Git käsu abil tehtav toiming, millega saadetakse lokaalses arvutis tehtud muudatused GitHubi kaug-repositooriumisse. Kui oled loonud uusi faile, kirjutanud õppematerjali sisu või täiendanud olemasolevaid osasid ning need commit toiminguga salvestanud, siis git push abil jõuavad need muudatused ka GitHubi, kus neid saavad näha ja kasutada ka teised arendajad või õpetajad. Push on seega oluline samm, et sinu töö oleks kättesaadav kõigile, kes projektis osalevad.

Push-i kasutamine on koostöövõtmes kriitiline: see tagab, et kogu meeskond töötab sama ajakohase versiooni kallal. Näiteks kui oled töötanud uues harus osa3-lisamine, siis: 
~~~ 
git push origin osa3-lisamine 
~~~ 
saadab selle haru GitHubi. Seejärel saad selle põhjal avada Pull Requesti, mille kaudu saab töö ametlikult põhiharusse liita. Push toimib ainult siis, kui puuduvad konfliktid või kui oled andnud loa konfliktiolukorras üles surumiseks.

## Commit

Commit on Git versioonihalduses toiming, millega salvestatakse lokaalses repositooriumis tehtud muudatused kindla tähisega. Iga commit on kui hetkepilt projekti seisust: see sisaldab infot selle kohta, milliseid faile muudeti, kes muudatuse tegi ja millal, ning lühikest selgitust (commit message), mis annab ülevaate muudatuse sisust. Commit'id moodustavad Git-projekti ajatelje ja võimaldavad vajadusel minna ajas tagasi, võrrelda erinevaid versioone või taastada varasema seisu.

Commit'e tehakse tavaliselt pärast seda, kui on tehtud sisulisi täiendusi – näiteks kirjutatud uus peatükk, parandatud vigu või lisatud uusi pilte. Commit'iga ei saadeta muudatusi veel GitHubi; need salvestatakse ainult lokaalsesse koopiasse. Alles pärast push käsu kasutamist jõuavad commit'id ka kaug-repositooriumisse. Korralikult dokumenteeritud commit-sõnumid aitavad kogu arendustiimil mõista, miks mingi muudatus tehti, ja loovad läbipaistva ning usaldusväärse töövoo.

## GitHub Releases

GitHub Releases on GitHubi funktsioon, mille abil saab tähistada repositooriumi kindlaid verstaposte või valmis versioone. Release on nagu „ametlik väljalase“, mis koondab ühe arendustsükli jooksul tehtud muudatused selgeks ja viidatavaks versiooniks (nt v1.0, v2.1-beta). See sobib õppematerjalide puhul, kus soovitakse kinnitada, et konkreetne versioon on täielik, ülevaadatud ja kasutamiseks valmis. Release loomisel saab lisada versiooni numbri, pealkirja, muutuste loetelu (changelog) ja vajadusel ka manuseid (nt PDF-versioonid, näidisfailid vms).

GitHub Releases põhineb Git tags funktsionaalsusel, mille kaudu märgitakse ära kindel commit, mis tähistab versiooni algust. Näiteks kui õppematerjali versioon v1.0 on valmis, saab selle commit’ile lisada tag’i ja selle põhjal teha Release. Iga Release jääb ajalukku ning seda saab alla laadida või sellele viidata – näiteks jagada õppijatele just seda versiooni, mille järgi kursus toimub. Nii välditakse olukorda, kus õppijad kasutavad erinevaid või pooleliolevaid versioone.

Releases sobivad suurepäraselt ka koostöösituatsioonidesse: õpetajad ja arendajad saavad teada, millal mingi osa on ametlikult valmis ning mille kallal töö jätkub. Samuti saab Releases abil teavitada sihtrühma uutest muudatustest – GitHub võimaldab lisada vabatekstilise kirjelduse või isegi lingid muudatuste üksikasjadele. Lisaks on iga Release’il oma URL, mida saab jagada dokumentatsioonis, õpikeskkonnas või õppematerjali tutvustustes.

## CHANGELOG.md fail

CHANGELOG.md on dokument, kuhu kirjeldatakse projekti muudatusi versioonide kaupa. Selle eesmärk on anda selge ja struktureeritud ülevaade sellest, mis on igas versioonis muutunud, lisandunud või eemaldatud. Fail aitab nii arendajatel kui ka kasutajatel jälgida, kuidas õppematerjal on arenenud ajas. Tavapäraselt kirjutatakse muudatused kronoloogilises järjestuses – uusimad versioonid kõige eespool – ning iga kirje juures märgitakse versiooninumber, kuupäev ja muudatuse tüüp (nt „Lisatud“, „Muudetud“, „Parandatud“, „Eemaldatud“).

Õppematerjalide arenduses võimaldab CHANGELOG.md dokumenteerida sisulisi täiendusi: näiteks kui lisatakse uus teema, parandatakse näidete vigu või uuendatakse viiteid. See teeb koostöö läbipaistvamaks ja võimaldab õpetajatel või õppijatel kiirelt tuvastada, mis on uues versioonis teisiti. Kuigi Git versioonihaldus salvestab kõik commit’id, on CHANGELOG.md loetavam ja suunatud tavakasutajale, mitte ainult tehnilisele jälgimisele.

## Kasutatud allikad: 
* *https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues*

* *https://docs.github.com/en/issues/quickstart*

* *https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects*

* *https://docs.github.com/en/issues/planning-and-tracking-with-projects/quickstart*

* *https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests*

* *https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request*

* *https://docs.github.com/en/get-started/using-git/about-branches*

* *https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository*

* *https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-request-merges*

* *https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/merging-a-pull-request*

* *https://docs.github.com/en/pull-requests/committing-changes-to-your-project/resolving-merge-conflicts/about-merge-conflicts*

* *https://docs.github.com/en/pull-requests/committing-changes-to-your-project/resolving-merge-conflicts/resolving-a-merge-conflict-on-github*

* *https://docs.github.com/en/get-started/using-git/resolving-merge-conflicts*

* *https://docs.github.com/en/get-started/quickstart/fork-a-repo*

* *https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks*

* *https://docs.github.com/en/get-started/quickstart/fork-a-repo*

* *https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks*

* *https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository*

* *https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories*

* *https://docs.github.com/en/get-started/using-git/syncing-your-branch*

* *https://git-scm.com/docs/git-pull*

* *https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository*

* *https://git-scm.com/docs/git-push*

* *https://docs.github.com/en/get-started/using-git/saving-changes-with-commit*

* *https://git-scm.com/docs/git-commit*

* *https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases*

* *https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository* 

* *https://keepachangelog.com/en/1.0.0/*

* *https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases*

* *https://github.com/github/feedback/discussions/8101*