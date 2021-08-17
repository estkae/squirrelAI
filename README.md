# squirrelAI


## Projektanleitung 5

----
<table>

<tr>
<td>Produktname:</td
<td>Eichhörnchen AI</td
<td>Version:</td
<td>V 2.2</td
</tr>

<tr>
<td>Autor:</td
<td>Yibin Zhang</td
<td>Aktualisierungsdatum:</td
<td>2018/10/13</td
</tr>

</table>


#### 一、制作背景

Im Zeitalter der Im-Proliferation wird die Kommunikation zwischen den Menschen immer bequemer, und man hat immer weniger Zeit und Raum für sich selbst. Jeden Tag sind Sie mit der Arbeit und dem Leben beschäftigt, und gleichzeitig müssen Sie eine Menge Energie aufwenden, um Nachrichten aus verschiedenen Szenarien zu bearbeiten.
Möchten Sie innehalten und eine Weile allein sein, ohne Anrufe oder Nachrichten, und "die Welt für einen Moment für sich spüren"?
WeChat ist aus dem Leben der chinesischen Nutzer nicht mehr wegzudenken; der größte Vorteil besteht darin, dass es die Menschen durch Peer-to-Peer-Instant-Messaging näher zusammenbringt. Diese Bequemlichkeit hat jedoch auch ein neues Problem mit sich gebracht: die "soziale Angst".
Squirrel AI ist ein Tool, das Ihnen helfen kann, die meisten Nachrichten zu bearbeiten, die Sie für unwichtig halten, ohne dabei zu "höflich" zu sein; und durch die Technologie der "Turing-Bots" kann es Ihnen auch mehr Gesellschaft in Ihrem Leben bieten.
![image](./image/squirrelAI.png)

Beispiel für die Nachricht:<br
! [image](. /image/msg.png)

#### II. Vielen Dank für Ihre Spende

Wenn Sie denken, dass "Squirrel Ai" ein interessantes Programm ist, und wenn Sie die Absicht haben, zu spenden, spenden Sie bitte an:<br>
1. alipay-Konto: 13067760265 <br>
2) WeChat-Nummer: zhyblx<br>
3. die Kartennummer der China Merchants Bank: 6214 8557 1279 0845<br>
4. die Kartennummer der Ping An Bank: 623058 000018 3696983<br>

Vielen Dank an die Einzelpersonen und Unternehmen, die gespendet haben.
<table>

<tr>
<td>Datum der Spende</td
<td>Name des Unternehmens (/der Einzelperson)</td
<td>Spendenbetrag</td
</tr>

<tr>
<td>2018-12-15</td
<td>Zhi Rang Händler für Dekorationsmaterial, Hangzhou Jiahao Jia Meiju Einkaufszentrum für Dekorationsmaterial</td
<td>¥500.0</td
</tr>

</table>



#### III. Prozessgestaltung

! [image](. /image/image.png)


#### IV. Schnittstellenbeschreibung

Das gesamte Squirrel AI-Projekt ist in zwei Schichten unterteilt: die Funktionsschicht und die Nutzungsschicht. <br>

*Funktionsschicht:<br

Die funktionale Schicht als Ganzes ist in drei Teile unterteilt, und zwar in die Entwurfsschicht (Basisschicht), die Anwendungsschicht (Anwendungsschicht) und die Funktionsschicht (AI-Funktionsschicht). <br>

a) Fundament (Basisschicht):
<table>
<tr
<td>Funktionen</td
<td>Pakete</td
<td>Klassen</td
<td>Methoden</td
<td>Parameter</td>
<td>Rückgabeart</td
<td>Beschreibung</td
</tr>
    
<tr>
<td>Schnittstellendefinition</td
<td>com.zhangyibin.foundation.wechatinterface;</td
<td>WechatSchnittstelle</td
<td>/</td>
<td>/</td>
<td>/</td>
<td>Definieren von Konstanten</td
</tr>
    
