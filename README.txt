Кратко что происходит в главном changeLog'e

1) закомменченный changeLog "changelog-droptable.xml" - удаление таблицы public.testLiquibase
2) changeLog "changelog-createtable-v.1.xml" - создание таблицы public.testLiquibase
3) changeLog "changelog-add_column-v.1.xml" - добавление столбца time_plus
4) changeLog "changelog-add_column_toDrop-v.1.xml" - добавление столбца time_toDrop
5) changeLog "changelog-rename_column_toDrop-v.1.xml" - переименование столбца time_toDrop --> time_toDrop_renamed
6) changeLog "changelog-drop_column_toDrop-v.1.xml" - удаление столбца time_toDrop_renamed
7) changeLog "changelog-initdata-v.1.xml" - добавление данных
8) changeLog "changelog-procedure-v.2.xml" - создание функции по .sql файлу

Последнюю неделю все это дело запускал на своем ноуте, на котором стоит Postgres, поэтому часть modifySql при создании таблицы закомментил. Но эта штука отрабатывала в июле через Jenkins на ИФТ. Таблица s_grnplm_as_cib_gm_tmp."test_liquibase_v.1.3" - пример таблицы с with, distributed, partition
Соотве

Запуск с проверкой contexts можно производить как через командную строку Liquibase:
liquibase upgrade contexts="test"

Либо указав в liquibase.propetries:
contexts=test