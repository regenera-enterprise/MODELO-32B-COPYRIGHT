# Regenera 32B

**Autor único do modelo e desenvolvedor dos pesos · Paulo Ricardo de Leão**  
**Organização do projeto · Regenera Corporate**

Dossiê público de autoria, integridade e documentação técnica da **Regenera 32B**, um modelo de linguagem de 32 bilhões de parâmetros.

## Autoria do modelo e dos pesos

**Paulo Ricardo de Leão** é o autor da Regenera 32B. Desenvolveu pessoalmente o modelo e conduziu, etapa por etapa, o desenvolvimento dos seus pesos. A Regenera Corporate é a organização do projeto. O manifesto vincula a declaração de autoria aos sete arquivos de pesos por SHA-256.

[Declaração de autoria de Paulo Ricardo de Leão](evidencias/DECLARACAO-AUTORIA-PAULO-RICARDO-DE-LEAO.md) · [Campo de autoria em `config.json`](config.json)

## Ficha técnica

| Campo | Valor documentado |
| --- | --- |
| Identificador da arquitetura | `RegeneraForCausalLM` |
| Parâmetros lógicos reportados | 32.233.522.176 |
| Camadas | 64 |
| Dimensão oculta e intermediária | 5.120 e 27.648 |
| Cabeças de atenção e de chave/valor | 40 e 8 |
| Tokenizer | BPE no nível de bytes, com vocabulário de 100.278 tokens |
| Posições máximas declaradas na configuração | 65.536 |
| Formato dos pesos | 7 shards SafeTensors |
| Quantização | Afim de 8 bits, com grupos de 64 |

A [auditoria técnica de 17 de novembro de 2026](AUDITORIA-TECNICA-AUTORIA-REGENERA-32B-2026-11-17.md) documenta os metadados, os cabeçalhos dos shards e a consistência do tokenizer. Também registra uma divergência entre o campo `total_size` do índice e a soma dos bytes dos tensores.

A observação sobre a ausência de Git descreve o diretório no momento da auditoria. Depois daquele exame, o dossiê foi versionado e publicado. O [primeiro commit do dossiê](https://github.com/regenera-enterprise/MODELO-32B-COPYRIGHT/commit/e5c4245723864acf83726853e726fca5af2ec439) registra a declaração de autoria, a licença, o aviso legal e o manifesto.

## Evidências e verificação

| Documento | O que registra |
| --- | --- |
| [Auditoria técnica](AUDITORIA-TECNICA-AUTORIA-REGENERA-32B-2026-11-17.md) e [SHA-256 da auditoria](AUDITORIA-TECNICA-AUTORIA-REGENERA-32B-2026-11-17.sha256) | Escopo do exame e impressão digital do relatório. |
| [Manifesto SHA-256](evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256) | Impressões digitais de 19 arquivos, incluindo os sete shards, a documentação e os metadados. |
| [Comprovante OpenTimestamps](evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256.ots) | Carimbo externo associado ao hash do manifesto. O estado do comprovante pode ser consultado com `ots info`. |
| [Versão inicial do dossiê](https://github.com/regenera-enterprise/MODELO-32B-COPYRIGHT/commit/e5c4245723864acf83726853e726fca5af2ec439) | Snapshot Git que preserva o README original referenciado no manifesto. |

Para verificar a integridade da auditoria na raiz do repositório:

```bash
shasum -a 256 -c AUDITORIA-TECNICA-AUTORIA-REGENERA-32B-2026-11-17.sha256
```

Para consultar o comprovante com o cliente OpenTimestamps:

```bash
ots info 'evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256.ots'
```

A confirmação do carimbo vincula a existência do manifesto à data do bloco de ancoragem. A declaração de autoria documenta a atribuição feita pelo desenvolvedor. A verificação dos hashes dos pesos exige os sete shards originais. O hash do README no manifesto se refere à versão registrada no snapshot acima.

## Licença

© 2026 Regenera Corporate. Todos os direitos reservados quanto ao material de sua titularidade. Os termos aplicáveis estão em [LICENSE](LICENSE) e [NOTICE](NOTICE). Componentes de terceiros seguem seus respectivos termos.

## Como citar

Leão, Paulo Ricardo de. *Regenera 32B. Dossiê de autoria e integridade.* Regenera Corporate, 2026. [Repositório do projeto](https://github.com/regenera-enterprise/MODELO-32B-COPYRIGHT).

## Hashtags

`#Regenera32B` `#RegeneraCorporate` `#PauloRicardoDeLeao` `#InteligenciaArtificial` `#IAProprietaria` `#LLM` `#ModelosDeLinguagem` `#SafeTensors` `#Quantizacao8Bits` `#TokenizerBPE` `#Autoria` `#PropriedadeIntelectual` `#ProvenienciaDigital` `#IntegridadeDigital` `#SHA256` `#OpenTimestamps` `#AuditoriaTecnica`
