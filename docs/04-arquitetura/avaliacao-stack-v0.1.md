# Avaliação preliminar de tecnologias

Status PROPOSTO • ARQ-C3-0.1 • 10/11/2026 • Referências públicas consultadas nesta etapa.

As famílias abaixo constituem candidatas para a prova técnica. Versões exatas, dependências transitivas, vulnerabilidades e compatibilidade conjunta serão registradas no congelamento da implementação. A documentação consultada demonstra caminhos de integração, enquanto a homologação da composição depende da execução futura. Links de documentação são atualizáveis e não fixam um conjunto de versões reproduzível.

## Avaliação da stack indicada em F01

| Tecnologia | Faixa candidata e função | Avaliação / condição |
|---|---|---|
| Node.js | Linha 24 LTS, patch de segurança a fixar | Base proposta para servidor e ferramentas. Conferir ciclo de suporte e disponibilidade no provedor antes da instalação |
| Next.js + React | Next.js 16, React/React DOM 19 em versões compatíveis | Proposta para aplicação única com interface e servidor. Confirmar patches suportados, avisos de segurança e exigências do App Router |
| TypeScript | Versão estável que atenda Prisma e Zod, a fixar | Tipagem do projeto. O piso de Prisma 7 é 5.4, mas a composição deve satisfazer o maior piso das dependências escolhidas |
| Tailwind CSS | Família 4 | Mobile-first e tokens visuais. Conferir dispositivos, principalmente Safari/iPhone/iPad |
| shadcn/ui | Componentes da revisão compatível com React 19/Tailwind 4 | Código incorporado à aplicação, com responsabilidade de manutenção local e dependências a inventariar |
| PostgreSQL | Família 17 com minor suportado no provedor | Relações, transações e restrições. Validar suporte do Prisma/driver e janela de manutenção |
| Prisma ORM | Família 7 e adaptador PostgreSQL compatível | Modelos e migrações. Documentação v7 exige adaptador para conexão direta. Confirmar ESM, geração do cliente e configuração de conexão |
| React Hook Form | Família 7 | Formulários. Verificar versão do resolver compatível com Zod escolhido |
| Zod | Família 4 | Formatos e validação compartilhada. Autorização e transações continuam no servidor |
| Better Auth | Release estável compatível, a fixar | Candidato à autenticação consolidada com integração Next.js e adaptador Prisma. Testar conta administrativa, revogação e recuperação assistida antes da escolha |
| Vitest | Release estável compatível, a fixar | Regras e testes de integração. Documentação consultada exige Node >=22.12 e Vite >=6.4. Conferir a versão efetivamente selecionada |
| Playwright | Release estável compatível, a fixar | Fluxos ponta a ponta e navegadores. Documentação inclui Node 24 entre requisitos suportados |
| GitHub / Projects | Ferramentas de código e organização | Usar plano/conta aprovados e repositório privado apropriado. O backlog local já permite revisão sem criar projeto externo |
| OpenAI Codex | Apoio de engenharia previsto em F01 | Uso sob revisão de Ismael e regras de confidencialidade. Licença/assinatura pertencem à contratação da ferramenta |

