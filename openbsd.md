--title OpenBSD
--date 20.10.2020
--author Jan Helbling

---
--newpage

--heading OpenBSD?
  * Das sicherste System
  * Freie Software mit attraktiver Lizenz
  * Ein Unix-Derivat <3

---
--newpage

--heading OpenBSD ist Frei?

OpenBSD ist vollstaendig freie Software. Alle Teile von OpenBSD unterliegen Urheberrechtsbestimmungen die die freie Weiterverbreitung erlauben.
OpenBSD kannst du samt Code und Binaerdateien fuer private als auch kommerzielle projekte verwenden. Einzige Bedingung ist, dass der Copyright-Vermerk des urspuenglichen Programms nicht entfernt werden darf.
Am besten liest du die BSD-Lizenz durch ;)

---
--newpage

--heading Erste Schritte

Folgende Manpages die dir den Start mit OpenBSD erleichtern:
  * afterboot
  * help
  * hier
  * man
  * intro
  * adduser
  * vipw
  * disklabel
  * shutdown, reboot und halt
  * dmesg
  * ifconfig

So verwendest du Manpages:

--beginshelloutput
$ man afterboot
--endshelloutput

---
--newpage

--heading Wieso ist Paket X nicht enthalten?

Ein Produkt muss stabil, sicher und freie Software sein, deshalb kann es sein das ein Paket nicht oder nicht in der aktuellsten Version vorhanden ist.
Eine hoehere Versionsnummer bedeutet nicht immer das es ein besseres Produkt ist!


---
--newpage

--heading Linux & OpenBSD

Linux, z.B. ein Debian-basiertes:
--beginoutput
# systemctl enable nginx    <-- Dienst aktivieren
# apt search nginx          <-- In den Repos nach nginx suchen
# apt show nginx            <-- Infos ueber das Paket nginx anzeigen
# apt install nginx         <-- nginx installieren
# apt update && apt upgrade <-- Pakete aktualisieren
--endoutput

OpenBSD:
--beginoutput
# rcctl enable nginx        <-- Dienst aktivieren
# pkg_info -Q nginx         <-- In den Repos nach nginx suchen
# pkg_info nginx            <-- Infos ueber das Paket nginx anzeigen
# pkg_add nginx             <-- nginx installieren
# pkg_add -ivu              <-- Pakete aktualisieren
# fw_update                 <-- Firmwareupdates installieren
# syspatch                  <-- OpenBSD-Patches installieren
--endoutput

---
--newpage

--heading OpenBSD Sicherheit?

  * OpenBSD hat viele Sicherheitsfunktionen wie z.B. pledge und unveil. So kann z.B. Firefox nur auf den Ordner /tmp und ~/Downloads zugreiffen.
  * PF (Packet Filter) ist eine stabile und sichere Firewall die einfach zu konfigurieren ist.
  * OpenBSD erstellt bei jedemeustart einen eindeutigen Kernel (KARL) so dass Exploits keine Chance haben.
  * OpenBSD hat diverse Technologien um das System vor Overflow-Angriffen zu schuetzen.
  * OpenBSD patcht Pakete bevor sie verfuegbar fuer die Installation sind.
  * OpenBSD ueberprueft den Code kontinuierlich auf Sicherheit.
  * Secure by default
  * Spectre, Meltdown, und alle Sicherheitsfunktionen bekommst du neverever ausgeschaltet
  * ASLR, W^X, RETGUARD, arc4random, Otto's malloc, RELRO, PIE, fork+exec, library relinking, trapsleds, guard pages, ROP gadget reduction, privsep, privdrop,...
