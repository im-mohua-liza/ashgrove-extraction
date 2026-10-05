# Ashgrove Extraction

A third-person survival action prototype that runs in the browser (three.js, no build step).

Elias has to reach Mara in an abandoned mill town held by the Ravel militia, keep her alive, call for help from a radio tower, hold a landing zone and get both of them onto an evacuation helicopter.

## Play

Open `index.html` through any static web server (the character models are loaded with `fetch`, so opening the file directly from disk will fall back to simple figures):

```
npx serve .
```

Or turn on GitHub Pages for this repository and open the Pages URL.

The title screen also has **Watch demo**, which plays a cinematic run through the mission.

## Phone and tablet

Touch controls appear automatically: drag on the left half to move, drag on the right half to look, hold FIRE to shoot (drag on it to aim while firing), and tap AIM, RELOAD, CROUCH, USE, RUN, Mara, Medkit and Swap. Turn the phone sideways. Phones start on low graphics; laptops switch to low graphics automatically if the frame rate drops below 30.

## Controls

| Key | Action |
|---|---|
| W A S D | Move |
| Shift | Sprint (uses stamina) |
| C | Crouch / stand |
| Right mouse | Aim |
| Left mouse | Fire |
| R | Reload |
| 1 / 2 | Carbine / sidearm |
| E | Interact (hold for some) |
| F | Tell Mara to wait / follow |
| H | Use a medkit |
| V | Swap shoulder |
| Tab | Inventory |
| Esc | Pause |
| Arrow keys | Look around without a mouse |

## What is in the prototype

- One map: industrial yard and warehouse, six enterable houses, factory ruins, radio tower, landing zone, vehicles, vegetation, rain, lightning and mist.
- Rigged human characters with motion-captured idle, walk and run, plus procedural aiming, crouching, weapon hand placement, hit reactions and death falls.
- Mara: path-finding follower who takes cover from enemies, cowers under fire, gives spoken and subtitle warnings, and can be told to wait or follow.
- Militia AI: riflemen, flankers and heavies with patrols, suspicion, investigation, search, cover use, flanking and shared target information. Three difficulty levels.
- Combat: two original weapons with recoil, spread, reloading and headshots.
- Mission flow: find Mara, leave the yard, scavenge supplies, use the radio, reach the landing zone, hold it against waves, board the helicopter. Checkpoints after each objective.

## Credits and licenses

- Engine: [three.js](https://threejs.org) r147 (MIT), loaded from jsDelivr.
- Elias: the AvatarSDK MetaPerson sample avatar from [TalkingHead](https://github.com/met4citizen/TalkingHead) (`avatarsdk.glb`), licensed for non-commercial use. The printed logo on the shirt was replaced with a plain colour.
- Mara: the Avaturn sample avatar from [TalkingHead](https://github.com/met4citizen/TalkingHead) (`avaturn.glb`), licensed for non-commercial use.
- Militia soldier model and the idle, walk and run motion capture: `Soldier.glb` from the three.js examples (Mixamo).
- Models are stored as glTF JSON with embedded buffers so they load from any static host.

Because the Elias and Mara models are licensed for non-commercial use only, this prototype must not be sold or used commercially unless those models are replaced. Both were shrunk for the web: morph targets removed and textures resized to 1024 px.
