# Faculdade de Informática e Administração Paulista 

<p align="center">
  <a href="https://www.fiap.com.br/">
    <img src="docs/examples/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" width="40%" />
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

Nesta entrega treinamos o modelo **YOLOv5** para reconhecer dois objetos distintos: **Escova** e **Martelo**.  
As imagens foram rotuladas no [Make Sense AI](https://www.makesense.ai/) e divididas em treino, validação e teste.  
O objetivo foi avaliar como o número de épocas impacta no desempenho do modelo.

---

## Resultados Comparativos

| Modelo (Épocas) | Objetos Detectados (de 10) | mAP50 (Validação) | Precisão (Validação) | Recall (Validação) | Observações |
|-----------------|-----------------------------|-------------------|-----------------------|---------------------|-------------|
| 30              | 4                           | 0.480             | 0.247                 | 0.401               | Sub-treinado, muitas falhas (falsos negativos). |
| 60              | 9                           | 0.825             | 1.000                 | 0.684               | Grande melhoria, quase perfeito nos martelos. |
| 90              | 9                           | 0.886             | 0.957                 | 0.800               | Mais refinado, mas ainda com falhas. |
| 120             | 10                          | 0.902             | 0.963                 | 0.695               | **Melhor modelo**, identificou todos os objetos e maior mAP.|

---

## Exemplos de Detecção

Exemplos de imagens detectadas no conjunto de teste (bounding boxes):

![Exemplo 1](results/teste1.jpg)  
![Exemplo 2](results/teste2.jpg)  
![Exemplo 3](results/teste3.jpg)

---

## Gráfico de Treinamento

O gráfico gerado pelo YOLO durante o treinamento (`results.png`) mostra a evolução de **loss**, **precisão**, **recall** e **mAP** ao longo das épocas.

![Gráfico de Treino](results/results.png)

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