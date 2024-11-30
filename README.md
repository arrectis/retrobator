
This is the hub for Retrobator, a NES emulator available on Steam and Itch.io.

To report an issue, see [Issues](https://github.com/arrectis/retrobator-home/issues) or contact [support@arrectis.com](mailto:support@arrectis.com) directly.

#### Supplemental Package ####
(Check here periodically for updates to this package.)
This package contains:
- The OpenAI Provider mod.
- Basic event labels for several games.
<>
To install, save the image above to your PC and open it in Retrobator, or drag and drop the file into the Retrobator window.
You can also download the mod in .Zip form here.

## Features ##

- **Timeline** - Use the Timeline slider to go back in time, watch again, or restart gameplay from any point.
- **Map** - Reveal traversed areas of the game by simply zooming out or by using a wide aspect ratio.  Replays are also shown on top of the map for your entertainment.
- **Butter Mode** - Interpolation enables smoother background and sprite movement, especially during slow-motion (re)play.
- **Backgrounds** - Replace in-game 'sky' pixels with custom or generated* images.
- **Audio** - Smooth, unmixed audio channel waveforms, with adjustable octaves for deeper bass.
- **AI Integration*** - Interact with your own AI agent. See [AI](#ai-Assistant).
- **(Other Features)** - Fast-forward, rewind, slo-motion, input lag mitigation, CRT mode, save states and more.

## FAQ ##

### What is Retrobator? ###
Retrobator is a nes emulator aiming to deliver a new experience.
I plan to achieve this by:
- Implementing rare or novel features.
- Integrating AI for entertainment and control.
- Providing a platform for the community to build upon.

### Who is behind this? ###
A single highly-motivated insane man.

### What are the supported platforms? ###
Windows is the only officially supported platform at the moment, with others tentatively planned.  If you have a particular platform in mind, let me know [here](https://github.com/arrectis/retrobator-home/issues).

### What games are supported? ###
Although most games are compatible with Retrobator, a few notable games are not at this time.  If you want a particular game to be supported, let me know [here](https://github.com/arrectis/retrobator-home/issues).

### Where do I find games to use with Retrobator? ###
Retrobator requires NES games in digital file form (typically called 'ROMs'). You can find indie NES games in digital form on Itch.io. 

When it comes to classic NES games, I can't help you there. Personally, I've used INLRetro and RetroBlaster hardware to create digital backups of games that I physically own, which is how I source my games.

### What is an AI assistant? ###
This is an __optional__, __experimental__ feature that is provided as a downloadable mod, and __requires OpenAI API credit to use.__
Alternate AI providers may be available in the future.

What you can do with the AI assistant:
- Command your AI assistant (via voice or text) to do various things for you: Open games, load cheats, generate backgrounds, etc. 
- Converse, banter, and have your assistant react to in-game events*.
- Give your AI different personalities.

Note: This is currently utilizing OpenAI's Advanced Voice Mode, which is currently accessible as a 'Preview'.  This means that:
- This service may have a daily limit. As of this writing, it does.
- This service may suffer from outages or changes that will cause the assistant to go down. Check this page for updates to the OpenAI mod that may address these changes.
- The "bring your own key" (BYOK) model of connecting to OpenAI may change in the future, or may even be forcibly nuked by OpenAI. Expect a transition period in the future to a different model.
- Services like this are likely to get better, cheaper, and more ubiquitous in the coming months and years. 

### How do I use the AI Assistant? ###
First, you must install the supplemental package found on this page.

Then, navigate to "Packages" in Retrobator, and check the appropriate box to enable OpenAI.

Finally, to connect the assistant, you must provide an OpenAI API key:
1. Create an OpenAI API developer platform account on their site. (Currently platform.openai.com)
2. Add some _Pay as you go_ credit. (Currently in the settings under _Billing_)
3. In the Dashboard, create an API key, and copy it.
4. In Retrobator, open the OpenAI widget, and paste the key into the field.";

This will allow Retrobator to communicate with OpenAI on your behalf. 

Retrobator does not store or share your OpenAI API key. However, it may include application state in its messages to the API.

### Why is AI provided only as a mod? ###
Some app stores, like Steam, require that any features that incur charges (even if optional / 3rd-party) be funneled through the app store's microtransaction or subscription systems.  Since this would increase the cost of any AI services the user connects, I have opted to unbundle this feature from the product and offer it as an open-source mod.

### What are events? ###
Retrobator does not send video of your gameplay session to the AI assistant.  So how does it know what's happening? 

That's where _events_ come in. Example events:
- Game opened (built-in)
- Player died
- Game over
- Finished stage

etc.

Retrobator does recognize most of these events by default; __you must provide examples__ of each event in order to "**teach**" Retrobator how to identify them on a per-game basis. Alternatively, you can import pre-defined events that others have exported; some have been provided in the supplement package.

The general procedure for labelling events is as follows:
- Load up a game.
- Play it for a while; long enough to provide multiple examples of a specific event you want to identify.
- Select 'Event Labels' in the main menu.
- Mark __all__ occurrences of the event happening in the timeline.
  This means marking a frame before and frame after the example event occured.
- Discover the event and label it appropriately.

### What tile labels? ###
Graphics are made up of squares of pixels called 'tiles'.  Together, these tiles form things like enemies, items, characters, etc.

By highlighting and labelling groups of tiles you see in-game, you can provide the AI assistant with knowledge of what is showing on screen during an event. Tile groups may provide further uses as Retrobator's feature set grows.

The procedure for labelling tiles is fairly straightforward:
- Load up a game.
- In game, find some graphics you want to label.
- Select 'Tile Labels' in the main menu.
- Using a mouse, select and highlight the thing you want to label, including all of its tiles.
- Right-click to group the tiles into a 'tile group'.
- Label the tile group with the name of it (duplicate names are allowed.)

### What kinds of things can be imported and exported to/from Retrobator? ###
- Transformations (Backgrounds)
- Labels (Tile groups, events)
- Mods (AI providers, etc.)

Transformations and labels are game-specific, whereas mods may apply to any/all games.

### How do mods work? ###
Mods are simply C# code files that are compiled and cached at runtime. These mods can provide services that interact with Retrobator at the application level or on a per-game basis.
The mod API is evolving, and is not yet documented.

### I found an issue, I have a suggestion. How do I forward it to your brain? ###
See [Issues](https://github.com/arrectis/retrobator-home/issues).
