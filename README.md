# InstagramApiSharp ![InstagramApiSharp](http://s8.picofile.com/file/8336601292/insta50x.png)
An complete Private Instagram Api for .NET (C#, VB.NET).

Supports: Create new account, verify account, edit profile, set profile picture and many more...

| Target | Branch | Version | Download link |
| ------ | ------ | ------ | ------ |
| Nuget | master | v1.0.5.5 | [![NuGet](https://img.shields.io/nuget/v/InstagramApiSharp.svg)](https://www.nuget.org/packages/InstagramApiSharp) |


## Note
This library is based on [InstaSharper](https://github.com/a-legotin/InstaSharper) with more functions and flexibility.

## Install
Use this library as dll, reference from [NuGet](https://www.nuget.org/packages/InstagramApiSharp/).

Nuget package manager command:
```
PM> Install-Package InstagramApiSharp
```

Note: this library uses [Json.NET v10.0.3 and above](https://www.nuget.org/packages/Newtonsoft.Json/) for serialize and deserialize json.

## Cross Platform
| Platform | Supported Version |
| ------ | ------ |
| .NET Framework | 4.5.2 |
| .NET Standard | 2.0 |
| .NET Core(UWP) | 10.0.14393 |

## Overview
There's a lot of functions and bug fix me and [NGame1](https://github.com/NGame1) added to this library.
Check [sample projects](https://github.com/ramtinak/InstagramApiSharp/tree/master/samples) and [wiki pages](https://github.com/ramtinak/InstagramApiSharp/wiki) to see how it's works.

## Features
Some of features:

|    |    |    |    |
| ------ | ------ | ------ | ------ |
| Login | Login with Facebook | Logout | Create new account email/phone number |
| Edit profile | Change/remove profile picture | Story settings | Get user explore feed |
| Get user timeline feed | Get all user media by username | Get media by its id | Get user info by its username |
| Get current user info | Get tag feed by tag value | Get current user media | Get followers list |
| Get followers list for logged in user | Get following list | Get recent following activity | Get user tags by username |
| Get direct mailbox | Get recent recipients | Get ranked recipients | Get inbox thread |
| Get recent activity | Like media | Unlike media | Follow user |
| Unfollow user | Set account private | Set account public | Send comment |
| Delete comment | Upload photo | Upload video | Get followings list |
| Delete media (photo/video) | Upload story (photo/video) | Change password | Send direct message |
| Search location | Get location feed | Collection create/get by id/get all/add items | Support challenge required |
| Upload album (videos/photo) | Highlight support | Share story | Send direct photo/video/ stories/profile/ link/location |
## Usage
#### Use builder to get Insta API instance:
```c#
var api = new InstaApiBuilder()
                .UseLogger(new SomeLogger())
                .UseHttpClient(new SomeHttpClient())
                .SetUser(new UserCredentials(...You user...))
                .UseHttpClientHandler(httpHandlerWithSomeProxy)
                .Build();
```
##### Note: every API method has synchronous implementation as well.

## Contract, warning, note
Every method returns object IS NOT COMPLETED YET!
For example:
```
Task<IResult<object>>
```

## Version changes
v1.0.5.5
- [Bugfix] for random device (user agent). now supports 20 device
- [Add] Android version to device (randomly from android v4.0 to v9.0)
- [Add] GetCurrentDevice to InstaApi
- [Add] Biography with entities property to InstaUserInfo
- [Add] Search users by location to LocationProcessor
- [Bugfix] For some functions in LiveProcessor
- [Add] GetJoinRequestsAsync to LiveProcessor
- [Add] Send disappering photo to direct thread

v1.0.5.4
- [Add] Resend two factor login code by username, email and phone (thx to [@Lorymi](https://github.com/Lorymi) )

v1.0.5.3
- [Update] GetRequestForEditProfileAsync in AccountProcessor
- [Update] EditProfileAsync parameters, please check updated [samples/Examples/Samples/Account.cs](https://github.com/ramtinak/InstagramApiSharp/blob/master/samples/Examples/Samples/Account.cs#L71)
- [Add] Set biography (support hashtags and user mention) in AccountProcessor
- [Add] Send disappering video to direct thread
- [Cleanup] some classes and functions

v1.0.5.2
- [Add] More properties for InstaStoryLocation (Positioning properties)

v1.0.5.1
- [Add] StoryCTA Added. This used for stories with links in see more.

v1.0.5.0
- [Add] link support for direct threads
- [Add] Send link as direct message
- [Add] location support for direct threads
- [Add] Send location as direct message
- [Bugfix] for SendDirectProfileAsync

v1.0.4.9
- [Bugfix] for highlight

v1.0.4.8
- [Add] Highlight support (create, delete, get) to StoryProcessor

v1.0.4.7
- [Add] Placeholder support for direct threads
- [Add] some other info to InstaUserInfo [thx to [@GormYa](https://github.com/GormYa)]
- [Move] InstagramApiSharp to src folder
- [Move] examples projects to samples folder

v1.0.4.6
- [Add] ActionLog support for direct threads
- [Add] Profile support for direct threads
- [Add] Send profile as direct message 
- [Add] UpdateDirectThreadAsync to Messaging
- [Add] mute/unmute thread to Messaging
- [Add] DeclineDirectPendingRequestsAsync to Messaging
- [Bugfix] for GetDirectInboxThreadAsync
- [Bugfix] for ApproveDirectPendingRequestAsync
- [Bugfix] for DeclineAllDirectPendingRequestsAsync
- [Bugfix] for DicoverProccesor.GetSuggestedSearchesAsync

[Version changes](https://github.com/ramtinak/InstagramApiSharp/wiki/Version-changes) page

## Known Issues
Nothing!!!!

## Wiki
Check [Wiki page](https://github.com/ramtinak/InstagramApiSharp/wiki) for documentation.

## [InstaPost](https://github.com/ramtinak/InstaPost/) app.
You can download source code or app from [InstaPost](https://github.com/ramtinak/InstaPost/) github page.
![InstaPost](http://s9.picofile.com/file/8335529176/sc1.PNG)
![InstaPost](http://s8.picofile.com/file/8335529250/sc5.PNG)

## Language
You can ask questions or report issues in Persian or English language.
I can't answer to other languages, because I don't understand them.

## License
Do whatever you want to do! Except changing library name!!!!

## Terms and conditions
- Use this Api at your own risk.
- By using this api in your app, you agreed [Instagram Policy](https://www.instagram.com/about/legal/terms/api/).
- Please don't use this library for sending spam or massive direct messages.

## Donation
If you in Iran, feel free to donate:
https://zarinp.al/@ramtin

## Contribute
Feel free to contribute and submit pull requests.

## Thanks
Special thanks to [mgp25](https://github.com/mgp25) and his [php wrapper](https://github.com/mgp25/Instagram-API/).

## Legal
This code is in no way affiliated with, authorized, maintained, sponsored or endorsed by Instagram or any of its affiliates or subsidiaries. This is an independent and unofficial API wrapper.


## Developers

| Name | Github | Email | Telegram | Instagram |
| ------ | ------ | ------ | ------ | ------ |
| Ramtin Jokar | [@Ramtinak](https://github.com/ramtinak) | [Ramtinak@live.com](mailto:ramtinak@live.com) | https://t.me/Ramtinak | https://instagram.com/Rmt4006 |
| Ali Noshahi | [@NGame1](https://github.com/NGame1) | [NGame1390@hotmail.com](mailto:ngame1390@hotmail.com) | https://t.me/NGameW | https://instagram.com/alingame |



Iranian developers - (c) 2018
