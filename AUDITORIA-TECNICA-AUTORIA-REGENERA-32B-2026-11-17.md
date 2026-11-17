# Auditoria técnica de autoria

Relatório de exame local. Não é laudo judicial, registro de direito autoral nem certidão de titularidade.

## Identificação

- Objeto: pacote de modelo `regenera-32b-copyright`
- Caminho examinado: `/Users/enterprise/Desktop/MODELO-BY-REGENERA-OK/regenera-32b-copyright`
- Data do exame: 2026-11-17
- Escopo: somente os arquivos desse diretório. Histórico git, metadados de arquivo, documentos de atribuição, cabeçalhos dos pesos e tokenizer.
- Fora do exame: pastas vizinhas, rede, treinamento, bases de dados e comparação byte a byte com modelos de terceiros.

## 1. Autoria declarada no próprio pacote

Os documentos de atribuição existentes neste diretório nomeiam a Regenera Corporate e Paulo Ricardo de Leão.

README.md, texto integral:

```
# regenera-32b-copyright
Regenera Corporate.
Desenvolvido por Paulo Ricardo de Leao.
```

Campos de `config.json`:

- `model_type`: regenera
- `architectures`: RegeneraForCausalLM
- `_name_or_path`: regenera-32b-copyright
- `regenera_org`: Regenera Corporate
- `regenera_author`: Paulo Ricardo de Leao

`chat_template.jinja` e o campo `chat_template` de `tokenizer_config.json` repetem a mesma identificação de sistema: inteligência artificial criada pela Regenera Corporate, desenvolvida por Paulo Ricardo de Leão, co-fundada e liderada por Raphaela Cerveski, CEO.

Grafia: README e `config.json` escrevem "Leao". O template escreve "Leão". Raphaela Cerveski aparece no template de conversa. Não aparece no README nem em `regenera_author`.

## 2. Leitura técnica dessa declaração

A autoria Regenera que este diretório contém é a declaração escrita nos próprios arquivos do pacote. README, config e template concordam no núcleo: organização Regenera Corporate, desenvolvedor Paulo Ricardo de Leão.

Esse registro é atribuição inserida no pacote. O exame não encontrou evidência independente de que todo o desenvolvimento dos pesos tenha sido autoral da Regenera Corporate. Por isso este relatório não declara essa conclusão.

No cabeçalho dos sete shards `.safetensors` consta `__metadata__` com autor Paulo Ricardo de Leao, organização Regenera Corporate e modelo regenera-32b-copyright.

Ausências registradas no diretório:

- Não há repositório git, commits, autores de commit nem remoto.
- Não há `LICENSE`, `NOTICE` nem arquivo de assinatura.
- Não há atributos estendidos, URL de origem, autor, copyright ou criador no metadado do sistema de arquivos.
- Não há código-fonte de arquitetura (`modeling`) neste diretório. O nome `RegeneraForCausalLM` está no `config.json`.

## 3. Metadados de arquivo

Gravação local em 17 de novembro de 2026, usuário do diretório `enterprise`. Os shards foram escritos em sequência. `config.json` é o único arquivo cujo horário de modificação é posterior ao de criação.

| Arquivo | Bytes | Modo | Criação | Modificação |
|---|---:|---|---|---|
| `README.md` | 85 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:31:23 |
| `chat_template.jinja` | 2751 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:31:23 |
| `config.json` | 773 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:32:49 |
| `generation_config.json` | 88 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:31:23 |
| `model-00001-of-00007.safetensors` | 5585848600 | `-rw-------` | 2026-11-17 15:30:47 | 2026-11-17 15:30:51 |
| `model-00002-of-00007.safetensors` | 5645299656 | `-rw-------` | 2026-11-17 15:30:51 | 2026-11-17 15:30:57 |
| `model-00003-of-00007.safetensors` | 5645299664 | `-rw-------` | 2026-11-17 15:30:57 | 2026-11-17 15:31:03 |
| `model-00004-of-00007.safetensors` | 5680730984 | `-rw-------` | 2026-11-17 15:31:03 | 2026-11-17 15:31:09 |
| `model-00005-of-00007.safetensors` | 5680714600 | `-rw-------` | 2026-11-17 15:31:09 | 2026-11-17 15:31:15 |
| `model-00006-of-00007.safetensors` | 5645299664 | `-rw-------` | 2026-11-17 15:31:15 | 2026-11-17 15:31:21 |
| `model-00007-of-00007.safetensors` | 2382730184 | `-rw-------` | 2026-11-17 15:31:21 | 2026-11-17 15:31:23 |
| `model.safetensors.index.json` | 138588 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:31:23 |
| `tokenizer.json` | 7137190 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:31:23 |
| `tokenizer_config.json` | 3082 | `-rw-r--r--` | 2026-11-17 15:31:23 | 2026-11-17 15:31:23 |

