# Resumo do Lab - Curso AZ-900 (DIO)
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO do Curso Az-900


**Localizando Serviços por Categoria**
- Ajustes de aparência e idioma: No ícone de configurações (a engrenagem no canto superior), você pode personalizar o visual do portal e escolher o idioma que preferir.  
- Descobrindo serviços: No menu lateral, ao clicar em "Todos os Serviços", dá para explorar tudo o que o Azure oferece, organizado por categorias.  
- Serviços em "Versão Prévia": Alguns serviços aparecem com a etiqueta "Versão Prévia". Isso significa que eles ainda estão em fase de testes e, por isso, não têm um SLA (Acordo de Nível de Serviço). Em outras palavras, não há garantia de continuidade ou estabilidade desses serviços.  


# Benefícios da Nuvem Azure

- **Alta Disponibilidade**  
  Os recursos da nuvem estão disponíveis sempre que você precisar.  
  - O SLA (Acordo de Nível de Serviço) define quanto tempo um serviço pode ficar indisponível por ano, mês ou semana. Caso o tempo de indisponibilidade exceda o limite acordado, você pode receber créditos relacionados ao valor do serviço.  
  - O foco da alta disponibilidade é garantir o funcionamento contínuo, mesmo em situações de interrupções ou eventos imprevistos.  

- **Escalabilidade**  
  A escalabilidade permite ajustar os recursos conforme a demanda.  
  - Se a demanda aumentar, você pode adicionar mais recursos.  
  - Por outro lado, se a demanda cair, é possível reduzir os recursos, otimizando custos. Como a nuvem é baseada no consumo, você paga apenas pelo que usa.  

- **Elasticidade**  
  A elasticidade garante que seus recursos possam ser ajustados rapidamente para atender a mudanças repentinas na demanda.  
  - Por exemplo, em um aumento súbito de uso, você pode expandir automaticamente ou manualmente o número de máquinas virtuais ou contêineres.  
  - Da mesma forma, em uma queda significativa de demanda, é possível reduzir os recursos implantados.  

- **Confiabilidade**  
  A nuvem foi projetada para ser resiliente e confiável, graças à sua estrutura descentralizada.  
  - Com recursos implantados em várias regiões do mundo, mesmo em eventos catastróficos em uma região, outras continuam funcionando normalmente.  

- **Previsibilidade**  
  A previsibilidade na nuvem permite ter confiança tanto no desempenho quanto nos custos.  
  - Esses fatores são influenciados por práticas recomendadas do **Microsoft Azure Well-Architected Framework**.  

- **Segurança**  
  A nuvem oferece diversas ferramentas de segurança para atender às necessidades dos clientes.  
  - É importante lembrar que a implementação de várias dessas ferramentas deve ser feita pelo cliente.  
  - Se você deseja controle total, a infraestrutura como serviço permite gerenciar sistemas operacionais e softwares instalados, incluindo manutenção e aplicação de patches.  

- **Governança**  
  A auditoria baseada na nuvem ajuda a identificar recursos fora de conformidade com os padrões corporativos e oferece estratégias para correção.  
  - Patches de software e atualizações podem ser aplicados automaticamente, o que contribui para uma gestão mais eficiente e segura.  
  - Estabelecer governança logo no início ajuda a manter sua presença na nuvem atualizada e bem gerenciada.  

- **Gerenciabilidade**  
  A computação em nuvem traz diversas opções de gerenciamento:  
  - **Gerenciamento da nuvem**: Focado em gerenciar os recursos, como escalar automaticamente a implantação de acordo com a necessidade ou implantar recursos baseados em modelos pré-configurados, eliminando configurações manuais.  
  - **Gerenciamento na nuvem**: Relacionado à forma como você gerencia o ambiente e os recursos, podendo ser feito através de:  
    - Portais Web  
    - Interfaces de linha de comando  
    - APIs  
    - PowerShell


# Tipo de Serviços de Nuvem

- **IaaS (Infraestrutura como Serviço)**
  - O que é? Infraestrutura de TI (servidores, redes, armazenamento) oferecida pela nuvem. É como alugar um data center.
  - Para quem é? Desenvolvedores ou empresas que precisam de flexibilidade para gerenciar seus sistemas.
  - **Exemplos:**
      - AWS EC2: Aluguel de servidores para hospedar sites e aplicativos.
      - Microsoft Azure Virtual Machines: Criação de máquinas virtuais personalizadas.
 
