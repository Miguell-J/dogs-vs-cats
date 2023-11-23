# Classificador de Imagens de Cães e Gatos com TensorFlow e Keras
Este projeto consiste em um classificador de imagens para diferenciar entre cães e gatos usando a poderosa combinação de TensorFlow e Keras. Abaixo estão detalhes sobre cada parte do código.

<div align=center>
<img src="https://s35949.pcdn.co/wp-content/uploads/2016/10/c%C3%A3es-e-gatos-1.jpg"/>
</div>

## Pré-requisitos
Antes de executar o código, certifique-se de ter as seguintes bibliotecas instaladas:

- TensorFlow
- OpenCV (cv2)
- Matplotlib
- NumPy
- Pandas
Você pode instalar essas dependências executando o seguinte comando:

```bash
pip install tensorflow opencv-python matplotlib numpy pandas
```

## Organização do Conjunto de Dados
Organize seu conjunto de dados no diretório 'data' com subdiretórios para cada classe (por exemplo, 'dog', 'cat').
O código inclui uma etapa de limpeza de dados para remover imagens inválidas. Certifique-se de colocar seu conjunto de dados no diretório 'data' antes de executar o script.

## Treinamento do Modelo
- O script carrega os dados da imagem usando a função image_dataset_from_directory do TensorFlow.
- As imagens são pré-processadas, removendo imagens inválidas e normalizando os valores de pixel para o intervalo [0, 1].
- O conjunto de dados é dividido em conjuntos de treinamento, validação e teste.
- O modelo CNN é definido e compilado com o otimizador Adam e a perda de entropia cruzada binária.
- O histórico de treinamento é visualizado usando o Matplotlib.

## Registros do TensorBoard
Os registros do TensorBoard são salvos no diretório 'logs'. Monitore o progresso do treinamento executando:

```bash
tensorboard --logdir=logs
```

## Avaliação do Modelo
Após o treinamento, o modelo é avaliado no conjunto de teste usando métricas como acurácia binária, precisão e recall.

## Predição
O script inclui exemplos de fazer previsões em novas imagens. Substitua 'cat_test.jpg' e 'dog_y.jpg' por suas próprias imagens para previsão.

## Salvando o Modelo
O modelo treinado é salvo como 'dogs_cats_classifier.h5' no diretório 'modelos'.

Sinta-se à vontade para experimentar com diferentes arquiteturas, hiperparâmetros e conjuntos de dados para melhorar o desempenho do modelo. Explore e divirta-se com o aprendizado de máquina!
