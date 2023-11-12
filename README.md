# XR Prototypes

A collection of my XR prototypes as apk files. All apk files are in the `Builds` folder.

## How to install an apk
The simplest way to do it is to intall the apps via [Meta Quest Developer Hub](https://developer.oculus.com/downloads/package/oculus-developer-hub-win/).

### 1. Add an app to MQDH
Press the `Add Build` button and select an app on your disk.

<img src="Images/add_build.png" width="800px">


### 2. Launch the app
Open the context menu ("three dots") and hit the `Launch App` button.

<img src="Images/launch_build.png" width="800px">

## #154 Numeric Keyboard with Eye Tracking

<img src="Images/154_numeric_keyboard_with_eye_tracking.gif" width="800px">

Prototyped a numeric keypad with eye-tracking and hand-tracking inputs similar to what we saw on Apple's Vision Pro demo. I used Oculus Integration and ran it on Quest Pro (it's the only Quest that supports eye-tracking).

It feels very natural and familiar. We already use the same principles for regular keyboard-based, non-blind typing. First, you visually allocate a target, and then your hand confirms an intended action. But the eye-tracking version is less laborious since this hand confirmation is remote, and you don't need to "physically" interact with the keyboard. 

[Download APK](https://github.com/Volorf/xr-prototypes/blob/main/Builds/154_numeric_keyboard_with_eye_tracking.zip)

[Learn more](https://twitter.com/Volorf/status/1721833148957241494)

## #156 Keypad with Eye Tracking

<img src="Images/156_keypad_with_eye_tracking.gif" width="800px">

I made a prototype inspired by a telephone keypad. It uses eye-tracking to hover over a key and finger pinches to define which letter you will type. 

As you can see, each key encodes up to 4 signs (with SYM mode, it's 8) in a single mode:

**Pinch Invocation**:
1. `Index` -> Top Left ->	"A"
2. `Middle` -> Top Right -> "B"
3. `Ring` -> Bottom Right -> "C"
4. `Pinky` -> Bottom Left -> "1"

**Observations**:
- Sometimes, during typing, I accidentally triggered the system menu. Adding visual signifiers to the virtual hand to specify a dedicated typing mode would help. It would visually guide users to stay in the mode. Or, OS holders might add the signifiers to the mode where you invoke system commands. The point is it should be easy for users to recognize when they switch from an app interaction layer to a system one.
- The current Computer Vision-based hand tracking is not reliable enough. There are a lot of false positives for detecting Ring/Pinky Pinches. A dedicated hand-tracking device would improve the experience. As a quick hack — since there are no significant issues with Index/Middle pinches recognition — to type the left side symbols ("A 1" column), you use index/middle pinches on your left hand, and for the right side ones ("B C" column), you use your right hand respectively.
- The key layout doesn't consider the letters' use frequency. Arranging the layout based on it would speed up typing dramatically. But it would involve training and make the learning curve steeper.
- Smart suggestions ("T9") would allow us to use only Index Pinch for typing.

Overall, it's a very promising approach that massively reduces physical fatigue for spatial typing. With dedicated, accurate hand-tracking devices, input systems like this will make spatial interactions truly approachable.

[Download APK](https://github.com/Volorf/xr-prototypes/blob/main/Builds/156_keypad_with_eye_tracking.zip)

[Learn more]()