- **PaaS (Plataforma como Serviço)**
  - O que é? Ambiente completo para criar, testar e implantar aplicativos, sem se preocupar com infraestrutura.
  - Para quem é? Desenvolvedores que querem focar no código sem gerenciar servidores.
  - **Exemplos:**
      - Google App Engine: Desenvolvimento e implantação de aplicativos sem gerenciar servidores.
      - Heroku: Plataforma para criar e hospedar aplicativos.
        
- **SaaS (Software como Serviço)**
  - O que é? Software pronto acessado via internet, sem necessidade de instalação ou manutenção.
  - Para quem é? Usuários que precisam de soluções prontas e simples.
  - **Exemplos:**
      - Google Workspace (Gmail, Google Docs): Ferramentas de produtividade online.
      - Netflix: Streaming de vídeos.
      - Salesforce: Software de CRM.


  **Modelo de responsabilidade Compartilhada**

  **IaaS (Infraestrutura como Serviço)**
  - Provedor: Gerencia o hardware, redes, armazenamento e virtualização.
  - Cliente: É responsável pelo sistema operacional, aplicativos, dados, e configurações de segurança.

  **PaaS (Plataforma como Serviço)**
  - Provedor: Gerencia a infraestrutura, o sistema operacional, e a plataforma (banco de dados, ferramentas de desenvolvimento).
  - Cliente: É responsável pelo código do aplicativo e seus dados.

  **SaaS (Software como Serviço)**
  - Provedor: Gerencia tudo (infraestrutura, plataforma, e o software).
  - Cliente: É responsável apenas pela configuração e uso seguro do serviço (como senhas e permissões).


  **Comparação do Serviço de nuvem**

  **Iaas**
  - O Serviço de nuvem mais fexível.
  - Você configura e gerencia o hardware para seu aplicativo.

  **PaaS**
  - Focado no desennvolvimento de aplicativos.
  - O gerenciamento de plataforma é realizado pelo provedor de nuvem.

  **SaaS**
  - Modelo de preço de pagamento conforme o uso.
  - Os usuários pagam pelo software que utilizam em um modelo de assinatura.

