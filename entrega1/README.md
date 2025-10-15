# Faculdade de Informática e Administração Paulista 

<p align="center">
  <a href="https://www.fiap.com.br/">
    <img src="../Ir_alem2/docs/examples/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" width="40%" />
  </a>
</p>

<br>

## Grupo 32

## Integrantes: 
- <a href="https://github.com/FelipeSabinoTMRS">Felipe Sabino da Silva</a>
- <a href="https://github.com/juanvoltolini-rm562890">Juan Felipe Voltolini</a>
- <a href="https://github.com/Luiz-FIAP">Luiz Henrique Ribeiro de Oliveira</a> 
- <a href="https://github.com/marcofiap">Marco Aurélio Eberhardt Assimpção</a>
- <a href="https://github.com/PauloSenise">Paulo Henrique Senise</a> 

## Professores:
### Tutor(a) 
- <a href="https://github.com/Leoruiz197">Leonardo Ruiz Orabona</a>
### Coordenador(a)
- <a href="https://github.com/agodoi">André Godoi</a>

---

# Fase 6 – Entrega1 – YOLO Customizado

## Descrição

Nesta primeira entrega, a equipe da **FarmTech Solutions** desenvolveu um modelo de **visão computacional** utilizando **YOLOv5** para detectar dois objetos distintos:

- **Martelo**  
- **Escova de dente**

O objetivo foi demonstrar ao cliente fictício da FarmTech a aplicabilidade da detecção de objetos em cenários reais, organizando o dataset, treinando a rede e avaliando seu desempenho.

---

## Resultados Comparativos

| Modelo (Épocas) | Objetos Detectados (de 10) | mAP50 (Validação) | Precisão (Validação) | Recall (Validação) | Observações |
|-----------------|-----------------------------|-------------------|-----------------------|---------------------|-------------|
| 30              | 4                           | 0.480             | 0.247                 | 0.401               | Sub-treinado, muitas falhas (falsos negativos). |
| 60              | 9                           | 0.825             | 1.000                 | 0.684               | Grande melhoria, quase perfeito nos martelos. |
| 90              | 9                           | 0.886             | 0.957                 | 0.800               | Mais refinado, mas ainda com falhas. |
| 120             | 10                          | 0.902             | 0.963                 | 0.695               | **Melhor modelo**, identificou todos os objetos e maior mAP.|

---

## Metodologia

1. **Organização do Dataset**  
   - 40 imagens de martelo + 40 imagens de escova.  
   - Divisão em **treino (32)**, **validação (4)** e **teste (4)** para cada classe.  

2. **Rotulação**  
   - As imagens foram anotadas no [Make Sense AI](https://www.makesense.ai/).  
   - As anotações foram exportadas no formato YOLO e salvas em `entrega1/labels/`.  

3. **Treinamento no Google Colab**  
   - O modelo YOLOv5 foi treinado com diferentes números de épocas: **30, 60, 90 e 120**.  
   - Utilização de GPU gratuita do Colab.  
   - Resultados salvos automaticamente na pasta `runs/train/exp/`.  

---

## Resultados do Treinamento (YOLO Customizado)

- Foram realizados treinos com **30, 60, 90 e 120 épocas**.  
- A cada aumento de épocas, a acurácia do modelo melhorou progressivamente.  
- Com 120 épocas, o modelo atingiu **100% de acurácia nos testes**.  
- Prints de algumas imagens detectadas (martelo e escova) estão disponíveis na pasta `entrega1/results/`.

> Os gráficos de acurácia e loss não foram exportados no notebook, mas podem ser consultados no diretório `runs/train/exp/` gerado automaticamente pelo YOLO durante o treino.

---

## Exemplos de Detecção

O modelo treinado com 120 épocas foi capaz de detectar com sucesso todos os objetos do conjunto de testes:  

*(Inserir aqui imagens de `entrega1/results/` com bounding boxes)*

---

## Conclusão

O modelo treinado com **120 épocas** foi o que apresentou o melhor desempenho.  
Ele conseguiu identificar todos os objetos no conjunto de teste, alcançou as maiores métricas de confiança e obteve o maior mAP50.  

O treinamento adicional entre 90 e 120 épocas foi essencial para refinar o modelo e eliminar as maiores falhas, resultando em um detector de objetos mais confiável.

---

## Acesso ao Dataset e Resultados Completos

Para não sobrecarregar o repositório, o dataset completo e todos os resultados foram armazenados no Google Drive do grupo:

[Acessar Editar Colab](https://colab.research.google.com/drive/1VWfnKT9DSHvnZYkYOvalKQRPiONKgcQX?usp=sharing)
[Acessar dataset e resultados no Drive](https://drive.google.com/drive/folders/1Zt-C7CjrsTF_jqeGo3UnyPNfnPQe9gkj?usp=sharing)

---
