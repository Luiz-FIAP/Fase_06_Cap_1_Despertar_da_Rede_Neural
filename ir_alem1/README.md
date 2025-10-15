# Faculdade de Informática e Administração Paulista 

<p align="center">
  <a href="https://www.fiap.com.br/">
    <img src="../ir_alem2/docs/examples/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" width="40%" />
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

# Projeto ESP32-CAM – Ir Além 1

Esta pasta contém os arquivos referentes à implementação do **Ir Além 1** da Fase 6, utilizando o módulo **ESP32-CAM**.

## Conteúdo da Pasta

- **best.pt** → modelo YOLOv5 treinado na Entrega 1, usado para detecção.  
- **detector_objeto.py** → script Python que recebe as imagens do ESP32-CAM e aplica o modelo.  
- **espcam/** → código em C++ para ser gravado no ESP32-CAM (Arduino IDE / PlatformIO).  

## Funcionamento

1. O ESP32-CAM captura imagens em tempo real e envia via Wi-Fi.  
2. O script Python `detector_objeto.py` recebe essas imagens.  
3. O modelo `best.pt` (YOLOv5 treinado) faz a detecção dos objetos escolhidos (martelo e escova).  
4. As imagens resultantes são exibidas com **bounding boxes** indicando os objetos reconhecidos.  

## Vídeo de Demonstração

[https://youtu.be/RUuZz9o76YQ](Ir além 1 - ESP32-CAM)

---

## Observações

- Este projeto faz parte do **Ir Além 1**  
- A pasta contém código para reprodutibilidade, mas é necessário configurar rede Wi-Fi e ambiente Python corretamente.  

