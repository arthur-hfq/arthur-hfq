# Arthur H. Faria Queiros (@Mepper)

```text
+------------------------------------------------------------------------------+
|  MEPPER // ACERVO TÉCNICO & REGISTRO DE ENGENHARIA DE SISTEMAS               |
+------------------------------------------------------------------------------+
|  IDENTIDADE  : Arthur H. Faria Queiros (@Mepper / @arthur-hfq)               |
|  OCUPAÇÃO    : Engenharia de Software & Matemática                           |
|  STATUS      : REGISTRO: Acervo Ativo // REV 2026.10                         |
|  AMBIENTE    : Linux x86_64 (Kernel >= 6.x) // POSIX // Btrfs CoW            |
+------------------------------------------------------------------------------+
```

<div align="center">
  <img src="./assets/avatar.png" width="144" height="144" alt="Arthur H. Faria Queiros" style="border-radius: 50%; border: 2px solid #292f39;" />
  <br/><br/>
  <b>Arthur H. Faria Queiros</b> &nbsp;|&nbsp; <code>@Mepper</code><br/>
  <i>Engenheiro de Software & Estudante de Matemática</i>
  <br/><br/>
  <code>REGISTRO: Acervo Ativo</code> &nbsp;·&nbsp; <code>REV 2026.10</code> &nbsp;·&nbsp; <code>LÂMINAS B5</code>
  <br/><br/>
  <a href="https://mepper.xyz"><code>[ Acervo Técnico (mepper.xyz) ↗ ]</code></a> &nbsp;
  <a href="https://x.com/my_name_is_arth"><code>[ X (@my_name_is_arth) ↗ ]</code></a> &nbsp;
  <a href="https://github.com/arthur-hfq"><code>[ Repositórios GitHub ↗ ]</code></a>
</div>

---

### § 00 // Propedêutica & Filosofia de Construção

Engenheiro de software e estudante dedicado de matemática — com foco formal em álgebra linear, cálculo diferencial e integral, computação científica e sistemas de baixo nível. Desenvolvo sistemas robustos partindo estritamente de primeiros princípios, rejeitando atalhos superficiais e fundamentando cada linha de código em rigor dedutivo e modelagem axiomática.

