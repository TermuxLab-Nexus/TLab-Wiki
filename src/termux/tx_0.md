# INTRODUÇÃO AO TERMUX
<p align="justify">
    O Termux é um aplicativo de emulador de terminal aprimorado com um amplo conjunto de utilitários CLI (command Line), 
    adaptado para o sistema operacional Android. Seu principal objetivo é fornecer uma experiência de terminal analoga
    a um ambiente linux tradicional em dispositivos móveis, sem necessidade de root ou qualquer outra modificação técnica. 
</p>

## Como funciona?
<p align="justify">
    Ele não é uma <a href="https://www.ibm.com/br-pt/think/topics/virtual-machines">máquina virtual</a> nem qualquer outro tipo de ambiente emulado ou simulado. Todos os pacotes
    fornecidos são compilados com o <a href="https://developer.android.com/ndk/guides?hl=pt-br">Android NDK</a> e contêm apenas patches de compatibilidade para funcionar 
    no Android. O sistema operacional não fornece acesso total ao seu <a href="https://www.ibm.com/docs/pt-br/aix/7.3.0?topic=management-file-systems">sistema de arquivos</a>, portanto, o Termux
    não pode instalar arquivos de pacotes em <em style="font-weight:bold;">diretórios</em> padrão de sistemas GNU/Linux como:

- /bin -> Diretório onde ficam armazenados os binários do S.O;

- /etc -> Diretório onde ficam armazenados os arquivos de configuração dos binários;

- /usr -> Diretório onde ficam os utilitários adicionais(não pertecem ao núcleo do S.O);

- /var -> Dirétorio onde ficam os arquivos voláteis do S.O(cache,logs etc...).

</p>

### Diretório Raiz /

```
├── apex
├── bin -> usr/bin
├── boot
├── data
├── dev
├── etc
├── home
├── lib -> usr/lib
├── linkerconfig
├── media
├── mnt
├── odm
├── opt
├── proc
├── product
├── root
├── run
├── sbin -> usr/sbin
├── sdcard
├── srv
├── storage
├── sys
├── system
├── tmp
├── usr
├── var
└── vendor
```

## Onde se encontra o ambiente Termux dentro do Android?
<p align="justify">
    Como dito anteriormente, o Termux não é uma maquina virtual ou similares,portanto,
    seu ambiente está contido em <strong>/data/data/com.termux/files/home</strong>  e pode ser acessado
    nativamente via <a href="https://developer.android.com/guide/topics/providers/document-provider?hl=pt-br">SAF</a> ou um aplicativo de gerenciamento de arquivos convencional.
</p>

## O que eu posso fazer com o Termux?
<p align="justify">
    Existem diversas aplicações para o termux, desde gerenciar arquivos e diretórios através do CLI a atuar
    como um ambiente desktop <em>quase</em> completo, com suporte ao <a href="https://www.x.org">servidor gráfico Xorg</a>
    e diversos <a href="">"Desktop Environments" (DE)</a>.
</p>

 Dentre as multiplas capacidades que essa ferramenta proporciona, nós das TermuxLab enfatizamos:
- Uso como computador pessoal através de ferramentas como proot, VNC e X11;
- Ambiente de desenvolvimento, com suporte a linguagens como Rust, Python, Javascript, Go, C etc;
- Servidor multimidia ou Homelab;
- Ambiente de pentest e Cybersecurity.

<p>
    Embora ainda esteja  limitado as regras de sistema do Android, os maiores limitadores desse ambiente são a paciência, conhencimento e capacidade de execuçao do usuário. Com o tempo, a comunidade vem diminuindo e contornando essas barreiras técnicas, portanto nós encorajamos você a contribuir com o projeto, seja através de código, tutoriais ou mesmo reportando bugs e problemas, além de adotar a norma TLAB26 da TermuxLab no seu contidiano.
</p>

