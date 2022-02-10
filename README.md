# EQI Simulador de Investimentos | Teste Front-End
Este é o repositório de um Simulador de Investimentos feito para a empresa EQI Investimentos (Front-end).

Requisitos para utilização do sistema:
* NodeJS
* NPM

- Esse projeto eu fiz utilizando HTML, CSS e Javascript e Bootstrap. 
- Utilizei também algumas bibliotecas Jquery para atribuir máscaras nos campos e montar o gráfico. São elas:
  - Mask.js
  - MaskMoney.js
  - Chart.js

## Como simular um investimento
Primeiramente faça o download ou clone este repositório, execute `npm install` e `npx json-server db.json`.<br>
Feito isso, a API Fake já está rodando no seu http://localhost:3000;<br>
Em seguida, abra o arquivo 'index.html' que está localizado dentro da pasta 'src';


## Tela Inicial
![Tela Inicial](https://user-images.githubusercontent.com/73489159/153093031-47997e05-db4f-4d08-b465-9d3be9435869.png)
Temos uma tela com 2 botões para o usuário escolher o tipo de Rendimento do investimento, sendo eles: Bruto e Líquido. Temos também outros 3 botões para definir o tipo de indexação utilizado.
Logo abaixo temos 6 campos de texto, onde os 4 primeiros são para o usuário inserir valores e os dois ultimos são somente para leitura, onde estão sendo alimentados pela nossa API.

Logo abaixo temos dois botões, um que reseta todos os campos editáveis e um botão é responsável por simular o investimento, porém o mesmo só é habilitado após o preenchimento de todos os campos anteriores. 

### Campos Preenchidos
![Campos preenchidos](https://user-images.githubusercontent.com/73489159/153100239-7447f941-902a-46cf-ad3f-c71a89216150.png)
Aqui temos uma imagem de como os campos ficam após serem preenchidos pelo usuário e o botão de simular o investimento habilitado.

#### Validação dos Campos
Para validação dos campos utilizei duas bibliotecas de máscara para os inputs (JQuery), sendo assim o usuário não consegue digitar outra coisa a não ser números e o valor já fica formatado para melhor legibilidade.
A validação feita para verificar se todos os campos estão preenchidos é feita após tirar o foco do input.

### Tela Após Simulação
![Resultados da Simulação](https://user-images.githubusercontent.com/73489159/153100487-2cebdd27-459b-43c4-8e30-7da58acfdb67.png)
Após simular o investimento, os resultados aparecem no lado direito da tela, os valores vem através da requisição para a API Fake e são valores diferentes conforme a seleção do tipo de Rendimento e Tipo de Indexação.

Para fazer o gráfico, utilizei uma biblioteca chamada Chart.js, onde atribuo os valores que vem da API para o gráfico.

### Telas Mobile
![TelaMobile](https://user-images.githubusercontent.com/73489159/153319058-134883fd-7c34-4776-9d7a-7b37185cbaa0.png)<br>
Tela mobile inicial
<br>

![Tela Mobile](https://user-images.githubusercontent.com/73489159/153102818-43bfff0a-bc65-489b-845d-1bb88181da64.png)<br>
Tela mobile com os dados preenchidos
<br>

![TelaMobileResultados](https://user-images.githubusercontent.com/73489159/153319142-c6aeb14f-c40b-40b6-b038-c0436f2f8790.png)<br>
Resultados aparecendo em uma tela Mobile
