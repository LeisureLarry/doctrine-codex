# doctrine-codex

## Codex for Doctrine 2

EN: German style guide for Doctrine 2 projects

DE: Deutschsprachige Programmierrichtlinien für Projekte auf Basis von Doctrine 2

Die vorliegenden Programmierrichtlinien basieren auf PSR-1 und PSR-2 der PHP FIG.

Die Schlüsselwörter MÜSSEN/MÜSSEN NICHT/DÜRFEN NUR/DARF KEIN und SOLLTEN/SOLLTEN NICHT definieren innerhalb dieser beiden PSRs, wie verpflichtend eine Regel einzuhalten ist.

## PSR-1: Framework-Interoperabilität
[PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)

1. Dateien DÜRFEN NUR die PHP-Tags
2. Dateien MÜSSEN als Zeichenkodierung UTF-8 ohne BOM für PHP-Code verwenden.
3. Dateien SOLLTEN entweder Symbole (wie Klassen, Funktionen, Konstanten, etc.) definieren oder Nebenwirkungen verursachen (z.B. Ausgabe generieren, .ini Einstellungen ändern, etc.). Sie SOLLTEN NICHT beides machen.
4. Namespaces und Klassen MÜSSEN einen Autoloading-Standard befolgen.
5. Klassen-Namen MÜSSEN den UpperCamelCase verwenden.
6. Klassen-Konstanten müssen Großbuchstaben verwenden. Einzelne Wörter innerhalb dieser Bezeichner werden mittels Underscore getrennt.
7. Methoden-Namen MÜSSEN den lowerCamelCase verwenden.

## PSR-2: Stilistische Programmierrichtlinien
[PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)

1. Programmiercode MUSS vier Leerzeichen als Einrückung verwenden (keine Tabulatoren bzw. Tabs).
2. Es DARF KEIN hartes Zeichenlimit für einzelne Zeilen geben; das softe Limit MÜSSEN 120 Zeichen pro Zeile sein; Zeilen SOLLTEN 80 Zeichen oder weniger enthalten.
3. Nach der Deklaration des Namespaces MUSS eine Leerzeile folgen und es MUSS eine weitere Leerzeile nach dem Block mit den USE-Deklarationen geben.
4. Die öffnenden und schließenden geschweiften Klammern einer Klasse MÜSSEN einzeln in einer eigenen Zeile stehen.
5. Die öffnenden und schließenden geschweiften Klammern einer Methode MÜSSEN einzeln in einer eigenen Zeile stehen.
6. Die Sichtbarkeit von Attributen und Methoden MUSS immer angegeben werden; abstract oder final MUSS vor der Sichtbarkeit angegeben werden; static MUSS nach der Sichtbarkeit angegeben werden.
7. Kontrollstrukturen MÜSSEN ein Leerzeichen zwischem dem jeweiligen Schlüsselwort und der öffnenden runden Klammer haben; Funktions- und Methodenaufrufe DÜRFEN kein Leerzeichen vor der öffnenden runden Klammer haben.
8. Die öffnenden geschweiften Klammern von Kontrollstrukturen DÜRFEN KEINE eigene neue Zeile einnehmen, die schließenden geschweiften Klammern MÜSSEN hingegen einzeln in einer eigenen Zeile stehen.
9. Nach den öffnenden und vor den schließenden runden Klammern von Kontrollstrukturen DARF KEIN Leerzeichen stehen.
10. Alle PHP-Dateien MÜSSEN den Unix-Zeilenumbruch (LF) verwenden. In den meisten Windows-Editoren und IDEs kann man angeben, welcher Zeilenumbruch für neue Dateien verwendet werden soll.
11. Das schließende PHP-Tag am Dateiende ist optional. Enthält eine Datei nur PHP-Code, so MUSS dieses optionale Tag weggelassen werden.
12. Alle PHP-Dateien MÜSSEN mit einer einzigen Leerzeilen enden.
13. PHP-Schlüsselwörter MÜSSEN in Kleinbuchstaben geschrieben werden (z.B. if und for).
14. Die PHP-Konstanten true, false und null MÜSSEN in Kleinbuchstaben geschrieben werden.
15. Die Bezeichner von Attributen und Methoden DÜRFEN NICHT mit einem Underscore begonnen werden.