<tr>
<td>UUUID abrufen</td>
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>getUUID()</td
<td>/</td>
<td>String</td>
<td>Eigene Identifizierungsdaten für die Wechat-Anmeldung</td
</tr>

<tr
<td>QR-Code für die Anmeldung</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>QrCode anzeigen()</td
<td>/</td>
<td>/</td>
<td>Den QR-Code für die Anmeldung abrufen</td
</tr>

<tr>
<td>QR-Code anzeigen</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>QRCodeFrame</td
<td>QRCodeFrame()</td
<td>Dateipfad:QR-Code-Bildadresse</td
<td>/</td>
<td>Dimensionscode, der über ein Formular angezeigt wird</td
</tr>

<tr
<td>Anmeldung wartet</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>waitForLogin() ()</td>
<td>/</td>
<td>/</td
<td>Scannen des QR-Codes zur Überprüfung der Anmeldung</td
</tr>

<tr>
<td>Anmeldung wartet</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>anmelden()</td
<td>/</td>
<td>Boolean</td
<td>Anmeldung erfolgreich: true</td
</tr>

<tr>
<td>Initialisierung</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>wxInit()</td
<td>/</td
<td>Boolean</td
<td>Initialisierungsausnahme: gibt false zurück; funktioniert, um zu überprüfen, ob das Konto auf der schwarzen Liste von WeChat steht</td
</tr>

<tr
<td>Statusmeldung</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>wxStatusNotify()</td
<td>/</td>
<td>Boolean</td
<td>StatusNotifyMonitorException: gibt false zurück;</td
</tr>

<tr>
<td>Eine Liste von Freunden erhalten</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>Kontakt herstellen()</td
<td>/</td>
<td>Boolean</td
<td>Freundesliste erhalten fehlgeschlagen: return false;</td
</tr>

<tr>
<td>Überwachungsmeldungen</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>syncCheck()</td
<td>/</td>
<td>int</td>
<td>Aktion, ob der Inhalt der Nachricht eines Freundes abgerufen werden soll</td
</tr>

<tr>
<td>Senden Sie eine Nachricht</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>webwxsendmsg()</td
<td
String content:Inhalt der Nachricht
String an: den empfangenden Freund
</td>
<td>/</td>
<td>Nachrichtenzustellung handhaben</td
</tr>

<tr>
<td>Neueste Nachrichten</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>webwxsync()</td
<td>/</td>
<td>JSON</td
<td>Nachrichteninhalt abrufen</td
</tr>

<tr>
<td>Auf eine Nachricht antworten</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>handleMsg()</td
<td>JSONObject data:Nachrichteninhalt</td
<td>/</td>
<td>Einführung einer Antwort auf die Nachricht eines Freundes</td
</tr>

<tr
<td>Name der Benutzerkennung</td
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>BenutzermarkenName()</td
<td>String id:WeChatID</td
<td>String</td>
<td>GetUserRemarkName</td
</tr>

<tr
<td>Listener</td>
<td>com.zhangyibin.foundation.wechatapp;</td
<td>WechatApp</td
<td>listenMsgMode()</td
<td>/</td>
<td>/</td>
<td>Aufrechterhaltung der Netzverbindung</td
</tr>

<tr>
<td>Adressbuch der Freunde</td
<td>com.zhangyibin.foundation.util;</td
<td>Adressbuch</td>
<td>getAddressBookList()</td>
<td>JSONObject jsonObject:buddy list JSON</td
<td>/</td>
<td
1. eine Liste von Freunden erstellen<br
2. neue Freunde in die Datenbank einfügen
</td>
</tr>

<tr>
<td>Cookie-Informationen</td
<td>com.zhangyibin.foundation.util;</td
<td>CookieUtil</td
<td>getCookie()</td
<td>HttpRequest Anfrage:Http-Anfrage</td
<td>String</td
<td>Browser-Cookie-Informationen simulieren</td
</tr>