Node 24 atende documentalmente às famílias de requisitos consultadas para Next.js, Prisma 7 e ferramentas de teste. Essa é uma inferência de compatibilidade dos pisos publicados. Build, migração, autenticação e execução em hospedagem precisam de prova integrada. [Node.js](https://nodejs.org/en/about/previous-releases), [Next.js](https://nextjs.org/docs/app/getting-started/installation), [Prisma 7](https://www.prisma.io/docs/orm/v7/reference/system-requirements), [Vitest](https://vitest.dev/guide/), [Playwright](https://playwright.dev/docs/intro)

A documentação de shadcn/ui oferece suporte a React 19/Tailwind 4. Tailwind 4 depende de navegadores modernos, incluindo Safari 16.4 e Chrome 111 como pisos documentados, com recursos adicionais sujeitos a compatibilidade própria. A matriz efetiva será confirmada pelos aparelhos da C3. [shadcn/ui](https://ui.shadcn.com/docs/tailwind-v4), [Tailwind](https://tailwindcss.com/docs/compatibility)

Better Auth documenta integração com Next.js, e Prisma apresenta guia conjunto. Isso fundamenta a candidatura. O fluxo de recuperação assistida precisa ser compatibilizado com a solução e com a gestão exclusiva de contas por Master. [Better Auth](https://better-auth.com/docs/integrations/next), [Guia Prisma](https://docs.prisma.io/docs/guides/authentication/better-auth/nextjs)

As versões de formulários e schema serão congeladas juntas. [React Hook Form](https://react-hook-form.com/get-started), [Zod](https://zod.dev/)

## Licenças e obrigações de inventário

Licenças principais consultadas nos repositórios oficiais. Conferir novamente no tag exato e inventariar componentes transitivos antes da aprovação final. Preservar avisos e textos exigidos pelas licenças no produto entregue. A análise contratual de propriedade intelectual incluirá componentes próprios e de terceiros.

| Componente | Licença principal consultada | Evidência |
|---|---|---|
| Next.js | MIT | [Licença](https://raw.githubusercontent.com/vercel/next.js/canary/license.md) |
| React | MIT | [Licença](https://raw.githubusercontent.com/facebook/react/main/LICENSE) |
| TypeScript | Apache-2.0 | [Licença](https://raw.githubusercontent.com/microsoft/TypeScript/main/LICENSE.txt) |
| Tailwind CSS | MIT | [Licença](https://raw.githubusercontent.com/tailwindlabs/tailwindcss/main/LICENSE) |
| shadcn/ui | MIT | [Licença](https://raw.githubusercontent.com/shadcn-ui/ui/main/LICENSE.md) |
| PostgreSQL | PostgreSQL License | [Licença](https://www.postgresql.org/about/licence/) |
| Prisma ORM | Apache-2.0 no repositório consultado | [Licença](https://github.com/prisma/orm/blob/main/LICENSE) |
| React Hook Form | MIT | [Licença](https://raw.githubusercontent.com/react-hook-form/react-hook-form/master/LICENSE) |
| Zod | MIT | [Licença](https://raw.githubusercontent.com/colinhacks/zod/main/LICENSE) |
| Better Auth | MIT | [Licença](https://raw.githubusercontent.com/better-auth/better-auth/main/LICENSE.md) |
| Vitest | MIT | [Licença](https://raw.githubusercontent.com/vitest-dev/vitest/main/LICENSE) |
| Playwright | Apache-2.0 | [Licença](https://raw.githubusercontent.com/microsoft/playwright/main/LICENSE) |

Node.js e seus componentes incorporados, driver PostgreSQL, adaptador Prisma, bibliotecas de decimal/arquivos, primitivas de interface e ferramentas auxiliares entram no inventário do conjunto fixado. Planos de hospedagem, GitHub e ferramentas de apoio têm termos próprios. O custeio de serviços será formalizado com a C3. O suporte do PostgreSQL varia por versão principal e minor, exigindo manutenção planejada. [Política PostgreSQL](https://www.postgresql.org/support/versioning/)

## Prova técnica para aprovação final

1. Registrar versões exatas e suporte. Conferir advisories e licença no tag de cada dependência.
2. Demonstrar build e teste em Windows de desenvolvimento e Linux de hospedagem escolhida.
3. Demonstrar login, sessão revogada, recuperação assistida e recusa de autorização direta.
4. Demonstrar migração, transação, restrição de visita aberta e vínculo exclusivo sob concorrência.
5. Demonstrar Wega, decimal exato, PDF e XLSX em limites de memória/tempo do serviço.
6. Demonstrar upload privado e restauração coerente da base e arquivos.
7. Registrar resultado, limitações e decisão de aprovação por Ismael antes de consolidar o desenho.

As etapas de execução técnica dependem da autorização de implementação pertinente. Este documento registra a avaliação documental e o roteiro de prova.
