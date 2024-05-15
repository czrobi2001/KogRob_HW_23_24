[//]: # (Image References)

[image1]: ./assets/race_car_cad.png "Race car"
[image2]: ./assets/track_cad.png "Monaco track"
[image3]: ./assets/gazebo_model_tree.png "Gazebo model - Monaco"
[image4]: ./assets/Gazebo_sim.png "Gazebo szimuláció"
[image5]: ./assets/rqt_cam.png "Kamera kép - rqt"

# Kognitív robotika projekt feladat
Kognitív robotika tárgynak féléves projekt feladata, ahol ROS Noetic környezetben fejlesztettem egy mobil robotot.

# Tartalomjegyzék
1. [Kezdőcsomag](#Kezdőcsomag)  
2. [Versenyautó megtervezése](#Versenyautó-megtervezése)
3. [Versenypálya](#Versenypálya)
4. [Gazebo szimuláció](#Gazebo-szimuláció)
5. [Alaklmazott szenzorok](#Alaklmazott-szenzorok)  
5.1. [Kamera](#Kamera)
6. [Ackermann kormányzás](#Ackerman-kormányzás)
7. [Képfeldolgozás neurális hálóval](#Képfeldolgozás-neurális-hálóval)  
7.1. [Neurális háló tanítása](#Neurális-háló-tanítása)
8. [Szimuláció futtatása](#Szimuláció-futtatása)
9. [Telepítési útmutató](#Telepítési-útmutató)

# Kezdőcsomag
A kezdőcsomagban a tantárgy során használt plug-in-ket már tartalmazza, illetve az alapvető .launch fájlokat, amikkel megjeleníthetjük a robotot, pályát, illetve a kettőt egy térben.

# Versenyautó megtervezése
A versenyautó tervezésnék ötletét internetes forrásból vettük, ami egy kis lego kocsi, amit Solidworks-ben az egyszerűbb kezelhetőség érdekében módosítottam.

  Lego verseny kocsi: 

  ![alt text][image1] 

# Versenypálya
A versenypályát szintén Solidworks-ben egy letöltött, és importált kép segítségével terveztem meg, aminek kontúrját körberajzoltam Besier-spline-ok segítségével, és kiexportáltam egy `.stl` fájlt.

  A pálya kontrúja:

  ![alt text][image2] 

Blenderbe beimportálva készítettem egy a gazebo által is feldolgozható collada mesht, a színek megfelelő megjelenítése érdekében, amit az alapértelmezett Gazebo modellek telepítési könyvtárában kell elhelyezni, hogy megtalálja a modell behíváskor a gazebo a `.dae` és `.stl` fájlokat. Amennyiben nem látjuk a `.gazebo` könyvtárat akkor láthatóvá kell tenni a rejtett könyvtárakat is a számítógép beállításaiban.


  A sikeres futtatáshoz az alábbi fájlokat kell a pálya neve alatti Gazebo modell  könyvtárban létrehozni. A `Gazebo_modell` könyvtárban a `monaco` mappát kell ide beilleszteni:

  ![alt text][image3]

# Gazebo szimuláció

  A versenyautó és pálya megjelenítése a szimulációban:

  ![alt text][image4]

# Alkalmazott szenzorok
A képfeldogozáshoz egy kamera került elhelyezésre a versenykocsi elején, aminek paramétereit az órán használtak alapján állítottuk be.

## Kamera
  Az élőkép RQT-ben:

  ![alt text][image5]

# Ackermann kormányzás

# Képfeldolgozás neurális hálóval

## Neurális háló tanítása

# Szimuláció futtatása

# Telepítési útmutató