## 4. Consistência interna do pacote

Os pesos conferem com a ficha numérica do `config.json`.

- 7 shards, 1.607 tensores, camadas 0 a 63, sem lacuna.
- Cada shard preenche o arquivo até o último offset do cabeçalho, sem sobra.
- Hidden 5120, intermediário 27648, 40 cabeças de atenção, 8 cabeças de chave/valor, vocabulário 100278.
- O tokenizer tem 100278 peças, ids 0 a 100277 contínuos, e esse tamanho coincide com `embed_tokens` e `lm_head`.
- Quantização do config: 8 bits, grupo 64, modo afim. Os 450 pesos estão em `U32` empacotado. Escalas e vieses em `F32`. Normas em `F32`.
- Há `q_norm`, `k_norm`, `post_attention_layernorm` e `post_feedforward_layernorm`.
- Parâmetros lógicos dos pesos mais as normas: 32.233.522.176. Esse valor é igual a `total_parameters` do índice.
- `total_size` do índice: 34249105152. A soma dos bytes dos tensores gravados é 36265741824. O campo `total_size` do índice diverge dos shards. Os shards, entre si, fecham.

O tokenizer é BPE byte-level, versão 1.0, 100.000 merges, sem campo de autor ou licença. Tokens especiais finais incluem marcadores de ChatML (`<|im_start|>`, `<|im_end|>`), FIM, `<|endoftext|>`, `<|endofprompt|>` e `<|pad|>`.

## 5. Conclusão

No diretório examinado, a autoria registrada pelos documentos de atribuição é da Regenera Corporate, com desenvolvimento atribuído a Paulo Ricardo de Leão. O template de conversa acrescenta Raphaela Cerveski como co-fundadora e CEO.

A ficha técnica do pacote está coerente com os tensores e com o tokenizer. O histórico de desenvolvimento autoral dos pesos não está neste diretório. Este relatório registra a declaração de autoria encontrada. Não a converte em prova de que todo o desenvolvimento foi autoral.

## 6. Chaves SHA-256 dos arquivos de texto, índice e tokenizer

Hashes calculados na emissão deste relatório. Os shards de peso, acima de 2 GB cada, não entram nesta chave.

| Arquivo | SHA-256 |
|---|---|
| `README.md` | `2056abe64e8ab871e2083d19c8b30d19f55b8a0c7518ec68b51b3723dc832aa7` |
| `chat_template.jinja` | `412a275ed6bac2274dee6d205bd5120152e7cea9acd0fec02f178caf7f13ad9f` |
| `config.json` | `14f8be466993664b9dc4c44ab462e7b0bec9285cb7413ebc3c0be320485304eb` |
| `generation_config.json` | `ad639452275692b59256f87dab93e395506b4dfe7efcd753b6b13ee3e3724e47` |
| `model.safetensors.index.json` | `84f9f7573d4afe2cfa7c4f0468d8f52bd043a03e5b4ba30fb325b5b90f6b9753` |
| `tokenizer.json` | `6a6b266d2726d8b67d9ababa39be46cc5617a240d15c83c30255abdbbece5d8a` |
| `tokenizer_config.json` | `339b1a7b7d5c6b8688aa9c43a0b07af8240a32b67e328922105167268d85d61f` |

## 7. Chave deste relatório

A chave SHA-256 do arquivo deste relatório está no arquivo ao lado, de mesmo nome e extensão `.sha256`. Ela foi calculada depois do fechamento deste texto e não faz parte do conteúdo hasheado.
