## [Unreleased/Working on]

### [1.12.4] - T.B.D.

#### [NEW]

- Changed the way voice channel logging handles Husqy tempchannels

#### [Bugfixes]

- Fix for Kick Role

## [Released]

### [1.12.3] - 06-01-2023

#### [NEW]

- Added `/utils color view` command to view colors based on a given HEX or RGB value
- Added `/volume` command to change volume of the audio Husqy plays for all members (NOTE: This is different from the individual sound slider that users have!)

#### [BREAKING]

- Migrate `/reaction_roles configure` command to `/settings module configure` (Note: Make sure to select the reaction roles module!)

#### [Bugfixes]

- Fix for some message components (like buttons) on module functions not working
- Add credits/attribution for TuneIn radio

### [1.12.2] - 04-01-2023

#### [NEW]

- Command parameters which requires a channel to be selected, are now only showing the channel types which are allowed to be selected
- `/play radio {country code} {radiostation}` is now changed to `/play radio {radiostation}` and uses TuneIn for radiostations. The radiostation parameter uses Discord Autocomplete!

#### [Bugfixes]

- Fix for some message components (like buttons) not working

### [1.12.1] - 03-01-2023

#### [NEW]

- Added logging for: `User server mute`, `User server unmute`, `User server deafend`, `User server undeafend`, `User self deafend`, `User self undeafend`, `User self muted`, `User self unmuted`, `User started streaming`, `User stopped streaming`, `User turned on camera`, `User turned off camera`
- Voice channel is now mentioned in logging when Husqy joins a channel

#### [Bugfixes]

- Fix for `User join` logging event triggering when a user muted, deafend, started streaming, etc.
- Fix for socials configuration wizard reddit button not working

### [1.12.0] - 02-01-2023

#### [NEW]

- Added Autoresponder module
- Added Ticket module
- Added Reddit monitoring to the socials module
  - Added `/socials reddit` command
- Added `/play tts` command (Experimental!)
- Added audio playback support for TikTok, Reddit and PornHub (Experimental!)
- Added `/mod_user vckick` and `/mod_user move` commands
- Added `/mod_server lock` and `/mod_server unlock` commands
- Added new label to `/support submit` > Code Cleanup
- Added `/loop` command to toggle if a song loops
- Added logging to user joining, leaving and moving voice channels
- Added `/utils custom_modal create` and `/utils custom_modal preview` commands
- Added support for Forum Channels in `/info channel` command

#### [BREAKING]

- Bump hikari to 2.0.0.dev114
- Removed all `/password` commands!
- Migrate `/socials {components}` commands to `/settings module configure`
  - Because of this migration, only admins can add, remove or list accounts
  - This change is valid for: `Twitter` and `Reddit` components!
  - Getting the monitored list of the components is now located at: `/info bot module_info: socials`
