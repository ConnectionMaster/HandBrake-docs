---
Type:            article
Title:           Inhaltsverzeichnis
Project:         HandBrake
Project_URL:     https://handbrake.fr/
Project_Version: 1.1.0
Language:        Deutsch
Language_Code:   de
Authors:         [ Bernhard Rader (raderb) ]
Copyright:       2024 HandBrake Team
License:         Creative Commons Attribution-ShareAlike 4.0 International
License_Abbr:    CC BY-SA 4.0
License_URL:     https://handbrake.fr/docs/license.html
---

Inhaltsverzeichnis
=================

## Einführung

- [Quick Start](introduction/quick-start.markdown)
  *Lernen in ein paar Minuten dein erstes Video zu erstellen*
- [Über HandBrake](introduction/about.markdown)
  *Was ist HandBrake, was kann es, und was kann es nicht*


## HandBrake herunterladen

- [Wo kann ich HandBrake herunterladen](get-handbrake/where-to-get-handbrake.markdown)
  *Die offiziell unterstütze Version*
- [HandBrake herunterladen und installieren](get-handbrake/download-and-install.markdown)
  *Wie du HandBrake auf deinen Computer bringst*
- [Nach Updates suchen](get-handbrake/check-for-updates.markdown)
  *Bleib up-to-date mit den neuesten Features und Fehlerbehebungen*


## Videos erstellen

- [Öffnen einer Video Quelldatei](workflow/open-video-source.markdown)
  *Wie du deine Videos in HandBrake importierst*
- [Eine Voreinstellung auswählen](workflow/select-preset.markdown)
  *Zugeschnittene Einstellungen für sofortige Kompatibilität mit vielen Geräten*
- [Qualitätseinstellungen](workflow/adjust-quality.markdown)
  *Einfach die visuelle Qualität erhöhen oder Dateigrößen reduzieren*
- [Deine Einstellungen testen](workflow/preview-settings.markdown)
  *Sehe wie dein Video in einer kurzen Zeitspanne aussehen würde*
- [Kodierung starten](workflow/start-encoding.markdown)
  *Starte die Kodierung deines neuen Videos mit einem Klick*


## Fortgeschrittene Workflows

- [Die Warteschlange verwenden](advanced/queue.markdown)
  *Richte mehrere Kodierungsjobs auf einmal ein*
- [Punkt zu Punkt Kodierung](advanced/point-to-point.markdown)
- [Benutzerdefinierte Voreinstellungen](advanced/custom-presets.markdown)
- [Audio und Untertitel Standardeinstellungen](advanced/audio-subtitle-defaults.markdown)
- [Video Größenänderung](advanced/resizing-video.markdown)
- [Surround Sound beibehalten](advanced/surround-sound.markdown)
- [Untertitel hinzufügen](advanced/subtitles.markdown)
- [Kapitelmarkierungen hinzufügen](advanced/chapter-markers.markdown)

<!-- - [Managing Audio Tracks](advanced/managing-audio.markdown) -->
<!-- - [Post-processing metadata](advanced/post-processing.markdown) -->


<!-- ## Restoration and enhancement

- Common video problems
  - Cropping, Black bars at top/bottom or sides
  - Combing effects caused by interlacing or telecine
    - Detelecine filter
    - Decomb filter vs. Deinterlace filter
    - Bob mode and frame rates, motion
  - Noise (grainy appearance and/or color splotches)
    - Denoise filters: NLMeans and HQDN3D
  - Blocky picture
    - Deblock filter
  - Stretched picture (too wide or too tall)
    - Scaling and anamorphic
- Common audio problems
  - Volume level too low
  - Dynamics too wide (soft whispers, loud booms)
-->

<!-- ## Advanced workflows part 2

- [Understanding source types](advanced/video-sources.markdown)
- [Selecting a container format and encoders](advanced/containers.markdown)
- [Selecting a video angle](advanced/video-angles.markdown)
- [Working with frame rates](advanced/frame-rates.markdown)
- [Adjusting audio quality](advanced/audio-quality.markdown)
- [Progressive download support](advanced/web-optimised.markdown)
- [Compatibility with legacy devices](advanced/old-ipod-support.markdown)
- [Automatically naming files](advanced/automatic-file-naming.markdown)
-->

