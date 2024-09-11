# Használt parancsok

`find /home/anon/Projects/Downloaded/gyires.inf.unideb.hu/KMITT/c12/ -name '*.html' -exec sed -i "s@ISO-8859-1@utf-8@g" {} +`

`wget -r -np -k --no-check-certificate --content-disposition "https://gyires.inf.unideb.hu/KMITT/c12/index.html"`


-------

Az `-exec sed -i "s@ISO-8859-1@utf-8@g" {} +` rész kicserélte az összes ISO... kódolású karaktert utf-8-ra. Azonban ez nem volt elég, az egyes furcsább, pl \371 kódolású karaktereket is lekellett cserélni.
