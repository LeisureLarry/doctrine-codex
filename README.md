# doctrine-codex

## Codex for Doctrine 2

EN: German style guide for Doctrine 2 projects

DE: Deutschsprachige Programmierrichtlinien für Projekte auf Basis von Doctrine 2

Die vorliegenden Programmierrichtlinien basieren auf PSR-1 und PSR-2 der PHP FIG, beinhalten jedoch nicht alle der dortigen Empfehlungen.

Die Schlüsselwörter MÜSSEN/MÜSSEN NICHT/DÜRFEN NUR/DARF KEIN und SOLLTEN/SOLLTEN NICHT definieren, wie verpflichtend eine Regel einzuhalten ist.

## PSR-1: Framework-Interoperabilität
[PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)

1. Dateien DÜRFEN NUR die PHP-Tags <?php und <?= verwenden.
2. Dateien MÜSSEN als Zeichenkodierung UTF-8 ohne BOM für PHP-Code verwenden.
3. Dateien SOLLTEN entweder Symbole (wie Klassen, Funktionen, Konstanten, etc.) definieren oder eine Auswirkung haben (z.B. eine Ausgabe mit echo generieren). Sie SOLLTEN NICHT beides tun.
4. Namespaces und Klassen MÜSSEN einen Autoloading-Standard befolgen.
5. Klassen-Namen MÜSSEN den UpperCamelCase verwenden.
6. Klassen-Konstanten MÜSSEN Großbuchstaben verwenden. Einzelne Wörter innerhalb dieser Bezeichner werden mittels Underscore getrennt.
7. Methoden-Namen MÜSSEN den lowerCamelCase verwenden.

## PSR-2: Stilistische Programmierrichtlinien
[PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)

### Struktur

1. Programmiercode MUSS vier Leerzeichen als Einrückung verwenden (keine Tabulatoren bzw. Tabs).
2. Es DARF KEIN hartes (verpflichtendes) Zeichenlimit für einzelne Zeilen geben; das softe Limit MÜSSEN 120 Zeichen pro Zeile sein; Zeilen SOLLTEN 80 Zeichen oder weniger enthalten.
3. Eine Zeile DARF NUR eine Anweisung enthalten, d.h. nach einem Semikolon erfolgt immer ein Zeilenumbruch.
4. Nach der Deklaration des Namespaces MUSS eine Leerzeile folgen und es MUSS eine weitere Leerzeile nach dem Block mit den USE-Deklarationen geben.
5. Die öffnenden und schließenden geschweiften Klammern einer Klasse MÜSSEN einzeln in einer eigenen Zeile stehen.
6. Die öffnenden und schließenden geschweiften Klammern einer Methode MÜSSEN einzeln in einer eigenen Zeile stehen.
7. Die Sichtbarkeit von Attributen und Methoden MUSS immer angegeben werden; abstract oder final MUSS vor der Sichtbarkeit angegeben werden; static MUSS nach der Sichtbarkeit angegeben werden.
8. Kontrollstrukturen MÜSSEN ein Leerzeichen zwischen dem jeweiligen Schlüsselwort und der öffnenden runden Klammer aufweisen; Funktions- und Methodenaufrufe DÜRFEN KEIN Leerzeichen vor der öffnenden runden Klammer haben.
9. Die öffnenden geschweiften Klammern von Kontrollstrukturen DÜRFEN KEINE eigene neue Zeile einnehmen, die schließenden geschweiften Klammern MÜSSEN hingegen einzeln in einer eigenen Zeile stehen.
10. Nach den öffnenden und vor den schließenden runden Klammern von Kontrollstrukturen DARF KEIN Leerzeichen stehen.

### Namenskonventionen

1. PHP-Schlüsselwörter (z.B. if und for) und PHP-Konstanten (true , false und null) MÜSSEN in Kleinbuchstaben geschrieben werden.
2. Die Bezeichner von Attributen und Methoden DÜRFEN NICHT mit einem Underscore beginnen.

### Dateien

