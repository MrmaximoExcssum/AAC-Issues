# AAC-Issues
AAC Issue Tracker. 

*Please make sure to take a quick search in existing issues before posting your issue.*

*AAC development is currently paused. You can and should still report bugs.*

When creating an issue, please include lots and lots of detail. Videos are preferred, screenshots and full console logs at the very minimum. The following will also be nessecary:
- AAC version
- ProtocolLib version
- Full plugin list
- Explanation of how to reproduce the issue.

If your explanation is too vague, or the issue can't be reproduced, then your issue will be closed.

The AAC Test Server is currently public and is at **test.kons.co**

A public **discord server** is available at **https://discord.gg/uc9w2nx**

### Those who join the test server purely to develop bypasses, without any obvious intention of helping AAC develop, will be removed from the server.

## Useful stuff

Some links
- [SpigotMC resource](https://www.spigotmc.org/resources/6442/)
- [Current AAC default config](https://gist.github.com/konsolas/400c9678e0264fab8d04d84780ec4c63)

### Conditional Commands

The ConditionalCommands plugin (written by konsolas) allowes you to check certain conditions before another command is issued.
Possible conditions: ping, tps, time online, server uptime, player count, permission, aacvl, chance
More information: https://www.spigotmc.org/resources/conditionalcommands.14295/

### JsonMessageMaker

The JsonMessageMaker plugin (written by Janmm14) allows you to simply add hover and click effects to chat messages. This might be a useful replacement to /aacstaffnotify.
Check it out here:
https://www.spigotmc.org/resources/jsonmessagemaker.7938/

### AAC API

The API of AAC is documented in the [SpigotMC resource description](https://www.spigotmc.org/resources/6442/). 

Plugins built against older versions of the AAC API usually work with newer versions of AAC, but not the other way round.

In case a plugin developer has not bought AAC, he can code against a dummy AAC API which is available in this repository, just scroll up to the file list.

Alternatively the dummy AAC API is also available in a maven repository:

```xml
        <repository>
            <id>janmm14-public</id>
            <url>https://repo.janmm14.de/repository/public/</url>
        </repository>

```
```xml
        <dependency>
            <groupId>de.janmm14</groupId>
            <artifactId>aac-api</artifactId>
            <version>3.6.0</version>
        </dependency>
```

### AAC Debug logging


#### AAC 3.3.4+
If enabled, AAC will log check specific data and many player actions from all online players into a debug log file inside `plugins/AAC/`.

_WARNING: AAC debug logging can generate really huge files._

You can toggle the debugging state with `/aacdebug`, everytime debug is disabled a new debug file will be generated.
A debug log is especially useful for movement related issues.

#### Up to AAC 3.3.3
A debug log shows extended information on what AAC is doing.
AAC is capable of debugging one player at a time.

**Start debbuging**: `/aacdebug <player>`, `<player>` needs to be replaced with the name of the player to debug.

**Stop debugging**: `/aacdebug`
Saves the debug log to `plugins/AAC/`.
