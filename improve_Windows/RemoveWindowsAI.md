# Entfernen der Windows Ai
## Warum?
Der aktuelle 25H2 Build von Windows 11 und zukünftigen Builds wird immer mehr KI-Funktionen und Komponenten enthalten. Dieses Skript zielt darauf ab, ALLE diese Funktionen zu entfernen, um die Benutzerfreundlichkeit, Privatsphäre und Sicherheit zu verbessern.

### [Erklärendes YouTube von WindowsArea](https://www.youtube.com/watch?v=RuqA9fgyEDY)

### [ORIGINAL Github von zoic!](https://github.com/zoicware/RemoveWindowsAI)



----------------------



### Skript-Funktionen
 - **Registrierungsschlüssel deaktivieren** 
   - Copilot deaktivieren
   - Rückruf deaktivieren
   - Deaktivieren Sie Input Insights und Tippen von Datenerfassung
   - Copilot in Edge
   - KI-Experimente-Programm in Paint deaktivieren
   - AI Fabric Service entfernen
   - KI-Aktionen deaktivieren
   - Sprachzugriff Deaktivieren
   - KI-Spracheffekte deaktivieren
   - KI in Einstellungen deaktivieren Suche
   - Gaming Copilot deaktivieren
   - Copilot in allen Office-Apps deaktivieren
   - KI-Funktionen in der Fotos-App deaktivieren
   - Deaktivieren Klicken Sie zum Tun in Snipping Tool
 - **Verhindern Sie die Neuinstallation von KI-Paketen**
   - Installiert benutzerdefiniertes Windows Update-Paket, um die Neuinstallation von KI-Paketen im CBS (Component-Based Servicing) Store zu verhindern 
 - **Copilot-Richtlinien deaktivieren** 
   - Deaktiviert Richtlinien in Bezug auf Copilot und Recall in IntegratedServicesRegionPolicySet.json 
 - **AI Appx-Pakete entfernen**
   - Entfernt alle AI Appx-Pakete einschließlich `Nonremovable` Pakete und WindowsWorkload 
 - **Optionale Funktion von Recall entfernen**
 - **Entfernen von KI-Paketen in CBS**
   - Dadurch werden versteckte und gesperrte KI-Pakete im CBS (Component-Based Servicing) Store entfernt
 - **AI-Dateien entfernen**
   - Dadurch wird eine vollständige Systembereinigung durchgeführt, die alle verbleibenden KI-Installationsprogramme, Registrierungsschlüssel und Paketdateien entfernt
 - **AI-Komponenten ausblenden**
   - Dadurch wird die Einstellungsseite ausgeblendet `AI Components` 
 - **KI-Funktion im Editor deaktivieren**
 - **Recall-Aufgaben entfernen**
   - Entfernt gewaltsam alle Instanzen der geplanten Aufgaben von Recall
  - **Update Cleanup Check**
     - Erstellt eine geplante Aufgabe, um zu überprüfen, ob Windows aktualisiert wurde und ob es vorhanden ist, werden neu installierte KI-Funktionen entfernt

 - #### Installieren Sie klassische Apps
   - Mit diesen Optionen können Sie die modernen KI-befallenen Apps durch ihre klassische Version ersetzen
   - **Optionen:** Ersetze Editor, Paint, Snipping Tool, Photo Viewer, und Installiere Photos Legacy 
 
#### Manuelle KI-Deaktivierung
- Leider können nicht alle Funktionen und Einstellungen über ein Skript deaktiviert werden. Dieser Leitfaden zeigt zusätzliche KI-Funktionen zum Deaktivieren an.
> **[Andere KI-Funktionen deaktivieren](https://github.com/zoicware/RemoveWindowsAI/blob/main/OtherAIFeatures.md)**
  
### Lesen Sie hier die Script Docs
  > **[Dokumentation](https://github.com/zoicware/RemoveWindowsAI/blob/main/Documentation.md)**

  > [!WARNING]
  > Einige Antivirenprogramme von Drittanbietern werden das Skript fälschlicherweise als bösartig erkennen, offensichtlich ist dies falsch positiv und das Antivirenprogramm muss vorübergehend deaktiviert oder das Skript als Ausschluss festgelegt werden.
  >
  > Aufgrund der Art der fortgeschrittenen Änderungen am System werden viele Debloat-Tools / Skripte fälschlicherweise als Malware erkannt... wenn Sie sich über das Skript nicht sicher sind, empfehle ich immer, zuerst Software in einer virtuellen Maschine zu testen

---


 ### Wie zu verwenden
 
 #### Von der Powershell Console als Administrator aus ausführen
 ---

 > [!WARNING]
 > Das Ausführen des Skripts mit PowerShell 7 wird nicht mehr unterstützt und verursacht Probleme, bitte sicherstellen, dass du Windows PowerShell (5.1) benutzt
 >

 ### Starten mit UI
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1")))
 ```


 <details>  
  <summary>Klicken, um die Benutzeroberfläche anzuzeigen</summary>
  <img width="586" height="693" alt="Capture2" src="https://github.com/user-attachments/assets/fa105ba5-c1dc-447c-ae2e-7ee373291042" />
  <img width="586" height="693" alt="Capture2" src="https://github.com/user-attachments/assets/8a446a23-7c47-468e-856b-1e783205c511" />
</details>  

&nbsp;

### Befehlszeilenoptionen

**Ausführen im nicht-interaktiven Modus mit allen Optionen**
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1"))) -nonInteractive -AllOptions
 ```

--- 

**Mit spezifischem Optionsbeispiel ausführen**
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1"))) -nonInteractive -Options DisableRegKeys,RemoveAppxPackages,DisableCopilotPolicies 
 ```

**Alle Möglichen Optionen:**
```
DisableRegKeys          
PreventAIPackageReinstall     
DisableCopilotPolicies       
RemoveAppxPackages        
RemoveRecallFeature 
RemoveCBSPackages         
RemoveAIFiles               
HideAIComponents            
DisableRewrite      
RemoveRecallTasks
UpdateCleanupCheck
```

**Installieren Sie Klassische Apps**
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1"))) -nonInteractive -InstallClassicApps photoviewer,mspaint,snippingtool,notepad  
 ```

**Alle Möglichen Optionen:**
```
photoviewer          
mspaint     
snippingtool       
notepad        
photoslegacy 
```


**Mit aktiviertem Backup-Modus ausführen**

> [!NOTE]
> Der Sicherungsmodus muss aktiviert sein, um vollständig zurückkehren zu können
> 
 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1"))) -nonInteractive -backupMode -AllOptions
 ```

---

**Änderungen rückgängig machen**

 ```PowerShell
 & ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1"))) -nonInteractive -revertMode -AllOptions
 ```

---



### YT Guide
#### [How to Remove ALL Windows AI Features - zoic!](https://youtu.be/j5_eEBWGHFw)
