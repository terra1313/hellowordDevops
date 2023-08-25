# OmniView
OmniView ist eine universelle GUI um die Messgeräte der Forschungskooperation AW4null anzuzeigen. 
Mehr Informationen über AW4null finden sich unter [[www.autowerkstatt40.org](https://www.autowerkstatt40.org/)].

## Prototype 
Ein Prototype der Software befindet sich in [[www.figma.com](https://www.figma.com/file/daQFBzV59T8xOlL4JXXwBG/OmniView?type=design&node-id=0%3A1&t=8xcLaxbuGwCj4EBE-1)](FIGMA). Nach einem Klick auf den Link, muss die Einsicht erst von @bjoekeldude freigegeben werden.
Der Prototype wird kontinuierlich geupdated und soll das Entwicklungsergebnis visualisieren. 
Die konkreten Entwicklungsschritte werden im  [Projektplan](https://github.com/orgs/skunkforce/projects/1/views/1?pane=issue&itemId=30039286) festgehalten, welcher von @markuskae gepflegt wird.

## Hilfe und Onboarding
Auf [https://moodle.aw4null.de/] (unserer Lernplattform) finden sich weitere Hilfen und Ressourcen zum aw4null Projekt. Ansprechpartner ist @wasilina83 

## Teilnehmen und Mitarbeiten
## Buildstatus
![example workflow](https://github.com/skunkforce/omniview/actions/workflows/build.yaml/badge.svg)


## Buildprozess Linux
ins OmniView Verzeichnis wechseln

submodule updaten und initalisieren:
```shell
git submodule update --init --recursive
```
buildordner erstellen:
```shell
mkdir build
```

in den buildordner navigieren:
```shell
cd build
```
cmake ausführen:
```shell
cmake ..
```

make ausführen:
```shell
cmake --build .
```


OmniView ausführen:
```shell
Sudo ./OmniView
```

OmniView funktioniert auch ohne den Sudobefehl. Noch kann die Software aber so nicht mit angeschlossenen Omniscopes kommunizieren.

## Buildprozess Windows
ins OmniView Verzeichnis wechseln

submodule updaten und initalisieren:
```shell
git submodule update --init --recursive
```

buildordner erstellen:
```shell
mkdir build
```

in den buildordner navigieren:
```shell
cd build
```

cmake ausführen:
```shell
cmake .. -DVCPKG_TARGET_TRIPLET="x64-windows-static"
```

make ausführen:
```shell
cmake --build .
```
Die Executable landet nicht in '/omniview/build/', sondern in '/omniview/build/debug/'.
Sie muss momentan nach '/omniview/build/' verschoben werden, damit die Pfade stimmen.

