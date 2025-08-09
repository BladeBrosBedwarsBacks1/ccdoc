# $createThread <Badge type="warning" text="Read Below" vertical="middle" />
Create a thread, corresponding to the messageID specified in the function
#### Usage: 
`$createThread[Channel ID;Message ID;Thread Name;Reason;Duration (1h/1d/3d/7d)(optional);Return ID (yes/no)(optional);Private Thread? (yes/no)]`

#### Example (Create Thread on user message):
```bash
$createThread[
    {channel=$channelID}
    {message=$messageID}
    {name=Example}
]
```

#### Example (Create A private thread):
```bash
$createThread[
    {channel=$channelID}
    {message=$messageID}
    {name=Example}
    {private=yes}
]
```
::: tip
```php
$createThread[$channelID;$sentMessageID;New Thread;<@&1403404906433613969> was asked to create this thread.;3d;no;yes]
```
This adds a link inside the recently sent message (`$sentMessageID`) to the thread which is in the same channel as the message (`$channelID`) and calls the thread 'New Thread' (`New Thread`) and keeps the thread active for 3 Days (`3d`) because Custom Command (Mentions Custom Command) was asked to create the thread (`<@&1403404906433613969> was asked to create this thread.`) and the code doesn't return the ID of the thread (`no`) and the thread is private (`yes`).
:::

::: danger
You can only use the durations, allowed by your boosting level! Please do not try to use `7d` if your server hasn't got level 3 boosting perks
:::

::: danger
You can make private threads only if your server perks allow it.
:::

::: tip Related Functions
[$createChannel](../Channel/createChannel.md), create a channel

[$createRole](../Role/createRole.md), create a role
:::

::: tip
This Command supports Curl Arguments, a link to the page explaining it, will get added when done
:::

##### Function difficulty <Badge type="danger" text="Difficult" vertical="middle" /> 
###### Tags: <Badge type="tip" text="channel" vertical="middle" /> <Badge type="tip" text="create" vertical="middle" /> <Badge type="tip" text="Threads" vertical="middle" /> <Badge type="tip" text="Create Threads" vertical="middle" />
