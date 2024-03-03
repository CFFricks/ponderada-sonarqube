# ponderada-sonarqube

# SonarQube
O sonarqube é uma plataforma utilizada por desenvolvedores de software para medir, avaliar e aprimorar a qualidade do código-fonte. A ferramenta permite identificar e corrigir problemas de forma proativa, melhorar a manutenção e assegurar a aderência a padrões de código. 
Incorporando o SonarQube ao ciclo de vida do desenvolvimento de software, as equipes podem aprimorar significativamente a qualidade do código, resultando em aplicações mais seguros, robustos e de fácil manutenção 
## Conceitos Principais

### Qualidade do Código
A qualidade do código é uma medida que reflete quão limpo, eficiente e seguro o código-fonte é. Um código de alta qualidade é mais fácil de ler, entender, testar e manter. SonarQube ajuda a identificar problemas que afetam a qualidade do código, como bugs e vulnerabilidades de segurança

### Análise Estática
Sonarqube realiza análise estática do código-fonte. Isso significa que ele examina o código sem executá-lo, identificando padrões que podem indicar problemas, permitindo detectar e corrigir problemas precocemente no ciclo de desenvolvimento.


## Vou fazer um passo a passo sobre a configuração do SonarQube:
### Primeiro eu subi as informações do SonarQube no docker pelo comando docker compose up -d:
<img src="/imgs/img1.jpg">
<img src="/imgs/img2.jpg">

### Depois acessei o sonarquebe na web pelo http://localhost:9001/ que foi a minha porta escolhida:
<img src="/imgs/img3.jpg">

#### Depois desse passo, eu tive que recomeçar pelo computador da Maria Luisa, pois o meu dotnet SDK não estava baixando.

### Instalando o SonarScaner para .NET Core pelo comando dotnet tool install -–global dotnet-sonarscaner:
<img src="/imgs/img4.png">

#### Para analisar o código rodei os comandos alterando o que era pedido:  
dotnet sonarscanner begin /k:"ponderada" /d:sonar.login=admin /d:sonar.password=admin : 
<img src='/imgs/img5.png'>


dotnet build <path_to_solution.sln> :
<img src="/imgs/img6.png">

dotnet sonarscanner end /d:sonar.login=admin /d:sonar.password=admin : 
<img src="/imgs/img7.png">

#### Resultando:
<img src="/imgs/img8.png">

## Mostrando a interface do sonarScaner:
<img src="/imgs/img9.png">
<img src="/imgs/img10.png">

