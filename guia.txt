🚩 Guia de Preparação e Sobrevivência: CTF

--------------------------------------------------------------------------------
📑 Sumário
Regras de Engajamento e Ética
Preparação do Laboratório
Metodologia — Sala de Aula Invertida
Kit de Sobrevivência Linux 
4.1 Navegação e Arquivos
4.2 Busca, Filtro e Inspeção
4.3 Criptografia e Codificação Nativa
4.4 Processamento Avançado e Pipelines
4.5 Redes e Conexões
4.6 Permissões, Usuários e Processos
4.7 Compactação e Arquivos Estranhos
OverTheWire Bandit 
Próximos Passos: TryHackMe, Ferramentas e Exploração

--------------------------------------------------------------------------------
⚖️ 1. Regras de Engajamento e Ética
A regra de ouro da cibersegurança: Só teste sistemas que você possui ou onde tem permissão explícita por escrito.
Durante o intensivão:
Nada de testar coisas na empresa, wi-fi do shopping ou servidor de amigo.
Tudo será feito em laboratórios dedicados.
Hacking é uma ferramenta poderosa — use com ética.

--------------------------------------------------------------------------------
🛠️ 2. Preparação do Laboratório
Para não perdermos tempo na aula, você precisa preparar seu ambiente de testes sem usar seu sistema operacional principal.
Instale o Hypervisor
VirtualBox
VMware Workstation Player
Instale o Sistema Operacional
Ubuntu (recomendado para iniciantes)
Kali Linux (para quem já quer ferramentas integradas)
Recursos da VM
2–4 GB RAM
40–60 GB de disco
Rede: NAT (para mantê-la segura e isolada)
Dicas adicionais
Tire snapshots antes de bagunçar o sistema.
Aprenda a restaurar rapidamente o ambiente.

--------------------------------------------------------------------------------
📚 3. Metodologia — Sala de Aula Invertida
O curso segue o modelo Flipped Classroom. O tempo síncrono será 100% focado na prática.
Antes das aulas
Leitura dos materiais
Execução de comandos simples
Microtarefas individuais
Durante as aulas
Resolução de desafios em grupo
Demonstrações ao vivo
Aprendizado baseado em problemas (PBL)
Depois das aulas
Revisão
Minitarefas práticas
Consolidação do aprendizado

--------------------------------------------------------------------------------
🐧 4. Kit de Sobrevivência Linux (Versão Estendida)
A seguir está seu “canivete suíço” do terminal. Isso resolve 80% dos problemas iniciais de CTF.
4.1 Navegação e Arquivos
pwd: Mostra em qual diretório você está no momento.
ls -la: Lista todos os arquivos da pasta, incluindo os ocultos e detalhes de permissão.
cd <pasta>: Entra em uma pasta. Use cd .. para voltar.
cat <arquivo>: Imprime todo o conteúdo de um texto na tela.
less <arquivo>: Lê arquivos grandes página por página.
4.2 Busca, Filtro e Inspeção
grep "<palavra>" <arquivo>: Filtra o arquivo e mostra apenas as linhas que contêm a palavra buscada.
find / -name "<nome>": Busca um arquivo pelo nome em todo o sistema.
file <arquivo>: Analisa a estrutura do arquivo para dizer qual é o tipo real dele.
strings <arquivo>: Extrai textos legíveis de dentro de um arquivo binário.
4.3 Criptografia e Codificação Nativa
Cifra de César (ROT13): O comando tr substitui caracteres nativamente: echo "texto" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
Base64: Decodifique textos nativamente usando echo "texto_base64" | base64 -d
Hexadecimal: xxd <arquivo> ou hexdump visualizam o conteúdo hexadecimal de um arquivo.
4.4 Processamento Avançado e Pipelines
O "Pipe" |: O símbolo mais poderoso do Linux. Pega o resultado do comando da esquerda e joga para o da direita (Ex: cat log.txt | grep "admin").
awk e sed: Ferramentas para processar e recortar pedaços específicos de texto.
wc -l: Conta a quantidade de linhas em um arquivo.
4.5 Redes e Conexões
ping <IP>: Testa se uma máquina está respondendo.
curl <URL> ou wget <URL>: Baixa arquivos ou interage com sites ignorando o navegador.
nc <IP> <Porta> (Netcat): Conecta a portas específicas ou cria conexões reversas.
ssh usuario@IP -p <porta>: Conecta remotamente e de forma segura ao terminal de outra máquina.
4.6 Permissões, Usuários e Processos
chmod: Altera as permissões de leitura, escrita e execução.
sudo: Executa um comando com privilégios máximos de administrador.
4.7 Compactação e Arquivos Estranhos
(Durante o laboratório, aprenderemos comandos como tar, unzip e gzip para lidar com arquivos compactados em desafios).

--------------------------------------------------------------------------------
🎮 5. OverTheWire Bandit (Guia Estendido)
O Bandit é nosso dojo inicial para aprender comandos Linux.
5.1 O login inicial
Abra o seu terminal Linux e digite:
ssh bandit0@bandit.labs.overthewire.org -p 2220
(A senha inicial é bandit0)
5.2 Dicas estendidas por níveis
Explore o ambiente com os comandos da Seção 4 para encontrar o arquivo que contém a senha (flag) do próximo nível. Ao achar a senha, copie-a, saia digitando exit e faça um novo login SSH como bandit1, usando a senha descoberta.

--------------------------------------------------------------------------------
🚀 6. Próximos Passos: TryHackMe, Ferramentas e Exploração
Após dominar Bandit até nível ~20: Ferramentas que começaremos a usar:
Nmap
Wireshark
Gobuster
Burp Suite
Hydra
John the Ripper
Conceitos que você aprenderá:
Reconhecimento ativo e passivo
Enumeração web e de serviços
Exploração de vulnerabilidades
Elevação de privilégios
Coleta e pós-exploração
Fundamentos de pentest profissional
Objetivo dos próximos meses: Criar a “intuição hacker”: saber onde procurar, como pensar e como montar o quebra-cabeça.
Nos vemos no primeiro encontro
