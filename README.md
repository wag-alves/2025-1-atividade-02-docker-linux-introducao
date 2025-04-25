# S.O. 2025.1 - Atividade 02 - Introdução a linux usando docker no windows

## Informações gerais

- **Objetivo do repositório**: Repositório da disciplina para atividade avaliativa dos alunos
- **Assunto**: Introdução a linux
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** [Sistemas Operacionais](https://github.com/sistemas-operacionais/)
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)


## Sumário

1. Tutorial Linux
2. Prática e atividade avaliativa

## 1. Tutorial de Conceitos Básicos de Linux

Este tutorial abordará os fundamentos do Linux, incluindo sua estrutura básica, comandos essenciais e conceitos importantes para iniciantes.  

Foi construído com o auxílio do [deepseek](https://chat.deepseek.com/).
---

### 1.1. O que é Linux?
Linux é um **sistema operacional de código aberto** baseado no kernel Linux, criado por **Linus Torvalds** em 1991. Ele é amplamente utilizado em servidores, desktops e dispositivos embarcados.  

#### 1.1.1. Distribuições (Distros) mais populares:
- [Ubuntu](https://ubuntu.com/)  
- [Debian](https://www.debian.org/)  
- [Fedora](https://getfedora.org/)  
- [CentOS](https://www.centos.org/)  
- [Arch Linux](https://archlinux.org/)  
- [Linux Mint](https://linuxmint.com/)  

---

### 1.2. Estrutura de Diretórios no Linux
O Linux segue uma hierarquia de diretórios padrão:  

| Diretório       | Descrição |  
|----------------|-----------|  
| **/**          | Raiz do sistema |  
| **/bin**       | Binários essenciais |  
| **/etc**       | Arquivos de configuração |  
| **/home**      | Diretórios dos usuários |  
| **/var**       | Arquivos variáveis (logs, bancos de dados) |  
| **/tmp**       | Arquivos temporários |  
| **/usr**       | Programas e bibliotecas |  
| **/root**      | Home do superusuário (root) |  

---

### 1.3. Comandos Básicos no Terminal

#### 1.3.1. Navegação
| Comando        | Descrição |  
|---------------|-----------|  
| `pwd`         | Mostra o diretório atual |  
| `ls`          | Lista arquivos e pastas |  
| `cd [pasta]`  | Muda de diretório |  
| `cd ..`       | Volta um nível |  
| `cd ~`        | Vai para a home do usuário |  

#### 1.3.2. Manipulação de Arquivos
| Comando        | Descrição |  
|---------------|-----------|  
| `touch [arquivo]` | Cria um arquivo vazio |  
| `mkdir [pasta]`   | Cria uma pasta |  
| `cp [origem] [destino]` | Copia arquivos |  
| `mv [origem] [destino]` | Move ou renomeia arquivos |  
| `rm [arquivo]`    | Remove arquivos |  
| `rm -r [pasta]`   | Remove pastas recursivamente |  

#### 1.3.3. Permissões
| Comando        | Descrição |  
|---------------|-----------|  
| `chmod [permissões] [arquivo]` | Altera permissões |  
| `chown [usuário:grupo] [arquivo]` | Muda dono/grupo |  

Exemplo:  
```bash
chmod 755 script.sh  # Dá permissão de execução  
chown root:root arquivo.txt  # Define dono como root  
```

#### 1.3.4. Tarefas (Processos) e Sistema
| Comando        | Descrição |  
|---------------|-----------|  
| `ps`          | Lista processos ativos |  
| `top`         | Monitora processos em tempo real |  
| `kill [PID]`  | Encerra um processo |  
| `df -h`       | Mostra espaço em disco |  
| `free -h`     | Mostra uso de memória |  

#### 1.3.5. Rede
| Comando       | Descrição |  
|--------------|-----------|  
| `ping [host]` | Testa conexão com um servidor |  
| `ifconfig`   | Mostra interfaces de rede |  
| `ssh [usuário@host]` | Conecta-se remotamente |  

---

### 1.4. Editores de Texto no Terminal

#### 1.4.1. Nano (Simples)
```bash
nano arquivo.txt  # Abre o editor Nano  
```
- `Ctrl + O` → Salva  
- `Ctrl + X` → Sai  

#### Vim (Avançado)
```bash
vim arquivo.txt  # Abre o Vim  
```
- Modos:  
  - `i` → Modo de inserção  
  - `ESC` → Volta ao modo normal  
  - `:wq` → Salva e sai  

---

### 1.5. Gerenciamento de Pacotes

#### 1.5.1. Debian/Ubuntu (APT)
```bash
sudo apt update          # Atualiza lista de pacotes  
sudo apt install [pacote] # Instala um pacote  
sudo apt remove [pacote]  # Remove um pacote  
```

#### 1.5.2. Fedora (DNF)
```bash
sudo dnf install [pacote]  
sudo dnf remove [pacote]  
```

#### 1.5.3. Arch Linux (Pacman)
```bash
sudo pacman -S [pacote]    # Instala  
sudo pacman -R [pacote]    # Remove  
```

---

### 1.6. Próximos Passos
- Aprenda **shell scripting** para automatizar tarefas.  
- Explore **serviços de rede** (Apache, Nginx, SSH).  
- Estude **gerenciamento de usuários e permissões**.  

---
