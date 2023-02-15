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
- locomotion (add Locomotion System)
  - Snap Turn Provider (Action-based)
  - check Continuous Turn Provider (Action Based)
  - add Teleportation Provider
  - add Teleportation Area ad un tappeto
  - add Teleportation Anchor
  - test Custom Reticle
- grabbable ()
  - add VR_Hands to controlleers
  - tennis ball - XR Grab Interactable
  - XR Ray Interactor component, disable the Anchor Control setting
  - XR Ray Interactor component, enable the Hide Controller on Select
  - improve the ball material / colliders / smooth
  - add Racchetta tennis, con Attach
- sockets ()
  - cappelli e attaccapanni
  - Add XR Grab Interactable
  - crea sfere colliders per gli hooks e XR Socket Interactor
  - add Attach Transform to Socket (Z == forward, Y == upward)
  - duplicate
  - check Starting Selected Interactable
  - cappello in testa?
  - Interaction Layer Mask

## Interaction

- audio 
- haptics
- remote controller
- UI
