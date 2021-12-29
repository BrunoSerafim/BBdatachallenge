# BB Data Challenge - Fila de atendimento
Competição interna realizada para criação de um modelo de machine learning que pudesse prever os dias com elevada demanda onde o início do atendimento nas filas dos caixas supere 15 minutos.   

>ID; ID_UOR; TS_INC_EPR; TS_INC_CHMD

>0; 0; 01/09/2020 10:01; 01/09/2020 10:02

>1; 0; 01/09/2020 10:04; 01/09/2020 10:22

>2; 0; 01/09/2020 10:16; 01/09/2020 10:25

Onde:

>ID - Código identificador único para cada protocolo gerado;

>ID_UOR - Código de identificação da UOR da agência, indicado por uma sequência de 0 a 24;

>TS_INC_EPR – Timestamp do início de espera, ou seja, a data e hora da emissão do protocolo;

>TS_INC_CHMD – Timestamp da primeira chamada do protocolo.

Os protocolos deverão ser agrupados por faixa de horário. Atendimentos antes das 10h devem ser contabilizados como entre 10h00 e 10h59 e atendimentos iniciados após as 14h devem ser contabilizados como entre 14h00 e 14h59.

Deve ser calculado o PC_ACI_PZ (percentual acima do prazo) que é a razão entre os atendimentos que foram iniciados após 15 minutos da emissão da senha e os atendimentos totais naquela faixa horária. A submissão deve ser realizada com os ID fornecidos no dataset X e o PC_ACI_PZ calculado pelo modelo.

# Submissão
Em relação a submissão, foi utilizado o RMSE (root mean squared error) para classificação dos trabalhos. Embora o modelo de Deep Learning tenha apresentado o melhor RMSE na base de teste, o modelo que apresentou o melhor resultado na plataforma de submissão dos trabalhos foi o Catboost. Isso ocorreu devido a base de dados de treino não conter o mês de agosto, e o dataset para submissão conter apenas atendimentos do mês de agosto.  