1. Alle PHP-Dateien MÜSSEN den Unix-Zeilenumbruch (LF) verwenden.
2. Das schließende PHP-Tag am Dateiende MUSS weggelassen werden, sofern die Datei nur PHP-Code enthält (sogenannte pure PHP-Dateien).
3. Alle (puren) PHP-Dateien MÜSSEN mit einer einzelnen Leerzeile enden.

## Ergänzungen aus den Symfony-Standards
[Symfony-Standards](http://symfony.com/doc/current/contributing/code/standards.html)

### Struktur

1. Nach jedem Komma-Separator MUSS genau ein Leerzeichen folgen.
2. Vor und hinter binären Operatoren (z.B. bei == und &&) MUSS genau ein Leerzeichen gesetzt werden.
3. Zwischen unären Operatoren (z.B. ! und --) und dem Operanden DARF KEIN Leerzeichen gesetzt werden.
4. Hinter jedem Element in einem mehrzeiligen Array (auch und vor allem hinter dem letzten Element) MUSS ein Komma folgen.
5. Vor return-Anweisungen MUSS genau eine Leerzeile ergänzt werden, außer das Return steht als einzige Anweisung innerhalb geschweifter Klammern (z.B. bei einer if-Anweisung).
6. Unabhängig von der Anzahl der Anweisungen MÜSSEN immer geschweifte Klammern benutzt werden, um den Rumpf von Kontrollstrukturen zu kennzeichnen (z.B. bei if-Anweisungen oder Schleifen).
7. Pro Datei DARF NUR genau eine Klassen-Definition notiert werden.
8. Alle Klassen-Attribute MÜSSEN über den Methoden deklariert werden.
9. Methoden MÜSSEN bei der Deklaration nach ihrer Sichtbarkeit sortiert werden, zuerst kommt public, dann protected und zuletzt private. Laut Symfony-Standards bildet der Konstruktor eine Ausnahme, der zur besseren Lesbarkeit unabhängig von seiner Sichtbarkeit immer direkt nach den Attributen kommen sollte. Ich persönlich würde dies auf alle magischen Methoden ausweiten und den Konstruktur als Erstes angeben.
10. Bei der Instanziierung einer Klasse MÜSSEN die runden Klammern nach dem Klassen-Namen immer angegeben werden.

### Namenskonventionen

1. Für die Bezeichner von Variablen, Funktionen und Parametern MUSS immer der lowerCamelCase verwendet werden.
2. Für die Schlüssel von Options-Arrays und bei den Namen von Formularfeldern MÜSSEN Kleinbuchstaben verwendet werden. Einzelne Wörter werden durch Underscores getrennt.
3. Für alle Klassen MÜSSEN Namespaces verwendet werden.
4. Bei abstrakten Klassen MUSS das Präfix Abstract im Bezeichner verwendet werden.
5. In Dateinamen DÜRFEN NUR alphanumerische Zeichen (lateinische Buchstaben und arabische Ziffern) und der Underscore verwendet werden.

## Eigene Ergänzungen

### Struktur

1. Für Kontrollstrukturen SOLLTE die C-Syntax mit geschweiften Klammern verwendet werden. Lediglich in Templates SOLLTE zur besseren Lesbarkeit die [alternative Syntax] (http://php.net/de/control-structures.alternative-syntax) verwendet werden, wobei der Doppelpunkt direkt nach der schließenden runden Klammer kommt.
2. Die öffnenden und schließenden geschweiften Klammern von Funktionen SOLLTEN genauso wie bei den Methoden einzeln in einer eigenen Zeile stehen.
3. Vor und hinter dem Pfeiloperator -> DÜRFEN KEINE Leerzeichen stehen.

### Namenskonventionen

1. Klassen-Namen SOLLTEN im Singular formuliert werden.
2. Tabellennamen in Datenbanken SOLLTEN im Plural formuliert werden.
3. In den Namen von Datenbanken, Tabellen und Tabellenspalten DÜRFEN NUR Kleinbuchstaben verwendet werden. Einzelne Wörter werden durch Underscores getrennt.

### Idea
[Jan Teriete](https://plus.google.com/106660436858103395374?rel=author)