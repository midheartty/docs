---

copyright:
  years: 2016, 2017
lastupdated:  "2017-02-17"

---

#	Professional Per Capacity-Plan verwenden
{: #using_mobilefoundation_p4}

Mit dem Professional Per Capacity-Plan können Benutzer eine beliebige Anzahl von mobilen Anwendungen mit mehreren mobilen Betriebssystemen erstellen.
Nach der Erstellung der Serviceinstanz von {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity lesen Sie die folgende Prozedur, um die Arbeit mit dem Service zu beginnen.

## Voraussetzungen
{: #prerequisites_p4}

Beachten Sie Folgendes, bevor Sie die Serviceinstanz von {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity konfigurieren.
* {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity wird nur von {{site.data.keyword.dashdbshort_notm}}: Enterprise Transactional (Unterstützung für OLTP) {{site.data.keyword.Bluemix_notm}}-Plänen unterstützt.

* Sie benötigen Zugriff auf die Berechtigungsnachweise der {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz, bevor Sie die Einstellungen für die {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz konfigurieren.

**Hinweis**: Die {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz kann sich in jedem `Bereich` in Ihrer {{site.data.keyword.Bluemix_notm}}-`Organisation` bzw. in jeder anderen `Organisation`, auf die Sie zugreifen können, befinden. Stellen Sie sicher, dass Sie über die Berechtigungen für den Zugriff auf den `Bereich` verfügen, in dem sich die {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz befindet.


## Datenbankverbindung hinzufügen
{: #configure_dashdb_p4}

###  Erste Schritte
{: #firststeps_p4}

Führen Sie nach der Erstellung der Serviceinstanz von {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity die beschriebene Prozedur aus, um mit der Verwendung des Service zu beginnen.

### Verbindung zur dashDB-Serviceinstanz herstellen
{: #connect_dashdb_p4}

Nachdem die Serviceinstanz von {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity erstellt wurde, sehen Sie die Seite *Übersicht*, auf der Sie die Verbindungsinformationen für die Serviceinstanz von {{site.data.keyword.dashdbshort_notm}} for Transactions angeben müssen, zu der die {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz eine Verbindung herstellen soll.

**Hinweis:** Wenn Sie bereits über eine Serviceinstanz von {{site.data.keyword.dashdbshort_notm}} for Analytics: Enterprise for Transactions verfügen, können Sie diese verwenden, um die Verbindung zur {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz herzustellen.

Sie können auch eine neue Serviceinstanz von {{site.data.keyword.dashdbshort_notm}} for Transactions erstellen, falls noch keine vorhanden ist.

Führen Sie die folgenden Schritte aus, um eine neue dashDB for Transactions-Serviceinstanz zu erstellen:

1. Wählen Sie auf der Seite *Übersicht* den Abschnitt **Neuen Service erstellen** aus.

+ Wählen Sie `Ja` für die Option **Hochverfügbarkeitskonfiguration** aus, wenn Sie eine hochverfügbare Serviceinstanz von {{site.data.keyword.dashdbshort_notm}} for Transactions benötigen.

+ Prüfen Sie die Plandetails und klicken Sie auf **Erstellen**.

Eine neue Serviceinstanz von {{site.data.keyword.dashdbshort_notm}} for Transactions: EnterpriseForTransactions2.8.500 wird erstellt, die eine dedizierte {{site.data.keyword.dashdbshort_notm}}-Instanz mit 8 GB RAM und 2 vCPUs sowie mit 500 GB Speicher bereitstellt.

Führen Sie die folgenden Schritte aus, um die Verbindung zu einer vorhandenen {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz oder zu der Serviceinstanz von {{site.data.keyword.dashdbshort_notm}} for Transactions herzustellen, die Sie gerade erstellt haben:

1. Wählen Sie die {{site.data.keyword.Bluemix_notm}} `Organisation` aus, in der sich die {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz befindet.

+ Wählen Sie den {{site.data.keyword.Bluemix_notm}}-`Bereich`, in dem sich die {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz befindet, in der Liste der Bereiche aus, die in der ausgewählten `Organisation` verfügbar sind.   
**Hinweis:** Wenn die `Organisation` und der `Bereich`, in denen sich Ihre {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz befindet, nicht aufgeführt sind, prüfen Sie, ob Sie ein Mitglied der betreffenden `Organisation` bzw. des betreffenden `Bereichs` sind. Sie benötigen die Zugriffsrolle *Entwickler* für die Organisation und den Bereich, da der {{site.data.keyword.mobilefoundation_short}}-Service über den {{site.data.keyword.dashdbshort_notm}}-Service auf die Berechtigungsnachweise zugreift.

+ Wählen Sie den `Servicenamen` und die `Berechtigungsnachweise` für {{site.data.keyword.dashdbshort_notm}} aus, um eine Verbindung zur vorhandenen {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz herzustellen.

+  Testen Sie die Verbindung zur angegebenen {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz.

+  Klicken Sie auf **Hinzufügen**. Mit dieser Aktion werden die erforderlichen Tabellen in der konfigurierten {{site.data.keyword.dashdbshort_notm}}-Datenbankserviceinstanz erstellt.

Nach einigen Sekunden können Sie auf die Seite `Übersicht` zugreifen, auf der die Lernprogramme und Videos zur Verfügung stehen, die Sie beim Einstieg in die Verwendung des {{site.data.keyword.mobilefoundation_short}}-Service unterstützten.

**Hinweis**: Sie können die {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz, die zur Verwendung durch die {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz konfiguriert ist, nicht ändern. Sie können jedoch dieselbe {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz für mehrere {{site.data.keyword.mobilefoundation_short}}-Serviceinstanzen verwenden, da jede {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz ein eigenes Schema in der ausgewählten {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz erstellt.

## MobileFirst-Server starten
{: #start_mobilefoundation_p4}

* Um den {{site.data.keyword.mfserver_short_notm}} mit den Standardeinstellungen zu starten, klicken Sie auf **Basisserver starten**.

* Diese Auswahl stellt einen {{site.data.keyword.mfserver_long_notm}} mit den folgenden Einstellungen bereit:
    -  2 Knoten mit jeweils 1 GB Hauptspeicher. Diese Größe ist für Entwicklungs- und kleinere Testaktivitäten sowie für kleinere Produktionsworkloads ausreichend.

    -	`Benutzername` und `Kennwort` werden automatisch für Sie generiert. Sie können darauf zugreifen, wenn der Server betriebsbereit ist.

Der Prozess der Bereitstellung Ihres Servers wird gestartet. Dieser Prozess dauert ungefähr 10 Minuten;
in einem Nachrichtenfenster wird der Fortschritt dieser Operation angezeigt. Ist der Vorgang abgeschlossen, wird ein Dashboard mit folgenden
Informationen angezeigt:

  -	Status Ihres Servers, der ausgeführt wird (Zustand, Größe).

  -	Für Sie erstellte Serverroute. Verwenden Sie diese Route in Ihrer mobilen Anwendung, um eine Verbindung zum {{site.data.keyword.mfserver_short_notm}} herzustellen.

  -	Ihr persönlicher `Benutzername` und das `Kennwort` für den Zugriff auf die {{site.data.keyword.mfp_oc_short_notm}}. Das `Kennwort` wird ausgeblendet. Klicken Sie auf das Symbol **Kennwort anzeigen**, um es einzublenden.

*	Klicken Sie auf **Konsole starten**, um die {{site.data.keyword.mfp_oc_short_notm}} zu öffnen.


<!--This console runs inside the container.--> Mit der Konsole können Sie Ihre mobilen Apps, Adapter und Geräte verwalten, Ihren Server als mobiles Back-End verwenden, Push-Benachrichtigungen senden usw.

##  Mobile Analytics-Server hinzufügen
{: #adding_analytics_server_p4}

 Sie können Ihre mobile Anwendung nun auf dem {{site.data.keyword.mobilefirst}}-Server überwachen, indem Sie einen Mobile Analytics-Server zur Instanz des Service {{site.data.keyword.mobilefoundation_short}} hinzufügen.

 Durch den professionellen Plan wird der Mobile Analytics-Server in einer Containergruppe erstellt; der Benutzer kann die Konfiguration durch Auswahl der Anzahl von Containerknoten in der Containergruppe anpassen.

 Benutzer können auch Datenträger an die Container anhängen, um Daten dauerhaft zu speichern. Wird ein Datenträger einmal ausgewählt, kann er nicht mehr geändert werden. 20 GB Speicherplatz für die Dateifreigabe stehen dem Benutzer standardmäßig zur Verfügung. Benötigt der Benutzer zusätzlichen Speicherplatz, um die Analysedaten dauerhaft zu speichern, muss er weiteren Speicherplatz für die Dateifreigabe erwerben und mit dieser Dateifreigabe einen Datenträger erstellen. Anschließend kann er diesen neuen Datenträger auswählen und den Analyseserver bereitstellen.

 Weitere Informationen zum Hinzufügen von Datenträgern zu {{site.data.keyword.containerlong}} finden Sie im Abschnitt zum [Speichern persistenter Daten auf einem Datenträger mit dem {{site.data.keyword.Bluemix_notm}}-Dashboard ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.ng.bluemix.net/docs/containers/container_volumes_ov.html#container_volumes_ui.html){: new_window}.

* Klicken Sie auf die Option zum Hinzufügen der Analyse, um den Mobile Analytics-Server zur Instanz des {{site.data.keyword.mobilefoundation_short}}-Service hinzuzufügen.

* Sie können die Mobile Analytics-Serverkonfiguration verwenden; die unterstützte Mindestkonfiguration für den Analytics-Server sind 2 Knoten mit jeweils 1 GB Hauptspeicher; Sie können einen Analytics-Server bis zu einer Maximalkonfiguration von 32 Knoten mit jeweils 16 GB Hauptspeicher erstellen.

Der Prozess der Bereitstellung wird gestartet. Dieser Prozess dauert ungefähr 10 Minuten; in einem Nachrichtenfenster wird der Fortschritt dieser Operation angezeigt.  

* Starten Sie die MobileFirst Analytics Console über die {{site.data.keyword.mfp_oc_short_notm}}.

* Für den {{site.data.keyword.mfserver_short_notm}} und den Mobile Analytics-Server ist Single Sign-on aktiviert. Der Mobile Analytics-Server ist mit denselben LTPA-Schlüsseln und denselben Benutzerberechtigungen konfiguriert wie der {{site.data.keyword.mfserver_short_notm}}-Server. Sie können für die Anmeldung an der Mobile Analytics Console den `Benutzernamen` und das `Kennwort` verwenden, die Sie auch für die Anmeldung bei der {{site.data.keyword.mfp_oc_short_notm}} verwendet haben.

Weitere Informationen zu MobileFirst Analytics finden Sie unter [MobileFirst Foundation Operational Analytics ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://mobilefirstplatform.ibmcloud.com/tutorials/en/foundation/8.0/analytics/){: new_window}.

**Anmerkung:** Der Mobile Analytics-Server wird entfernt, wenn Sie die Instanz des Service {{site.data.keyword.mobilefoundation_short}} löschen oder wenn Sie versuchen, den {{site.data.keyword.mfserver_short_notm}} erneut zu erstellen.

##  Mobile Analytics-Server löschen
{: #deleting_analytics_server_p4}

Sie können jetzt den Mobile Analytics-Server, der zur {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz hinzugefügt wurde, im {{site.data.keyword.mobilefoundation_short}}-Service-Dashboard löschen.

* Klicken Sie auf die Option zum Löschen der Analyse****, um den Mobile Analytics-Server zu löschen, der zur {{site.data.keyword.mobilefoundation_short}}-Serviceinstanz hinzugefügt wurde.

 Bei dieser Aktion wird die Analytics-Containergruppe gelöscht. Das Löschen der Analytics-Container dauert ca. 10 Minuten. Sie können die Anzeige aktualisieren, um den aktuellen Status anzuzeigen. Nach dem Löschen der Analysecontainer wird die Schaltfläche zum Hinzufügen der Analyse**** wieder aktiviert und kann verwendet werden, um den Mobile Analytics-Server bei Bedarf erneut hinzuzufügen.

## MobileFirst-Server erneut erstellen
{: #recreate_mobilefoundation_p4}

*	Klicken Sie auf die Schaltfläche **Neu erstellen**, um den Server erneut zu erstellen.

* Diese Aktion stoppt Ihre vorhandenen Server und löscht die Daten. Eine neue Serverinstanz wird mit einer aktualisierten Version erstellt, falls verfügbar. Diese Aktion nimmt einige Minuten in Anspruch.

**Hinweis**: Alle Daten der vorherigen Serverinstanz, einschließlich Informationen zu den Apps und Adaptern, werden in der konfigurierten {{site.data.keyword.dashdbshort_notm}}-Serviceinstanz beibehalten; diese Daten werden zur erneuten Erstellung des Servers verwendet.

##	Erweiterte Konfiguration einrichten
{: #using_mfs_advanced_p4}

Mit der Option **Server mit erweiterter Konfiguration starten** auf der Seite `Übersicht` können Sie einen Server mit erweiterten oder benutzerdefinierten Einstellungen erstellen. Sie können die
Servereinstellungen auch aktualisieren, um Ihre Serverkonfiguration anzupassen; klicken Sie hierfür auf die
Registerkarte **Konfiguration**. {{site.data.keyword.mobilefoundation_short}} bietet Ihnen Zugriff auf einige erweiterte Einstellungen.

*	Auf der Registerkarte **Topologie** können Sie die Servergröße und die Anzahl der Serverinstanzen auswählen, die den jeweiligen Anforderungen entsprechen. Die Standardgröße von 1 GB für den Server ist für die Entwicklung und kleinere Tests ausreichend.
  - Wählen Sie in Abhängigkeit von Ihrem Bedarf die richtige Größe für Ihren Server aus.

  - **Knoten** zeigt die Anzahl der erstellten Knoten an.

      - Die {{site.data.keyword.mobilefirst}}-Server-Farm kann durch die Konfiguration der Anzahl der Knoten hier unterstützt werden. Die unterstützte Mindestkonfiguration sind 2 Knoten mit jeweils 1 GB Hauptspeicher, die unterstützte Höchstkonfiguration sind 32 Knoten mit jeweils 16 GB Hauptspeicher.

Weitere Details finden Sie in der [{{site.data.keyword.mobilefoundation_long}}-Dokumentation ![Symbol für externen Link icon](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/support/knowledgecenter/SSHS8R_8.0.0/wl_welcome.html){: new_window}.
