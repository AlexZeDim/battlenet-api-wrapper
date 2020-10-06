# Warning! This fork is already deprecated. If you want to use alternative library to access Blizzard Battle.net API, try Lukem's [BlizzAPI](https://github.com/lukemnet/blizzapi)

## Battle.net API Wrapper

A promised-based Node.js wrapper for the Battle.net Community and Data APIs (supports WoW, WoW Classic, SC2, D3, and Hearthstone).

## Installation

`$ npm install --save "git+https://github.com/AlexZeDim/battlenet-api-wrapper.git"`

## Prerequisites / General Information

- To get your `Client ID` and `Client Secret` needed for this library, please refer to the steps in the [Battle.net API Getting Started documentation](https://develop.battle.net/documentation/guides/getting-started).
- Battle.net API Documentation Reference: https://develop.battle.net/documentation

## Usage

The basic implementation of this library is as follows:

```
const battleNetWrapper = require('battlenet-api-wrapper');  
  
const clientId = 'YOUR_CLIENT_ID';  
const clientSecret = 'YOUR_CLIENT_SECRET';  
const providedToken = '';
const region = 'eu';
const locale = 'en_GB';
  
(async function() {  
   const bnw = new battleNetWrapper();  
   await bnw.init(clientId, clientSecret, providedToken, region, locale);
   /* make request here with bnw.className.methodName(..args) */
}());  
```

Once you have the `battleNetWrapper` class object instantiated, you then have access to all of the classes
that exist under that umbrella.  For each of the classes below, you will see a link to the full abstraction
documentation.  Each of functions are available on the respective class objects.

- `bnw.Diablo3Community` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/d3#diablo-3-community)
- `bnw.Diablo3GameData` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/d3#diablo-3-game-data)
- `bnw.HearthstoneGameData` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/hearthstone#hearthstone-game-data)
- `bnw.Starcraft2Community` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/sc2#starcraft-2-community)
- `bnw.Starcraft2GameData` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/sc2#starcraft-2-game-data)
- `bnw.WowGameData` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/wow#wow-game-data)
- `bnw.WowProfileData` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/wow#wow-profile-data)
- `bnw.WowClassicGameData` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/wowClassic#wow-classic-game-data)
- `bnw.WowCommunity` [Usage Documentation](https://github.com/AlexZeDim/battlenet-api-wrapper/tree/master/src/wow#wow-community)

WoWCommunity endpoints has been deprecated since 16 March 2020 and no longer working. ([See this thread](https://us.forums.blizzard.com/en/blizzard/t/wow-community-api-turned-off/4281))

## Having issues, wanna contribute or another crazy idea?

[Create a PR](https://github.com/AlexZeDim/battlenet-api-wrapper/pulls) or [post an issue](https://github.com/AlexZeDim/battlenet-api-wrapper/issues) in this fork (reviewed by me)

Or [make PR](https://github.com/QuadDamn/battlenet-api-wrapper/pulls), [post an issue](https://github.com/QuadDamn/battlenet-api-wrapper/issues) at the origin source (reviewed by QuadDamn)

## License

The original library has been made by **[QuadDamn](https://github.com/QuadDamn)**

Battle.net API Wrapper is released under the [MIT License](https://opensource.org/licenses/MIT).
