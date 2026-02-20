# 🧪 TubeWinder
Schlauchmaschine 1

# 📄 Dokumentation: Antriebsanalyse Aufwickler-Prozess

## ⚙️ Bestandsaufnahme: MSF-Vathauer Motor

| Parameter | Wert | Anmerkung |
| :--- | :--- | :--- |
| **Hersteller** | MSF-Technik Vathauer | Sitz in Detmold |
| **Typ** | DMF 112M - 12a | Baugröße 112M, 12-polig |
| **Motorenart** | 3-Phasen Asynchron | Auslegung als Drehmoment-/Schlupfmotor |
| **Spannung** | 230/400 V | Schaltung: Dreieck (D) / Stern (Y) |
| **Strom** | 6,1 A / 3,5 A | Entsprechend der D/Y Schaltung |
| **Frequenz** | 50 Hz | Europäisches Stromnetz |
| **Drehzahl** | 0 - 500 U/min | Ausgelegt für variablen Betrieb bis Stillstand |
| **Drehmoment** | 17,0 Nm | Nenndrehmoment |
| **Schutzart** | IP 54 | Staub- und Spritzwassergeschützt |
| **Isolierklasse** | F | Ausgelegt für Temperaturen bis 155 °C |
| **Motorschutz** | 3 Thermokontakte | In den Wicklungen integriert |

---

## 🧮 Berechnungen & Ableitungen

* **Polzahl:** Die Synchrondrehzahl von 500 U/min bei 50 Hz ergibt physikalisch einen **12-poligen Motor** (6 Polpaare).
* **Mechanische Nennleistung:** Die Leistung lässt sich aus Drehmoment ($M$) und Drehzahl ($n$) über die folgende Formel berechnen: 
  $P = M \cdot 2 \cdot \pi \cdot \frac{n}{60}$
* **Ergebnis:** Bei 17 Nm und 500 U/min liefert dieser Motor ca. **0,89 kW** (890 W) mechanische Nennleistung.

---

## 📊 Prozessverhalten: Aufwickeln & Drehmoment

Beim Aufwickeln wächst kontinuierlich der Rollendurchmesser. Um die Materialspannung (Zugkraft) konstant zu halten, muss das Drehmoment proportional zum Radius zunehmen.

* **Ursache für Stillstand:** Erreicht das vom Material geforderte Drehmoment bei einer dicken Rolle den Wert von > 17 Nm, stößt der aktuelle Motor an seine physikalische Grenze und bleibt stehen.
* **Frequenzumrichter-Einfluss:** Ein FU mit Vektorregelung kann das Nennmoment auch bei sehr niedrigen Drehzahlen (nahe 0 U/min) optimal und ohne Ruckeln bereitstellen. Er kann die absolute mechanische Dauerleistungsgrenze des Motors von 17 Nm jedoch nicht anheben.

---

## 🚀 Zukunftsplan: Retrofit / Modernisierung

Geplant ist der Umbau auf eine dedizierte **Wickler-Applikation von Siemens** zur präzisen Zug- und Drehmomentregelung.

* **Neuer Antriebsstrang:** Motor-Getriebe-Einheit inklusive Encoder für exakte Drehzahl- und Lageerfassung (Closed-Loop).
* **Plattform:** Siemens SINAMICS **S120** (Modulares Mehrachssystem) oder **S210** (Hochdynamisches Servo-Einzelachssystem).
* **Inbetriebnahme:** Konfiguration und Tuning mittels Siemens Starter, Startdrive (TIA Portal) oder Scout.

