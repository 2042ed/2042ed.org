# GameLab AR Image

- Unity version used: 2021.3.x
- supported Android devices: https://developers.google.com/ar/discover/supported-devices  
- iOS: iPhone o iPad con iOS >= 12.0

## Procedure

### 1 - Creo nuovo progetto Unity "3D URP"

### 2 - Lo ripulisco

- rimuovo `TutorialInfo`
- tolgo i packages non usati e li aggiorno

### 3 - Installo AR Foundation base

- com.unity.xr.arfoundation
- com.unity.xr.arcore
- com.unity.xr.arkit

XR Plugin management è una dipendenza

- installa Android Logcat

### 4 - Project Settings

#### Player

- configuro Company, App Name e app bundle android e ios
- Android: modifico le Graphics APi in SOLO OpenGLES3 (no Vulkan o altro)
- minimum API level: 24
- scripting Backend: IL2CPP (per abilitare build ARM64)

#### XR Plugin Management

- abilito ARCore per Android e ARKit per iOS
- verifico i required

#### Build Settings
Switcho ad Android

#### URP renderer

activate `URP-Performant` and add `ARBackgroundRendererFeature` to `URP-Performant-Renderer`

### Project Assets

- creo una Prefab/Materials con un bel AR Cubo e suo materiale rosso
- creo una `XR/ReferenceImageLibrary` e ci metto dentro due immagini marker


### AR scene setup

- creo una `XR/AR Session`
- creo una `XR/AR Session Origin`

- aggiungo a Origin un ARTrackedImageManager

### In Project aggiungo le mie immagini

- aggiungo due immagini (alta risoluzione, contrasto)
- configuro le dimensioni
- enable at Runtime

- importo mio modello 3D

### Build

- check Run Device

## Part 2

- instanzamo due oggetti Image
- applichiamo il nuovo script per le immagini multiple

## Part 3

creiamo un Plane Visualizer

- creo Prefab `AR Default Plane`
- aggiungo `ARPlaneManager` a Origin
- aggiungo script `PlaceOnPlane`

## Parte 4

check attivazione LightEstimation


## Upgrade to AR Foundation preview

verificare le nuove ersioni.  
si parte dalle docs: <https://docs.unity3d.com/Manual/com.unity.xr.arfoundation.html>

per installarle dal Package Manager:

`Add Package by Name:"

- com.unity.xr.arfoundation 5.1.0-pre.2
- com.unity.xr.arcore 5.1.0-pre.2
- com.unity.xr.arkit 5.1.0-pre.2