<tr>
<td>Fänger</td
<td>com.zhangyibin.foundation.util;</td
<td>Passstücke</td
<td>match()</td
<td
String p :regulärer Ausdruck
String str : Übereinstimmung mit String
</td>
<td>String</td>
<td>Verarbeitung von regulären Ausdrücken, die für den Anmeldevorgang bei WeChat verwendet werden</td
</tr>

<tr>
<td>Verbinden (Erstellen) einer Datenbank</td
<td>com.zhangyibin.foundation.databaseservice;</td
<td>CreateSQLiteService</td
<td>Haupt()</td>
<td>/</td>
<td>/</td>
<td>Verbinden (Erstellen) einer Datenbank</td
</tr>

<tr>
<td>Bibliothek für die Einfügung von Nachrichtendaten</td
<td>com.zhangyibin.foundation.databaseservice;</td
<td>EinfügenDienst</td
<td>getInsertService()</td
<td
String date:date
String name: Nutzername
String message: der Inhalt der Nachricht
</td
<td>/</td>
<td>Nachricht in die Datenbank eingefügt</td
</tr>

<tr>
<td>Bibliothek für die Einfügung von Nachrichtendaten</td
<td>com.zhangyibin.foundation.databaseservice;</td
<td>EinfügenDienst</td
<td>getInsertService()</td
<td
String strSql: die vollständige SQL-Anweisung
</td>
<td>/</td>
<td>Nachricht in die Datenbank eingefügt</td
</tr>

<tr>
<td>Abfragedienst</td
<td>com.zhangyibin.foundation.databaseservice;</td
<td>Dienst auswählen</td
<td>GetSelectService()</td
<td
String sql: die vollständige Select-Anweisung
</td>
<td>/</td>
<td>Datenabfrage</td>
</tr>

</table>


b) Anwendung (Anwendungsschicht):

<table>
<tr>
<td>Funktionen</td
<td>Pakete</td
<td>Klassen</td
<td>Methoden</td
<td>Parameter</td
<td>Rückgabeart</td
<td>Beschreibung</td
</tr>

<tr>
<td>Sonderkonto-Aufzählung</td
<td>com.zhangyibin.application.specialusers;</td
<td>SpecialUsersEnum</td
<td>GetNameList()</td
<td>/</td>
<td>String</td>
<td>AccountEnumerationList-Klasse (Liste der nicht antwortenden Nachrichten)</td
</tr>

<tr
<td>Aufzählungswerte in Liste umgewandelt</td
<td>com.zhangyibin.application.speciauserslist;</td
<td>SpecialUsersList</td
<td>getSpecialUsersList()</td
<td>/</td>
<td>Liste<String></td>
<td>Kontoaufzählungslistenklasse (Liste mit nicht antwortenden Nachrichten)</td
</tr>

<tr
<td>Launcher-Eintrag</td
<td>com.zhangyibin.application;</td
<td>StartWechatApp</td
<td>GETStartWechatApp</td
<td>/</td>
<td>/</td>
<td>Haupteingang des Programms ausführen</td
</tr>

</tabelle


c) aifunction (AI-Funktionsschicht):

<table>
<tr>
<td>Funktion</td
<td>Pakete</td
<td>Klassen</td
<td>Methoden</td
<td>Parameter</td
<td>Rückgabeart</td
<td>Beschreibung</td
</tr>

<tr>
<td>Roboteraufruf</td
<td>com.zhangyibin.aifunction;</td
<td>EichhörnchenAiRoboter</td
<td>EichhörnchenRoboter()</td
<td>String msg:Inhalt der Nachricht</td
<td>String</td>
<td>Aufruf der Turing-Bot-Schnittstelle (ohne auf die Nachrichtenliste zu antworten)</td
</tr>

</table>


*Benutzerebene:<br

Die Nutzungsschicht als Ganzes ist in zwei Teile unterteilt, für den Designtest (Test) und die Nutzung (Nutzungsschicht). <br>