## Ergänzungen aus den Symfony-Standards
[Symfony-Standards](http://symfony.com/doc/current/contributing/code/standards.html)

### Struktur

1. Ergänze genau ein Leerzeichen nach jedem Komma-Separator.
2. Ergänze genau ein Leerzeichen vor und hinter Operatoren (z.B. bei == und &amp;&amp;).
3. Ergänze ein Komma hinter jedem Element in einem mehrzeiligen Array (auch und vor allem hinter dem letzten Element).
4. Ergänze genau eine Leerzeile vor return-Anweisungen, außer das Return steht als einzige Anweisung innerhalb geschweifter Klammern (z.B. bei einer if-Anweisung).
5. Benutze unabhängig von der Anzahl der Anweisungen immer geschweifte Klammern, um den Rumpf von Kontrollstrukturen zu kennzeichnen (z.B. bei if-Anweisungen oder Schleifen).
6. Notiere pro Datei genau eine Klassen-Definition.
7. Deklariere alle Klassen-Attribute über den Methoden.
8. Sortiere Methoden bei der Deklaration nach ihrer Sichtbarkeit, zuerst kommt public, dann protected und zuletzt private. Laut Symfony-Standards bildet der Konstruktor eine Ausnahme, der zur besseren Lesbarkeit unabhängig von seiner Sichtbarkeit immer direkt nach den Attributen kommen sollte. Ich persönlich würde dies auf alle magischen Methoden ausweiten und den Konstruktur als erstes angeben.
9. Bei der Instanziierung einer Klasse werden die runden Klammern nach dem Klassen-Namen immer angegeben.

### Namenskonventionen

1. Benutze den lowerCamelCase für die Bezeichner von Variablen, Funktionen und Parametern.
2. Benutze Kleinbuchstaben für die Schlüssel von Options-Arrays und bei den Namen von Formularfeldern. Einzelne Wörter werden durch Underscores getrennt.
3. Benutze Namespaces für alle Klassen.
4. Benutze bei abstrakten Klassen das Prefix Abstract im Bezeichner.
5. Benutze in Dateinamen nur alphanummerische Zeichen (lateinische Buchstaben und arabische Ziffern) und den Underscore.

## Eigene Ergänzungen

### Struktur

1. Es ist nur genau eine Anweisung pro Zeile gestattet. Nach einem Semikolon erfolgt also immer ein Zeilenumbruch. Eine Ausnahme dieser Regel bildet natürlich der Kopf einer for-Schleife.
2. Benutze den C-Syntax mit geschweiften Klammern für Kontrollstrukturen. Lediglich in Templates sollte zur besseren Lesbarkeit die alternative Syntax verwendet werden, wobei der Doppelpunkt direkt nach der schließenden runden Klammer kommt.
3. Die öffnenden und schließenden geschweiften Klammern von Funktionen sollten genauso wie bei den Methoden einzeln in einer eigenen Zeile stehen.
4. Vor und hinter dem Pfeiloperator -> kommen keine Leerzeichen.

### Namenskonventionen

1. Bei Konfigurationsdateien ist ausnahmsweise im Dateinamen das Minuszeichen als Trenner erlaubt.
3. Formuliere Klassen-Namen sofern möglich im Singular.
3. Formuliere die Tabellennamen in Datenbanken sofern möglich im Plural.
4. Benutze Kleinbuchstaben für die Namen von Datenbanken, Tabellen und Tabellenspalten. Einzelne Wörter werden durch Underscores getrennt.

### Idea
[Jan Teriete](https://plus.google.com/106660436858103395374?rel=author)
