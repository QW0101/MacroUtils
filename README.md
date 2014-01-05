MacroUtils
==========

Класс для более быстрой инициализации flash.Vector
----------
Данный макрокласс предназначен прежде всего для быстрой инициализации flash.Vector в случаях подобным этим
<pre>
var t = Vector.ofArray([1, 2, 3, 4, 5]);
</pre>
когда заранее известны все элементы вектора, который мы хотим получить.
Изначальной целью является получение as3 подобного синтаксиса объявления вектора.

Пример использования
<pre>
package ;

import flash.Vector;
using haxe.macro.MacroUtils;
	
class Main {
		
	static function main() 
	{
		var t = [5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5].toVector();
		trace(t);
	}
}
</pre>

Типы с параметрами не поддерживаются, потому что ~мне лень~ не вижу смысла использования вектора как контейнера для "тяжелых" типов.