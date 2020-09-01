# Tecnologias utilizadas
- [Ruby](https://www.ruby-lang.org/pt/)
- [Cucumber](https://cucumber.io/)
- [Capybara](https://www.rubydoc.info/github/jnicklas/capybara)
- [HTTParty](https://www.rubydoc.info/github/jnunemaker/httparty/HTTParty/ClassMethods)
- [Chromedriver](https://chromedriver.chromium.org/downloads)

# Funcionalidades
- Automação de testes dos Endpoints de pedidos e pagamentos da API
- Automação de testes de interface do ambiente de Sandbox referente à pedidos

# Como executar os testes da API
Para executar os testes da API deve-se possuir instalado o **Ruby**, **Bundle**, clonar o projeto e executar os seguintes comandos dentro da pasta "api/"
- *bundle install*
- *cucumber -t @pedido* (para executar os testes referente aos endpoints de pedidos)
- *cucumber -t @pagamento* (para executar os testes referente aos endpoints de pagamentos)
- *cucumber* (para executar testes tanto de pedidos, quanto de pagamentos)

**_Observações: A execução dos testes gera um relatório de report em HTML dentro de api/log. Facilita na visualização dos cenários executados, e se deram certo (verde) ou falharam (vermelho)._**

# ChromeDriver
- Para rodar os testes de interface, é necessário possuir o ChromeDriver.
- Verifique a versão do chrome [aqui](https://chromedriver.storage.googleapis.com/LATEST_RELEASE)
- Baixe a versão do ChromeDriver compatível com o seu navegador [aqui](https://chromedriver.storage.googleapis.com/index.html)
- Por fim, mova o ChromeDriver para o diretório correto:
- *sudo mv chromedriver /usr/local/bin* 

# Como executar os testes de Interface

Para executar os testes de Interface deve-se possuir instalado o **Ruby**, **Bundle**, **ChromeDriver**, clonar o projeto e executar os seguintes comandos dentro da pasta "interface/"
- *bundle install*
- *cucumber -t @buscarpedido* (para executar os testes referente a busca de pedidos)
- *cucumber -t @loginFail* (para executar os testes referente as falhas de login) (recomendo rodar por ultimo por conta do problema comentado nas observações)
- *cucumber* (para executar testes referente a busca de pedido, e falhas no login)

*Observações: Alguns empecilhos quanto ao teste de interface, por conta da inconstância dos **alerts** da aplicação. Outro problema quanto
ao login, por conta da validação de **robô** quando é realizado multiplas tentativas de login. Por conta disso, pode acontecer
falhas na execução dos testes*
