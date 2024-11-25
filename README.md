Template-Sensor Blueprints für Home Assistant: Absolute Luftfeuchtigkeit und Taupunkt

Dieses Repository enthält zwei Blueprints für Home Assistant, die Template-Sensoren zur Berechnung der absoluten Luftfeuchtigkeit und des Taupunkts erstellen. Beide Sensoren basieren auf den Eingabewerten von Temperatur- und Feuchtigkeitssensoren, die du in deinem Home Assistant System bereits eingerichtet hast.
Blueprint 1: Template-Sensor für Absolute Luftfeuchtigkeit

Der erste Blueprint berechnet die absolute Luftfeuchtigkeit in g/m³, basierend auf der gemessenen Temperatur und relativen Luftfeuchtigkeit. Die Berechnung erfolgt mithilfe der Magnus-Formel, die den Dampfdruck in Abhängigkeit von Temperatur und Feuchtigkeit berechnet. Der Sensor gibt den Wassergehalt der Luft als absolute Luftfeuchtigkeit aus, was besonders nützlich ist, um die Luftqualität oder den Zustand von Klimaanlagen und Lüftungssystemen zu überwachen.
Blueprint 2: Template-Sensor für Taupunkt

Der zweite Blueprint berechnet den Taupunkt in °C, der angibt, bei welcher Temperatur die Luft gesättigt ist und Wasserdampf kondensiert. Der Taupunkt ist eine wichtige Größe für die Analyse von Feuchtigkeit und Luftqualität. Dieser Sensor verwendet ebenfalls Temperatur- und Feuchtigkeitssensoren und berechnet den Taupunkt anhand der Ternary-Formel.
Funktionen und Vorteile

    Flexibilität: Beide Blueprints ermöglichen es, Temperatur- und Feuchtigkeitssensoren nach Belieben auszuwählen, sodass du sie an deine bestehende Sensorik anpassen kannst.
    Automatisierung: Die berechneten Werte können in Automatisierungen und Szenen genutzt werden, um auf Veränderungen der Luftfeuchtigkeit oder des Taupunkts zu reagieren.
    Einfache Konfiguration: Die Blueprints bieten eine benutzerfreundliche Möglichkeit, neue Sensoren zu erstellen, ohne dass tiefgehende YAML-Kenntnisse erforderlich sind.

Installation und Verwendung

    Lade die jeweiligen YAML-Dateien für die Blueprints herunter.
    Importiere sie über Einstellungen → Blueprints → Blueprint importieren in Home Assistant.
    Erstelle neue Template-Sensoren basierend auf den Blueprints und wähle die gewünschten Eingabewerte (Temperatur- und Feuchtigkeitssensoren).
    Die neuen Sensoren sind sofort verfügbar und können für Automatisierungen, Dashboards und weitere Analysen genutzt werden.

Diese Blueprints bieten eine einfache und flexible Möglichkeit, die Luftfeuchtigkeit und den Taupunkt in deinem Home Assistant System zu überwachen und zu nutzen.
