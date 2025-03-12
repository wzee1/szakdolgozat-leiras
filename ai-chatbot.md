# AI Chatbot Különböző Személyiségekkel  

## Leírás  
Ez az alkalmazás egy **AI-alapú chatbot**, amely lehetővé teszi a felhasználók számára, hogy híres karakterekkel és személyiségekkel folytassanak beszélgetéseket. A rendszer egyedi kontextusokat használ, így minden karakter a saját jellegzetes stílusában és tudásával kommunikál.  

## Főbb funkciók  
- **Karakterválasztás** – A felhasználók kedvenc karaktereiket választhatják ki (pl. Batman, Yoda, Einstein).  
- **Személyre szabott AI válaszok** – A chatbot az adott karakter egyedi beszédstílusát és tudását tükrözi.  
- **Beszélgetési előzmények tárolása** – Lehetőség a korábbi interakciók visszanézésére.  
- **Felhasználói fiókok** – Bejelentkezés után személyre szabott élmény és adatmentés biztosított.  
- **Modern, reszponzív felület** – Letisztult, könnyen kezelhető UI a zavartalan élményért.  

## Technológiai stack  

### Frontend  
A felhasználói felület fejlesztése modern és hatékony eszközökkel történik:  
- **Next.js 15** és **React 19** – gyors, dinamikus és interaktív élmény biztosítása érdekében, SSR.  
- **Tailwind CSS 4 + shadcn/ui** – reszponzív és esztétikus megjelenés könnyedén testreszabható komponensekkel.  
- **Jest** – egységtesztelés a stabil és hibamentes működés érdekében.  
- **Zod** – adatvalidáció a biztonságos és megbízható adatintegrációért.  

### Backend  
A háttérrendszer megbízható és skálázható architektúrára épül:  
- **Laravel** – robusztus PHP keretrendszer, amely beépített validációval és unit teszteléssel biztosítja a megbízhatóságot.  
- **REST API** – jól dokumentált és könnyen integrálható végpontok a frontend és a backend összekapcsolására.  

### Adatbázis  
Az adatok hatékony tárolására és kezelésére a következő megoldások állnak rendelkezésre:  
- **MongoDB** vagy **PostgreSQL**
- **Eloquent ORM** – egyszerű és intuitív adatbázis-kezelés Laravel környezetben.  

### Mesterséges intelligencia  
A chatbot egyedisége a Google AI-alapú modelljén alapszik:  
- **Google Gemini API** – az AI személyre szabott kontextusok alapján generálja a karakterhű válaszokat.
