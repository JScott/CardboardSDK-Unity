Cardboard Controls+ is all you need to develop the best Cardboard games in Unity. These scripts enhance [Google's official Cardboard SDK for Unity](https://developers.google.com/cardboard/unity/) with improvements such as discrete magnet control, raycast data, and event-driven architecture. Stop limiting your creative options!

[![Join the chat at https://gitter.im/JScott/cardboard-controls](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/JScott/cardboard-controls?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# What's added?

[![Join the chat at https://gitter.im/JScott/cardboard-controls](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/JScott/cardboard-controls?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Google's SDK only has one hook into the magnet: `bool CardboardTriggered`. It's available for one frame that you have to waste cycles polling for. Instead of limiting yourself to that, you can now utilize C# methods and delegates for:

- Magnet down
- Magnet up
- Magnet click
- Boolean if the magnet is held
- Seconds magnet held for

This expands your opportunities, allowing interactions like holding the magnet to move and clicking to interact to provide a more natural experience.

There are also methods and delegates for:

- Tilting the device, as used in the official Cardboard app to navigate menus
- Gaze raycasting, capturing what you look at and for how long

These helpers let you focus on what makes your game cool instead of boilerplate code.

# Prerequisites

If you got this from the Asset Store then I've already packaged a version of the prerequisites for you.

If not then you'll need to import the base Cardboard SDK if you haven't already:
- [Download CardboardSDK.unitypackage](https://github.com/googlesamples/cardboard-unity/blob/master/CardboardSDKForUnity.unitypackage?raw=true) from [Google's repository](https://github.com/googlesamples/cardboard-unity).
- Import it in your scene
- Use the `CardboardMain` prefab for your camera

If you're working on iOS then you might want to look into replacing Google's SDK with [rsanchezsaez's CardboardSDK-iOS](https://github.com/rsanchezsaez/cardboardsdk-ios). It ports the Android code to iOS with nearly feature parity.

If neither of those work, you might want to look into the [Durovis Dive Plugin Package](https://www.durovis.com/sdk.html) as a last resort. You will also not be able to use controls that rely on Google's API, such as the Raycast Gaze.

# Usage

When you import [the latest package](https://github.com/JScott/cardboard-controls/releases/latest), just add the `CardboardControlManager` prefab to the root of your scene. Now you can start using the API which is documented in [the DemoScene code](https://github.com/JScott/CardboardSDK-Unity/blob/master/CardboardControl/DemoScene/ExampleCharacterController.cs).
