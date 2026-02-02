# Arquitetura de Software

## Definição Arquitetura de Software
A arquitetura de software define a estrutura fundamental de um sistema, organizando seus componentes, as formas de comunicação entre eles e as regras que orientam o desenvolvimento. Ela atua como um guia que direciona decisões técnicas ao longo de todo o ciclo de vida do software.
Um dos principais objetivos da arquitetura é promover a decomposição do sistema em unidades modulares, cada uma com responsabilidades bem delimitadas. Essa modularização facilita a compreensão, o desenvolvimento colaborativo e a manutenção do sistema.
As decisões arquiteturais tomadas nas fases iniciais do projeto têm impacto direto na capacidade de evolução do software, influenciando aspectos como manutenibilidade, escalabilidade, testabilidade e organização do código ao longo do tempo.

## Evolução da Arquitetura
Respeitar a separação em camadas, como apresentação, regras de negócio, persistência e banco de Dados ajuda no desenvolvimento e organização. Ignorar essa organização tende a gerar forte acoplamento, dificultando testes, manutenção e evolução do sistema. Adicionalmente, torna-se evidente que anti-padrões, como o *architecture sinkhole*, prejudicam a clareza e a sustentabilidade do código. A ausência de uma separação clara de responsabilidades compromete a qualidade do software e aumenta o custo de manutenção.
A arquitetura de software evoluiu historicamente de modelos centralizados e monolíticos para arquiteturas cliente-servidor e, posteriormente, para arquiteturas em múltiplas camadas, como 2-Tier, 3-Tier e 4-Tier. Essa evolução trouxe maior descentralização, flexibilidade e facilidade na automação de atualizações.

## Estilos e Padrões Arquiteturais

Os estilos arquiteturais definem a estrutura macro do sistema, como monolítico, em camadas ou baseado em microsserviços. Eles determinam o “tipo” de sistema e suas características principais. Já os padrões arquiteturais, como MVC, MVVM e Clean Architecture, descrevem como organizar responsabilidades internamente dentro de um determinado estilo.

## MVC

O padrão MVC divide a aplicação em Model, View e Controller, facilitando o desenvolvimento inicial e a organização do código. Ele é amplamente utilizado por sua simplicidade e clareza conceitual. Em sistemas mais complexos, o MVC pode levar a forte acoplamento entre componentes, dificultando testes automatizados, reutilização de código, controle transacional e evolução da aplicação. 

## SOLID e Arquitetura em Camadas

Para superar as limitações do padrãao MVC aplicar os princípios SOLID, como responsabilidade única, inversão de dependência e injeção de dependências é uma boa opção. Esses princípios promoveram maior desacoplamento, flexibilidade e testabilidade.
A adoção de uma arquitetura em quatro camadas: Apresentação, Aplicação, Domínio e Infraestrutura, permitirá uma separação mais clara das responsabilidades.


## Qualidade, Design e Sustentabilidade

O foco passa a ser a qualidade interna do software, priorizando alta coesão, baixo acoplamento e facilidade de manutenção. Princípios de design, padrões de projeto e práticas como TDD foram incorporados para garantir sistemas mais confiáveis e sustentáveis. A longevidade de um sistema depende da sua capacidade de evoluir sem se tornar excessivamente complexo ou frágil.

## Arquiteturas Modernas e Escalabilidade

Com o crescimento das aplicações, tornou-se necessário adotar arquiteturas mais robustas para produção. A organização passou a incluir componentes especializados, como Frontend, Load Balancer, API Gateway, serviços independentes, cache, filas, banco de dados, storage e integrações com APIs externas.Essa estrutura favorece escalabilidade, segurança, desempenho e autonomia das equipes de desenvolvimento.

## Hexagonal e Clean Architecture

A Arquitetura Hexagonal (Ports & Adapters) protege o núcleo do sistema de mudanças externas e melhora a testabilidade. Esse estudo evoluiu para a Onion Architecture e, principalmente, para a Clean Architecture, que organiza o sistema em camadas concêntricas com dependências sempre apontando para o centro. Essa abordagem garante que regras de negócio permaneçam independentes de frameworks, bancos de dados e interfaces.

## Dependências, Microserviços e Comunicação Assíncrona

O isolamento do núcleo — entidades e casos de uso — promove independência tecnológica e maior facilidade de manutenção. A adoção de microserviços, organizados por domínio, permitiu escalabilidade horizontal e maior autonomia das equipes, apesar do aumento da complexidade infraestrutural. A comunicação entre serviços passou a ocorrer tanto via HTTP REST quanto por mensageria assíncrona, utilizando ferramentas como Kafka e RabbitMQ. O modelo Publish-Subscribe reduziu acoplamento e aumentou a resiliência do sistema.

