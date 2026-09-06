=== Mobile First by Motion Media ===
Contributors:      wpmfs
Tags:              mobile, mobile-first, blocks, editor, gutenberg
Requires at least: 6.5
Tested up to:      7.0
Requires PHP:      7.4
Stable tag:        0.1.1
License:           GPLv2 or later
License URI:       https://www.gnu.org/licenses/gpl-2.0.html

Der Block-Editor öffnet in der Mobil-Vorschau, dazu ein paar mobil-native Blöcke. Übernimmt Theme-Styles, statt sie zu ersetzen.

== Description ==

Kein Page Builder und keine Block-Sammlung, sondern zwei gezielte Dinge, die Astra und Gutenberg nicht mitbringen:

1. **Mobile-First-Editing** — der Block-Editor öffnet in der Mobil-Vorschau und ist pro Nutzer auf „Desktop First" (WordPress-Standard) umschaltbar. Mobil ist die Voreinstellung, bis man sie ändert.
2. **Mobil-native Blöcke**, die es so nicht gibt — **Floating CTA** (klebrige Aktionsleiste im Daumenbereich) und **Mobile Cards** (Swipe-Karten mobil, Grid am Desktop).

= Grundsatz =

Das Theme bestimmt das Aussehen, das Toolkit bringt das Mobile-First-Verhalten. Farben, Schriften und Größen kommen aus dem Theme beziehungsweise `theme.json` und werden in `--mmwpmfs-*`-Tokens übernommen, nicht ersetzt. Ein Wechsel des Themes ändert das Aussehen der Blöcke mit.

= Blöcke =

* `mm-wpmfs/floating-cta` — Aktionsleiste, die mobil im Daumenbereich klebt. Varianten Bar und Pill, Einblendung sofort oder nach Scroll-Schwelle, ausblendbar pro Gerät.
* `mm-wpmfs/cards` und `mm-wpmfs/card` — Karten, die mobil gewischt und am Desktop als Grid dargestellt werden. Spaltenzahl responsiv, Kartenstil und Schatten an Design-Tokens gebunden.

= Editor-Bedienung =

Die Inspector-Tabs folgen dem vertrauten General/Style/Advanced-Modell. Style-Controls schreiben ausschließlich Token-Werte oder begrenzte Auswahlen — freie Hex-Farben und freie Pixelabstände sind bewusst ausgeschlossen, damit die Theme-Konsistenz erhalten bleibt.

= Barrierefreiheit und Performance =

Landmarks, sichtbare Fokus-Ringe und Touch-Ziele ab 48 Pixel sind eingebaut. Assets werden nur geladen, wenn ein Block auf der Seite vorkommt. Keine externen CDNs oder Fonts.

== Installation ==

1. ZIP über Plugins → Installieren → Plugin hochladen einspielen.
2. Aktivieren. Der Editor öffnet danach in der Mobil-Vorschau.
3. Unter „Mobile First" im Admin-Menü lässt sich das pro Nutzer umstellen.

Updates kommen automatisch über den Plugins-Bildschirm.

== Frequently Asked Questions ==

= Brauche ich Astra? =

Nein. Das Plugin liest Farben und Abstände aus `theme.json`; mit Astra sind zusätzlich dessen Presets abgedeckt. Ohne beides greifen dokumentierte Fallback-Werte.

= Überschreibt das Plugin mein Theme-Design? =

Nein. Es liest Theme-Werte und leitet daraus Komponenten-Tokens ab. Wo das Theme nichts vorgibt, greift ein Fallback.

= Kann ich die Blöcke ohne die anderen WPMFS-Plugins nutzen? =

Ja. Jedes Plugin der Familie läuft eigenständig. Ist dieses Toolkit aktiv, ordnen sich die Blöcke der anderen Produkte in dieselbe Kategorie ein.

== Changelog ==

= 0.1.1 =
* Der Hinweis auf ein unvollständiges Paket wird nicht mehr über die Textdomain des Core übersetzt. Die Datei liegt in allen Plugins der Familie, eine feste Domain wäre dort die falsche gewesen.

= 0.1.0 =
* Erste Fassung: Mobile-First-Editor-Umschalter, Theme-Token-Bridge, Blöcke Floating CTA und Mobile Cards.
* Editor-UX auf General/Style/Advanced umgestellt, Style-Controls an Tokens gebunden.
* Block-Kategorie „Mobile First" wird nur noch einmal registriert, auch wenn weitere WPMFS-Plugins aktiv sind.
* Fehlender Build wird im Debug-Betrieb als Hinweis gemeldet, statt Blöcke stillschweigend wegzulassen.

== Upgrade Notice ==

= 0.1.1 =
Wartungsrelease. Kein Handlungsbedarf.

= 0.1.0 =
Erste Fassung.
