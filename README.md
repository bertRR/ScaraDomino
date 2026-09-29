# 🤖 Domibot - Capa de Hardware, Control i Firmware

Aquest repositori conté la **capa de baix nivell i control de hardware** del projecte **Domibot**. Inclou el desenvolupament del "firmware" (controladors modulars en Python), els esquemes de connexió elèctrica, la documentació dels components i els tests de validació.

> 🌟 **Projecte Principal:**
> Aquest repositori s'encarrega de la integració física, l'electrònica i els drivers de control. Per veure la integració completa, la visió per computador i les estratègies de joc de dominó, **visita el projecte principal a [Domibot - GitHub**](https://github.com/LinceRojo/Domibot).
> 
> 

---

## 📌 Descripció General

Aquest mòdul gestiona la connexió física i el control programàtic dels perifèrics i servomotors del robot SCARA.

S'organitza en diferents **capes d'abstracció**:

1. **Controladors individuals (`drivers/controladors/`):** Reinterpretació de les biblioteques recomanades per a cada component (càmera, altaveu, micròfon, servomotors, motor pas a pas, electroimant) enfocades a un ús directe i simplificat.
2. **Capes d'Abstracció Superior (`drivers/` / `ScaraControllerIntermediary.py`):** Mòduls d'alt nivell que engloben i coordinen múltiples classes per gestionar el robot de manera conjunta i unificada (gestió d'instàncies, fitxers i moviment SCARA).

---

## 📂 Estructura del Repositori

```text
.
├── Controladors/             # Capa principal de control i firmware del robot
│   ├── drivers/              # Drivers principals del sistema
│   │   ├── controladors/     # Abstracció individual de cada perifèric (Càmera, Servo, Imant, etc.)
│   │   ├── controladorsTest/ # Tests unitaris per als controladors individuals
│   │   ├── GestorInstancies.py
│   │   └── ScaraController.py
│   ├── driversTest/          # Proves d'integració dels controladors superiors
│   ├── info/                 # Fitxers de configuració (requirements.txt, config.json, etc.)
│   ├── recursos/             # Fitxers i proves de suport
│   ├── captures/             # Historial de captures d'àudio i dades generades
│   ├── ScaraControllerIntermediary.py # Interfície intermediary de control
│   ├── main.py               # Punt d'entrada de control
│   └── setup.sh / venv       # scripts d'entorn virtual i configuració
│
├── Diagrama/                 # Esquemes elèctrics del robot SCARA en Draw.io, SVG i PNG
│   └── Esquema/              # Diagrames de connexió de hardware (DiagramaScaraDomino)
│
├── Documentacio/             # Datasheets i manuals dels components
│   ├── Altabeu/             # Amplificador i dades tècniques d'àudio
│   ├── Camera/              # Manuals i esquemes mecànics de la Pi Camera
│   ├── Font_d'Alimentacio/  # Documentació de l'alimentació del sistema
│   ├── Iman/                # Datasheets i manuals de l'electroimant (Grove)
│   ├── Microfon/            # Especificacions del micròfon I2S
│   ├── MicroServo/          # Datasheets del servo SG90
│   ├── RaspberryPi/         # Pinout GPIO i esquemes de la Raspberry Pi 4
│   └── StepMotor_i_Controlador/ # Esquemes del motor 28BYJ-48 i controlador ULN2003
│
└── Proves/                   # Test d'aïllament preliminars per a cada hardware
    ├── Altabeu/
    ├── Camara/
    ├── Electroiman/
    ├── Microfon/
    ├── MicroServo/
    └── MotorPasAPas/

```

---

## ⚙️ Arquitectura de Firmware i Hardware

* **Unitat Central:** Raspberry Pi 4 Model B


* **Actuadors i Perifèrics:**
* **Motor Pas a Pas (28BYJ-48 + ULN2003):** Control de posició dels eixos.
* **MicroServo (SG90):** Mecanismes d'elevació/orientació.
* **Electroimant (Grove):** Agafador per a les fitxes de dominó.
* **Càmera (Raspberry Pi Camera):** Captura d'imatges del tauler.
* **Micròfon I2S i Altaveu (Amplificador TPA2016):** Interacció d'àudio i veu.


---

## 🔗 Enllaços d'Interès

* 🤖 **Projecte Principal (Visió + Lògica + AI)**: [github.com/LinceRojo/Domibot](https://github.com/LinceRojo/Domibot)
