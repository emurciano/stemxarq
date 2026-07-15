# Documentació del Recurs Didàctic: Qüestionari d'Avaluació Inicial (Arduino/ESP32)

Aquest recurs consisteix en un qüestionari interactiu web auto-corregible basat en una estructura de tres arxius (`index.html`, `style.css` i `script.js`). Està dissenyat per a ser utilitzat com a eina d'avaluació diagnòstica o de repàs en l'aula de Tecnologia.

---

## 1. Fitxa Curricular (4t d'ESO)

* **Matèria:** Tecnologia
* **Nivell:** 4t d'Educació Secundària Obligatòria (ESO)
* **Bloc Temàtic:** Tecnologia Digital, Robòtica i Pensament Computacional.

### A. Objectius d'Aprenentatge
* Avaluar el nivell de partida de l'alumnat en conceptes de programació estructurada, arquitectura de microcontroladors i IoT (Internet de les Coses).
* Fomentar l'autoaprenentatge i la coavaluació mitjançant el *feedback* formatiu immediat (explicacions de les respostes).
* Desenvolupar la competència digital i la lectura comprensiva de codi font en entorns basats en text (C++ / Arduino IDE).

### B. Sabers Bàsics Connectats (LOMLOE)
* **Sistemes de control programats:** Arquitectura d'un sistema de control basat en microcontrolador (entrades, sortides, processament). Diferències clau entre plaques de desenvolupament (Arduino Uno vs. ESP32).
* **Programació en blocs i text:** Sintaxi bàsica de llenguatges basats en text (C/C++), variables, tipus de dades, estructures de control de flux (`setup`, `loop`, condicionals) i funcions bloquejants vs. no bloquejants (`delay` vs. `millis`).
* **Comunicacions i IoT:** Introducció als protocols de comunicació bàsics (Sèrie, I2C, SPI) i tecnologies sense fils (Wi-Fi, Bluetooth) per a l'intercanvi de dades i telemetria.

---

## 2. Guia d'Ús per al Docent (Instruccions de Muntatge i Gestió)

Com a docent, pots utilitzar aquest recurs de manera local o en línia per a plantejar una avaluació inicial dinàmica.

### A. Com posar-lo en marxa?
1.  **Descarrega els fitxers:** Desa els tres fitxers del qüestionari (`index.html`, `style.css` i `script.js`) dins d'una mateixa carpeta en el teu ordinador o en el servidor del centre.
2.  **Execució local:** Fes doble clic sobre l'arxiu `index.html`. S'obrirà directament al navegador de l'ordinador de l'alumne (no requereix connexió a Internet per a funcionar, a menys que s'allotgi en línia).
3.  **Allotjament (Opcional):** Pots pujar la carpeta a un servei d'allotjament gratuït (com *GitHub Pages*) o integrar-lo com un paquet de fitxers dins de la plataforma Moodle del centre.

### B. Com modificar o ampliar el qüestionari?
* **Modificar preguntes:** Obre el fitxer `script.js` amb un editor de text (com *VS Code* o el bloc de notes). Busca l'array `questionBank`. Pots afegir, eliminar o editar qualsevol pregunta seguint el format JSON proporcionat.
* **Canviar el nombre de preguntes del test:** Per defecte, el codi agafa 10 preguntes de les 50 disponibles. Si vols que el test sigui més curt o més llarg, busca en el `script.js` la línia:
    ```javascript
    currentQuizQuestions = selectRandomQuestions([...questionBank], 10);
    ```
    I canvia el número `10` pel valor que desitgis.

---

## 3. Guia d'Ús per a l'Alumnat (Instruccions de l'Activitat)

Benvingut/da al qüestionari de nivell sobre **Arduino i ESP32**. Aquesta activitat serveix per a conèixer què recordes d'anys anteriors i quins conceptes nous començarem a treballar durant el curs.

### Què has de fer?

1.  **Tria el teu idioma:** A la cantonada superior dreta de la pantalla, pots seleccionar si vols fer el qüestionari en **Català** o en **Castellà**. El canvi es fa a l'instant.
2.  **Respon les preguntes:** Se't mostraran un total de **10 preguntes** triades a l'atzar del nostre banc de dades. Selecciona la resposta que consideris correcta i prem el botó **"Següent"** (o *"Siguiente"*). 
    * *Nota: No pots passar de pregunta sense haver seleccionat una resposta.*
3.  **Consulta la teva puntuació:** En acabar l'última pregunta, el botó canviarà a **"Finalitzar"**. En prémer-lo, veuràs immediatament el teu percentatge d'encert.
4.  **Analitza el teu feedback (Molt important):**
    * A sota de la puntuació apareixerà una llista amb totes les preguntes que has contestat.
    * Veuràs en **verd** les encertades i en **vermell** les fallades.
    * Llegeix atentament l'apartat **"Per què? / ¿Por qué?"** de cada pregunta. Allà s'explica de manera tècnica el motiu pel qual la resposta correcta és la que és. Això et permetrà aprendre dels teus errors de manera immediata!
5.  **Torna a provar-ho:** Si vols millorar la teva nota o repassar conceptes diferents, clica a **"Torna a intentar-ho"**. Com que les preguntes s'agafen a l'atzar, et sortirà un qüestionari gairebé nou!