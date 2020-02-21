# Tag eins 

## Zieldemonstration: Wie sieht ein funktionierendes Setup mit Monitoring aus?
--> Key Elements: 
  ### Capacity planning/ Alerting
  --> Clusterweit verfügbarer RAM
  --> Clusterweit verfügbare CPU 
  --> Demo: Was passiert wenn Ressourcen knapp werden? Ein Alarm wird rausgesendet.
  ### Systemfehler
  --> Die Webseite ist down
  --> Ein Alarm wird versendet mit Hinweisen, wo im Dashboard weitereInformationen zu finden sind.

Slot: 1h
Acceptance criteria: Das System steht, voller Fokus auf einen funktionierenden Demo-Ablauf.

## Kurzübersich beteiligter Komponenten
### Logging (Hilft beim Debuggen)
  Technisch: Loki
### Trending (ermöglicht proaktives Alerten und damit vermeiden von Katastrophen)
  Technisch: Prometheus
### Alerting (Hinweis auf Fehler/ kritische Trends)
  Technisch: Grafana

Slot: 1h
Acceptance criteria: Fokus auf Zusammenhang der Komponenten

## Pause

Slot: 1h
Acceptance criteria: All members are refreshed.

## Kurzübersicht eines Deployments

#### History roll up:
  Using Helm (notwendig zur Kapselung/ Vereinfachung/ Benutzung bestehender Komponenten. Größter Nutzen: Wir müssen nichts erfinden)
  Using DNSaaS (Voraussetzung für TLS)
  Using cert-manager (Implementierung TLS)
  Deploying Monitoring/ Application / The rest of the stack

Slot: 1,5h
Acceptance criteria: Tech-Stack is tested and works 
  
## Diskussion:

 * Alternativen zu DNSaaS
 * Alternativen zu cert-manager

## Ansprechen offener Fragen

 * DNS:
  ** Namensschema
  ** technisches Verfahren (Delegation an DNSaaS vs. nutzen bestehender Infrastrukturen)
 * TLS
  ** Letsencrypt vs. "Enterprise"-Zertifikate 
 * gemeinsames Code-Repo

--> evtl. Hausaufgabe: Zertifikate/ Domains organisieren

## Hands on: wir bauen/ nutzen interssante Dashboards
 
 * Was ist ein Dashboard?
 * Was ist ein Notofication-Channel?
 * Was ist ein Alert?
  Threshholds, Actions
 * Wie sieht der Entwicklungs-Workflow für neue Dashboards aus?
 * Wie passe ich Notification-Channel an?
 * Welche Optionen gibt es? Verschiedene Wege der Notifikation

==> Verweis auf Literatur, andere Ressourcen


# Tag zwei 

Ziel: Implementierung Monitoring in ausgewählte Kubernetes-Umgebung.

## Klärung offener Fragen

 * DNS:
  ** Namensschema
  ** technisches Verfahren (Delegation an DNSaaS vs. nutzen bestehender Infrastrukturen)
 * TLS
  ** Letsencrypt vs. "Enterprise"-Zertifikate 

## Abarbeiten der Voraussetzungen

* Cluster-Zugriff
* Funktionierendes Helm
* Bereitstellen des Repositories/ eventuelle offfensichtliche Anpassungen
* erstes Deployment
  "Exploring" 
  "Rumspielen mit Dashboards"
  ""
* Dashboards revisionssicher in VCS einpflegen, Umgebung abreißen
* Umgebung neu ausrollen

## Perspektiven/ Fragen:

* Multi-Cluster-Monitoring: Einer für alle? Vorteile/ Nachteile
* Scaling/ Capacity planning: Wann geht das Monitoring kaputt?
* Who watches the watcher? 
* HA-Konzepte und offene Fragen für das vorgestellt Toolset
* Auditierbarkeit
* revisionssicheres Wegspeichern von Logfiles/ Log-Retention / etc.
* Offene Fragen