## Hilfe bekommen

- [Fehlerbehebung bekannter Probleme](help/troubleshooting-common-issues.markdown)
  *Was zu tun ist, falls etwas schiefläuft*
- [Community Support](help/community-support.markdown)
  *Bekomme Hilfe von realen Menschen*
- [Aktivitäten Logs](help/activity-log.markdown)
  *Aktivitäten Logs helfen dir, besseren Support zu erhalten*


## Mehr Informationen

- [Projekt Historie](about/history.markdown)
- [Mithelfen](contributing/contribute.markdown)
  *Wie du mithelfen kannst*

## Commandline Dokumentation

- [CLI Guide](cli/cli-guide.markdown)
- [Liste von CLI Optionen](cli/cli-options.markdown)

## Technische Dokumentation

- [Systemvoraussetzungen](technical/system-requirements.markdown)
  *Stelle sicher, dass auf deinem System HandBrake laufen kann*
- [Unterstützte Formate](technical/source-formats.markdown)
  *Arten von Videodateien die HandBrake lesen kann*
- [Offizielle Voreinstellungen](technical/official-presets.markdown)
  *Technische Zusammenfassung der offiziellen Voreinstellungen*
- Video
  - [Video Kodierer](technical/video-codecs.markdown)
  - [Video Kodierer Performance](technical/video-encoding-performance.markdown)
  - [Konstante Qualität versus durchschnittliche Bitrate](technical/video-cq-vs-abr.markdown)
  - [x264 Voreinstellungen und Anpassungen](technical/video-x264-presets-tunes.markdown)
  - [x264 Profile und Level](technical/video-x264-profiles-levels.markdown)
  - [Video Blickwinkel/Perspektiven](technical/video-angles.markdown)
  - [Anamorphisches Video](technical/anamorphic-guide.markdown)
  - [Modulus](technical/modulus.markdown)
  - [Framerate](technical/frame-rates.markdown)
  - [Intel QuickSync Video (QSV) Optionen](technical/video-qsv-options.markdown)
- Audio
  - [Dynamikumfang Komprimierung (DRC)](technical/dynamic-range-compression.markdown)
  - [Audio Qualität](technical/audio-quality.markdown)
- Dateien und Kompatibilität
  - [Container Formate](technical/containers.markdown)
  - [iPod 5. Generation Unterstützung](technical/old-ipod-support.markdown)
  - [Automatische Dateibenennung](technical/automatic-file-naming.markdown)
- Filter
  - [Filter Zusammenfassung](technical/filters-summary.markdown)

<!--
-  [Web optimized](advanced/web-optimised.markdown)
-  [Video source type](advanced/video-sources.markdown)
-  Advanced Filter Settings
-  Advanced preferences
-->

## Entwickler Dokumentation

- HandBrake bauen
  - [HandBrake für BSD bauen](developer/build-bsd.markdown)
    - Abhängigkeiten unter [FreeBSD](developer/install-dependencies-freebsd.markdown) installieren
  - [HandBrake für Linux bauen](developer/build-linux.markdown)
    - Abhängigkeiten für [Arch Linux](developer/install-dependencies-arch.markdown) / [CentOS](developer/install-dependencies-centos.markdown) / [Debian](developer/install-dependencies-debian.markdown) / [Fedora](developer/install-dependencies-fedora.markdown) / [Gentoo](developer/install-dependencies-gentoo.markdown) / [Ubuntu](developer/install-dependencies-ubuntu.markdown)
 installieren
  - [HandBrake für Mac bauen](developer/build-mac.markdown)
  - [HandBrake für Windows bauen](developer/build-windows.markdown)
- Packaging HandBrake
  - [Flatpak apps für Linux](developer/flatpak-repo.markdown)
    *Flatpak Applikationen kompatibel mit mehreren Linux distributionen*

<!-- TODO: link to contributing guide -->
