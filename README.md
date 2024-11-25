# Template-Sensor Blueprints für Home Assistant: Absolute Luftfeuchtigkeit und Taupunkt

Dieses Repository enthält zwei **Blueprints für Home Assistant**, die Template-Sensoren zur Berechnung der **absoluten Luftfeuchtigkeit** und des **Taupunkts** erstellen. Beide Sensoren basieren auf den Eingabewerten von Temperatur- und Feuchtigkeitssensoren, die du in deinem Home Assistant System bereits eingerichtet hast.

## 🚀 Blueprint 1: Template-Sensor für Absolute Luftfeuchtigkeit
Der erste Blueprint berechnet die **absolute Luftfeuchtigkeit** in g/m³, basierend auf der gemessenen Temperatur und relativen Luftfeuchtigkeit. Die Berechnung erfolgt mithilfe der **Magnus-Formel** für den Sättigungsdampfdruck:

### Berechnungsformel:
Die Magnus-Formel zur Berechnung des Sättigungsdampfdruckes (es) lautet:

\[
e_s(T) = 6.112 \cdot e^{\left(\frac{17.67 \cdot T}{T + 243.5}\right)}
\]

Dabei ist:
- \( T \) die Temperatur in °C.
- \( e_s(T) \) der Sättigungsdampfdruck in hPa.

Die absolute Luftfeuchtigkeit (AH) wird dann mit der folgenden Formel berechnet:

\[
AH = \frac{216.7 \cdot (e_s(T) \cdot RH)}{T + 273.15}
\]

Dabei ist:
- \( RH \) die relative Luftfeuchtigkeit in Prozent (von 0 bis 100).
- \( T \) die Temperatur in °C.
- \( AH \) die absolute Luftfeuchtigkeit in g/m³.

Der Sensor gibt den Wassergehalt der Luft als absolute Luftfeuchtigkeit aus, was besonders nützlich ist, um die Luftqualität oder den Zustand von Klimaanlagen und Lüftungssystemen zu überwachen.

## 🌡️ Blueprint 2: Template-Sensor für Taupunkt
Der zweite Blueprint berechnet den **Taupunkt** in °C, der angibt, bei welcher Temperatur die Luft gesättigt ist und Wasserdampf kondensiert. Der Taupunkt ist eine wichtige Größe für die Analyse von Feuchtigkeit und Luftqualität.

### Berechnungsformel:
Der Taupunkt \( T_d \) wird mit der **Ternary-Formel** berechnet:

\[
\alpha = \frac{17.27 \cdot T}{T + 237.7} + \ln\left(\frac{RH}{100}\right)
\]

\[
T_d = \frac{237.7 \cdot \alpha}{17.27 - \alpha}
\]

Dabei ist:
- \( T \) die Temperatur in °C.
- \( RH \) die relative Luftfeuchtigkeit in Prozent (0–100).
- \( T_d \) der Taupunkt in °C.

Diese Formel liefert den Punkt, an dem die Luft bei gegebener Temperatur und relativer Luftfeuchtigkeit zu kondensieren beginnt.

## 🛠️ Funktionen und Vorteile
- **Flexibilität**: Beide Blueprints ermöglichen es, Temperatur- und Feuchtigkeitssensoren nach Belieben auszuwählen, sodass du sie an deine bestehende Sensorik anpassen kannst.
- **Automatisierung**: Die berechneten Werte können in Automatisierungen und Szenen genutzt werden, um auf Veränderungen der Luftfeuchtigkeit oder des Taupunkts zu reagieren.
- **Einfache Konfiguration**: Die Blueprints bieten eine benutzerfreundliche Möglichkeit, neue Sensoren zu erstellen, ohne dass tiefgehende YAML-Kenntnisse erforderlich sind.

## 📥 Installation und Verwendung

Um die Blueprints direkt in Home Assistant zu verwenden, folge diesen einfachen Schritten:

https://my.home-assistant.io/create-link/?redirect=blueprint_import

1. **Klicke auf die folgenden Links**, um die Blueprints direkt zu importieren:
   - [Template-Sensor für Absolute Luftfeuchtigkeit](https://github.com/nico123469/Absolute-Luftfeuchtigkeit-und-Taupunkt/raw/refs/heads/main/Absolute%20Luftfeuchtigkeit.yaml)
   - [Template-Sensor für Taupunkt](https://github.com/nico123469/Absolute-Luftfeuchtigkeit-und-Taupunkt/raw/refs/heads/main/Taupunkt.yaml)

2. **Importiere den Blueprint in Home Assistant**:
   - Gehe in Home Assistant zu **Einstellungen** → **Blueprints** → **Blueprint importieren**.
   - Füge die obenstehenden Links in das **URL-Feld** ein und klicke auf **Importieren**.

3. **Erstelle neue Template-Sensoren**:
   - Nach dem Import kannst du neue Template-Sensoren basierend auf den Blueprints erstellen.
   - Wähle die Eingabewerte aus (Temperatur- und Feuchtigkeitssensoren) und konfiguriere die Sensoren nach deinen Bedürfnissen.

4. **Verwendung**:
   - Die neuen Sensoren sind sofort verfügbar und können für Automatisierungen, Dashboards und weitere Analysen genutzt werden.

Diese Blueprints bieten eine einfache und flexible Möglichkeit, die Luftfeuchtigkeit und den Taupunkt in deinem Home Assistant System zu überwachen und zu nutzen.
