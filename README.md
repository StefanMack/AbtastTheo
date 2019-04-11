# Das Abtasttheorem und die sinc-Interpolation mit Python Skripten nachvollziehen und verstehen  

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/StefanMack/AbtastTheo/master)

> Hinweis: Wenn Sie oben im File Explorer auf eine der beiden Jupyter Notebooks (Endung ".ipnyb") klicken, dann wird lediglich ein Viewer geöffnet, in dem Sie das Notebook nur anschauen können. Dieser Viewer funktioniert nicht immer zuverlässig.  
Daher verwenden Sie zum Anschauen der Notebooks besser den Viewer "nbviewer" [über diesen Link](https://nbviewer.jupyter.org/github/StefanMack/AbtastTheo/tree/master/).
Möchten Sie die Codebeispiele darin einzeln ausführen und ändern, dann klicken Sie bitte auf das Icon "launch|binder". **Das Starten des Webservice binder kann bis zu einer Minute dauern.**


Es gibt viele verschiedene Formulierungen des Abtasttheorems -oder wie man es auch nennt- des Nyquist-Shannon-Abtasttheorems. Eine gängige Formulierung ist folgende - die Abkürzung B steht hier für den Begriff Bandbreite:

**"Wenn ein Signal Frequenzen bis B Hz enthält, dann muss es mit einer Frequenz von mehr als 2 mal B Hz abgetastet werden, damit keine Information verloren geht."**

In Wikipedia ist folgende Formulierung zu lesen:  
**"Wenn ein Signal keine Frequenzanteile größer B Hz enthält, dann kann es aus einer Folge von äquidistanten Abtastwerten exakt rekonstruiert werden kann, wenn es mit einer Frequenz von größer als 2 mal B abgetastet wurde."**  


Letztlich steckt in dieser Aussage das Erfolgsgeheimnis der Digitalisierung: Wenn man die Bandbreite eines Signals kennt, dann kann auf einen Großteil der Signaldaten verzichtet werden. Im Rundfunk nennt man so etwas digitale Dividende - auf einem ehemals analogen Fernsehkanal werden heute eine Vielzahl digitale Sender übertragen.

**Kann man das Abtasttheorem auch beweisen? Hierbei stellen sich zwei getrennte Fragen:**
* Steckt wirklich die komplette Information des Signals in den Abtastwerten. Bzw. wieso geht Information verloren, wenn mit der Frequenz 2 mal BW Hz oder langsamer abgetastet wird?
* Wie kann man aus den Abtastwerten das Signal wieder so rekonstruieren, ohne dass beispielsweise bei einem Sinussignal auf einmal Kanten im rekonstruierten Signalverlauf auftauchen?

#### Im Jupyter Notebook hierzu wird zuerst gezeigt, wieso eine sogenannte Unterabtastung mit 2 mal B Hz oder weniger zu einem Informationsverlust führt. Weiter wird darauf eingegangen, wie man ein mit wenig mehr als 2 mal B Hz abgetastetes Signal wieder originalgetreu rekonstruiert - die sogenannte "sinc-Interpolation", welche z.B. auch bei Oszilloskopen verwendet wird.
