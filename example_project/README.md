Hello!

This has two defined sources for tables 'actual' and 'reference' in the schema 'schema_name' and the database 'database_name'

Once you are connected to your db, please run 'dbt deps' to install dbt-utils.

Then you can test your unioning with teh following jinja code

{{ dbt_utils.union_relations(relations=[source('test', 'reference'),source('test', 'actual')]) }}
