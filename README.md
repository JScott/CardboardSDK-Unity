Cardboard Controls+ is all you need to develop the best Cardboard games in Unity. These scripts enhance [Google's official Cardboard SDK for Unity](https://developers.google.com/cardboard/unity/) with improvements such as discrete magnet control, raycast data, and event-driven architecture. Stop limiting your creative options!

# What's added?

In addition to everything from Google's impressive SDK, you get better interactions to improve the experience for developers and players alike.

## Discrete Magnet Control

Google's SDK only has one hook into the magnet: `bool CardboardTriggered`. It's available for one frame that you have to waste cycles polling for. 

Now you can utilize C# methods and delegates to expose:

- Magnet down
- Magnet up
- Magnet click
- Boolean if the magnet is held
- Seconds magnet held for

This expands your opportunities, allowing interactions like holding the magnet to move and clicking to interact to provide a more natural experience.

## Standard Gestures

Google's SDK has nothing for the gesture of tilting the Cardboard vertically. This is used in the official Cardboard app as an excellent way to navigate menus. Now you don't need to code it yourself.

## Raycast Gaze

Google's SDK provides a Gaze vector to represent the direction you're facing. I've taken the courtesy of building a Gaze raycast that covers a lot of common uses for game developers. More events and delegates mean that you can focus on what cool things your game does and not building the same boilerplate again.

# Prerequisites

If you got this from the Asset Store then I've already packaged a version of the prerequisites for you.

If not then you'll need to import the base Cardboard SDK if you haven't already:
- [Download CardboardSDK.unitypackage](https://github.com/googlesamples/cardboard-unity/blob/master/CardboardSDKForUnity.unitypackage?raw=true) from [Google's repository](https://github.com/googlesamples/cardboard-unity).
- Import it in your scene
- Use the `CardboardMain` prefab for your camera

If you're working on iOS then you might want to look into replacing Google's SDK with [rsanchezsaez's CardboardSDK-iOS](https://github.com/rsanchezsaez/cardboardsdk-ios). It's a port of the Android code for iOS that nearly has feature parity.

If neither of those work, you might want to look into the [Durovis Dive Plugin Package](https://www.durovis.com/sdk.html) as a last resort. You will also not be able to use controls that rely on Google's API, such as the Raycast Gaze.

# Usage

When you import this package, just add the `CardboardControlManager` prefab to the root of your scene. Now you can start using the API which is thoroughly documented in [the DemoScene code](https://github.com/JScott/CardboardSDK-Unity/blob/master/CardboardControl/DemoScene/ExampleCharacterController.cs).
