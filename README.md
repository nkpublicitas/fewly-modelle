# fewly-modelle

Modelle für die Erkennung von Personen und Tieren in der iPhone-App Fewly. Die App lädt sie einmal nach dem Ja des Nutzers und rechnet danach alles auf dem Gerät. Nichts wird hochgeladen.

Die Modelle liegen als Core-ML-Dateien in den Releases (`modelle-<Fassung>`). Ein `.mlpackage` ist ein Ordner, ein Release kennt keine Ordner: Jede Datei hat darum einen flachen Namen (`<modell>__<Pfad mit __ statt />`). Die App kennt die Liste der Dateien samt SHA-256 fest im Code und prüft jede Datei nach dem Laden. Ein Release wird nie überschrieben, eine neue Fassung bekommt einen neuen Tag.

| Modell | Quelle | Lizenz |
|---|---|---|
| AuraFace (glintr100, Gesichts-Fingerabdruck, 512 Zahlen) | [fal/AuraFace-v1](https://huggingface.co/fal/AuraFace-v1) | Apache 2.0 |
| D-FINE M (findet Hunde und Katzen als Rahmen) | [ustc-community/dfine-medium-obj2coco](https://huggingface.co/ustc-community/dfine-medium-obj2coco) | Apache 2.0 |
| SigLIP 2 (Bildhälfte, prüft Ausschnitte und gibt den Fingerabdruck eines Tiers) | [google/siglip2-base-patch16-256](https://huggingface.co/google/siglip2-base-patch16-256) | Apache 2.0 |

Geändert gegenüber den Quellen: nach Core ML umgewandelt (coremltools), Gewichte auf 16 oder 8 Bit gebracht, Bildeingabe mit fester Normierung eingebaut. Die Gewichte sind sonst unverändert.

Der Lizenztext steht in `LICENSE`.