<table>
<tr>
<td>Funktionen</td
<td>Pakete</td
<td>Klassen</td
<td>Methoden</td
<td>Parameter</td
<td>Rückgabeart</td
<td>Beschreibung</td
</tr>

<tr>
<td>Testcode</td
<td>com.squirrelAi.test;</td
<td>/</td>
<td>/</td>
<td>/</td>
<td>/</td>
<td>Engineering-Test-Code</td
</tr>

<tr>
<td>Eichhörnchen-KI starten</td
<td>com.squirrelAi.use;</td
<td>BenutzeEichhörnchenAi</td
<td>Hauptteil</td>
<td>/</td>
<td>/</td
<td>StartSquirrelAI,CallStartWechatApp Funktion</td
</tr>

</table>


#### IV. Versionierung

<table

<tr>
<td>Datum</td
<td>Versionsnummer</td
<td>Inhalt aktualisieren</td
<td>Bemerkungen</td
</tr>

<tr>
<td>2018.06.18</td
<td>V1.0</td
<td>
Funktionen gehen live
</td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr>

<tr>
<td>2018.08.03</td>
<td>V1.1</td>
<td>

a) Basisteil:<br
Implementierung einer WeChat-Imitation durch Scannen des QR-Codes des Kunden zur Anmeldung. <br>
Stellen Sie fest, dass sich das IOS-Gerät normal anmelden kann. <br>
Implementieren, um die Kontakte aus dem WeChat-Adressbuch zu erhalten. <br>
Implementieren, um Nachrichten von WeChat-Kontakten abzuhören. <br>
Implementieren Sie beantwortbare Freundschaftsnachrichten. <br>

b) Sitzungsfunktion:<br>
Implementieren Sie den Zugangs-Bot, um auf Nachrichten von Freunden zu antworten. <br>
Implementierung einer Blacklist-Funktion zum Blockieren von Antworten auf Buddy-Nachrichten. <br>
Die Funktion der schwarzen Liste umfasst das Blockieren von persönlichen, Chatgruppen- und öffentlichen Nachrichten von Freunden. <br>
Deaktivieren Sie die automatische Bot-Antwort und wechseln Sie zur manuellen Beantwortung der Nachrichten von Freunden. <br>

c) Erweiterte Funktionalität:<br>
Ermöglicht das lokale Speichern von Chat-Nachrichten. <br>
Implementieren Sie Testprogramm-Paketierung, Debugging kann Desktop ausgeführt werden. <br>

</td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr>

<tr>
<td>2018.08.16</td
<td>V1.2</td
<td>
Fügen Sie eine Whitelist-Funktionalität hinzu, um zwischen wichtigen Freunden, die eine manuelle Antwort auf Nachrichten geben, und unwichtigen Freunden, die eine Bot-Antwort auf Nachrichten geben, unterscheiden zu können. <br>
</td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr

<tr>
<td>2018.09.28</td
<td>V2.0</td
<td>Ersetzung von JDK11<br> </td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr>

<tr>
<td>2018.10.12</td
<td>V2.1</td
<td 
1. umbenanntes Projekt: Eichhörnchen-KI.<br 
2. Code-Refactoring; funktionale Schicht unterteilt in drei Teile: Basisschicht, Anwendungsschicht, AI-Funktionsschicht. <br
3. der Zugang zu Datenbankdiensten, die vollständige Speicherung von Nachrichten. <br>
4. ersetzen Sie das Web-Framework: blade-kit-1.3.4.jar

</td
<td
1. Web-Framework: blade-kit-1.3.4.jar<br>
2.JDBC: sqlite-jdbc-3.21.0.jar<br>
</td
</tr


<tr>
<td>2018.10.28</td
<td>V2.2</td
<td 
Aktualisierungen:<br>
Implementiert, um neue Freunde in die Datenbank aufzunehmen.
</td
<td>
--
</td
</tr>

</table>

Lokale Sicherung: /home/zhangyibin/documentation/Squirrel AI Sicherungsliste



