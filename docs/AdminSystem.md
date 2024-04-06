# AdminSystem v1.0

## Datenbank (MySql)
Beispiel für PhP my admin: <br> <br>
Dieses Script benutzt die MySql Datenbank von deinem Server. <br>
Um diese nun einzurichten musst du dich zuerst auf deinem Datenbank Dashboard anmelden


## Discord logs:

Alle Aktionen werden auf Discord über einen WebHook geloggt.

### WebHook erstellen
1. Gehe auf die Channel einstellungen von dem Kanal in den die Logs gesendet werden sollen.
2. Gehe in den Einstellungen auf Intigrationen
<br>
![Einstellungrn](https://cdn.discordapp.com/attachments/1226145703877939250/1226146172628893776/image.png?ex=6623b49c&is=66113f9c&hm=93c35729de4bba3bc948b103500b69331827e414a381c5001aa89fef6d90198f&)
3. Clicke auf Web WebHook erstellen
<br>
![WebHook Erstellen](https://cdn.discordapp.com/attachments/1226145703877939250/1226147200283709460/image.png?ex=6623b591&is=66114091&hm=9e2b433f52ad7cf142f1e793344446ea360332e14bf292ce11777d169f0099ad&)
4. Clicke auf den WebHook
<br>
![WebHook](https://cdn.discordapp.com/attachments/1226145703877939250/1226147349542207578/image.png?ex=6623b5b4&is=661140b4&hm=ccba21c0b1a4d24634a9e32676684b645f3ca13b9d081f8d2f62a898efc20551&)
5. Clicke auf WebHook-URL kopieren
<br>
![WebHook-URL kopieren](https://cdn.discordapp.com/attachments/1226145703877939250/1226147835636875364/image.png?ex=6623b628&is=66114128&hm=f234f2e4446911f691ab647d04a841f0c3e92a6cd519079b13c470a5e77b5848&)

### WebHook im Script Configurieren
Um den WebHook nun im Admin System zu nutzen, musst du in der ``config.lua`` die Zeilen 5 und 6 bearbeiten.
```lua title='config.lua' linenums='5'
Config.ReportLogs = '' -- Alle neu erstellten reports
Config.ActionLogs = '' -- Alle aktionen die die Admins durchführen
```
Du kannst natürlich auch den Gleichen Webhokk für beides nutzen

## Commands
### Standart Commands

|Command            |info               |Nutung             |Group              |
|-------------------|-------------------|-------------------|-------------------|
|/support           |Ein ticket öffnen. |/support [anliegen]|User(keine Gruppe benötigt)|
|/sup               |Amdin Panel öffnen.|/sup               |admin              |
|/noadmin           |Toggle deine eigenen Notifications <br> => Nur die Admin notifications | /nodadmin| admin|

### Commands anpassen

Um die Commands zu ändern musst du in der ``config.lua`` die Zeilen 54 bis 56 bearbeiten.

```lua title='config.lua' linenums='54'
Config.UserCommand = 'support' -- Player will use /support [the problem they have]
Config.AdminCommand = 'sup' -- Open the adminpanel
Config.NoSupport = 'noadmin' -- toggle the admin Notifications
```