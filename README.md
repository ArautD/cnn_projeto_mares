# CNN para Classificação de Marés

Este repositório contém um projeto de Machine Learning que utiliza uma Rede Neural Convolucional (CNN) para classificação de imagens de marés em diferentes categorias (maré baixa, mediana e alta). <br/>

O script utilizado para coleta de imagens no GEE (Google Earth Engine) pode ser encontrado no seguinte repositório: https://github.com/ArautD/coleta_de_imagens_gee. <br/>
As imagens de treino podem ser encontradas em: https://drive.google.com/drive/folders/1o8pYNUYthiJmWrKMQ4RkteXOGKCKQlTi?usp=sharing. <br/>
As imagens de teste podem ser encontradas em: https://drive.google.com/drive/folders/1_D5Onxg2JwQNhdwAq1wIHUuD0aiK0zLD?usp=drive_link. <br/>

# 📄 Descrição do Projeto

O projeto realiza a classificação de imagens de marés utilizando uma CNN. As imagens são pré-processadas, divididas em conjuntos de treino, validação e teste, e um modelo é treinado para prever a classe da maré.

# 🔧 Treinamento do Modelo

O modelo é treinado utilizando o seguinte trecho de código:

history = model.fit(X_train_gen, y_train_gen, epochs=epochs, batch_size=batch_size, validation_data=(X_val_gen, y_val_gen))

# 📊 Avaliação do Modelo

Após o treinamento, o modelo é avaliado com dados de teste:

scores = model.evaluate(X_test, y_test, batch_size=batch_size)
print(f"Acurácia do modelo: {scores[1] * 100:.2f}%")

# 📁 Exportação do Modelo

model.save('/content/drive/MyDrive/projeto_mares/models/CNN_MARE_model_AP-CE.h5')

📈 Visualizações

Diversas visualizações são geradas durante o treinamento:

Curva de Acurácia: figs/curve_accuracyTrain.png

Curva de Loss: figs/curve_lossTrain.png

Matriz de Confusão: figs/confusion_matrix.png

# 🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para enviar PRs ou abrir issues.
