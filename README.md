# HB-UNI-Sen-DUMMY-BEACON-V2 mit Sniffer fuer AskSinAnalyzer
**Dummy-Device zum Vermeiden von "Kommunikation gestört"-Servicemeldungen von bis zu 16 inaktiven HomeMatic-Geräten (nur HM-RF, kein HmIP / Wired) mit integrierten Paketsniffer zur Nutzung mit dem AskSinAnalyzer oder AskSinAnalyzerXS.**<br/>

Das Geraet vereint zwei geniale Homematic-Helfer von Jérôme:

1. ![Den HB-UNI-Sen-DUMMY-BEACON-V2](https://github.com/jp112sdl/HB-UNI-Sen-DUMMY-BEACON-V2)
2. ![Den zum AskSinAnalyzer gehoerenden Sniffer](https://github.com/jp112sdl/AskSinAnalyzer)

Weitere Informationen finden sich auf den verlinkten Projektseiten.

Ziel der Zusammenfuehrung beider Geraete ist das Einsparen von Hardware, ggf. auch separater Netzteile. Ein ueblicher use case ist der ohnehin bestehende 24/7-Betrieb eines Raspberry Pi o.ae. Auf dem Pi kann unter anderem ein ![AskSinAnalyzerXS von Christoph](https://github.com/psi-4ward/AskSinAnalyzerXS) als ![Service](https://github.com/psi-4ward/AskSinAnalyzerXS/blob/master/docs/Install_as_Debian_Service.md) zur laufenden Ueberwachung des Homematic-Funkverkehrs und zur rudimentaeren Jamming-Erkennung laufen. Ueber den USB-Port des Pi wird in dem Fall eine rein als Sniffer arbeitende AskSinPP-Minimalschaltung oder eben auch ein ausgewachsener AskSinAnalyzer mit Display versorgt und liefert gleichzeitig die empfangenen Funktelegramme an den AskSinAnalyzerXS.

 Benoetigt man nun ausserdem einen Dummy Beacon zur Vermeidung von Kommunikationsstoerungsmeldungen bei saisonal nicht in Betrieb befindlichen Geraeten wie Weihnachtsbeleuchtungen, kann statt des originaeren Sniffer-Sketches einfach der hier vorgestellte Sketch geflasht und das Geraet als HB-UNI-Sen-DUMMY-BEACON-V2 an die CCU angelernt werden. Beide Funktionen stehen nun zur Verfuegung und es wird keine weitere Hardware benoetigt.  

 Natuerlich kann der Analyzer dann keine Pakete empfangen, die der Dummy Beacon gesendet hat. Dies sollte in den meisten Anwendungsfaellen jedoch unproblematisch sein.


Damit das Gerät von der CCU erkannt und unterstützt wird, ist es erforderlich, das [JP-HB-Devices-addon](https://github.com/jp112sdl/JP-HB-Devices-addon) zu installieren.<br/>Es wird mindestens Version 3.3 benötigt.
