``w.data_sources``: Data Sources (legacy)
=========================================
.. currentmodule:: databricks.sdk.service.sql

.. py:class:: DataSourcesAPI

    This API is provided to assist you in making new query objects. When creating a query object, you may
    optionally specify a `data_source_id` for the SQL warehouse against which it will run. If you don't
    already know the `data_source_id` for your desired SQL warehouse, this API will help you find it.

    This API does not support searches. It returns the full list of SQL warehouses in your workspace. We
    advise you to use any text editor, REST client, or `grep` to search the response from this API for the
    name of your SQL warehouse as it appears in Databricks SQL.

    **Note**: A new version of the Databricks SQL API is now available. [Learn more]

    [Learn more]: https://docs.databricks.com/en/sql/dbsql-api-latest.html

    .. py:method:: list() -> Iterator[DataSource]


        Usage:

        .. code-block::

            from databricks.sdk import WorkspaceClient
            
            w = WorkspaceClient()
            
            srcs = w.data_sources.list()

        Retrieves a full list of SQL warehouses available in this workspace. All fields that appear in this
        API response are enumerated for clarity. However, you need only a SQL warehouse's `id` to create new
        queries against it.

        **Note**: A new version of the Databricks SQL API is now available. Please use :method:warehouses/list
        instead. [Learn more]

        [Learn more]: https://docs.databricks.com/en/sql/dbsql-api-latest.html

        :returns: Iterator over :class:`DataSource`
        