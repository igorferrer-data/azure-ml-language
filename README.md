# Inteligência Artificial (IA) com Azure - Language Studio
Objetivo criar a configuração e realizar de usabilidade.

Dê aos seus aplicativos a capacidade de ouvir, entender e até mesmo falar com seus clientes com recursos como fala para texto e texto para fala.

- Primeiro teste: Transformar um audio em texto.

- Segundo teste: Analisar um texto (Positivo/Nuetro/Negativo)

### Ferramentas utilizadas:
- Portal Azure: https://portal.azure.com
- Portal Laguage Studio: laguage.cognitive.azure.com
- Portal Speech: https://speech.microsoft.com/portal

### Pontos Importantes:
- Caso esteja realizando apenas um prática de estudo, no final excluir tudo que foi construído nesse laboratório. Desta forma, minimiza o risco de ser cobrado algum valor. Lembre-se você está em um ambiente real de produção.
- Documentação:
    + https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/06-text-analysis.html
    + https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/09-speech.html

### Resumo (Passo-a-passo):

- Entrar no ambiente Azure

### Detalhamento (Passo-a-passo):

01 - Após logar no portal Azure. Iremos criar um ``` Create a resource  ```, selecionar ``` AI + Machine Learning  ``` e escolher a opção ``` Language service  ```.
![image](https://github.com/user-attachments/assets/a4ed19b3-b179-4cd1-8589-308ab6917407)

02 - Após clicar no botão para clicar no botão ``` Create  ``` da opção de serviço: ``` Language service  ```. Apresentara uma nova tela com as opções de serviço e caso queira adicionar outros também permitirá. No nosso caso, mantém as opções padrão de serviço, pois é o suficiente. Então clicamos no botão ``` Continue tp create your resource  ```.
![image](https://github.com/user-attachments/assets/dd8cb228-9a2a-477f-8bea-53d2dfe229b5)

03 - Iniciar a configuração criando o repositório onde será salvo nosso projeto, modelo, laboratório. Fique a vontade para chamar do melhor padrão para sua necessidade.
   * Subscription: é a conta que você está logado. É como se você a sua empresa. Repositótorio geral de tudo que é criado, a Pasta principal. Já vem preenchido de padrão, Esse padrão é criado automaticamente quando realiza o cadastro. Mas pode ser criado outras opções.
   * Resource group: é uma sub-repositório do "Subscription".
Imagina uma gaveteiro onde o gaveteiro inteiro é Subscriptiom e uma gaveta desse gaveteiro é o Resource group.
   * Region: basicamente, quer dizer em qual servidor da Microsoft você quer salvar(Brasil, USA etc). Acredito que também determina a moeda que será cobrado por utilizar esse serviço.
   * Name: nome do seu projeto, modelo (Deve ser único)
   * Pricing tier: O método de cobrança. Nesse nosso caso vamos selecionar a opção Free por 3 dias.
   * Check box: "By checking this box I certify that I have reviewed and acknowledge the terms in the Responsible AI Notice". Deve marcar, pois precisa aceitar os termos e condições.
   ![image](https://github.com/user-attachments/assets/48731618-f04f-47d5-ba3c-a3186f12b07b)

04 - Demais Abas: vamos manter o padrão, pois estamos realizando uma configuração basica e iremos excluir esse modelo no final. Então, click no botão ``` Review + create ``` para validar as configurações e depois click novamente no botão ``` Create ``` 
   * Networking: configuração de privacidade do seu modelo(Publico/Privado)
   * Identity: usar o controle de acesso
   * Tags: muito usado para criar filtros. Por exemplo: Quero fazer rateio para lançamento de custo por Departamento, então, cria as tags por departamento. Conforme sua necessidade.
   ![image](https://github.com/user-attachments/assets/1b88a9bd-dc97-4ee0-ac4f-31d3b765a92c)

### PORTAL: https://speech.microsoft.com/portal

05 - Entrar no portal: "https://speech.microsoft.com/portal" e criar o recurso. Caso já tenha um recurso criado, pode utilizar o mesmo.
![image](https://github.com/user-attachments/assets/d2f8d35d-13ab-409b-9f2c-90a607f0f57e)

Preencher os dados solicitados, clicar em ``` Create resource ```:
   * Name of new resource: nome do projeto, modelo que será criado
   * Subscription: Já vem preenchedo com o padrão da sua conta criada. Caso, tenha mais de uma conta, selecionar a melhor para sua solução.
   * Region: basicamente, quer dizer em qual servidor da Microsoft você quer salvar(Brasil, USA etc). Acredito que também determina a moeda que será cobrado por utilizar esse serviço.
   * Pricing tier: O método de cobrança. Nesse nosso caso vamos selecionar a opção "Standard S0"
   * Resource group: Selecionar o recurso criado nos primeiro passos no portal da Azure.
   ![image](https://github.com/user-attachments/assets/6549aeba-07a9-4bd6-83d8-57b9e6457fa7)

06 - Próximo passo, selecionar o resource e clicar no botão ``` Use resource ```. Informando o sistema que você quer usar esse "cara". Pois pode ser que tenha mais uma opção.
![image](https://github.com/user-attachments/assets/a15ac0d6-523f-4188-aba3-23dce2cb5b18)

07 - Testar a funcionalidade "Conversão de falar em texto em tempo real".
   * Na tela principal selecionar a opção:  ``` Real-time speech to text ```
   * Quando abrir a tela deve:
       * marcar o check box, qu está ciente que está usando o recurso XXX.
       * Selecionar o idioma do audio que vai inputar na ferramenta.
       * Adicionar o audio que será testado. 
![image](https://github.com/user-attachments/assets/5f68430f-567d-4f2c-ad1b-c51724ee677e)

Resultado do teste:
![image](https://github.com/user-attachments/assets/68f00b51-3b26-4e85-b087-4245467dee1b)

### PORTAL: https://language.cognitive.azure.com/

08 - Ao entrar no portal: https://language.cognitive.azure.com/, a ferramenta vai solicitar algumas configurações conforme a tela abaixo. Nada diferente que já tenha visto diferente.

O único campo diferente é o ``` Resource type ```. Essa opção é para selecionar o tipo de serviço que gostaria de realizar. Pois essa ferramente, atualmente trabalha com mais de um tipos de serviço. No nosso caso usar ``` Language ```.

![image](https://github.com/user-attachments/assets/a875e01f-6305-451b-9b78-897a76086138)

09 - Testar a funcionalidade "Sentiment and opinion mining tryout". Para isso selecionar primeiro: ``` Classify text ``` e depois ``` Analyze setiment and mine opinion ```.
Essa tela é bem similar do teste anterior, mas neste caso, você vai digitar um texto ou importar e a ferramenta vai analisar o texto. Usamos um exemplo de uma avaliação de um curso.
![image](https://github.com/user-attachments/assets/ace95e72-1f4d-47ee-9142-de8069db17b9)
