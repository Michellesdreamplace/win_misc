# Kurz und knapp Windows "verbessern":

----------------------

&nbsp;
&nbsp;
&nbsp;
&nbsp;

 ### WinUtil
 #### von [Chris Titus Tech](https://christitus.com/windows-tool)

 ##### In der Windows Powershell Console als Administrator ausführen:
 ```PowerShell
irm "https://christitus.com/win" | iex
 ```

&nbsp;
&nbsp;
&nbsp;
&nbsp;

----------------------

&nbsp;
&nbsp;
&nbsp;
&nbsp;


 ### ExplorerPatcher
 #### von [valinet](https://github.com/valinet/ExplorerPatcher)
 
 #### Dieses Projekt zielt darauf ab, die Arbeitsumgebung unter Windows zu verbessern.
 
 Lade die neueste Version des Setup-Programms [hier](https://github.com/valinet/ExplorerPatcher/releases/latest) herunter.
 * Wähle `ep_setup.exe` wenn dein Gerät einen Intel- oder AMD-Prozessor verwendet oder  `ep_setup_arm64.exe` wenn dein Gerät einen Snapdragon-Prozessor verwendet.


&nbsp;
&nbsp;
&nbsp;
&nbsp;

----------------------

&nbsp;
&nbsp;
&nbsp;
&nbsp;
 
 ### Entfernen der Windows Ai
 #### von [zoic!](https://github.com/zoicware/RemoveWindowsAI)
 
 ##### In der Windows Powershell Console als Administrator ausführen:
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1")))
 ```

 > [!WARNING]
 > Das Ausführen des Skripts mit PowerShell 7 wird nicht mehr unterstützt und verursacht Probleme, bitte sicherstellen, dass du Windows PowerShell (5.1) benutzt
 >
