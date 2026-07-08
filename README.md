# Virtualni Osciloskop 📊🔌

**Fakultet tehničkih nauka, Novi Sad (2026)** **Autori:** Marija Milenković (RA 89/2023), Maša Božić (RA 74/2023), Milena Božić (RA 51/2023)

---

## 📝 O projektu

Ovaj projekat predstavlja **Virtuelni osciloskop** realizovan u programskom okruženju **LabVIEW**. Sistem omogućava akviziciju analognih električnih signala u realnom vremenu, njihovu digitalnu obradu, vizuelizaciju i spektralnu analizu pomoću hardverske kartice kompanije National Instruments.

### 🛠️ Hardverska i softverska osnova
* **Hardver:** NI USB-5133 (Dvokanalni digitalizator, 50 MHz propusni opseg, uzorkovanje do 100 MS/s, 8-bitni ADC)
* **Softver:** LabVIEW, NI-SCOPE drajverski API

---

## ✨ Ključne funkcionalnosti

* **Akvizicija u realnom vremenu:** Stabilan prikaz signala u vremenskom domenu uz korišćenje *Immediate Trigger* režima rada.
* **Skaliranje i pozicioniranje (Zoom & Offset):** Manuelno podešavanje vertikalne i horizontalne skale (zuma) i softversko pomeranje grafika po osama (ofset).
* **Automatska merenja:** Kontinualno računanje i prikaz parametara: *Frequency, Rise Time, Voltage Peak-to-Peak, Voltage Max*.
* **Digitalno filtriranje:** Integrisani niskopropusni (Low-pass) i visokopropusni (High-pass) filteri za uklanjanje šuma i DC komponente.
* **Spektralna analiza (FFT):** Prikaz frekvencijskog spektra u logaritamskoj skali uz podršku za prozorske funkcije (npr. *Blackman-Harris*) i usrednjavanje.
* **Skladištenje podataka:** Istovremeno čuvanje numeričkih podataka u `.lvm` fajl i izvoz vizuelnog prikaza grafika u `.png` formatu klikom na taster *Save plot*.
* **Bezbedno gašenje:** Automatsko oslobađanje resursa i zatvaranje sesije instrumenta u slučaju greške ili pritiska na taster *FullStop*.

---

## 🚀 Kako pokrenuti aplikaciju

1.  Povežite **NI USB-5133** karticu na računar putem USB interfejsa.
2.  Instalirajte neophodne **NI-SCOPE** drajvere.
3.  Otvorite glavni VI fajl u **LabVIEW** okruženju.
4.  Na prednjoj ploči (Front Panel) izaberite odgovarajući uređaj (*Device*) i aktivni *Kanal*.
5.  Kliknite na prekidač **Start/Pauza** za početak merenja.
