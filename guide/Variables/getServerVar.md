# $getServerVar
Gets a server variable value

#### Usage: `$getServerVar[variable]`
<br/>
<discord-messages>
	<discord-message :bot="false" role-color="#ffcc9a" author="Member">
		!!exec $getServerVar[holder]
	</discord-message>
	<discord-message :bot="true" role-color="#0099ff" author="Custom Command" avatar="https://media.discordapp.net/avatars/725721249652670555/781224f90c3b841ba5b40678e032f74a.webp">
		Mika
	</discord-message>
</discord-messages>

::: tip Related Functions
Check out: [$setServerVar](../Variables/setServerVar.md)

Check out: [$deleteServerVar](../Variables/deleteServerVar.md)
:::
::: tip For JSON variables with subvariable names in other variables
```bash
$let[theServerVar;$getServerVar[theServerVar]]
$let[subvarName;name]
The value for the subvariable $subvarName is $theServerVar[$subvarName].
```
:::
