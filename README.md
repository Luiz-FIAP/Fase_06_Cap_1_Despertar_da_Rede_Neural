# Faculdade de Informática e Administração Paulista 

<p align="center">
  <a href="https://www.fiap.com.br/">
  <img src="https://github.com/Luiz-FIAP/Fase_06_Cap_1_Despertar_da_Rede_Neural/blob/main/Ir_alem2/docs/examples/logo-fiap.png?raw=true" width="40%" />
  </a>
</p>

<br>

# Sistema de Modelo de Visão Computacional com YOLO e ESP32-CAM

---

## **Fase 6 - Cap 1: Despertar da Rede Neural**

### **Descrição Rápida do Projeto**

Este projeto faz parte da Fase 6 da FIAP, onde desenvolvemos uma rede neural para visão computacional. A FarmTech Solutions está expandindo seus serviços de IA para além do agronegócio, atuando em áreas como saúde animal, segurança patrimonial, controle de acessos e análise de documentos, com foco especial em visão computacional.

O objetivo é criar um sistema de visão computacional usando YOLO que demonstre seu potencial e acurácia, comparando diferentes abordagens de redes neurais para classificação e detecção de objetos.

---

## **Grupo 32**

### **Integrantes:** 
- <a href="https://github.com/FelipeSabinoTMRS">Felipe Sabino da Silva</a>
- <a href="https://github.com/juanvoltolini-rm562890">Juan Felipe Voltolini</a>
- <a href="https://github.com/Luiz-FIAP">Luiz Henrique Ribeiro de Oliveira</a> 
- <a href="https://github.com/marcofiap">Marco Aurélio Eberhardt Assimpção</a>
- <a href="https://github.com/PauloSenise">Paulo Henrique Senise</a> 

### **Professores:**
#### Tutor(a) 
- <a href="https://github.com/Leoruiz197">Leonardo Ruiz Orabona</a>
#### Coordenador(a)
- <a href="https://github.com/agodoi">André Godoi</a>

---

## **Descrição Detalhada do Projeto**

### **Entrega 1: Sistema de Visão Computacional com YOLO Customizado**

Como parte do time de desenvolvedores da FarmTech, criamos um sistema de visão computacional para demonstrar o potencial da tecnologia YOLO a um cliente. O projeto utiliza um dataset personalizado com dois objetos distintos: **Escova de Dente** e **Martelo**.

#### **Metas Alcançadas:**
- ✅ Dataset organizado com 100 imagens (50 de cada objeto)
- ✅ Divisão estratégica: 40 imagens para treino, 5 para validação e 5 para teste por classe
- ✅ Organização no Google Drive com estrutura de pastas adequada
- ✅ Rotulação completa das imagens usando Make Sense IA
- ✅ Notebook Colab integrado ao Google Drive
- ✅ Múltiplas simulações com diferentes épocas (30, 60, 90, 120)
- ✅ Análise comparativa de acurácia, erro e desempenho
- ✅ Documentação completa dos resultados

### **Entrega 2: Comparação de Abordagens de Redes Neurais**

Implementamos e comparamos três abordagens diferentes:

1. **YOLO Customizado** (Entrega 1)
2. **YOLO Tradicional** (Padrão)
3. **CNN Treinada do Zero**

#### **Critérios de Avaliação:**
- Facilidade de uso/integração
- Precisão do modelo
- Tempo de treinamento/customização
- Tempo de inferência (predição)

---

## **Estrutura do Projeto**

```
📁 Fase_06_Cap_1_Despertar_da_Rede_Neural/
├── 📁 ESP-CAM/                    # Código para ESP32-CAM
│   ├── best.pt                    # Modelo treinado
│   ├── detector_objeto.py         # Script de detecção
│   └── espcam/espcam.ino         # Código Arduino
├── 📁 Imagens/                    # Dataset organizado
│   ├── 📁 Escova/
│   │   ├── 📁 treino/            # 40 imagens
│   │   ├── 📁 validação/         # 5 imagens
│   │   └── 📁 teste/             # 5 imagens
│   └── 📁 Martelo/
│       ├── 📁 treino/            # 40 imagens
│       ├── 📁 validação/         # 5 imagens
│       └── 📁 teste/             # 5 imagens
├── 📁 Labels/                     # Arquivos de rotulação YOLO
├── 📁 Modelos/                    # Resultados dos treinamentos
│   ├── 📁 CNN_30_epochs/
│   ├── 📁 CNN_60_epochs/
│   ├── 📁 CNN_90_epochs/
│   ├── 📁 CNN_120_epochs/
│   ├── 📁 Yolo_30_epochs/
│   ├── 📁 Yolo_60_epochs/
│   ├── 📁 Yolo_90_epochs/
│   ├── 📁 Yolo_120_epochs/
│   └── 📁 Yolo_padrao/
└── treino.ipynb                  # Notebook principal
```

