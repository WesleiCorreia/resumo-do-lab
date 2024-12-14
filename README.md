# Resumo do Lab - Curso AZ-900 (DIO)
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO do Curso Az-900


**Localizando Serviços por Categoria**
- Ajustes de aparência e idioma: No ícone de configurações (a engrenagem no canto superior), você pode personalizar o visual do portal e escolher o idioma que preferir.  
- Descobrindo serviços: No menu lateral, ao clicar em "Todos os Serviços", dá para explorar tudo o que o Azure oferece, organizado por categorias.  
- Serviços em "Versão Prévia": Alguns serviços aparecem com a etiqueta "Versão Prévia". Isso significa que eles ainda estão em fase de testes e, por isso, não têm um SLA (Acordo de Nível de Serviço). Em outras palavras, não há garantia de continuidade ou estabilidade desses serviços.  


# Benefícios da Nuvem Azure**

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
