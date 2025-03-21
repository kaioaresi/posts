# Evolução até Kubernetes

## Motivador

E aí, pessoal! Recentemente, conversando com uns amigos, me dei conta de como a área de TI pode parecer um bicho de sete cabeças para quem está começando. Mas a verdade é que, com o conhecimento certo e um pouco de dedicação, qualquer um pode se aventurar nesse mundo e se dar bem.

Inspirado por alguns amigos, resolvi começar a escrever alguns posts com o objetivo de compartilhar minhas experiências e visão sobre vários assuntos da área de tecnologia e como entender o nosso valor para o negócio.

Neste primeiro post, vou apenas contextualizar como era realizado o deploy antes da popularização dos contêineres e da nuvem, chegando ao momento em que o Kubernetes se tornou algo comum no dia a dia.

## Introdução

Em 2014, eu era um júnior em uma pequena empresa de Uberlândia, MG, e me desdobrava para dar conta das várias tarefas na área de suporte. As implantações de novos clientes eram maratonas com máquinas físicas.

Realizávamos a instalação do sistema operacional "Slackware 12" por um longo período, posteriormente trocamos para o `CentOS`, passando pelas versões 5, 6 e 7.

Após a instalação do sistema operacional, era executado um shell script para realizar a instalação de todas as dependências da aplicação.

Por fim, baixávamos a aplicação via `SVN` no servidor e seguíamos com as migrações e demais validações.

Bom, era um processo manual demorado, frustrante e muito suscetível a erros humanos. Foi aí que comecei a questionar como as grandes organizações faziam isso.

No primeiro momento, busquei orientação nas comunidades e, por sorte ou destino, um novo termo estava se popularizando, chamado `DevOps`. Esse termo era ainda um pouco confuso na época, pois parecia mais um grito de socorro de outros analistas que também sofriam com esse abismo de toil nas operações.

Conversando com outros profissionais com problemas parecidos, fui apresentado ao `Ansible`, que, no início, parecia ideal para auxiliar na resolução de alguns problemas. Mas claro que tive que estudar e realizar testes para entender seu funcionamento.

Algumas semanas depois, finalmente consegui entender seu funcionamento e automatizar atividades pequenas. Essas pequenas atividades ficaram maiores a cada dia, a ponto de eu conseguir tirar um tempo para automatizar todo o script de instalação dos pacotes. Nossa, quando finalizei essa automatização via Ansible, fiz os primeiros testes em ambiente real. Na época, se não me falha a memória, o tempo de execução do script levava em torno de 40-50 minutos. Consegui reduzir esse tempo para menos de 10-15 min. Isso fez um clique na minha cabeça. Logo chamei meus parceiros de trabalho na hora para demonstrar minha ideia. A primeira vista, eles ficaram com o pé atrás, porém, a cada dia, eles começaram a aceitar cada vez mais que todos aqueles benefícios eram a nova tendência do mercado.

## A era `Docker`

Após a adoção da nuvem e do `Ansible`, o processo de setup das ferramentas melhorou, mas ainda buscava mais eficiência. Com a popularização da nuvem, surgiram vários novos recursos que até hoje são utilizados de forma massiva, como Auto Scaling groups (ASG) e Amazon Machine Images (AMI) da AWS. Esses recursos abriram um mar de novas estratégias e possibilidades.

Com esse boom da nuvem, outra ferramenta que trouxe bastante notoriedade foi o Docker e a retomada do conceito de containers, bastante difundido nos canais do YouTube.

Com o Docker, criar imagens de aplicações com as exatas configurações e versionamento era algo sensacional, isso evitava bastante retrabalho.

Pouco tempo depois, o `Docker Compose` e `Docker Swarm` se popularizaram, facilitando a criação das stacks completa das aplicações, ou seja, nesse ponto, facilitou bastante a distribuição das aplicações para todos os ambientes.

A ideia de um ecossistema voltado para a aplicação já com todas as suas dependências era algo incrível. Muito diferente de alguns anos atrás.

Novos conceitos começaram a se popularizar, como continuous integration, continuous delivery, gerenciador de configuração, gerenciador de automação, pipeline etc.

Obviamente, nem tudo era um mar de flores, surgiram vários outros problemas junto, como O11y, escalabilidade, resiliência etc., mas, ao meu ver, o saldo ainda continuava positivo.

## A soberania do Kubernetes

`Kubernetes` a primeira vez que ouvi esse nome, não fazia ideia da revolução que ele representaria para a área de operações. Meus primeiros contatos foram desafiadores, confesso, tamanha a complexidade inicial. Mas bastou entender sua proposta para que a ficha caísse estávamos diante de uma nova era, com a escala globalizada que tanto almejávamos.

Hoje, o Kubernetes é um padrão de mercado incontestável. É quase impossível encontrar empresas que não o utilizem em algum contexto, seja para escalar aplicações, garantir a resiliência de serviços críticos ou otimizar o uso de recursos.

Mas o Kubernetes é muito mais do que um conjunto de ferramentas. Ele é a base para uma nova forma de pensar a área de operações. Com ele, as equipes ganham agilidade, eficiência e, principalmente, autonomia.

Recursos como o HPA (Horizontal Pod Autoscaler) permitem escalar aplicações automaticamente, respondendo a picos de demanda sem intervenção humana. O Ingress facilita a exposição de serviços para o mundo externo, de forma segura e controlada. O Service Mesh garante a comunicação confiável entre os microsserviços, mesmo em ambientes complexos. E o AutoScaler otimiza o uso de recursos, reduzindo custos e evitando desperdícios.

Com o Kubernetes, as equipes de operações deixam de ser meros "apagadores de incêndio" e se tornam parceiras estratégicas do negócio. Elas passam a utilizar métricas de negócio para guiar suas decisões, contribuindo para o crescimento e o sucesso da empresa.

A transformação é notável. A área de operações, antes vista como um centro de custos, se torna um motor de inovação e eficiência. De um departamento reativo e focado em tarefas manuais, ela se tornou um setor proativo e estratégico, que contribui diretamente para o sucesso dos negócios.

O futuro da área de operações é promissor, principalmente com esse adivindo da iAs que será uma nova era para todos áreas de tecnologia e negocio, sem falar da fase atual onde a "plataformização" está cada vez mais forte, mas isso será assunto para os próximos posts.

## Conclusão

Em resumo, gostaria apenas de compartilhar um pouco das minhas experiências e relatos de quem esteve no antes, no durante e depois dessas era dos containers.

Muitíssimo obrigado por ler este post! Não vou parar por aqui nos próximos, escreverei mais tecnicamente sobre questões que são bastante relevantes e vamos mergulhar ainda mais nesse mundo sensacional de container e kubernetes.