---

## **Tecnologias Utilizadas**

- **Python 3.x**
- **YOLOv5** - Detecção de objetos
- **TensorFlow/Keras** - CNN personalizada
- **OpenCV** - Processamento de imagens
- **Google Colab** - Ambiente de desenvolvimento
- **Google Drive** - Armazenamento de dados
- **Make Sense IA** - Rotulação de imagens
- **ESP32-CAM** - Implementação em hardware
- **Arduino IDE** - Programação do microcontrolador

---

## **Resultados e Análises**

### **Comparativo de Modelos por Épocas**

| Modelo | 30 Épocas | 60 Épocas | 90 Épocas | 120 Épocas |
|--------|-----------|-----------|-----------|------------|
| **YOLO Customizado** | ✅ | ✅ | ✅ | ✅ |
| **CNN do Zero** | ✅ | ✅ | ✅ | ✅ |
| **YOLO Padrão** | ✅ | - | - | - |

### **Métricas de Performance**

Os resultados detalhados, incluindo gráficos de acurácia, perda e exemplos de detecção, estão disponíveis na pasta `Modelos/` e documentados completamente no notebook principal.

---

## **Como Executar o Projeto**

### **1. Acesso ao Notebook**
- **Link do Colab:** [Abrir no Google Colab](https://colab.research.google.com/drive/1VWfnKT9DSHvnZYkYOvalKQRPiONKgcQX?usp=sharing)
- **Link do Drive:** [Acessar Dataset](https://drive.google.com/drive/folders/1Zt-C7CjrsTF_jqeGo3UnyPNfnPQe9gkj?usp=sharing)

### **2. Pré-requisitos**
```bash
# Instalar dependências (já incluído no notebook)
!pip install ultralytics
!pip install opencv-python
!pip install tensorflow
```

### **3. Execução Local**
```bash
# Clonar o repositório
git clone https://github.com/Luiz-FIAP/Fase_06_Cap_1_Despertar_da_Rede_Neural.git

# Navegar para o diretório
cd Fase_06_Cap_1_Despertar_da_Rede_Neural

# Executar o notebook
jupyter notebook treino.ipynb
```

---

## **Demonstração em Vídeo**

**[Link do Vídeo Demonstrativo](https://youtube.com/watch?v=PLACEHOLDER)** *(até 5 minutos)*

O vídeo demonstra:
- Funcionamento do sistema de detecção
- Comparação entre os modelos
- Resultados práticos com ESP32-CAM
- Análise de performance

---

## **Conclusões e Insights**

### **Principais Descobertas:**

1. **YOLO Customizado**: Excelente para detecção em tempo real com boa precisão
2. **CNN do Zero**: Maior controle sobre a arquitetura, mas requer mais tempo de treinamento
3. **YOLO Padrão**: Rápido para implementar, mas menos preciso para objetos específicos

### **Recomendações:**
- Para aplicações em tempo real: **YOLO Customizado**
- Para máxima precisão: **CNN com 120+ épocas**
- Para prototipagem rápida: **YOLO Padrão**

---

## **Referências e Recursos Adicionais**

- [Documentação YOLOv5](https://github.com/ultralytics/yolov5)
- [Make Sense IA](https://www.makesense.ai/)

---

## **Licença**

Este projeto é desenvolvido para fins acadêmicos como parte do curso da FIAP.

---

## **Contato**

Para dúvidas ou sugestões, entre em contato com qualquer membro do **Grupo 32** através dos links do GitHub fornecidos acima.

---

*Projeto desenvolvido com 💙 pelo Grupo 32 - FIAP 2025*
