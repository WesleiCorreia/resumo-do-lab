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

