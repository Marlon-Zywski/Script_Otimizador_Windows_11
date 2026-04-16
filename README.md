# Otimização Windows 11 - Edição Corporativa

Este repositório contém um poderoso script em Batch (`.bat`) projetado especificamente para **otimizar, limpar e acelerar o Windows 11 em ambientes corporativos e empresariais**. Diferente de scripts "gamers" agressivos que tendem a danificar redes e proteções do sistema, este script foi cuidadosamente arquitetado para manter a segurança do computador e preservar ferramentas essenciais de trabalho e gestão de TI corporativa.

## 🚀 O Que Este Script Faz

O `otimizar_win11.bat` atua em várias camadas do sistema operacional com o objetivo de entregar máxima performance de processamento sem sacrificar estabilidade. 

### 🛡️ 1. Otimizações Seguras e Refinamentos:
* **Desativação de Serviços Inúteis:** Desabilita serviços pesados e desnecessários como Telemetria DiagTrack, Mapas Offline, Fax, Modo Demo de Varejo (Retail Demo), Xbox Services, etc.
* **Efeitos Visuais Inteligentes:** Altera as preferências visuais para "Desempenho", removendo sombras pesadas e atraso de menus, porém **preserva** as fontes suavizadas (ClearType), as miniaturas de pré-visualização e a exibição do conteúdo de janelas ao arrastar.
* **Fim das Telas Irritantes (SCOOBE e Dicas):** Remove a incômoda tela branca de tela cheia que aparece na inicialização "Vamos terminar de configurar o seu dispositivo", assim como dicas encrustadas, sugestões no menu Iniciar e anúncios do sistema.
* **Performance Real:** Adiciona os ajustes de prioridade de GPU/CPU no registro e aplica imediatamente o Plano de Energia **Desempenho Máximo** (Ultimate Performance) / Alta Performance na raiz do sistema.
* **Remoção de Bloatwares:** Remove silenciosamente jogos embarcados como Candy Crush, Xbox Game Bar, 3D Builder, app nativo Clima/Maps, sem necessidade de intervenção do usuário.
* **Desativação de Custos Extras:** Desativa a Cortana, Widgets da barra de tarefas, Transparências do explorador, Hibernação (para liberar GBs no disco) e tarefas ocultas de envio de dados para a Microsoft.

### ⚙️ 2. Automação e Manutenção Contínua (Hands-Free):
* **Reboot Automático Programado:** O script gera uma tarefa agendada invisível diretamente acoplada ao sistema (`SYSTEM`) para forçar a **reinicialização da máquina todos os dias às 02:00 da manhã**. Isso elimina lentidão por acúmulo de uptime e renova as conexões de rede para o dia seguinte sem depender se há um usuário logado.
* **Limpador Global Automático (Logon Task):** Diferente de limpezas pontuais, ele cria um arquivo base oculto (no `C:\ProgramData\ScriptsTI`) e o agenda para rodar em modo invisível na conta primária a cada *Logon* de usuário. Esse atuador varre as pastas e caches temporários não-vitais do sistema (`Windows/Temp` e `AppData/Local/Temp`) impedindo que o Windows fique lento por estrangulamento de lixo, e poupando a pasta `Prefetch` para que ferramentas grandes, como navegadores e pacote Office abram quase instatâneamente.

### 🔒 3. Proteções Mantidas (Por que é "Corporativo"?):
* **TCP/IP e Rede Nativa:** Não faz descargas no IP ou *TCP Auto-Tuning* evitando que softwares como **AnyDesk**, **TeamViewer** e **RDP** ou servidores de Domínio caiam e fiquem inacessíveis pelo T.I.
* **Microsoft Teams / Ferramentas:** Preserva os comunicadores corporativos ativamente instalados.
* **Segurança Base (VBS/HVCI):** Não desliga as mitigações contra Meltdown e proteções do kernel de memória, respeitando as políticas do Active Directory corporativo.
* **WSearch e Registry:** O serviço de indexação `WSearch` é ignorado para garantir o funcionamento veloz das buscas vitais dentro do ***Microsoft Outlook***. Ações remotas e telemetria pontual (`WerSvc`) são salvas para que o painel de gerenciamento de TI consiga atuar caso haja tela azul na máquina de longe.

---

## 💻 Como Utilizar

⚠️ **Aviso antes do uso:** Se for aplicar isso em *Notebooks* empresariais, tenha ciência que a Hibernação será desligada. Alerte seu T.I local caso haja diretrizes de bateria mandatórias em viagens.

1. Baixe os arquivos (`.bat`) deste repositório para o PC alvo.
2. Clique com o botão direito sobre o arquivo **`otimizar_win11.bat`**.
3. Selecione **Executar como Administrador**.
4. Aceite o aviso inicial (Procurando a letra "S" + Enter).
5. O script correrá pelo sistema; ao emitir o log verde de encerramento, pressione qualquer tecla.
6. **REINICIE AS MÁQUINAS** para validar 100% dos registros criados!

Uma vez finalizado, as operações de autolimpeza e auto-reboot estão engatilhadas e a máquina se autogerenciará.

---

## ↩️ Como Reverter

Caso necessite desfazer e jogar as customizações de volta ao modo original de fábrica para aprovar alguma auditoria:
1. Clique no **`reverter_win11.bat`** com o botão direito e **Execute como Administrador**.
2. Uma vez finalizado, ele apagará as tarefas automatizadas, as trilhas de registro customizadas da UI e reativará a telemetria, hibernação, dicas e anúncios. 
3. Da mesma formma, o PC deverá ser **reiniciado**.
*(Lembrete: Os bloatwares excluídos da MS Store, como o Candy Crush, não serão baixados juntos, deverão sofrer busca manual na app store se necessários).*
