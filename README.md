# Двуязычный (рус. и англ.) словарь для Aspell

Состоит из дампа [англ. словаря Aspell](https://ftp.gnu.org/gnu/aspell/dict/en/), развернутых (unmunched) словоформ [словаря для Hunspell](https://code.google.com/archive/p/hunspell-ru/) (без буквы ё), а также русских фамилий и городов.

Пример использования:

```
aspell
--lang=ru
--encoding=utf-8
--master="/usr/bin/aspell/0.60.8/lib/aspell-0.60/ru-ye"
--personal="~/.aspell.ru.pws"
...
check [FILE]
```

Слова из русского [мастер-словаря Aspell](https://ftp.gnu.org/gnu/aspell/dict/0index.html) не дублируются. Слова, содержащие апостроф или дефис, исключены по техническим причинам.

Пополнять персональный словарь (любыми языками) легко - либо по одному слову через aspell в режиме `list`, либо добавляя готовые списки со склонениями сразу в файл и удаляя возможные дубликаты посредством `sort | uniq`.