> [!NOTE]
> **Declaração de Princípios & Natureza do Acervo**
> Este espaço e o acervo em [mepper.xyz](https://mepper.xyz) existem com uma finalidade única e intransigente: registrar formalmente o acervo de conteúdo que estudo, investigo e desenvolvo. Todo o material disponibilizado é de acesso inteiramente aberto e pode ser lido, copiado, compartilhado e utilizado sem quaisquer custos, travas de assinatura ou poluição publicitária.
> 
> Não se trata de tutoriais efêmeros ou receitas para consumo rápido, mas sim de um acervo intelectual voltado primariamente para documentação e consulta fundamentadas no método dedutivo.

---

### § 01 // Compêndio Fundamental: Tomo I

O núcleo teórico deste acervo encontra-se consolidado no **Compêndio 0**, estruturado na geometria física e digital de lâminas modulares B5.

```text
TOMO I // COMPÊNDIO 0: Da Fundamentação e Método Epistemológico
FIXAÇÃO: 05 OUT 2026 // MODULARIDADE: Lâminas B5 (f0 a f2)
```

Fundamentos da propedêutica formal, estruturação de axiomas, lemas e teoremas, modularidade em lâminas B5 e diretrizes analíticas para leitura dos tratados de ponta a ponta:

| Fascículo | Título | Escopo / Extensão |
| :--- | :--- | :--- |
| **§ f0** | **Propedêutica Formal & O Método Dedutivo** | Epistemologia, primeiros princípios e rejeição da indução ingênua |
| **§ f1** | **A Estrutura Tripartite: Axioma, Lema e Teorema** | Arquitetura de derivação lógica e encadeamento formal de premissas |
| **§ f2** | **Geometria do Suporte: A Lâmina B5 e Modularidade** | Restrição física, densidade tipográfica e atomicidade do conhecimento |

Consulte o acervo integral em: [mepper.xyz](https://mepper.xyz).

---

### § 02 // Projetos em Desenvolvimento (Engenharia de Sistemas)

#### 01. mkb-grid
*Bespoke Terminal UI & Infrastructure Control Node for Local Containers*

```text
+--------------------------------------------------------------+
|  [MKB-GRID] INFRASTRUCTURE CONTROL NODE                      |
+--------------------------------------------------------------+
|  SERVICES DASHBOARD                                          |
|  Total Nodes: 4 | Running: 3 | Paused: 1                     |
|                                                              |
|  > mkb_svc_postgres_5432       Up 4 hours      5432->5432    |
|    mkb_svc_redis_6379          Up 4 hours      6379->6379    |
|    mkb_svc_kafka_9092          Up 2 hours      9092->9092    |
|    mkb_svc_rabbitmq_5672       Exited (0)      5672->5672    |
|                                                              |
+--------------------------------------------------------------+
```

- **Classificação**: Infraestrutura & TUI
- **Estado**: `EM REESCRITA // v1.0 (Shell POC) -> v2.0 (Rust + Podman + Quickshell)`
- **Repositório**: [`arthur-hfq/mkb-grid`](https://github.com/arthur-hfq/mkb-grid)
- **Especificações de Arquitetura**:
  - Painel de controle TUI brutalista orientado a teclado para orquestração de infraestrutura local de bancos e mensageria (PostgreSQL 16, Redis 7, Kafka 3.7 KRaft mode, RabbitMQ 3).
  - Descoberta automatizada de portas livres via varredura de sockets TCP do host (`ss` e mapeamentos de runtime) para eliminação de colisões.
  - Snapshots atômicos de subvolumes Btrfs Copy-on-Write (CoW) para rollback instantâneo de bancos de dados a um ponto no tempo sem recriação de contêineres.
  - Isolamento e topologia de rede em pontes personalizadas (`mkb_net_*`) com hot-attach e panorama agregado de logs em tempo real.
  - Exportação determinística para `mkb-grid-compose.yml`.

---

#### 02. mkb-api-stress
*Docker-Isolated API Stress & Load Testing Engine with Live Telemetry*

```text
+--------------------------------------------------------------+
|  [MARKAB] STRESS TEST REPORT                                 |
+--------------------------------------------------------------+
|  ENVIRONMENT : Docker (0.5 CPU | 256m RAM)                   |
|  TOTAL REQS  : 100                                           |
|  SUCCESS     : 100 (100%)                                    |
|  FAILED      : 0 (0%)                                        |
|                                                              |
|  AVG LATENCY : 14ms (P95: 22ms | P99: 38ms)                  |
|  THROUGHPUT  : 168.42 req/s                                  |
|  MAX CPU     : 94.0% (Normalized Timeline)                   |
|  MAX RAM     : 54.1MiB / 256MiB                              |
+--------------------------------------------------------------+
```

- **Classificação**: Sistemas & Concorrência
- **Estado**: `EM REESCRITA // v1.0 (Shell POC) -> v2.0 (Go + Matemática Estocástica)`
- **Repositório**: [`arthur-hfq/mkb-api-stress`](https://github.com/arthur-hfq/mkb-api-stress)
- **Especificações de Arquitetura**:
  - Motor determinístico de testes de carga executado contra instâncias isoladas em contêineres efêmeros com tetos rígidos de hardware (`--cpus`, `--memory`).
  - Telemetria de alta frequência com amostragem a cada 200ms via daemon em segundo plano, computando linha do tempo normalizada de capacidade da CPU e pico de memória.
  - Relatório brutalista em terminal com visualizador de códigos de status HTTP e percentis de latência (P50, P90, P95, P99).
  - Integração nativa com buffers do Neovim via Lua para execução imediata durante o desenvolvimento de backends.

---

#### 03. Minerva
*Mindustry Logic High-Level Compiler*

- **Classificação**: Compiladores & Autômatos
- **Estado**: `PLANEJADO // Versão 0.0`
- **Especificações de Arquitetura**:
  - Compilador de linguagem de alto nível com tipagem estática voltado para o conjunto de instruções dos microprocessadores lógicos do Mindustry.
  - Front-end com parser léxico/sintático gerador de árvore de sintaxe abstrata (AST) validada formalmente.
  - Síntese de representação intermediária linearizada (IR) com otimização de expressões algébricas.
  - Alocador ótimo de registradores baseado em coloração de grafos de interferência (Chaitin-Briggs).
  - Minimização de saltos condicionais e fluxo de controle modelado por autômatos finitos determinísticos (DFA).

---

### § 03 // Matriz Operacional & Ferramental

```text
SISTEMAS OPERACIONAIS : Linux x86_64 (Arch Linux, Kernel >= 6.x)
SISTEMAS DE ARQUIVOS  : Btrfs (Subvolumes CoW, Snapshots Atômicos)
ISOLAMENTO & RUNTIMES : OCI Containers, Docker Engine, Podman
LINGUAGENS            : C, Rust, Go, POSIX Shell / Bash, Python, Lua, Typst / TeX
DESENVOLVIMENTO       : Neovim (Lua), Tmux, Git, GNU Toolchain, Make
PARADIGMA             : Primeiros Princípios, Teoria de Grafos, Modelagem Dedutiva
```

---

### § 04 // Comunicação & Canais Externos

- **Acervo Principal & Compêndios**: [mepper.xyz](https://mepper.xyz)
- **Repositório do Acervo**: [`arthur-hfq/mepper`](https://github.com/arthur-hfq/mepper)
- **Perfil de Código no GitHub**: [`github.com/arthur-hfq`](https://github.com/arthur-hfq)
- **Dispatches & Notas Técnicas (X)**: [`@my_name_is_arth`](https://x.com/my_name_is_arth)

```text
[ ARQUIVO FORMALIZADO // MEPPER.XYZ // REGISTRO 2026 ]
```
