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
6. Die Sichtbarkeit von Attributen und Methoden MUSS immer angegeben werden; abstract und final MUSS vor der Sichtbarkeit angegeben werden; static MUSS nach der Sichtbarkeit angegeben werden.
7. Kontrollstrukturen MÜSSEN ein Leerzeichen zwischem dem jeweiligen Schlüsselwort und der öffnenden runden Klammer haben; Funktions- und Methodenaufrufe DÜRFEN kein Leerzeichen vor der öffnenden runden Klammer haben.
8. Die öffnenden geschweiften Klammern von Kontrollstrukturen DÜRFEN KEINE eigene neue Zeile einnehmen, die schließenden geschweiften Klammern MÜSSEN hingegen einzeln in einer eigenen Zeile stehen.
9. Nach den öffnenden und vor den schließenden runden Klammern von Kontrollstrukturen DARF KEIN Leerzeichen stehen.

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
8. Sortiere Methoden bei der Deklaration nach ihrer Sichtbarkeit, zuerst kommt public, dann protected und zuletzt private. Eine der wenigen Ausnahmen bildet der Konstruktur, der zur besseren Lesbarkeit unabhängig von seiner Sichtbarkeit immer direkt nach den Attributen kommen sollte.
9. Bei der Instanziierung einer Klasse werden die runden Klammern nach dem Klassen-Namen immer angegeben.

### Namenskonventionen

1. Benutze den lowerCamelCase für die Bezeichner von Variablen, Funktionen und Parametern.
2. Benutze Kleinbuchstaben für die Schlüssel von Options-Arrays und bei den Namen von Formularfeldern. Einzelne Wörter werden durch Underscores getrennt.
3. Benutze Namespaces für alle Klassen.
4. Benutze bei abstrakten Klassen das Prefix Abstract im Bezeichner.
5. Benutze in Dateinamen nur alphanummerische Zeichen und den Underscore.

## Eigene Ergänzungen

### Struktur

1. Es ist nur genau eine Anweisung pro Zeile gestattet.
2. Benutze den C-Syntax mit geschweiften Klammern für Kontrollstrukturen. Lediglich in Templates sollte zur besseren Lesbarkeit die alternative Syntax verwendet werden, wobei der Doppelpunkt direkt nach der schließenden runden Klammer kommt.
3. Ein schließendes PHP-Tag am Ende einer Datei ist optional und sollte weggelassen werden, um Probleme mit versehentlichen Leerzeichen/-zeilen zu vermeiden.
4. Die öffnenden und schließenden geschweiften Klammern von Funktionen sollten genauso wie bei den Methoden einzeln in einer eigenen Zeile stehen.
5. Vor und hinter dem Pfeiloperator -> kommen keine Leerzeichen.

### Namenskonventionen

1. PHP-Schlüsselworte sind klein zu schreiben (z.B. if und for).
2. Bezeichner werden nicht mit einem Underscore begonnen.
3. Formuliere Klassen-Namen sofern möglich im Singular.
4. Formuliere die Tabellennamen in Datenbanken sofern möglich im Plural.
5. Benutze Kleinbuchstaben für die Namen von Datenbanken, Tabellen und Tabellenspalten. Einzelne Wörter werden durch Underscores getrennt.

### Idea
[Jan Teriete](https://plus.google.com/106660436858103395374?rel=author)