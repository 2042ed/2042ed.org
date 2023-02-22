# VR Oculus Lab

<https://github.com/StefanoCecere/GameLab_VR_Unity/>

## Setup

- Quest Developer Mode
- Quest Setup: <https://www.oculus.com/setup/>

## Room

- ognuno propria scena
- check XR simulator
- setup / environment
  - esterno, interno, forniture

### locomotion

- Snap Turn Provider (Action-based)
- check Continuous Turn Provider (Action Based)
- add Locomotion System
- add Teleportation Provider
- add Teleportation Area ad un tappeto grande
- add Teleportation Anchor a due tappeti piccoli
- test Custom Reticle all'Area

### grabbable

- add VR_Hands to controlleers
- tennis ball - XR Grab Interactable
- XR Ray Interactor component, disable the Anchor Control setting
- XR Ray Interactor component, enable the Hide Controller on Select
- improve the ball material / colliders / smooth
- add Racchetta tennis, con Attach

### sockets

- cappelli e attaccapanni
- Add XR Grab Interactable ai cappelli
- crea sfere trigger colliders per gli hooks e XR Socket Interactor
- add Attach Transform to Socket (Z == forward, Y == upward)
- duplicate
- check Starting Selected Interactable
- cappello in testa?
- Interaction Layer Mask per separare gli interactables

## QUIZ
<https://learn.unity.com/quiz/mission-1-quiz-vr-basics>

## Interaction

- audio: On Select Entered
- 3D audio on fireplace
- add Reverb Zone

- add haptic a hover e select

- remote controller: grab and activate TV
- add Play Quick Sound + AudioSource to remote and activate event
- add a Change Material component.
- add Video Player component to tv screen
- Material Property to _BaseMap
- add play action al remote

### attività

- telefono che suona audio al click
- pulsante che apre porta
- creare torcia elettrica (ToggleLight())
- pistola che spara dardi (LaunchProjectile() + DestroyObject())

- ANTA e LEVER: <https://www.youtube.com/watch?v=bYS35_hC6B0>

### haptic

- direct interactor a mano destra (+ sphere collider 0.05)
- 
