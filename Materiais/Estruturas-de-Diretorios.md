## Principais Diretórios no Linux

### /bin (Binários)

- **Função**: Armazena executáveis essenciais do sistema
    
- **Contém**: Comandos básicos como `ls`, `cp`, `mv` e outros binários críticos
    
- **Observação**: Acessível a todos os usuários
    

### /boot

- **Função**: Arquivos necessários para a inicialização do sistema
    
- **Contém**:
    
    - Kernel do Linux
        
    - Arquivos do GRUB (gerenciador de boot)
        
    - Configurações de inicialização
        

### /cdrom (obsoleto em muitas distros)

- **Função**: Ponto de montagem tradicional para mídias ópticas
    
- **Observação**: Substituído por `/media` em distribuições modernas
    

### /dev (Dispositivos)

- **Função**: Arquivos especiais que representam dispositivos de hardware
    
- **Exemplos**:
    
    - `/dev/sda` (discos rígidos)
        
    - `/dev/tty` (terminais)
        
    - `/dev/null` (dispositivo nulo)
        

### /etc

- **Função**: Configurações do sistema e aplicativos
    
- **Contém**:
    
    - Arquivos de configuração (`/etc/passwd`, `/etc/fstab`)
        
    - Scripts de inicialização
        
    - Configurações de rede
        

### /home

- **Função**: Diretórios pessoais dos usuários
    
- **Estrutura típica**:
    
    - `/home/usuario1/`
        
    - `/home/usuario2/`
        
    - Cada usuário tem seu próprio diretório com subpastas (Documentos, Downloads, etc.)
        

### /lib (Bibliotecas)

- **Função**: Bibliotecas compartilhadas essenciais para os binários em `/bin` e `/sbin`
    
- **Subdiretórios**:
    
    - `/lib32`: Bibliotecas para sistemas 32-bit
        
    - `/lib64`: Bibliotecas para sistemas 64-bit
        
    - `/libx32`: Bibliotecas para arquitetura x32
        

### /mnt e /media (Pontos de Montagem)

- **/media**: Montagem automática de dispositivos removíveis (USB, CDs)
    
- **/mnt**: Montagem temporária de sistemas de arquivos
    

### /proc (Processos)

- **Função**: Sistema de arquivos virtual que fornece informações sobre processos e recursos do sistema
    
- **Características**:
    
    - Arquivos representam processos em execução (PID)
        
    - Informações em tempo real sobre hardware e sistema
        
    - Não ocupa espaço em disco (existe apenas na memória RAM)
        

## Diferenciais Importantes

1. **Case-sensitive**: Diferencia letras maiúsculas de minúsculas
    
2. **Estrutura unificada**: Tudo parte do diretório raiz (`/`)
    
3. **Padronização**: Segue o Filesystem Hierarchy Standard (FHS)
