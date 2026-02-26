# ![bash+terminal](https://i.imgur.com/jVg5NA7.jpeg)

## Config-Project-Node-Typescript

Automatically configure a Node + TypeScript + MongoDB API.

## O que é necessário

1. Terminal Bash
2. curl
3. node >= 20

## Como funciona

Crie uma pasta com o nome do seu projeto e basta colocar o comando abaixo do curl dentro do diretória da basta que foi criada com o nome do seu projeto

> Ex: project/server/`curl -fsSL https://tinyurl.com/node22ts | bash`

## Install Script

```bash
curl -fsSL https://tinyurl.com/node22ts | bash
```

## Detalhes da config

- Node.js (version 24)
- Arquitetura das pastas (Monolítica)
- Tsconfig.json com configuração própria
- Gerenciador de Pacotes (npm)
- README.MD
- .env
- LICENSE (MIT)
- .gitignore [`node_modules`, `.env`]
- .prettierrc
- .npmrc

## Tsconfig

| Nome                             | Descrição                                                                                      |
| -------------------------------- | ---------------------------------------------------------------------------------------------- |
| rootDir                          | Define a pasta raiz onde estão os arquivos TypeScript de entrada.                              |
| outDir                           | Define a pasta onde os arquivos compilados (JavaScript) serão gerados.                         |
| baseUrl                          | Diretório base para resolver imports não relativos.                                            |
| paths                            | Permite criar aliases de importação (ex: @/ para src).                                         |
| ignoreDeprecations               | Suprime avisos de APIs depreciadas até a versão informada.                                     |
| strict                           | Ativa todos os checks de tipagem estrita do TypeScript.                                        |
| allowJs                          | Permite incluir arquivos .js no projeto.                                                       |
| pretty                           | Exibe erros formatados de maneira mais legível no terminal.                                    |
| skipDefaultLibCheck              | Pula verificação de tipos das bibliotecas padrão do TypeScript.                                |
| strictFunctionTypes              | Garante verificação rigorosa de compatibilidade entre funções.                                 |
| strictNullChecks                 | Obriga tratamento explícito de null e undefined.                                               |
| skipLibCheck                     | Ignora verificação de tipos dentro de node_modules.                                            |
| moduleDetection                  | Define como o TS detecta se um arquivo é módulo (ex: force obriga considerar como módulo).     |
| noUncheckedSideEffectImports     | Impede imports que só executam efeitos colaterais sem verificação.                             |
| resolveJsonModule                | Permite importar arquivos .json como módulos.                                                  |
| removeComments                   | Remove comentários do código compilado.                                                        |
| noUnusedParameters               | Gera erro se parâmetros de função não forem usados.                                            |
| noUnusedLocals                   | Gera erro se variáveis locais não forem usadas.                                                |
| noStrictGenericChecks            | Desativa verificações estritas em generics (false mantém verificação ativa).                   |
| noImplicitThis                   | Impede uso de this com tipo implícito any.                                                     |
| noImplicitReturns                | Gera erro se alguma execução de função não retornar valor quando esperado.                     |
| noImplicitAny                    | Impede variáveis com tipo implícito any.                                                       |
| forceConsistentCasingInFileNames | Garante consistência de maiúsculas/minúsculas nos imports.                                     |
| esModuleInterop                  | Facilita interoperabilidade entre CommonJS e ESModules.                                        |
| allowSyntheticDefaultImports     | Permite usar import default mesmo se o módulo não exportar default oficialmente.               |
| noFallthroughCasesInSwitch       | Impede que um case em switch continue para o próximo sem break.                                |
| noErrorTruncation                | Mostra mensagens de erro completas sem truncar.                                                |
| noEmitOnError                    | Impede geração de arquivos JS se houver erro de tipagem.                                       |
| noEmitHelpers                    | Evita gerar funções helper duplicadas no código compilado.                                     |
| noEmit                           | Impede a geração de arquivos JS (apenas checagem de tipos).                                    |
| declaration                      | Gera arquivos .d.ts junto com o JS compilado.                                                  |
| exactOptionalPropertyTypes       | Trata propriedades opcionais exatamente como definidas (não assume undefined automaticamente). |
| maxNodeModuleJsDepth             | Define profundidade máxima de verificação de arquivos JS dentro do node_modules.               |
| moduleResolution                 | Define estratégia de resolução de módulos (node segue padrão do Node.js).                      |
| lib                              | Define bibliotecas JS incluídas (ex: ES2023).                                                  |
| module                           | Define o sistema de módulos gerado no JS final (commonjs neste caso).                          |
| target                           | Define versão do JavaScript gerado na compilação.                                              |
| types                            | Lista pacotes de tipos incluídos automaticamente.                                              |
| typeRoots                        | Diretórios onde o TS deve procurar definições de tipos.                                        |
| exclude                          | Pastas/arquivos ignorados na compilação.                                                       |
| include                          | Arquivos/pastas incluídos na compilação.                                                       |

## Autor

[Vittor F. Serra](https://github.com/DevVittor)
