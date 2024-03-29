# CelestaDoc

[![Actions Status: build](https://github.com/courseorchestra/celestadoc/workflows/build/badge.svg)](https://github.com/courseorchestra/celestadoc/actions?query=workflow%3A"build")
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/ru.curs/celestadoc/badge.svg)](https://maven-badges.herokuapp.com/maven-central/ru.curs/celestadoc)


Generates celesta documentation report.

First, you should install project:

```shell
mvn clean install
```

After you can get zip-archive CelestaDoc, inside it you can find celestadoc.bat file.
Run it with the next command:

```shell
celestadoc.bat <path_to_directory_with_celesta_sql> <prefix> <output_file.adoc> [optional]-pdf [optional]-html [optional][-plantuml [optional]<param_file.pu>]
```

where 

* `path_to_directory_with_celesta_sql` - directory with celesta sql,

* `prefix` - some prefix which is used in celesta docs (For example, `doc-ru`)

* `output_file.adoc` - path to file which will be created. It should be .adoc file

* `-pdf` - optional flag for generating pdf file from adoc file. This file will be
created in the same directory as .adoc report, and it will had the same name `output_file.pdf`

* `-html` - optional flag for generating html file from adoc file. This file will be created in the same directory
as .adoc report, and it will had the same name `output_file.html`

* `-plantuml` - optional flag for generating plant UML file from celesta sql file. This file will be created in the same
directory as .adoc report, and it will had the same name `output_file.pu`

* `param_file.pu` - file with params for plant UML's diagram. It must be used only with flag `-plantuml`, and must be
after this flag. This param is optional parameter. For example, you can write `-plantuml my_param.pu` or `-plantuml`.
In second case in section `!include` will be included default file `pu_params.pu`, that can be found in project's sources.