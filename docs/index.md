<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;Nome do Projeto&gt;*
</center></font>

>*Observação 1: A estrutura inicial deste documento é só um exemplo. O seu grupo deverá alterar esta estrutura de acordo com o que está sendo solicitado na disciplina.*

>*Observação 2: O índice abaixo não precisa ser editado se você utilizar o Visual Studio Code com a extensão **Markdown All in One**. Essa extensão atualiza o índice automaticamente quando o arquivo é salvo.*

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do projeto](#introdução-do-projeto)
- [Análise de requisitos funcionais e não-fucionais](#descrição-dos-requisitos)
- [Diagrama de casos de uso](#diagrama-de-comportamento-atores)
- [Descrição dos casos de uso](#descrição-das-funcões)
- [Diagrama de senquencia](#diagrama-de-ordem-interações)
- [Diagrama de classes](#diagrama-orientado-objetos)
- [Diagrama de componentes](#diagrama-estrutura-componente)
- [Decisões de arquitetura](#decisões-de-arquitetura)
- [Diagrama de implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Victor Oliveira Santos
* Renan Silva Nunes
* Vinicius Melo
* Rapha De Lucca



# Descrição do projeto

Neste repositório, trabalhamos para aprimorar a entrega de pizzas da Pizza-Express, recuperar vendas perdidas e enfrentar a concorrência que garante entregas rápidas. Nosso foco é desenvolver sistemas para lidar com pedidos e otimizar a produção de pizzas nas lojas. Valorizamos a colaboração e estamos abertos a contribuições externas.

# Análise de requisitos funcionais e não-funcionais
&lt;*Requisitos Funcionais:*

Projeto 1: Sistema de Atendimento e Localização

1. *Sistema de Pedidos*
   - Os clientes devem ser capazes de fazer pedidos de pizza de forma rápida e intuitiva.
   - O sistema deve permitir que os clientes especifiquem suas preferências de pizza.
   - Deve haver um histórico de pedidos para clientes registrados.

2. *Central de Pedidos*
   - A central de pedidos deve receber, processar e encaminhar pedidos para a loja Pizza-Express mais próxima.
   - Os pedidos devem ser encaminhados em tempo real para a loja selecionada.
   - O sistema deve calcular o tempo estimado de entrega com base na localização do cliente e da loja.

3. *Localização da Loja*
   - O sistema deve identificar a loja Pizza-Express mais próxima do cliente com base em sua localização.
   - A seleção da loja deve ser automática e transparente para o cliente.
   - Deve haver um mecanismo de fallback para permitir que o cliente escolha uma loja manualmente, se necessário.

Requisitos Não-Funcionais:

1. *Desempenho*
   - O sistema deve ser capaz de lidar com picos de demanda durante horários de pico, mantendo o tempo de resposta rápido.
   - O tempo de processamento de pedidos deve ser mínimo.

2. *Confiabilidade*
   - O sistema deve ser altamente confiável, minimizando o risco de falhas devido a interrupções ou erros de software.

3. *Segurança*
   - Os dados dos clientes, como informações de pagamento e histórico de pedidos, devem ser protegidos com criptografia de ponta a ponta.
   - Deve haver autenticação e autorização adequadas para garantir que apenas pessoal autorizado acesse o sistema.

4. *Escalabilidade*
   - O sistema deve ser escalável para lidar com um aumento no número de lojas e pedidos sem perda de desempenho.

5. *Usabilidade*
   - A interface do usuário deve ser intuitiva e fácil de usar tanto para clientes quanto para funcionários da Pizza-Express.

6. *Compatibilidade com Dispositivos Móveis*
   - O sistema deve ser acessível e funcional em dispositivos móveis, como smartphones e tablets.

7. *Manutenibilidade*
   - O código do sistema deve ser bem documentado e modular, facilitando futuras atualizações e manutenções.

8. *Tempo de Entrega*
   - O sistema deve ser capaz de calcular com precisão o tempo estimado de entrega e garantir que as pizzas sejam entregues dentro de 10-15 minutos após o pedido.

9. *Disponibilidade*
   - O sistema deve estar disponível 24 horas por dia, 7 dias por semana, para atender a pedidos de clientes em qualquer momento.

10. *Integração*
    - Deve ser possível integrar o sistema com sistemas de pagamento online e outras ferramentas de terceiros, como serviços de mapas.
&gt;

# Diagrama de casos de uso

*&lt;O diagrama está disponível no link a seguir:
https://drive.google.com/file/d/1FuKSLvoZL87244AP77ngkf9rCLmCt7sY/view?usp=sharing
&gt;*

# Descrição dos casos de uso

&lt;1. Realizar Pedido

- *Ator Principal:* Cliente
- *Ator Secundário:* Sistema de Atendimento, Sistema de Localização
- *Pré-condições:* O cliente deve estar autenticado no sistema.
- *Fluxo Principal:*
   1. O cliente acessa o sistema.
   2. O cliente seleciona o tipo de pizza, tamanho e fornece o endereço de entrega.
   3. O sistema registra o pedido com os detalhes fornecidos.
   4. O sistema verifica a localização do cliente usando o Sistema de Localização.
   5. O sistema identifica a loja Pizza-Express mais próxima.
   6. O sistema encaminha o pedido para a loja selecionada.
- *Fluxos Alternativos ou Excepcionais:*
   - Se o cliente não estiver autenticado, o sistema solicita que ele faça login antes de prosseguir.
   - Se o sistema não conseguir encontrar a localização do cliente, ele solicita um endereço manualmente.
- *Pós-condições:* O pedido é registrado no sistema e encaminhado à loja correspondente para preparação.
&gt;

&lt;2. Processamento do Pedido

- *Ator Principal:* Sistema de Atendimento
- *Ator Secundário:* Sistema de Localização
- *Pré-condições:* Um cliente fez um pedido e forneceu os detalhes do pedido, incluindo tipo de pizza, tamanho e endereço de entrega.
- *Fluxo Principal:*
   1. O Sistema de Atendimento recebe o pedido do cliente.
   2. O Sistema de Atendimento verifica a localização do cliente usando o Sistema de Localização.
   3. O Sistema de Atendimento identifica a loja Pizza-Express mais próxima com base na localização do cliente.
   4. O Sistema de Atendimento encaminha o pedido para a loja selecionada.
   5. A loja recebe o pedido e começa a preparar a pizza de acordo com os detalhes fornecidos.
   6. O Sistema de Atendimento atualiza o status do pedido para "Em Preparação".
- *Fluxos Alternativos ou Excepcionais:*
   - Se o Sistema de Atendimento não conseguir identificar a localização do cliente, ele pode solicitar ao cliente um endereço manualmente.
   - Se não houver loja Pizza-Express próxima ao cliente, o sistema pode informar ao cliente que o serviço não está disponível em sua localização.
   - Se a loja não conseguir atender ao pedido devido a falta de ingredientes ou outros problemas, ela deve notificar o Sistema de Atendimento.
- *Pós-condições:* O pedido é encaminhado com sucesso à loja Pizza-Express mais próxima, e o status é atualizado para "Em Preparação".
&gt;

&lt;3. Entregar Pedido

- *Ator Principal:* Entregador
- *Ator Secundário:* Sistema de Atendimento
- *Pré-condições:* O pedido deve estar preparado e pronto para entrega.
- *Fluxo Principal:*
   1. O entregador recebe o pedido preparado da loja Pizza-Express.
   2. O entregador verifica o endereço de entrega e o prazo de entrega especificado (10 a 15 minutos).
   3. O entregador se desloca até o endereço de entrega.
   4. O entregador entrega o pedido ao cliente.
   5. O entregador atualiza o status do pedido para "Entregue" no sistema.
- *Fluxos Alternativos ou Excepcionais:*
   - Se o entregador não consegue encontrar o endereço de entrega, ele entra em contato com o cliente ou o sistema para obter orientações adicionais.
   - Se o entregador não consegue entregar o pedido devido a circunstâncias excepcionais (por exemplo, cliente ausente), ele registra o motivo no sistema.
- *Pós-condições:* O pedido é entregue com sucesso ao cliente, e o status é atualizado no sistema para "Entregue".
&gt;

# Diagrama de sequencia

*&lt;O diagrama de sequência está disponível no seguinte link:
https://drive.google.com/file/d/1Of8UwoDRk3Sp4_lUWks8OVT1stT2qSaV/view?usp=sharing
&gt;*

# Diagrama de classes

*&lt;O diagrama de classes está disponível no seguinte link:
https://drive.google.com/file/d/1WGCJI4_cbfpA9OD1JR82Vp8D2cTloKGk/view?usp=sharing
&gt;*

# Diagrama de Componentes

*&lt;O diagrama de componentes está disponível no seguinte link:
https://drive.google.com/file/d/1qYBMZ1HHSPu7BygqjnSL5kK6LUJi4y4g/view?usp=sharing
&gt;*

# Decisões de arquitetura

*&lt;
   1. Hospedagem de Aplicações:
Implantação de servidores para executar aplicações essenciais como ClienteApp, LojaApp e EntregadorApp.
Consideração de serviços de nuvem como AWS, Azure ou Google Cloud para escalabilidade e gerenciamento eficiente de recursos.
   
   2.Gerenciamento de Dados:
Estabelecimento de um banco de dados para armazenar informações cruciais relacionadas a clientes, pedidos, estoque de lojas e entregadores.
Avaliação de opções de bancos de dados relacionais (por exemplo, MySQL, PostgreSQL) ou NoSQL (por exemplo, MongoDB) baseando-se nas características e demandas específicas dos dados.

   3. Comunicação entre Componentes:
Desenvolvimento de APIs para facilitar a comunicação harmoniosa entre diferentes partes do sistema.
Implementação de protocolos como RESTful ou GraphQL para otimizar a integração dos diversos componentes.

   4. Sistema de Comunicação Assíncrona:
Estabelecimento de um sistema de mensageria para facilitar a comunicação assíncrona entre componentes, por exemplo, notificações de pedidos para lojas ou entregadores.
Exploração de ferramentas como RabbitMQ ou Apache Kafka para otimizar esse tipo de comunicação.

   5. Armazenamento Eficiente de Arquivos:
Emprego de serviços de armazenamento em nuvem como Amazon S3 ou Google Cloud Storage se for necessário armazenamento de arquivos, como imagens de pizzas.

   6. Ambientes Separados para Desenvolvimento e Testes:
Configuração de ambientes distintos para desenvolvimento, teste e produção, garantindo uma implementação sólida e prevenindo problemas inesperados no ambiente de produção.

   7. Garantias de Segurança:
Implementação rigorosa de práticas de segurança, incluindo o uso de HTTPS, autenticação robusta e autorização, além de monitoramento contínuo para proteger dados sensíveis e assegurar conformidade com regulamentações.
&gt;*

# Diagrama de implantação

*&lt;O diagrama de implantação está disponível no seguinte link:
https://drive.google.com/file/d/1xmOCXH9WugQLclhAwHEptHMPHDuecKbK/view?usp=sharing
&gt;*

# Referências

*&lt;
   1. Arquitetura de Software e Desenvolvimento Web:
"GraphQL: The Definitive Guide" by Preston So and Michael Hunger

   2. Desenvolvimento Ágil e Gestão de Projetos:
"The Lean Startup: How Today’s Entrepreneurs Use Continuous Innovation to Create Radically Successful Businesses" by Eric Ries

   3. Segurança da Informação e Práticas de Desenvolvimento Seguro:
"Certificação Certified Secure Software Lifecycle Professional (CSSLP)"

   4. Design de APIs:
Grupo de Discussão "APIs Brasil" (https://groups.google.com/g/apisbrasil)

   5. Considerações de Nuvem e Serviços Web:
Documentação Oficial dos Serviços Cloud (AWS, Azure, Google Cloud)
&gt;*
