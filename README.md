MBA IA e BigData ICMC-USP São Carlos

José Eduardo Athayde Ferrarini

Conteúdo dos arquivos
----------------------

AnaliseResultados.zip
- feedbacks_aspectos.xlsx                -> Planilha de análise de resultados das execuções dos modelos

CodigosFonte.zip
- analise_feedbacks_comparada.py          -> Arquivo código Python que executa os modelos SBERT, BerTimbau base e BerTimbau FT, utilizando Datasets feedback.json e aspectos.json. Grava resultado de saida como comparacao.json.
- analiseROC.py                           -> Script python para gera análise ROC e encontrar melhor limiar para ser usado para cada modelo
- SBERT_valida.py                         -> Script para validação dos dados gerados no dataset de treinamento para o fine-tuning
- TCC_FT_BT_ClassificaAspectos.ipynb      -> Notebook de treinamento do modelo BerTimbau, utilizando o dataset AspectClassification_fine_tuning.csv. Resultado é o modelo refinado. Foi executado no google colab para fazer uso de GPU.
- ValidaDadosScatterPlot.py               -> Script python para validar os dados e treinamento, verificando distribuição por similaridade

Dataset.zip
- AspectClassification_fine_tuning.csv    -> 5700 feedbacks para os 15 aspectos e label binária.
- aspectos.json                           -> definição dos 15 aspectos utilizada para execução do trabalho
- comparacaoLabel.json                    -> Arquivo de output da execução do analise_feedbacks_comparada.py, alterado para incluir label de classificação e é utilizado pelo Script analiseROC.py
- feedbacks.json                          -> Arquivo contendo os 15 feedbacks utilizados para testar SBERT, BerTimbau base, BerTimbau FT, ChatGPT 4, ChatGPT 5, Claude e Gemini
