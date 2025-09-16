
___
## 📁 Diretórios Fundamentais

### 🔧 `/bin` (Binários Essenciais)
**Função Principal:** Armazena executáveis essenciais do sistema

| Característica | Descrição |
|----------------|-----------|
| **Contém** | Comandos básicos: `ls`, `cp`, `mv`, `cat`, `grep` |
| **Acesso** | Disponível para todos os usuários |
| **Importância** | Crítico para funcionamento básico do sistema |

```bash
# Exemplos de binários em /bin
ls /bin/ls     # Comando para listar arquivos
ls /bin/cp     # Comando para copiar
ls /bin/bash   # Shell Bash
```

---

### 🚀 `/boot` (Inicialização)
**Função Principal:** Arquivos necessários para boot do sistema

#### 📦 Componentes Principais:
- **Kernel do Linux** (`vmlinuz`)
- **Imagem de RAM inicial** (`initrd` ou `initramfs`)  
- **Arquivos do GRUB** (gerenciador de boot)
- **Configurações de inicialização**

```bash
# Visualizar conteúdo do /boot
ls -la /boot/
# vmlinuz-5.x.x-generic    <- Kernel
# initrd.img-5.x.x-generic <- RAM disk inicial
# grub/                    <- Configurações do GRUB
```

---

### 💿 `/cdrom` (Legado)
**Status:** Obsoleto em distribuições modernas

| Antes | Agora |
|-------|-------|
| `/cdrom` | `/media` ou `/mnt` |
| Ponto fixo | Montagem dinâmica |

> ⚠️ **Nota:** Mantido apenas para compatibilidade com sistemas antigos

---

### ⚡ `/dev` (Dispositivos)
**Função Principal:** Interface com dispositivos de hardware

#### 🖥️ Dispositivos Comuns:
| Arquivo | Dispositivo |
|---------|-------------|
| `/dev/sda`, `/dev/sdb` | Discos rígidos/SSDs |
| `/dev/tty1`, `/dev/tty2` | Terminais virtuais |
| `/dev/random` | Gerador de números aleatórios |
| `/dev/zero` | Fonte de zeros infinitos |

```bash
# Exemplos práticos
echo "teste" > /dev/null  # Descarta saída
cat /dev/random | head -c 10  # Gera dados aleatórios
dd if=/dev/zero of=arquivo bs=1M count=100  # Criar arquivo de zeros
```

---

### ⚙️ `/etc` (Configurações)
**Função Principal:** Centro de configuração do sistema

#### 📋 Arquivos Importantes:
- **`/etc/passwd`** - Informações de usuários
- **`/etc/fstab`** - Pontos de montagem automática  
- **`/etc/hosts`** - Mapeamento de nomes para IPs
- **`/etc/crontab`** - Tarefas agendadas do sistema
- **`/etc/sudoers`** - Configurações do sudo

```bash
# Verificar usuários do sistema
cat /etc/passwd | head -5

# Ver pontos de montagem
cat /etc/fstab

# Configurações de rede local
cat /etc/hosts
```

---

### 🏠 `/home` (Diretórios Pessoais)
**Função Principal:** Espaço privado dos usuários

#### 📂 Estrutura Típica:
```
/home/
├── usuario1/
│   ├── Desktop/
│   ├── Documents/
│   ├── Downloads/
│   ├── Pictures/
│   └── .bashrc (arquivos ocultos)
├── usuario2/
└── usuario3/
```

#### 🔒 Características:
- Cada usuário tem permissões completas no seu diretório
- Arquivos iniciados com `.` são ocultos
- Configurações pessoais ficam em arquivos ocultos

---

### 📚 `/lib` (Bibliotecas Compartilhadas)
**Função Principal:** Bibliotecas essenciais para binários do sistema

#### 🏗️ Subdiretórios por Arquitetura:
| Diretório | Arquitetura |
|-----------|-------------|
| `/lib` | Padrão do sistema |
| `/lib32` | 32-bit |
| `/lib64` | 64-bit |
| `/libx32` | x32 (híbrido 32/64) |

```bash
# Ver bibliotecas carregadas por um programa
ldd /bin/ls

# Verificar arquitetura do sistema
uname -m
```

---

### 💾 `/mnt` e `/media` (Pontos de Montagem)

#### 🔄 Diferenças Principais:

| `/media` | `/mnt` |
|----------|--------|
| **Uso:** Automático | **Uso:** Manual |
| **Para:** USBs, CDs, DVDs | **Para:** Montagens temporárias |
| **Exemplo:** `/media/usb0` | **Exemplo:** `/mnt/backup` |

```bash
# Montagem automática (sistema faz)
ls /media/

# Montagem manual
sudo mount /dev/sdb1 /mnt/pendrive
sudo umount /mnt/pendrive
```

---

### 🧠 `/proc` (Sistema de Arquivos Virtual)
**Função Principal:** Interface com informações do kernel e processos

#### 💡 Características Especiais:
- ✅ **Virtual** - existe só na RAM
- ✅ **Dinâmico** - informações em tempo real  
- ✅ **Sem espaço** - não ocupa disco
- ✅ **Somente leitura** (maioria dos arquivos)

#### 📊 Informações Disponíveis:
```bash
# Informações da CPU
cat /proc/cpuinfo

# Uso de memória
cat /proc/meminfo

# Processos em execução
ls /proc/[0-9]*

# Informação do sistema
cat /proc/version
uname -a

# Dispositivos montados
cat /proc/mounts
```

---

## 🎯 Características Fundamentais do Linux

### 📝 Diferenciais Importantes

#### 🔤 **Case-Sensitive**
```bash
# Estes são arquivos DIFERENTES:
arquivo.txt
Arquivo.txt  
ARQUIVO.TXT
```

#### 🌳 **Estrutura Unificada**
- Tudo parte da raiz `/`
- Não há "drives" como C:, D:
- Dispositivos aparecem como diretórios

#### 📏 **Padronização FHS**
**Filesystem Hierarchy Standard** garante consistência entre distribuições

---

## 🗺️ Mapa Visual Rápido

```
/ (raiz)
├── bin/     → Comandos essenciais
├── boot/    → Arquivos de inicialização  
├── dev/     → Dispositivos de hardware
├── etc/     → Configurações do sistema
├── home/    → Diretórios dos usuários
├── lib/     → Bibliotecas compartilhadas
├── media/   → Montagem automática
├── mnt/     → Montagem manual
├── proc/    → Informações do sistema (virtual)
└── ...      → Outros diretórios
```

---

## 💡 Dicas Práticas

### 🚀 Comandos Úteis
```bash
# Navegação rápida
cd /              # Ir para raiz
ls -la /home/     # Ver usuários
df -h /boot/      # Espaço em /boot

# Informações do sistema  
cat /proc/cpuinfo | grep "model name" | head -1
free -h           # Memória disponível
lsblk            # Dispositivos de bloco
```

### ⚠️ Cuidados Importantes
- **Nunca delete** diretórios do sistema sem conhecimento
- **Use sudo** apenas quando necessário
- **Faça backup** antes de modificar `/etc/`
- **Monitore espaço** em `/boot/` (pode encher com kernels antigos)

---

*🔧 **Dica:** Use `man hier` para documentação oficial da hierarquia de diretórios!*