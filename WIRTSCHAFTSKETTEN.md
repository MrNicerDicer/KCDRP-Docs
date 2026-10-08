# Wirtschaftsketten – Kuttenberg RP

Stand: 8. Oktober 2026. Übersicht anhand der aktuellen Rezepte und Produktionskonfigurationen.

Ein Pfeil bedeutet: liefert Rohstoffe oder Produkte an den nächsten Beruf. Einige Materialien sind zusätzlich über NPCs erhältlich. Die Verbindungen sind deshalb nicht überall zwingende Abhängigkeiten.

## 1. Metall, Waffen und Rüstung

```text
Bergbau
   ↓ Eisen, Altmetall, Kupfer und weitere Metalle
Metallverarbeitung / Schmiedehandwerk
   ↓ Stahl, hochwertige Stähle, Befestigungsmaterial
   ├── Schmied → Nahkampfwaffen
   ├── Rüstungsmacher → Rüstungen
   ├── Feinschmied → Schmuck und feine Metallwaren
   ├── Büchsenmacher → Feuerwaffen und Munition
   └── Bogenmacher → Armbrüste, Pfeile und Bolzen
```

Brennstoffkette:

```text
Holzfällerei → Holz → Köhlerei → Holzkohle
                                  ├── Metallverarbeitung
                                  ├── Feinschmied
                                  ├── Büchsenmacher
                                  └── Wirt
```

Mehrere Handwerksberufe besitzen eigene Verarbeitungsschritte. Der Schmied ist aktuell kein exklusiver Zulieferer für sämtliches Metallhandwerk.

## 2. Bögen und Fernkampf

```text
Holzfällerei → Exotisches Holz ─────────────┐
Viehzüchter → Stoff, Rindsleder, Federn ────┼→ Bogenmacher
Metallhandwerk → Metalle und Beschläge ────┘       ↓
                                         Bögen und Armbrüste
                                         Pfeile und Bolzen
                                                ↓
                                         Jäger / Wache / Spieler
```

```text
Metallhandwerk + Holzfällerei + Köhlerei
                  ↓
             Büchsenmacher
                  ↓
        Feuerwaffen und Munition
```

Büchsenmacher-Munition benötigt zusätzlich Salpeter und Schwefel. Beide stehen in den Rezepten; eine eigene Spieler-Produktionskette für diese Stoffe ist in dieser Übersicht nicht belegt.

## 3. Kleidung und Leder

```text
Viehzüchter
   ├── Schafe → Stoff und Schafhaut ──┐
   └── Rinder → Rindsleder ───────────┼→ Schneider → Kleidung
                                     │
Jäger → Rehhaut und Hasenfell ────────┘
```

Weitere Abnehmer:

```text
Rindsleder → Rüstungsmacher
Rindsleder + Stoff → Bogenmacher
```

Schafe liefern technisch bereits das vorhandene Stoff-/Leinenitem. Eine zusätzliche Verarbeitungskette „Wolle → Garn → Stoff“ existiert nicht.

## 4. Lebensmittel und Getränke

```text
Landwirt → Gemüse, Obst und Walnüsse ──────┐
Viehzüchter → Fleisch, Eier und Milch ────┼→ Wirt
Jäger → Wildfleisch ──────────────────────┘    ↓
                                      Speisen und Backwaren
                                             ↓
                                      Auslage → Spieler
```

Zusätzliche Verbindungen:

```text
Landwirt → Karotten → Viehzüchter → Tierprodukte
Viehzüchter → Milch → Käse
```

Weinkette:

```text
Winzer
   ↓ Weinberg
interne Trauben → interner Most
   ↓
Einfacher Wein / Wein / Feiner Wein
   ├── Wirt → Ausschank über die Auslage
   └── direkter Spielerhandel
```

Trauben und Most sind interne Ressourcen des jeweiligen Weinguts, keine Inventaritems.

Honig wird in Wirt-Rezepten benötigt. Eine eigene Imker-Produktionskette wurde in den für diese Übersicht geprüften Systemen nicht bestätigt. „Imker → Wirt“ ist daher keine belegte fertige Verbindung.

Räuchern und Trocknen bleiben freie Verarbeitung für alle Spieler.

## 5. Heilkunde und Dienstleistungen

```text
Freies Kräutersammeln → Wundarzt / Alchemie
                              ↓
                       Heilmittel und Tränke
                              ↓
                            Spieler
```

Kräuter gehören nicht zum Landwirt.

Die Finanzierungskette der Wache:

```text
Steuern / regionale Einnahmen
              ↓
        Vogt / Landvogt
              ↓
          Wachbudget
              ↓
        Sold für die Wache
```

Barbier, Lehrmeister und Schreiber sind vor allem Dienstleister und Geldsenken: Spieler bezahlen für ihre Leistungen, statt ihnen Produktionsmaterialien zu liefern.

## 6. Zentrale Zulieferer und Abnehmer

- **Viehzüchter:** verbindet Lebensmittelwirtschaft, Schneider und Bogenmacher.
- **Holzfällerei und Köhlerei:** versorgen mehrere Handwerksberufe und den Wirt.
- **Metallgewinnung und -verarbeitung:** Grundlage für Waffen, Rüstungen und Schmuck.
- **Landwirt:** versorgt Wirt und Viehzüchter.
- **Wirt:** bündelt viele Rohprodukte zu verkäuflichen Speisen.
- **Jäger:** liefert gleichzeitig Lebensmittel und Schneider-Materialien.

## Gesamtübersicht

```text
Rohstoff-Tätigkeiten / Landwirtschaft / Tierhaltung
                         ↓
              Verarbeitung und Handwerk
                         ↓
             Auslagen und Spielerhandel
                         ↓
                  Spieler als Käufer
```

Die stärksten Verbindungen bestehen aktuell bei Nahrung, Tierprodukten, Holz und Metall. NPC-Grundversorgung und überlappende Verarbeitung sorgen dafür, dass die Wirtschaft noch nicht überall vollständig voneinander abhängig ist.

## Quellen im Projekt

- `config/armor_recipes.json`
- `config/jeweller_recipes.json`
- `config/gunsmith_recipes.json`
- `config/bowyer_recipes.json`
- `config/tailor_recipes.json`
- `config/innkeeper_recipes.json`
- `config/charcoal_recipes.json`
- `config/livestock.json`
- `config/agriculture.json`
- `config/winery.json`
- `src/KcdRp.Core/CommunityRepository.cs` – Ressourcen- und Tätigkeitendefinitionen

Diese Übersicht beschreibt Produktionsbeziehungen. Sie ist keine vollständige Prüfung aller aktuell platzierten Standorte oder aller Angebote der produktiven Datenbank.