# Componentes de Arquitetura do Azure

  **Regiões**
  - O valor dos recursos varia de acordo com a região, e nem todos os recursos estão disponíveis em todas as regiões.
  - Regiões são compostas por um ou mais datacenters muito próximos (geralmente são 3).
  - Proporcionam flexibilidade e escala para reduzir a latência do cliente.
  - Garantem a residência dos dados e oferecem conformidade abrangente (como a LGPD).
    
  **Zonas de Disponibilidade**
  - Localizações físicas distintas dentro de uma mesma região, compostas por um ou mais datacenters.
  - Projetadas com infraestrutura independente (energia, refrigeração e rede) para alta resiliência.
  - Garantem alta disponibilidade e continuidade dos serviços, isolando falhas localizadas.
  - Suportam aplicativos críticos e replicação de dados entre zonas dentro de uma região.
    
  **Pares de Regiões**
  - Separação mínima de 300 milhas entre pares de regiões (toda região tem uma região par).
  - Replicação automática para alguns serviços.
  - Recuperação de regiões priorizada em caso de interrupção.
  - Atualizações distribuídas sequencialmente para minimizar o tempo de inatividade.
  - [Consulte as Regiões Pares do Azure](https://learn.microsoft.com/pt-br/azure/reliability/cross-region-replication-azure).
    
  **Regiões Soberanas do Azure**
  - Serviços destinados a atender necessidades específicas de segurança e conformidade.
    
  Serviços Governamentais dos EUA
  - Focados em agências federais, governos estaduais e locais dos EUA e seus provedores de soluções.
    
  Azure Governamental
  - Instância separada e fisicamente isolada do Azure.
  - Acessível apenas a pessoal autorizado e verificado.
    
  Azure China
  - Conformidade com regulamentações locais, operado pela 21Vianet.
  - Dados mantidos exclusivamente na China para garantir conformidade.

  **Recursos do Azure**
  - Componentes utilizados para criar soluções de nuvem, como:
    - Máquinas virtuais
    - Contas de armazenamento
    - Redes virtuais
    - Serviços de aplicativos
    - Banco de dados SQL
    - Funções
  
  **Grupo de Recursos**
  - Contêiner utilizado para gerenciar e agregar recursos em uma única unidade.
  - Um recurso pertence a um único grupo, mas pode ser movido entre grupos ou regiões.
  - Permite a separação e organização de projetos.

  **Assinaturas do Azure**
  - Tipos: Desenvolvimento, Teste e Produção.
  - Uma conta pode ter várias assinaturas, mas cada assinatura está vinculada a uma única conta.
  - Usada para controlar cobrança e acesso:
    - Cobranças: Relatórios e faturas separados por assinatura.
    - Controle de Acesso: Gerenciamento de recursos provisionados.

  **Grupos de Gerenciamento**
  - Podem conter várias assinaturas do Azure.
  - Condições aplicadas aos grupos são herdadas pelas assinaturas incluídas.
    

# COMPUTAÇÃO E REDE

  **Serviços de Computação do Azure**
  - A Computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.

  **Máquinas Virtuais do Azure**
  - As máquinas virtuais do Azure (VMs) são emulações de software de computadores físicos.
  - Incluem processador virtual, memória, armazenamento e rede.
  - Oferta de IaaS que oferece personalização e controle total.

  **Conjunto de Dimensionamento de VMs**
  - Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar os recursos automaticamente.

  **Conjuntos de Disponibilidade de VM**
  - **Domínio de falha**: Rack.
  - **Domínio de atualização**: Fileira de VM.

  **Área de Trabalho Virtual do Azure**
  - A Área de Trabalho Virtual do Azure é uma virtualização de área de trabalho e aplicativo executada na nuvem.
  - Crie um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway.
  - Reduza o risco de que o recurso seja deixado para trás.
  - Implantações reais de várias sessões.

  **Serviços de Contêineres do Azure**
  - Os contêineres do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alterações sob demanda.
  - **Instâncias de Contêiner do Azure**: Uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure.
  - **Aplicativos de Contêiner do Azure**: Uma oferta de PaaS, como instâncias de contêineres, que pode balancear a carga e escalar.
  - **Serviço de Kubernetes do Azure**: Um serviço de orquestração para contêineres com arquiteturas distribuídas e grandes volumes de contêineres.

  **Azure Functions**
  - **Azure Functions**: Uma oferta de PaaS que dá suporte a operações de computação sem servidor.
  - O código baseado em eventos é executado quando chamado, sem exigir uma infraestrutura de servidor durante períodos inativos.

  **Comparar Opções de Computação do Azure**

  **Máquinas Virtuais**
  - Servidor baseado em nuvem que dá suporte a ambientes Windows ou Linux.
  - Útil para migrações de **lift-and-shift** para a nuvem.
  - Pacotes do sistema operacional completo, incluindo o sistema operacional do host.

  **Área de Trabalho Virtual**
  - Fornece uma experiência de área de trabalho do Windows baseada em nuvem.
  - Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno.
  - O logon de vários clientes permite que vários usuários façam logon no mesmo computador ao mesmo tempo.

  **Contêineres**
  - Ambiente leve e em miniatura adequado para a execução de microsserviços.
  - Projetado para escalabilidade e resiliência por meio da orquestração (AKS).
  - Os aplicativos e serviços são empacotados em um contêiner que fica na parte superior do sistema operacional do host. Vários contêineres podem ficar em um sistema     operacional do host.

  **Serviços de Aplicativos do Azure**
  - Os **Serviços de Aplicativos do Azure** consistem em uma plataforma totalmente gerenciada para criar, implantar e dimensionar aplicativos Web e APIs rapidamente.
  - Trabalha com **.NET, .NET Core, Node.js, Java, Python ou PHP**.
  - Oferta de **PaaS** com requisitos de nível corporativo de desempenho, segurança e conformidade.

  **Serviços de Rede do Azure**
  - A **Rede Virtual do Azure (VNet)** permite que os recursos do Azure se comuniquem uns com os outros, com a Internet e com as redes locais.
  - **Pontos de extremidade públicos**: Acessíveis de qualquer lugar na Internet.
  - **Pontos de extremidade privados**: Acessíveis somente de dentro da sua rede.
  - As **sub-redes virtuais** segmentam sua rede para atender às suas necessidades.
  - O **emparelhamento de rede** conecta suas redes privadas diretamente.

  **Serviços de Rede do Azure: Gateway de VPN**
  - O **Gateway de VPN** é usado para enviar tráfego criptografado entre uma rede virtual do Azure e uma rede no local pela Internet pública.

### **Serviços de Rede do Azure: ExpressRoute**
  - O **ExpressRoute** estende as redes locais para o Azure por meio de uma conexão privada facilitada por um provedor de conectividade (um cabo de fibra do seu datacenter até o datacenter da Microsoft).

  **DNS do Azure**
  - Confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNS usando a rede Anycast.
  - A segurança do DNS do Azure baseia-se no **Gerenciador de Recursos do Azure**, habilitando o controle de acesso baseado em função, monitoramento e registro em log.
  - Facilidade de uso para gerenciar seus recursos externos e do Azure com um único serviço DNS.
  - As **redes virtuais personalizáveis** permitem que você use nomes de domínio privados e totalmente personalizados em suas redes virtuais privadas.
  - Os **registros de alias** dão suporte a conjuntos de registros de alias para apontar diretamente para um recurso do Azure.
    

# Armazenamento no Azure

  **Contas de Armazenamento**
  - Deve ter um nome globalmente exclusivo.
  - Fornecer acesso à Internet em todo o mundo.
  - Determinar os serviços de armazenamento e as opções de redundância.

  **Redundância de Armazenamento**
  - **LRS (Locally Redundant Storage):** Armazena três cópias dos dados dentro de um único datacenter na mesma região. Protege contra falhas de hardware, mas não contra   desastres regionais.
  - **ZRS (Zone-Redundant Storage):** Armazena cópias dos dados em diferentes zonas de disponibilidade dentro da mesma região. Protege contra falhas de datacenters     individuais.
  - **GRS (Geo-Redundant Storage):** Mantém três cópias dos dados na região primária e replica automaticamente para outra região distante (com mais três cópias). Oferece   proteção contra desastres regionais.
  - **GZRS (Geo-Zone-Redundant Storage):** Combina ZRS e GRS, armazenando cópias em múltiplas zonas na região primária e replicando para uma região secundária. Oferece o mais alto nível de proteção e disponibilidade.

**Durabilidade Associada a Cada Tipo de Redundância:**
- **LRS (Locally Redundant Storage):** 99,999999999% (11 noves) de durabilidade dentro de um único datacenter.
- **ZRS (Zone-Redundant Storage):** 99,9999999999% (12 noves) de durabilidade, pois os dados são replicados em várias zonas dentro da mesma região.
- **GRS (Geo-Redundant Storage):** 99,99999999999999% (16 noves) de durabilidade, pois os dados são replicados para outra região geograficamente distante.
- **GZRS (Geo-Zone-Redundant Storage):** Também oferece 16 noves de durabilidade, combinando replicação entre zonas e entre regiões.

  **Qual Redundância é Indicada para Ambientes Não Produtivos?**
  - **LRS** (Locally Redundant Storage).

  **Serviços de Armazenamento do Azure:**
  - **Blob do Azure:** Armazenamento para dados não estruturados, como texto ou dados binários.
  - **Disco do Azure:** Fornece discos para máquinas virtuais e outros serviços.
  - **Fila do Azure:** Armazenamento de mensagens para grandes volumes de dados com até 64 KB por mensagem.
  - **Arquivos do Azure:** Compartilhamento de arquivos de rede disponível via SMB.
  - **Tabelas do Azure:** Armazenamento de dados estruturados não relacionais, usando um design de chave/atributo.

  **Pontos de Extremidade Públicos do Serviço de Armazenamento:**

  **Tipos de Pontos de Extremidade Públicos:**
  1. **Pontos de Extremidade Padrão:**
     - Cada conta de armazenamento recebe um endpoint público exclusivo baseado no nome da conta e no serviço utilizado.
     - Exemplos de URLs padrão para diferentes serviços:
       - **Blob Storage:** `https://<storage-account-name>.blob.core.windows.net`
       - **Table Storage:** `https://<storage-account-name>.table.core.windows.net`
       - **Queue Storage:** `https://<storage-account-name>.queue.core.windows.net`
       - **File Storage:** `https://<storage-account-name>.file.core.windows.net`

  **Camadas de Acesso de Armazenamento do Azure:**
  - **Frequente:** Otimizada para dados acessados frequentemente.
  - **Esporádico:** Otimizada para dados acessados esporadicamente e armazenados por pelo menos 30 dias.
  - **Frio:** Para dados acessados raramente e armazenados por pelo menos 90 dias.
  - **Arquivo Morto:** Para dados raramente acessados e armazenados por pelo menos 180 dias.

  **Migrações para o Azure:**
  - Plataforma de migração unificada com ferramentas integradas e autônomas.
  - Avaliação e migração de dados.

  **Azure Data Box:**
  - Armazena até 80 terabytes de dados.
  - Move backups e dados para o Azure.
  - Protege dados durante o trânsito.
  - Ideal para locais remotos com conectividade limitada.

  **Opções de Gerenciamento de Arquivos:**
  - **AzCopy:** Utilitário de linha de comando para copiar blobs ou arquivos para/da conta de armazenamento.
  - **Gerenciador de Armazenamento do Azure:** Interface gráfica para interação com armazenamento no Azure (semelhante ao Windows Explorer).
  - **Sincronização de Arquivos do Azure:** Sincroniza arquivos entre nuvem e locais de forma bidirecional.


# Identidade, Acesso e Segurança

 **ID do Microsoft Entra**
  O Microsoft Entra ID é o serviço de gerenciamento de identidades e acesso baseado em nuvem do Microsoft Azure.

  - **Autenticação**: Os funcionários entram para acessar os recursos.
  - **Login Único (SSO)**
  - **Gerenciamento de Aplicativos**
  - **Negócios para Negócios (B2B)**
  - **Gerenciamento de dispositivos**

  **Microsoft Entra Domain Services**
  O Microsoft Entra Domain Services é um serviço que permite usar recursos do Active Directory na nuvem, sem precisar de um servidor físico.

  - Permite login seguro em máquinas e aplicativos.
  - Conecta máquinas virtuais no Azure a um domínio.
  -  Aplica regras de segurança (Política de Grupo - GPO).
  - Funciona com aplicativos antigos que precisam de autenticação tradicional.
  - Sincroniza com o Microsoft Entra ID, sem precisar de servidores extras.

   **Comparar Autenticação e Autorização**

  **Autenticação**
  - Identifica a pessoa ou serviço buscando acesso a um recurso.
  - Solicita credenciais de acesso legítimo.
  - Base para criar princípios de identidade e controle de acesso seguro.

  **Autorização**
  - Determina o nível de acesso de uma pessoa ou serviço autenticado.
  - Define quais dados eles podem acessar e o que podem fazer com eles.

  **Autenticação Multifator**
  Fornece segurança adicional para as identidades, exigindo dois ou mais elementos para autenticação completa.

  **Estratégia para aplicar Autenticação Multifator:**  
    Algo que você sabe <--> Algo que você possui <--> Algo que você é

  **B2B do Microsoft Entra External ID**
    O Microsoft Entra External ID (B2B) permite que empresas concedam acesso seguro a usuários externos, como parceiros, fornecedores e clientes, sem precisar criar contas novas para eles.

  - Convida usuários externos para acessar aplicativos e recursos da empresa.
  - Usa o login existente do parceiro (Google, Microsoft, Facebook, etc.).
  - Aplica políticas de segurança, como autenticação multifator (MFA) e controle de acesso condicional.
  - Garante colaboração segura, sem comprometer a proteção dos dados internos.

  **B2C do Microsoft Entra External ID**
  O Microsoft Entra External ID (B2C) permite que empresas criem experiências de login personalizadas para clientes em aplicativos e sites.

  - Permite que clientes usem contas próprias (Google, Facebook, Apple, Microsoft ou e-mail/senha).
  - Personaliza a experiência de login com telas de autenticação personalizadas.
  - Garante segurança com autenticação multifator (MFA) e proteção contra fraudes.
  - Escala para milhões de usuários, ideal para aplicativos de grande público.

  **Acesso Condicional**
  O Acesso Condicional do Microsoft Entra ID é uma ferramenta que ajuda a proteger os recursos da empresa, permitindo ou bloqueando acessos com base em condições específicas.

  - Associação de usuário ou grupo
  - Local do IP
  - Dispositivo
  - Aplicativo
  - Detecção de risco

  **Controle de Acesso Baseado em Função (RBAC)**
  O Controle de Acesso Baseado em Função (RBAC - Role-Based Access Control) no Microsoft Entra ID permite gerenciar permissões de usuários com base em suas funções dentro da organização.

  - Gerenciamento de acesso de granularidade fina.
  - Divide as tarefas dentro da equipe e concede somente a quantidade de acesso necessária para trabalhar.
  - Habilita o acesso ao portal do Azure e o controle de acesso aos recursos.

  **Confiança Zero (Zero Trust)**
  O Confiança Zero (Zero Trust) é um modelo de segurança que parte do princípio de que nenhum acesso deve ser confiado automaticamente, mesmo dentro da rede da empresa.

  **Proteção Completa**
  - Uma abordagem em camadas para proteger os sistemas de computador.
  - Fornece vários níveis de proteção.
  - Ataques contra uma camada são isolados das camadas subsequentes.

  **Microsoft Defender para Nuvem**
  O Microsoft Defender para Nuvem é um serviço de monitoramento que fornece proteção contra ameaças nos datacenters do Azure e locais.

  - Fornece recomendações de segurança.
  - Detecta e bloqueia malware.
  - Analisa e identifica ataques potenciais.
  - Controle de acesso just-in-time para portas.


  

