# Como configurar/instalar/usar o `desabilitar as comfigurações do compositor` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `desabilitar as comfigurações do compositor` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `disable composer settings` on `Linux Ubuntu`._

## Descrição [2]

### `compositor`

Um `compositor` é um componente de _software_ em sistemas operacionais que gerencia a composição e a exibição de gráficos na tela. Ele é responsável por combinar várias camadas de janelas e elementos gráficos em uma única imagem visual antes de enviá-la para o display. Isso permite efeitos visuais avançados, como transparência, sombras e animações suaves. No contexto de ambientes gráficos modernos, o `compositor` melhora a estética e a funcionalidade da interface do usuário, proporcionando uma experiência visual mais rica e fluida ao garantir que todas as janelas e efeitos sejam renderizados corretamente e de forma eficiente.


## 1. Como configurar/instalar/usar o `desabilitar as comfigurações do compositor` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `listar as pastas dentro de outra com o maior volume de dados` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

O problema que você deve estar enfrentando, onde arrastar uma janela cria várias imagens dela e faz a tela piscar, é geralmente relacionado a um problema com o _driver_ gráfico ou as configurações do `compositor` de janelas no ambiente gráfico. Aqui estão algumas possíveis soluções para resolver isso:

### 1.1 Verificar as configurações do `Compositor`

No `Linux Ubuntu`, que usa o ambiente gráfico `XFCE`, você pode tentar desativar ou ajustar o `compositor`:

1. Vá para `Configurações > Configurações do Gerenciador de Janelas`.

2. Na aba `Compositor`, você pode tentar desativar a opção `"Ativar o compositor de janelas"` para ver se isso resolve o problema.

Se desativar o `compositor` resolver o problema, mas você quiser continuar usando o `compositor`, pode tentar ajustar algumas configurações, como desmarcar `"Sombrear janelas inativas"` ou ajustar a `"Sombra da janela"`.

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `listar as pastas dentro de outra com o maior volume de dados` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    NÃO há.
    ```


No `Linux Ubuntu`, há várias pastas que podem acumular arquivos desnecessários ao longo do tempo e que podem ser limpas com segurança. No entanto, é importante ter cuidado para não excluir arquivos importantes para o funcionamento do sistema ou dos aplicativos. Aqui estão algumas pastas que é conveniente limpar regularmente:

1. **`/tmp`**: Descrição: A pasta `/tmp` é usada para armazenar arquivos temporários que são criados e usados por programas em execução. O sistema limpa essa pasta periodicamente, mas você pode limpá-la manualmente. Como limpar: `sudo rm -rf /tmp/*`

2. **`/var/tmp`**: Descrição: Similar à `/tmp`, mas os arquivos aqui são mantidos por um período mais longo antes de serem excluídos automaticamente. Como limpar: `sudo rm -rf /var/tmp/*`

3. **`/var/cache/apt/archives`**: Descrição: Essa pasta armazena os pacotes `.deb` baixados durante as atualizações e instalações de _software_ usando o `apt`. Os arquivos aqui podem ser removidos após a instalação. Como limpar: `sudo apt-get clean`

4. **`/var/log`**: Descrição: Essa pasta contém arquivos de _log_ do sistema. Alguns _logs_ podem crescer muito com o tempo, ocupando espaço em disco. Como limpar:

    4.1 **Para remover _logs_ antigos**: `sudo journalctl --vacuum-time=2weeks`

    4.2 **Para limpar todos os _logs_ (use com cuidado)**: `sudo rm -rf /var/log/*`

5. **_Cache_ de navegadores**: Descrição: Navegadores como `Firefox` e `Chrome` armazenam caches locais para acelerar o carregamento de páginas. Esses _caches_ podem crescer bastante. Como limpar:

    5.1 **No `Firefox`**: Vá para `Configurações > Privacidade & Segurança > Cookies e dados do site > Limpar dados`.

    5.2 **No `Chrome`**: Vá para `Configurações > Privacidade e segurança > Limpar dados de navegação.`

6. **Arquivos de _cache_ no diretório do usuário**: Descrição: Muitos aplicativos criam caches no diretório do usuário, geralmente em `~/.cache`. Esses arquivos podem ser excluídos com segurança, mas alguns aplicativos podem precisar recriar o _cache_ posteriormente. Como limpar: `rm -rf ~/.cache/*`

7. **`/var/crash`**: Descrição: Contém relatórios de falhas de aplicativos. Se nenhum programa estiver travando, você pode limpá-lo. Como limpar: `sudo rm -rf /var/crash/*`

8. **Arquivos órfãos**: Descrição: Pacotes instalados como dependências que não são mais necessários. Como limpar: `sudo apt-get autoremove`

**Dica Adicional**

**`BleachBit`**: Uma ferramenta gráfica que ajuda a limpar o sistema, removendo _caches_, _logs_, e arquivos temporários de maneira segura.

Lembre-se de fazer _backup_ ou revisar o conteúdo antes de deletar qualquer coisa, especialmente em pastas que você não tem certeza sobre o propósito.

## Referências

[1] OPENAI. ***Listar pastas maiores linux.*** Disponível em: <https://chatgpt.com/c/eb532506-f911-4eb4-a483-6e060cd00863> (texto adaptado). Acessado em: 25/07/2024 13:33.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 25/07/2024 13:33.

