# Data Explorer

EnOS Data Explorer is designed to support flexible data analysis scenarios. It is based on the open-source Apache Zeppelin project, which is a web-based notebook that enables data-driven, interactive data analytics, and collaborative documents with SQL, Scala and more.

Data Explorer helps developers, data scientists, and relevant user roles process data more efficiently without having to use complex command lines or caring about clustering implementation details.

## Major benefits

- **Discovery & analytics**: Data Explorer supports multiple languages, you can easily write the queries or scripts to transform your data and extract insights.

- **Visualization & collaboration**: Data Explorer provides per-built diagrams such as histogram, pie chart, line chart, and scatter chart. Data visualization is not limited to SparkSQL queries. You can obtain different outputs through different languages.

.. image:: media/data_explorer_pic_1.png

## Key concepts

- **Interpreter**: A gateway connecting specific back-end framework to run actual code. The EnOS Data Explorer supports various interpreters. For more information, see [Supported interpreters](interpreter).

- **Paragraph**: The minimum executable unit for a specified interpreter.

.. note:: A set of paragraphs. A note can bind multiple interpreters.

<!--end-->
