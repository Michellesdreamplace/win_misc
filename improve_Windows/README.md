# Kurz und knapp Windows "verbessern":

 
 ### Entfernen der Windows Ai
 
 #### Von der Powershell Console als Administrator aus ausführen
 ---

 > [!WARNING]
 > Das Ausführen des Skripts mit PowerShell 7 wird nicht mehr unterstützt und verursacht Probleme, um sicherzustellen, dass Sie Windows PowerShell (5.1) ausführen
 >

 ### Starten mit UI
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1")))
 ```


