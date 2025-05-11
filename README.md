# Criando-uma-VM

Etapas de Criação da VM

## **Básico**

    -Selecione a sua inscrição
    -Escolha um Resource Group(ou crie um novo)

    -Dê um nome par a VM, preferencialmente seguindo algum padrão de nomenclatura para facilitar a criação de novas VMs
    -Selecione uma região para hostear a VM, lembrando que a localização pode aumentar ou diminuir a latência e afetar o preço da VM
    -Na opção de zonas, temos as zonas auto-selecionadas ou as selecionadas pelo Azure, caso vá na segunda opção, o Azure definirá qual a melhor zona para as suas necessidades.
    -Escolha uma ou mais zonas de disponibilidade
    -Escolha qual tipo de segurança o Azure oferecerá para a VM

    -O Azure oferece uma gama de opções de sistemas operacionais(imagens) para a maquina rodar, escolha ao seu gosto ou qual melhor servir as suas necessidades.

    Após isso temos a opção de rodar com desconto de Spot do Azure, marcar essa opção vai considerar a sua VM como "baixa prioridade" para os sistemas do Azure, você pagará menos para manter a sua maquina virtual ligada
    porém, sua maquina será desativada caso o excesso de VMs do Azure desaparecer, usando o espaço da sua VM para alocar outras VMs mais importantes. Neste caso temos a opção de remover por capacidade, ou seja, caso a sua maquina seja necessária, ou por capacidade e preço, botando um preço máximo para a VM usar, sendo ela excluida caso chegue nesse valor.

    Lembrando que chegando nesse limite, você pode deixar a opção de apenas parar a VM ou excluir ela totalmente.

    -Escolha o tamanho da maquina, essa seção é bem complexa pois temos diversos tamanhos referentes a memória Ram, vcpus e muitas coisas, e tudo isso afetando o preço da sua vm, então é necessário escolher de acordo com as suas necessidades.

    -Crie a sua conta de administrador

    -Defina as regras de portas de entrada, escolhendo quais portas estarão disponiveis para se conectar a sua maquina virtual
## **Disco**

    -Selecione o tamanho do disco e o seu tipo, é recomendado pegar pelo menos o SSD Standard, visto que o HD normal terá lentidões para executar as tarefas
    -Selecione quem vai gerenciar a chave de criptografia do sistema, o cliente ou a plataforma.
## **Rede**

    -O Sistema vai procurar uma rede virtual para a sua maquina, caso não tenha, ela irá criar uma nova concatenando o seu resource group com "vnet" no final.

    A plataforma vai criar uma sub-rede e um ip público para você se conectar a maquina.

    ATENÇÃO: SELECIONE EXCLUIR O IP PÚBLICO E O NIC QUANDO A VM FOR EXCLUÍDA, CASO CONTRÁRIO, QUANDO ELA FOR EXCLUIDA VOCÊ CONTINUARÁ SENDO COBRADO PELO SEU USO.

    Você também tem a opção de escolher um balanceador de carga para equilibrar o tráfego da rede, pesquisar com mais detalhes depois, no momento selecionar "Nenhum".
## **Gerenciamento**

    Aqui temos várias opções de gerenciamento que vão de cada um, uma coisa para manter atenção seria no horario de desligamento automático da VM, é interessante botar um horário em que você já não estará mais utilizando aquela maquina, deixando ela desligar sozinha para evitar uma cobrança maior, mantendo o sistema mais fácil de gerenciar, além de que o Azure manda um email confirmando o desligamento da VM
## **Monitoramento**

    Aqui podemos definir opções para monitorar o status da VM em diversos momentos, na opção "Diagnóstico de inicialização" sempre selecionar "Habilitar com a conta de armazenamento gerenciada" para um relatório mais detalhado sobre como a maquina está funcionando.
## **Avançado**

    No avançado podemos adicionar ou configurar funcionalidades da VM de diversas maneiras diferentes, como scripts, extensões ou aplicativos, podendo configurar a VM a realizar ações adicionais durante seu funcionamento.
## **Marcas**

    As marcas servem para anexar os recursos da sua VM a algum valor que você especificar para facilitar alguma pesquisa ou filtragem futuramente, não é necessário configurar nada aqui, é puramente opcional.
    

