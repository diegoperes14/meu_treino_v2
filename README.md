# 💪 Meu Treino - Diário de Acompanhamento Fitness

[![GitHub license](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

**Meu Treino v3** é um aplicativo web completo, projetado para ajudar entusiastas do fitness a rastrear seus treinos com precisão e monitorar sua evolução física ao longo do tempo. Deixe de lado planilhas complexas e use uma interface intuitiva que acompanha cada série, repetição e carga utilizada!

---

## ✨ Funcionalidades Principais

*   🏋️ **Registro Detalhado:** Registre exercícios por dia da semana (ex: Segunda-feira - Peito) com acompanhamento de Séries, Repetições e Carga para cada série individual.
*   📊 **Evolução Visual:** Visualize gráficos poderosos mostrando seu volume total levantado e sua carga máxima em exercícios específicos ao longo do tempo.
*   🔄 **Fluxo Contínuo:** Um sistema intuitivo que mantém o foco no treino, incluindo um *Timer de Descanso* integrado para manter a rotina correta.
*   🗓️ **Organização Semanal:** Organize seus treinos por dias da semana (Domingo a Sábado), facilitando a criação de rotinas consistentes.
*   ⚙️ **Configurável:** Permite ao usuário definir o tempo de descanso padrão e alternar entre Modo Claro/Escuro.

## 🚀 Começando

Este é um aplicativo *Single Page Application* (SPA) que deve ser rodado em um ambiente web moderno. Basta acessar o arquivo `index.html` para começar a usar!

### Como Usar:

1.  **Página "Hoje" (`🏠`):** Veja o treino agendado para hoje, com o progresso geral e os controles de registro.
2.  **Adicionar/Editar Exercícios (`🏋️`):** Clique no botão **+ Adicionar exercício** ou em **✏️** nos treinos diários para montar sua rotina. Você precisará nomear o exercício, definir o grupo muscular, o número de séries e reps padrão.
3.  **Registro:** Ao fazer um treino, marque cada série como concluída (`✓`) após completar o peso e rep desejados. Os dados são salvos automaticamente!
4.  **Evolução (`📊`):** Esta é a parte mais poderosa! Aqui você verá gráficos do seu desempenho passado, calculando volume total, séries concluídas e cargas máximas atingidas em exercícios específicos.
5.  **Configurações (`⚙️`):** Backup de dados (JSON), restauração e gerenciamento de temas.

## 💻 Estrutura Técnica (Para Desenvolvedores)

O projeto é um Single Page Application JavaScript robusto, seguindo o padrão MVVM (Model-View-ViewModel) simplificado.

*   **Modelo de Dados:** O estado principal (`state`) é armazenado em `localStorage` sob a chave `meuTreino_v3`.
    *   `exercises`: Mapeia os exercícios por dia da semana.
    *   `workouts`: Histórico dos treinos, mapeando data -> dia da semana -> exercício ID -> {séries: [...], done: bool}.
    *   `settings`: Preferências do usuário (modo escuro, descanso padrão).
*   **Componentes Chave:**
    *   `renderHeader()`: Gerencia a navegação e o estado ativo do dia.
    *   Funções de Manipulação de Estado (`save()`, `loadState()`, `normalizeState()`): Garantem que os dados são salvos e carregados corretamente, mesmo em versões futuras.
*   **Dependências:**
    *   Bootstrap 5.3.3 (Para UI/UX).
    *   Chart.js (Para visualização de gráficos estatísticos).

## 📚 Contribuições

Sinta-se à vontade para fazer um fork e contribuir! As melhorias podem incluir:
*   Integração com APIs de equipamentos de academia.
*   Adicionar suporte a novos tipos de exercícios (e.g., aquecimento/alongamento).
*   Melhorar a experiência mobile em telas menores.

---
_Desenvolvido para ser o companheiro ideal na jornada fitness._