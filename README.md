# Steam Group Restrict
A plugin that kicks players based on whether they are a member of a group

![Build include](https://github.com/Impact123/AutoExecConfig/workflows/Build%20include/badge.svg)


## Installation
1. Install [The SteamWorks extension](https://forums.alliedmods.net/showthread.php?t=229556)
2. Put `steamgrouprestrict.smx` in the `sourcemod/plugins` folder
3. Load the plugin
4. Configure it 

## ConVars
The plugin creates a `plugin.steamgrouprestrict.cfg` in the `cfg/sourcemod` folder when its loaded where you can configure these variables.

### sm_steamgrouprestrict_groupids (default: "")
List of group ids separated by a comma.
Spaces between the value and the comma are trimmed off so feel free to use them for better visibility.

The expected input is the result of `groupID64 % (1 << 32)`  
You can get a group's groupID64 by visiting  
`https://steamcommunity.com/groups/ADDYOURGROUPSNAMEHERE/memberslistxml/?xml=1`  
To convert the groupID64 you can use the `python` console.

### sm_steamgrouprestrict_notify (default: 1)
Whether or not admins should be notified about kicks.  
By default admins with the **BAN** flag are considered admins but you can [override this](https://wiki.alliedmods.net/Overriding_Command_Access_(SourceMod)) with `sm_steamgrouprestrict_admin`
 
### sm_steamgrouprestrict_reason (default: You are a member of a restricted group)
Kick reason displayed to client
