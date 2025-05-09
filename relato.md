# 2025-1-atividade-02-docker-linux-introducao


**Nome:** Wagner Alves de Souza  
**Data:** 09/05/2025

---

## Introdução

Neste exercício, o objetivo foi compreender e aplicar, na prática, os conceitos abordados em aula, por meio da manipulação de permissões, gerenciamento de diretórios e pacotes, encerramento de processos e navegação no sistema de arquivos Linux.

---

## Relato

### Para verificar se o Docker estava instalado corretamente na máquina, utilizei o comando:

![Imagem 1](./imagens/verificando-docker-1.png)

Conferi se o Docker estava instalado na minha máquina com o comando:  
`bash docker --version` -> Versão do Docker.
  
  

---

### Em seguida, baixei a imagem do Fedora, executei o container em modo interativo e defini um nome personalizado:

![Imagem 2](./imagens/baixando-imagem-fedora-e-renomeando-2.png)

`run` -> Baixa a imagem, caso ainda não exista localmente, e executa o container.  
`-it` -> Abre o container em modo interativo (com terminal conectado).  
`--name` -> Define um nome personalizado para o container (fedora-tutorial, no exemplo acima).
  
  

---

### Executei alguns comando do Shell:

![Imagem 3](./imagens/onde-estou-e-quem-sou-indo-para-home-e-criando-diretorio-3.png)  

Utilizei comandos do terminal para identificar o diretório atual, verificar o usuário logado, navegar até o diretório home e criar uma nova pasta.  

`pwd` -> Mostra o diretório de trabalho atual.  
`whoami` -> Exibe o nome do usuário atualmente logado.  
`cd ~` -> Navega para o diretório home do usuário.  
`ls -la` -> Lista todos os arquivos e diretórios, incluindo os ocultos, com detalhes como permissões, data, e tamanho.  
`mkdir [nome_do_diretório]` -> Cria um novo diretório.
  
  
---

### Naveguei entre os diretórios:
  

![imagem 4](./imagens/voltando-diretorio-conferindo-arquivos-e-voltando-home-conferindo-criando-arquivo1-4.png)
  
  
Naveguei entre os diretórios e criei um arquivo texto no diretório Home.
  
  
`touch [nome_arquivo]` -> Cria um arquivo vazio.

























### Imagens:

![Descrição da imagem 1](caminho/para/imagem1.png)  
*Figura 1 - Resultado da etapa X*

![Descrição da imagem 2](caminho/para/imagem2.png)  
*Figura 2 - Resultado da etapa Y*

---

## Conclusão

Com esta atividade, aprendi:

- [Ponto aprendido 1]
- [Ponto aprendido 2]

**Dificuldades encontradas:**

- [Descreva as dificuldades ou desafios enfrentados]
