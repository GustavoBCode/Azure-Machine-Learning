# Azure Machine Learning

Este projeto foi desenvolvido com o propósito de exemplificar a aplicação do Machine Learning na plataforma Azure, proporcionando insights valiosos a partir de dados específicos armazenados em um banco de dados. Através dessa abordagem, exploramos as capacidades da tecnologia para extrair informações relevantes e impulsionar tomadas de decisão fundamentadas.

Links utilizados no projeto:
| [Explore Azure AI Services](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html) | [Explore Automated Machine Learning in Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html) |

# 1 - Criando um recurso 
1.1 - Na tela inicial clique em **Criar um recurso**.

![1](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/96185592-9c38-4127-b579-4bc2af7968f6)

1.2 - Na barra de **Categorias**, selecione **Análises** e, em seguida, clique no botão Criar.

![2](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/45c3e2c2-c675-4b46-b66f-99d09155358f)

1.3 - Se você ainda não tiver um **Grupo de Recursos**, clique em **Criar Novo** e dê o nome de **LABAI-900**. No campo **Nome**, insira **laboratorioai900**.

![3](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/c4eee6db-a5ff-4720-9226-de037fbdf4c2)

1.4 - Após este processo, clique em **Examinar + Criar**. Se aparecer **Validação Aprovada**, clique no botão Criar.

![4](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/a350d047-b823-432a-a9e1-180b0e475e35)

1.5 - Agora que a implantação foi concluída, clique em **Ir para o Recurso**.

![5](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/55ef0305-5509-437b-bb27-08da2e614e1b)

1.6 - Em seguida, clique em **Iniciar o Estúdio**.

![6](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/f7a6acdb-b7f5-4e61-8919-ebd26ab47a7f)

# 2 - Configurando o Modelos e Conjuntos de Dados

2.1 - Nesta página, clique em **ML Automatizado**.

![7](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/55c603de-b62d-48c4-8392-aa21f5c01993)


2.2 - Em seguida, crie um Novo Trabalho de **ML Automatizado**.

![8](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/1bf27d53-ccaf-4291-a05a-6bc1dd0e5990)

2.3 - Nomeie alguns campos: **Nome do Trabalho** como "mslearn-bike-automl", **Novo Nome do Experimento** como "mslearn-bike-rental", e **Descrição** como "Aprendizado de máquina para previsão de aluguel de bicicletas". Após isso, clique em **Avançar**.

![9](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/118cc8a3-65aa-412e-817b-4a1fd5a104cb)

2.4 - No campo **Selecionar Tipo de Tarefa**, escolha **Regressão** e clique em **Criar**.

![10](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/467fd03f-e4e7-4546-9348-772424450db1)

2.5 - Nomeie alguns campos: **Nome** como "alugueldebicicletas", **Descrição** como "Dados Históricos de Aluguel de Bicicletas", e Tipo como "Tabular". Em seguida, clique em **Avançar**.

![11](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/842108a5-c307-452f-9cc4-77df62d51be0)

2.6 - Selecione **De Arquivos da Web**

![12](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/95c1430c-8b3a-401b-a1d2-14ccc4d4256b)

2.7 - insira a **URL da Web** como "https://aka.ms/bike-rentals". Depois, clique em **Avançar**.

![13](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/f5a410b0-02a0-4f4b-b17c-7d73eb66b4ac)

2.8 - Modifique os **Cabeçalhos da Coluna** para **Somente os Arquivos Têm os Mesmos Cabeçalhos** e clique em **Avançar**.

![14](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/55ebfce1-e067-4020-8afe-7c3dd5f0d89e)

2.9 - Na etapa de "**Esquema**", não há alterações necessárias, clique em **Avançar**.

2.10 - Finalize o processo clicando em Criar na etapa de "Examinar".

2.11 - Selecione **alugueldebicicletas** e clique em **Avançar**.

![15](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/44562fc8-f249-4e70-9b75-39ec9a71ce0e)

2.12 - Na **Coluna de Destino**, selecione **retals (integer)**. Clique em **Exibir Definições de Configuração Adicionais**. Desative **Explicar o Melhor Modelo** e **Usar Todos os Modelos Suportados**. Em **Modelos Permitidos**, selecione **RandomForest** e **LightGBM**. Em seguida, clique em **Salvar**.

![16](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/1dfa1187-052c-4c6c-8f89-eb6f160c6a69)

2.13 - No campo **Limites**, insira os seguintes números: | 3 | 3 | 3 | 0.085 | 15 | 15 | e selecione a opção **Habilitar Encerramento Antecipado**. Em **Validar e Testar**, escolha **Divisão de Validação de Treinamento** e insira o número **10** no campo de **Validação de Percentual de Dados**. Clique em Avançar.

![17](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/56e691b5-77d4-4336-9311-2c7beef84495)

2.14 - Na etapa de "**Computação**", não há alterações necessárias, clique em **Avançar**.

2.15 - Finalize o processo clicando em **Enviar Trabalho de Treinamento** na etapa de "**Examinar**".

2.16 - Aguarde aproximadamente **15 minutos** para a conclusão da validação.

![18](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/45621eb9-2691-43cb-9cc6-efa856a843c1)

# 3 - Análise e Teste de Modelo

3.1 - Clique em **Modelo de Registro** e depois em **Avançar**. Nomeie os campos: **Nome** como "mslearnbikeauto", e **Versão** como "**1**". Em seguida, clique em **Avançar** e depois em **Registro**.

![19](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/018197c1-2e71-42a0-94f9-4cbbd02fdd2f)

3.2 - Selecione **Modelos** e em seguida, clique em **mslearn-bike-automl_2**.

![20](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/809273f4-8129-4cd2-967e-06f1e49aba73)

3.3 - Ao clicar em **Métricas**, é possível visualizar todas as métricas obtidas a partir do banco de dados.

![21](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/5677f6b7-8b9c-4de2-909b-5d7c95d8e459)

3.4 - Para testar um modelo através da ferramenta de pontos de extremidade, selecione **Pontos de Extremidade**, clique em **Criar** e, em seguida, clique em **Selecionar**.

![22](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/babd26c6-aaea-42e6-9f08-bd207f860a66)

3.5 - Clique em **Implantar**

![23](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/a66e739d-6fef-412c-ae85-a720f6e9ab1b)

3.6 - Após um longo tempo de espera, clique em **Testar** e copie o código abaixo. Em seguida, cole o código no campo **Input** e clique em **Teste**.

![24](https://github.com/GustavoBCode/Azure-Machine-Learning/assets/146696103/c9f7f6c5-5e02-4f71-a83b-1190f3156959)


``` JASON
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
```

3.7 - Após realizar o teste, o resultado obtido foi: **361.95**.