## Integração, SOA e CQRS

Para integração entre sistemas modernos e legados, APIs REST, GraphQL, filas e adaptadores são usados. Em ambientes corporativos, a Arquitetura Orientada a Serviços (SOA) foi adotada para garantir contratos bem definidos e governança. Já o padrão CQRS foi aplicado em sistemas com alto volume de leitura e escrita, separando comandos e consultas para melhorar desempenho e escalabilidade.

## Conclusão

A arquitetura de software é um processo contínuo de aprendizado e tomada de decisões conscientes. Um sistema moderno deve ser modular, desacoplado, reativo e preparado para mudanças futuras. Mais do que uma estrutura fixa, a arquitetura representa o equilíbrio entre simplicidade, desempenho, qualidade e evolução constante do software.

## Segunda opção

| Tópico Principal | Subtópicos / Conceitos-Chave | Objetivo / Benefício |
|-----------------|----------------------------|----------------------|
| **1. Definição de Arquitetura de Software** | Estrutura principal do sistema; organização de componentes e comunicação; regras de desenvolvimento; decomposição modular | Facilitar manutenção e evolução; delimitar responsabilidades; organizar o sistema de forma sustentável |
| **2. Evolução e Boas Práticas** | Sequência de camadas (Apresentação → Negócios → Persistência → BD); anti-padrões (ex.: *architecture sinkhole*); evolução histórica (centralizada → monolítica → cliente-servidor → multicamadas) | Evitar acoplamento prejudicial; promover separação de responsabilidades; incentivar descentralização e automação |
| **3. Estilos vs. Padrões Arquiteturais** | Estilos: monolítico, em camadas, microsserviços; padrões: MVC, MVVM, Clean Architecture; distinção entre estilo e padrão | Definir a estrutura macro do sistema; organizar responsabilidades internas; dar clareza às decisões arquiteturais |
| **4. MVC**| Model, View e Controller; acoplamento forte; dificuldades em testes, reuso e controle transacional | Facilitar o desenvolvimento inicial; identificar limitações em sistemas complexos; motivar arquiteturas mais desacopladas |
| **5. SOLID e Arquitetura em Camadas** | Princípios SOLID; injeção de dependência; 4 camadas (Apresentação, Aplicação, Domínio, Infraestrutura); dependência apontando para o núcleo | Promover desacoplamento e testabilidade; separar responsabilidades; garantir autonomia e adaptabilidade |
| **6. Deploy e Infraestrutura** | Docker, VPS, Nginx; estrtégias de deploy; decisões de infraestrutura | Padronizar ambientes; controlar desempenho e custos; garantir disponibilidade do sistema |
| **7. Qualidade e Princípios de Design** | Alta coesão e baixo acoplamento; padrões de projeto; TDD | Melhorar manutenibilidade; garantir sustentabilidade e confiabilidade; apoiar evolução a longo prazo |
| **8. Arquiteturas Modernas e Escalabilidade** | Frontend, Load Balancer, API Gateway, Cache, Fila, Banco, Storage; arquitetura para produção | Aumentar flexibilidade, desempenho e segurança; permitir escalabilidade horizontal; dar autonomia às equipes |
| **9. Arquiteturas Hexagonal, Onion e Clean** | Hexagonal (Ports & Adapters); Onion Architecture; Clean Architecture e camadas concêntricas | Proteger o núcleo do sistema; garantir dependências unidirecionais; isolar a lógica de negócio |
| **10. Princípios de Dependência e Microserviços** | Isolamento do núcleo; microserviços por domínio; independência tecnológica | Facilitar manutenção e testes; escalar equipes e sistemas; lidar conscientemente com maior complexidade |
| **11. Comunicação Assíncrona e Eventos** | REST, Kafka, RabbitMQ; Publish-Subscribe; serviços independentes | Aumentar resiliência e escalabilidade; desacoplar componentes; reagir eficientemente a eventos |
| **12. Integração e Sistemas Legados** | APIs REST e GraphQL; filas; adaptadores; wrappers, ETL/ESB, gateways | Integrar sistemas modernos e legados; garantir compatibilidade e segurança; evitar reescrita completa |
| **13. SOA e CQRS** | SOA com contratos bem definidos; CQRS (separação entre comandos e consultas) | Reaproveitamento e governança (SOA); melhor desempenho e escalabilidade em alta carga (CQRS) |
| **14. Sistema Moderno e Conclusão** | Componentes desacoplados, reativos e escaláveis; comunicação assíncrona; responsabilidades bem definidas | Preparar sistemas para o futuro; equilibrar simplicidade, desempenho e evolução contínua |



