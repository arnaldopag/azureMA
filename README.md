
#azureMA
Introdução
O Azure Machine Learning (AzureML) permite configurar endpoints para implantações de modelos de aprendizado de máquina (ML) de forma automatizada. Neste tutorial, vamos abordar os passos necessários para configurar um endpoint no AzureML usando um exemplo prático.

Passos para Configuração do Endpoint
Criar ML Automatizado: Primeiramente, é preciso criar um processo de ML automatizado no AzureML. Esse processo envolve a seleção de algoritmos, o ajuste de hiperparâmetros e a geração de modelos candidatos.

Selecionar o Melhor Job: Após a execução do processo automatizado, é necessário analisar os resultados e selecionar o melhor job gerado. Esse job representa o modelo de ML com melhor desempenho com base nos critérios definidos.

Criar Modelo a partir do Job Selecionado: Com o job selecionado, o próximo passo é criar um modelo a partir dos artefatos gerados por esse job. Isso geralmente envolve a exportação do modelo treinado em um formato adequado para implantação.

Criar Endpoint e Realizar Testes: Com o modelo criado, é possível configurar um endpoint no AzureML para disponibilizá-lo como um serviço web. Após a configuração do endpoint, é crucial realizar testes para garantir que o modelo esteja funcionando corretamente.

Exemplo de Dados e Teste
Para demonstrar o uso do endpoint configurado, utilizamos um conjunto de dados fictício contendo informações meteorológicas. Abaixo está o JSON utilizado para testar o endpoint:
{
  "input_data": {
    "data": [
      {
        "day": 1,
        "mnth": 1,
        "year": 2022,
        "season": 2,
        "holiday": 0,
        "weekday": 1,
        "workingday": 1,
        "weathersit": 2,
        "temp": 0.3,
        "atemp": 0.3,
        "hum": 0.3,
        "windspeed": 0.3
      }
    ]
  }
}
O resultado obtido do teste foi o seguinte:

[
  358.13221320531335
]

