
*Navegação e Manipulação de Arquivos*

---

## 📁 Comandos de Navegação

### Navegação Básica
| Comando | Descrição |
|---------|-----------|
| `pwd` | Mostra o caminho atual (diretório de trabalho) |
| `ls` | Lista arquivos e diretórios do diretório atual |
| `ls *.<extensão>` | Lista todos os arquivos de uma extensão específica |
| `cd` ou `cd ~` | Navega para o diretório home do usuário |
| `cd -` | Retorna para o diretório anterior |
| `cd <diretório>` | Navega para o diretório especificado |

### 💡 Exemplos Práticos
```bash
# Verificar onde você está
pwd

# Listar arquivos Python
ls *.py

# Navegar para Documents
cd Documents

# Voltar ao diretório anterior
cd -
```

---

## 🗑️ Comando `rm` (Remoção)

### Sintaxe Básica
| Comando | Função |
|---------|--------|
| `rm <arquivo>` | Remove um arquivo específico |
| `rm <arquivo1> <arquivo2>` | Remove múltiplos arquivos |
| `rm *.<extensão>` | Remove todos os arquivos de uma extensão |
| `rm -r <diretório>` | Remove diretório e todo seu conteúdo |
| `rm -i <arquivo>` | Remove com confirmação interativa |

### ⚠️ Flags Importantes
- **`-r`** (recursive): Remove diretórios e subdiretórios
- **`-i`** (interactive): Solicita confirmação antes de remover
- **`-f`** (force): Força remoção sem confirmação
- **`-v`** (verbose): Mostra o que está sendo removido

### 🔧 Exemplos de Uso
```bash
# Remover arquivo com confirmação
rm -i documento.txt

# Remover todos os arquivos .log
rm *.log

# Remover pasta inteira
rm -r pasta_antiga

# Remoção forçada (cuidado!)
rm -rf temp/
```

---

## 📦 Comando `mv` (Mover/Renomear)

### Operações Principais
| Comando | Função |
|---------|--------|
| `mv <arquivo> <diretório>` | Move arquivo para outro diretório |
| `mv <nome_antigo> <nome_novo>` | Renomeia arquivo ou diretório |
| `mv *.<extensão> <diretório>` | Move todos os arquivos de uma extensão |

### 🛠️ Flags Úteis
- **`-i`** (interactive): Modo interativo com confirmações
- **`-n`** (no-clobber): Não sobrescreve arquivos existentes
- **`-v`** (verbose): Mostra detalhes da operação
- **`-f`** (force): Força operação sem confirmação

### 📋 Exemplos Práticos
```bash
# Renomear arquivo
mv relatorio.txt relatorio_final.txt

# Mover arquivo para pasta
mv documento.pdf ~/Documents/

# Mover todos os arquivos .jpg para pasta imagens
mv *.jpg imagens/

# Mover com confirmação
mv -i arquivo.txt backup/
```

---

## 📖 Comando `less` (Visualização)

### Função Principal
```bash
less <arquivo>    # Abre arquivo para visualização paginada
```

### 🎮 Controles Dentro do Less
| Tecla | Ação |
|-------|------|
| `q` | Sair (Quit) |
| `h` | Ajuda - lista todos os comandos |
| `n` | Repetir busca anterior |
| `Space` | Página seguinte |
| `b` | Página anterior |
| `/texto` | Buscar por texto |

### 💻 Exemplo de Uso
```bash
# Visualizar arquivo de log
less sistema.log

# Dentro do less:
# Digite /error para buscar por "error"
# Pressione 'n' para próxima ocorrência
# Pressione 'q' para sair
```

---

## 🎯 Dicas Importantes

### ⚡ Atalhos Úteis
- **Tab**: Autocompleta nomes de arquivos e diretórios
- **Ctrl + C**: Cancela comando em execução
- **Ctrl + L**: Limpa a tela
- **↑ ↓**: Navega pelo histórico de comandos

### 🛡️ Segurança
- Sempre use `-i` com `rm` para confirmação
- Tenha cuidado com `rm -rf` - pode apagar tudo!
- Faça backup antes de operações em massa
- Use `ls` para verificar antes de executar comandos destrutivos

### 📚 Recursos Adicionais
- Use `man <comando>` para manual completo
- `<comando> --help` para ajuda rápida
- Tab completion é seu amigo!

---

*💡 **Dica Pro**: Pratique estes comandos em um diretório de teste antes de usar em arquivos importantes!*