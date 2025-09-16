### **1. Conceitos Fundamentais**

- **O que é Linux?**
    
    - Diferença entre **Linux (kernel)** e **GNU/Linux (sistema operacional)**.
        
    - Distribuições populares (**Ubuntu, Debian, Fedora, Arch, CentOS**).
        
    - Filosofia Unix: "Tudo é arquivo", "Um programa deve fazer uma coisa bem".
        
- **Terminal e Shell**
    
    - Diferença entre **shell** (Bash, Zsh, Fish) e **terminal** (emulador).
        
    - Comandos básicos (`ls`, `cd`, `mkdir`, `rm`, `cp`, `mv`, `cat`, `echo`).
        
    - Redirecionamento (`>`, `>>`, `|`, `<`).
        

---

### **2. Sistema de Arquivos e Estrutura**

- **Hierarquia do sistema de arquivos** (`/bin`, `/etc`, `/home`, `/var`, `/usr`).
    
- **Permissões e propriedade** (`chmod`, `chown`, `umask`).
    
- **Links simbólicos e hard links** (`ln`).
    
- **Montagem de sistemas de arquivos** (`mount`, `umount`, `/etc/fstab`).
    

---

### **3. Gerenciamento de Pacotes**

- **Debian/Ubuntu (APT)**:  
    `apt update`, `apt install`, `apt remove`, `dpkg`.
    
- **Red Hat/Fedora (DNF/YUM)**:  
    `dnf install`, `yum remove`, `rpm`.
    
- **Arch Linux (Pacman)**:  
    `pacman -S`, `pacman -R`.
    
- **Snap e Flatpak** (pacotes universais).
    

---

### **4. Processos e Gerenciamento do Sistema**

- **Visualizar e gerenciar processos** (`ps`, `top`, `htop`, `kill`, `pkill`).
    
- **Inicialização do sistema (Systemd vs. SysVinit)**:
    
    - `systemctl start/stop/enable`.
        
    - `/etc/systemd/system/`.
        
- **Logs do sistema** (`journalctl`, `/var/log/`).
    

---

### **5. Redes no Linux**

- **Comandos básicos** (`ifconfig`/`ip`, `ping`, `netstat`, `ss`, `traceroute`).
    
- **Configuração de rede** (`nmcli`, `/etc/network/interfaces`).
    
- **Firewall** (`iptables`, `nftables`, `ufw`).
    
- **SSH** (`ssh`, `scp`, chaves públicas/privadas, `~/.ssh/config`).
    

---

### **6. Scripting e Automação**

- **Shell Script (Bash)**:
    
    - Variáveis, loops (`for`, `while`), condicionais (`if`).
        
    - Funções e argumentos (`$1`, `$@`).
        
- **Ferramentas de automação** (`cron`, `systemd timers`).
    
- **Processamento de texto** (`grep`, `awk`, `sed`, `cut`).
    

---

### **7. Segurança**

- **Controle de acesso** (`sudo`, `visudo`, grupos).
    
- **Auditoria** (`chroot`, `SELinux`, `AppArmor`).
    
- **Criptografia** (`GPG`, `openssl`, LUKS para discos).
    
- **Senhas e autenticação** (`/etc/shadow`, `passwd`).
    

---

### **8. Virtualização e Containers**

- **Máquinas virtuais** (`KVM`, `QEMU`, `VirtualBox`).
    
- **Containers** (`Docker`, `Podman`, `LXC`).
    
- **Orquestração** (`Kubernetes` básico).
    

---

### **9. Kernel e Drivers**

- **Módulos do kernel** (`lsmod`, `modprobe`).
    
- **Compilar o kernel** (opcional para avançados).
    
- **Gerenciamento de drivers** (`dkms`, `lspci`, `lsusb`).
    

---

### **10. Solução de Problemas (Troubleshooting)**

- **Diagnóstico de hardware** (`dmesg`, `lshw`).
    
- **Problemas de boot** (`GRUB`, `initramfs`).
    
- **Recuperação de sistemas corrompidos** (live USB, `fsck`).
    

---

### **11. Ferramentas Úteis para Dominar**

- **Editores de texto** (`vim`, `nano`, `emacs`).
    
- **Monitoramento** (`nmon`, `glances`, `iotop`).
    
- **Versionamento** (`git` para colaboração em projetos).
    

---

### **12. Aprofundamento (Opcional)**

- **Linux em servidores** (Apache/Nginx, PostgreSQL/MySQL).
    
- **Programação em C/Python para Linux**.
    
- **Automatização com Ansible/Puppet**.
    

---

### **Como Praticar?**

1. **Use Linux no dia a dia** (substitua Windows/macOS ou use dual boot).
    
2. **Experimente distribuições diferentes** (Ubuntu para iniciantes, Arch para aprendizado profundo).
    
3. **Contribua para projetos open-source** (GitHub, fóruns).
    
4. **Desafie-se** (configure um servidor em casa, crie scripts úteis).
    

---

### **Livros Recomendados**

- "The Linux Command Line" (William Shotts).
    
- "How Linux Works" (Brian Ward).
    
- "Linux Bible" (Christopher Negus).