# case_data_analyst

Como executar o notebook:

1. O notebook foi desenvolvido na plataforma Databricks Community Edition, utilizando o ambiente Apache Spark 3.2.2.

2. Para executar o notebook, é necessário realizar o download dos arquivos disponíveis no seguinte bucket S3: https://data-architect-test-source.s3-sa-east-1.amazonaws.com

3. Após o download, os arquivos devem ser importados para o Databricks, dentro do diretório lógico: dbfs:/tmp/ (Isso pode ser feito utilizando comandos como dbutils.fs.cp.) // Esse tratamento já está implementado em uma seção específica do notebook.

4. O arquivo ab_test_ref.tar.gz possui extensão .tar.gz, portanto requer um processamento específico: é necessário movê-lo para o sistema de arquivos físico do driver, descompactá-lo via comandos de shell, e em seguida mover o arquivo .csv extraído de volta para o diretório lógico do Databricks (dbfs:/tmp/). // Esse tratamento já está implementado em uma seção específica do notebook.

5. Executar o código em sequência.
