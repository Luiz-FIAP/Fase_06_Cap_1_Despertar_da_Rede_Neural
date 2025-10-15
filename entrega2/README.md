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

# Fase 6 – Entrega 2 – Comparação de Abordagens (YOLO vs CNN)

Nesta entrega comparamos diferentes arquiteturas de visão computacional aplicadas ao mesmo dataset de **Escova** e **Martelo**.  
O objetivo foi avaliar vantagens e desvantagens de cada abordagem em termos de **precisão**, **tempo de treino**, **tempo de inferência** e **facilidade de uso**.

---

## Modelos Avaliados

1. **YOLO Adaptável (Customizado)** – treinado na Entrega 1 com dataset próprio (30, 60, 90 e 120 épocas).  
2. **YOLO Padrão** – rede pré-treinada utilizada sem customização.  
3. **CNN do Zero** – rede convolucional simples implementada e treinada a partir do zero no mesmo dataset.  

---

## Resultados CNN – Treinada do Zero (Classificação)

- **30 Épocas**: Modelo ainda confuso, erra várias imagens com alta confiança no erro (ex: escovas como martelos).  
- **60–90 Épocas**: Precisão melhora drasticamente. Erros raros e com baixa confiança. Curvas de acurácia sobem e perda diminui.  
- **120 Épocas**: Atingiu **100% de acurácia de classificação** no conjunto de testes.  

**Avaliação**: Excelente para responder *“Esta imagem contém um martelo ou uma escova?”*.  
Mas incapaz de dizer **onde** o objeto está ou detectar múltiplos objetos.

---

## Análise Crítica Comparativa

### 1. Facilidade de Uso/Integração
- **YOLO Padrão**: O mais fácil. Não requer treinamento, basta carregar. Bom para protótipos rápidos.  
- **YOLO Adaptável**: Dificuldade intermediária. Exige anotação manual e configuração, mas frameworks simplificam.  
- **CNN do Zero**: O mais difícil. Requer conhecimento em arquiteturas, funções de ativação, otimizadores, etc.  

### 2. Precisão do Modelo
- **YOLO Padrão**: Muito baixa, falhou em classes customizadas.  
- **CNN do Zero**: Alta (para classificação), atingiu 100% no teste.  
- **YOLO Adaptável**: A mais alta, 100% de acurácia na detecção e localização com 120 épocas.  

### 3. Tempo de Treinamento/Customização
- **YOLO Padrão**: Nenhum (zero customização).  
- **YOLO Adaptável**: Médio, maior custo na anotação das imagens.  
- **CNN do Zero**: Alto, pois além do treino exige projetar e ajustar a arquitetura.  

### 4. Tempo de Inferência (Predição)
- **CNN do Zero**: O mais rápido, poucos ms por imagem.  
- **YOLO Padrão**: Rápido (~20ms por imagem).  
- **YOLO Adaptável**: Rápido também (~27ms por imagem).  

---

## Conclusão Final

| Abordagem     | Tarefa       | Facilidade | Precisão | Custo (Tempo) | Velocidade | Veredito |
|---------------|--------------|------------|----------|---------------|------------|----------|
| YOLO Padrão   | Detecção     | ★★★       | ☆☆☆    | ☆☆☆          | ★★☆      | Inadequado – falha em classes customizadas. |
| CNN do Zero   | Classificação| ★☆☆       | ★★★    | ★☆☆          | ★★★      | Eficaz, mas incompleto (diz *o quê*, mas não *onde*). |
| YOLO Adaptável| Detecção     | ★★☆       | ★★★    | ★★☆          | ★★☆      | **Solução ideal** – preciso, completo e resolve o problema real. |

Para o objetivo de detectar martelos e escovas de dente em imagens, a abordagem de fine-tuning com **YOLO Adaptável** é, sem dúvida, a melhor solução.  
Apesar do trabalho inicial na preparação de dados, ela gera um modelo especialista, robusto e confiável.  
O YOLO Padrão serve como demonstração de limitações de modelos generalistas, enquanto a CNN de classificação é eficaz mas insuficiente para tarefas de detecção.

---

## Acesso ao Dataset e Resultados Completos

Para não sobrecarregar o repositório, o dataset completo e todos os resultados foram armazenados no Google Drive do grupo:

[Acessar Editar Colab](https://colab.research.google.com/drive/1VWfnKT9DSHvnZYkYOvalKQRPiONKgcQX?usp=sharing)
[Acessar dataset e resultados no Drive](https://drive.google.com/drive/folders/1Zt-C7CjrsTF_jqeGo3UnyPNfnPQe9gkj?usp=sharing)

---

## Vídeo

O vídeo com a demonstração dos resultados está disponível no YouTube (não listado):  
([link do vídeo](https://youtu.be/Dd15XC_cJdU))

---
