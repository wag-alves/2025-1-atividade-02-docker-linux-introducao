# **Tutorial Básico de Permissões no Linux (Fedora) com `chmod`**

## Informações gerais
- **Objetivo**: conceitos básicos sobre permissões e comando `chmod`
- **Assunto**: Introdução a linux
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** [Sistemas Operacionais](https://github.com/sistemas-operacionais/)
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## **1. Entendendo as Permissões**
No Linux, cada arquivo/diretório tem 3 tipos de permissões:

| Símbolo | Tipo        | Descrição                          |
|---------|------------|-----------------------------------|
| **r**   | Read (ler) | Permissão para ler o arquivo       |
| **w**   | Write (escrever) | Permissão para modificar o arquivo |
| **x**   | Execute (executar) | Permissão para executar (arquivos) ou acessar (diretórios) |

Elas são aplicadas a 3 grupos:
1. **Dono (u)** → Usuário proprietário  
2. **Grupo (g)** → Grupo do dono  
3. **Outros (o)** → Demais usuários  

---

## **2. Sintaxe Básica do `chmod` com Letras**
```bash
chmod [quem][+/-][permissão] [arquivo/diretório]
```

### **Exemplos Práticos:**
### ▶ **Adicionar permissões**
- Dar permissão de **leitura** ao dono:  
  ```bash
  chmod u+r arquivo.txt
  ```
- Dar permissão de **execução** ao grupo:  
  ```bash
  chmod g+x script.sh
  ```
- Dar **todas as permissões** (ler+escrever+executar) a todos:  
  ```bash
  chmod a+rwx pasta/
  ```

### ▶ **Remover permissões**
- Remover permissão de **escrita** de outros:  
  ```bash
  chmod o-w arquivo.txt
  ```
- Remover **execução** do grupo:  
  ```bash
  chmod g-x script.sh
  ```

### ▶ **Definir permissões específicas**
- Resetar permissões para **dono:ler+escrever**, **grupo:ler**, **outros:nada**:  
  ```bash
  chmod u=rw,g=r,o= arquivo.conf
  ```

---

## **3. Como Verificar Permissões?**
Use `ls -l` para visualizar:  
```bash
ls -l arquivo.txt
```
Saída exemplo:  
```bash
-rw-r--r-- 1 user group 1024 Jan 1 10:00 arquivo.txt
```
- **Letras**: `rw-` (dono), `r--` (grupo), `r--` (outros).  
- **Traços (`-`)** indicam permissão ausente.  

---

## **4. Casos de Uso Comuns**
### 🔒 **Proteger um arquivo (somente dono pode editar):**
```bash
chmod u=rw,go= arquivo_secreto.txt
```

### 📂 **Permitir acesso total a uma pasta (recursivo):**
```bash
chmod -R u+rwx minha_pasta/
```
*(`-R` aplica a todos os arquivos dentro do diretório)*

### 🚀 **Tornar um script executável:**
```bash
chmod +x meuscript.sh
```
*(Equivalente a `a+x` – todos podem executar)*

---

## **5. Dica Bônus: Máscara Padrão (`umask`)**
O Linux usa `umask` para definir permissões padrão de novos arquivos.  
- Verificar máscara atual:  
  ```bash
  umask
  ```
- Exemplo: `umask 022` → Arquivos criados terão `644` (dono:rw, outros:r).  

---

## **Exercício Prático (Faça no Fedora!)**
1. Crie um arquivo:  
   ```bash
   touch teste.txt
   ```
2. Remova permissão de leitura para outros:  
   ```bash
   chmod o-r teste.txt
   ```
3. Verifique com:  
   ```bash
   ls -l teste.txt
   ```
   *(Saída esperada: `-rw-r-----`)*  

---

## **Resumo Visual**
```
chmod u+rwx  → Dono: +ler, +escrever, +executar  
chmod go-w   → Grupo e outros: -escrever  
chmod a=rx   → Todos: apenas ler e executar  
```

**Dica:** Use `man chmod` para mais opções! 🐧