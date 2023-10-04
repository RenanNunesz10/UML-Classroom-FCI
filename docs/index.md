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
*&lt;Descrição dos requisitos&gt;*

# Diagrama de casos de uso

*&lt;Diagrama para visualizar o comportamento dos atores&gt;*

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

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Componentes

*&lt;Diagrama para exibir a relação estrutural dos componentes de um sistema de software

# Decisões de arquitetura

*&lt;Descrever a infraestrutura escolhida para arquitetura do projeto&gt;*

# Diagrama de implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