- Migrated commands `/custom_embed create` and `/custom_embed send` to `/utils custom_embed create` and `/utils custom_embed send` respectively
- Open-Sourced translations (https://github.com/husqybot/translations)!
- Open-Sourced changelog (https://github.com/husqybot/CHANGELOG)!

#### [Changes]

- Update to internal logging
- Update internal file structure
- Added autocomplete for tag names

#### [Bugfixes]

- Fixed Queue embed bug
- Fixed nowplaying embed auto delete time when auto_delete is under 20 seconds
- Fixed bug where some messages with components would not send
- Fix for Channel updates logging not working when updating permissions

### [1.11.3] - 28-11-2022

#### [Bugfixes]

- Fixed multiple error messages on `/play music`, `/playnext music` and `/remove` commands
- Fixed an issue with the `/remove` command not working
- Added extra logging to `/play music`, `/playnext music` and `/remove` commands for troubleshooting

### [1.11.2] - 27-11-2022

#### [Bugfixes]

- Fixed an issue with the `/playnext` command not working
- Fixed an issue with the `/search` command logging displaying the wrong platform

### [1.11.1] - 26-11-2022

#### [NEW]

- Added position_in_queue parameter to `/play music` command to add the song to the queue in a particular spot
- Added support for Spotify, Deezer and Apple Music in the `/search` command
- Added support for Spotify, Deezer and Apple Music in the `/play music` and `/playnext music` commands

#### [Bugfixes]

- Removed queue embed timeout logging

### [1.11.0] - 12-11-2022

#### [NEW]

- Added ability for poll events to be changable in the logging module
- Added polls feature
  - Added polls create
  - Added polls delete
  - Added polls clear_votes
  - Added polls list
  - Added polls details
  - Added polls stop
- Reminder list now stays active for a minimum of 20 seconds
- Added optional auto_shuffle parameter to `/play music` and `/playnext music` commands
- Added autocomplete for reminder_ids
- Added `/admin restart` command to allow admins from the support server to restart the bot

#### [Bugfixes]

- Fixed an issue where `/info user` and `/info server` commands would not work
- Added debug for load_modules
- Fixed an issue where reaction would be deleted from non reaction role messages
- Fixed an issue where tag events could not be changed
- Fixed an issue where queue command would display wrong auto delete time
- Fix for host command using the wrong logging option
- Fixed type hints for reminders
- Fix for ended reminders not being deleted until restart
- Fix for Greeting module configuration displaying wrong module name
- Fixed an issue where all users in the support server would be able to block and unblock people from commands

### [1.10.1] - 12-11-2022

#### [Bugfixes]

- Fixed logging issue with queue command

### [1.10.0] - 11-11-2022

#### [NEW]

- Added the ability to see who added the current playing song in the `/nowplaying` dialog
- Added pagination to the queue command

#### [Bugfixes]

- Bumped dependencies
- Fixed startup caused after dependencies update
- Fixed `/host` command not working

### [1.9.2] - 30-10-2022

#### [Bugfixes]

- Fixed an issue where the timezone GMT offset could not be changed

### [1.9.1] - 09-10-2022

#### [Bugfixes]

- Fixed an issue where info bot module logging would not work

### [1.9.0] - 09-10-2022

#### [NEW]

- Added a tag system
- Added Rock, Paper, Scissors game

#### [Bugfixes]

- Fixed an issue where the `/info role` command did not work

### [1.8.0] - 06-10-2022

#### [NEW]

- Husqy logging will now mention users (without notifying)
- Added invite_link command for users to use a set invite link determined by the server admin
  - Added settings command for admins to update or remove the invite link from the Husqy configuration

#### [Bugfixes]

- Fix where a tempchannel could not be deleted if specific permissions where changed (added overwrites for Husqy)
- Fix where the queue list would disappear after the auto delete time of the server (even if this time is below the minimum time)
- Fix where reminder linked message link was not clickable

### [1.7.1] - 11-09-2022

#### [Bugfixes]

- Fix for host command latency values

### [1.7.0] - 02-09-2022

#### [NEW]

- Added host command to view host metric information.

#### [Bugfixes]

- Fix for modals not working
- Updated .gitignore
- Updated requirements.txt

### [1.6.6] - 08-08-2022

#### [BREAKING]

- Remove Instagram component from the socials module

### [1.6.5] - 27-07-2022

#### [Bugfixes]

- Revert Instagram fix

### [1.6.4] - 27-07-2022

#### [Bugfixes]

- Fix for instagram checker
- Fix MNM radio link

### [1.6.3] - 15-06-2022

#### [Bugfixes]

- Fix for components stopping if another interaction was made
- Fix in wait_for not checking channel in MessageCreateEvent

### [1.6.2] - 12-06-2022

#### [Bugfixes]

- Fix for logging module messages not accounting for the server timezone

### [1.6.1] - 10-06-2022

#### [Bugfixes]

- Fix for startup
- Fix for info bot logging

### [1.6.0] - 10-06-2022

#### [NEW]

- Added support to create reminders!
- Added seek command for music playback. This makes it possible to jump to a specified time in the song!
- Added support to change the role linked to an emoji
- Added support to change the emoji linked to a role

#### [BREAKING]

- Migrated reaction roles to a module

#### [Bugfixes]

- Fix for reaction roles not working
- Fix for radio stations not playing

### [1.5.2] - 31-05-2022

#### [Bugfixes]

- Fix for playnext and remove commands

### [1.5.1] - 28-05-2022

#### [Bugfixes]

- Fix for TwitterHandler KeyError
- Custom embed create start message now displays according to the servers auto_delete time

### [1.5.0] - 27-05-2022

#### [NEW]

- Added temporary mute command
- Added temporary timeout command
- Added Custom embed commands (Create and send)
- Added Socials module with support for Twitter and Instagram accounts

#### [Bugfixes]

- Fix for skip command not working
- Fix for info bot logging command not showing tempchannel logging status when enabled
- Users are now mentioned when a message and the value _<user_mention>_ is used in the greetings module (in server greetings component). Users can't be mentioned in an Embed!
- Fix for `/search` command not working when no results are found
- Fix for tempchannels module event firing when the module is disabled (Husqy internal logging)
- Fix for spotify albums failing to play
- Fix for music playlist stopping, but continuing one song (which should be stopped) when adding a new song

### [1.4.3] - 15-05-2022

#### [Bugfixes]

- Fix for tempchannels triggering channel events
- Fix channel, role and user events to only gather variables when the event is logged for that Guild

### [1.4.2] - 15-05-2022

#### [Bugfixes]

- Fix for role update event cache
- Fix for reaction role delete
- Fix for greetings module embed

### [1.4.1] - 14-05-2022

#### [Bugfixes]

- Fix for module logging
- Fix for Husqy internal logging

### [1.4.0] - 14-05-2022

#### [NEW]

- Added Temporary Channels

#### [BREAKING]

- Re-implementation of Modules
  - Logging is now a module. This is disabled for all servers and must be enabled if you wish to use this.
  - Greetings is now a module. This is disabled for all servers and must be enabled if you wish to use this.
  - Temporary Channels are added and are a module. This is disabled for all servers and must be enabled if you wish to use this.
- Re-worked `/info bot` command. It now support a parameter: module_info to select a module to get info about, this is an optional parameter, if not given, general bot info will be shown!

#### [Bugfixes]

- Change for channel update event.
- Fix bug where the music event loop would end unexpectedly by changing to Hikari Voice.
- Fix bug for tempchannels where it would result in a AttributeError.
- Fix ctx parameter to be type tanjun.abc.SlashContext instead of tanjun.abc.Context.
- Fix for bot and db variables.
  - \_bot -> bot.
  - \_db -> db.
  - \_lava_client -> lava_client.

### [1.3.10] - 18-04-2022

#### [Bugfixes]

- Fix for info bot command

### [1.3.9] - 15-04-2022

#### [BREAKING]

- Removed Modules

#### [Bugfixes]

- Fix for users not being mentioned when they join a server
- Fix for leave message not being sent when there is no kick entry available

#### [Changes]

- Change `/mod_server` clear_messages command to be faster

### [1.3.8] - 10-04-2022

#### [Bugfixes]

- Music commands change
  - `/radio play_{country_code}` -> `/play radio {country_code}`
  - `/music play` -> `/play music`
  - `/music playnext` -> `/playnext music`
  - `/music remove` -> `/remove`
  - `/music shuffle` -> `/shuffle`
  - `/music skip` -> `/skip`
  - `/music search_{platform}` -> `/search` (the platform is now a parameter!)

### [1.3.7] - 10-04-2022

#### [Bugfixes]

- Fix bug with spotify playlist and album playing
