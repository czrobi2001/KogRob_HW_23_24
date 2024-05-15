[//]: # (Image References)

[image1]: ./assets/race_car_cad.png "Race car"
[image2]: ./assets/track_cad.png "Monaco track"
[image3]: ./assets/gazebo_model_tree.png "Gazebo model - Monaco"
[image4]: ./assets/Gazebo_sim.png "Gazebo szimuláció"
[image5]: ./assets/rqt_cam.png "Kamera kép - rqt"

# Kognitív robotika projekt feladat
Kognitív robotika tárgynak féléves projekt feladata, ahol ROS Noetic környezetben fejlesztettem egy mobil robotot.

# Tartalomjegyzék
1. [Versenyautó megtervezése](#Versenyautó-megtervezése)
2. [Versenypálya](#Versenypálya)
3. [Gazebo szimuláció](#Gazebo-szimuláció)
4. [Alaklmazott szenzorok](#Alaklmazott-szenzorok)  
4.1. [Kamera](#Kamera)
5. [Skid steer kormáynzás](#Skid-steer-kormáynzás)
6. [Képfeldolgozás neurális hálóval](#Képfeldolgozás-neurális-hálóval)  
6.1. [Neurális háló tanítása](#Neurális-háló-tanítása)
7. [Szimuláció futtatása](#Szimuláció-futtatása)
8. [Telepítési útmutató](#Telepítési-útmutató)


# Versenyautó megtervezése
A versenyautó tervezésnék ötletét internetes forrásból vettem, ami egy kis lego kocsi, amit Solidworks-ben az egyszerűbb kezelhetőség érdekében módosítottam.

  Lego verseny kocsi: 

  ![alt text][image1] 

# Versenypálya
A versenypályát szintén Solidworks-ben egy letöltött, és importált kép segítségével terveztem meg, aminek kontúrját körberajzoltam Besier görbékkel, és kiexportáltam egy `.stl` fájlt.

  A pálya kontrúja:

  ![alt text][image2] 

Blenderbe beimportálva készítettem egy a gazebo által is feldolgozható collada mesht, a színek megfelelő megjelenítése érdekében. Ahhoz, hogy a Gazebo megnyitáskor lássa a modellt, az alábbi sort kell a `.bashrc` hozzá adni.

```console
export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:~/bme_catkin_ws/src/KogRob_HW_23_24/gazebo_models
```

# Gazebo szimuláció

  A versenyautó és pálya megjelenítése a szimulációban:

  ![alt text][image4]

# Alkalmazott szenzorok
A képfeldogozáshoz egy kamera került elhelyezésre a versenykocsi elején, aminek paramétereit az órán használtak alapján állítottuk be.

## Kamera
  Az élőkép RQT-ben:

  ![alt text][image5]

# Skid steer kormáynzás

# Képfeldolgozás neurális hálóval

## Neurális háló tanítása

# Szimuláció futtatása

# Telepítési útmutató
