# Regenera 32B

**Autor único e desenvolvedor do modelo e dos pesos · Paulo Ricardo de Leão**  
**Concepção do projeto · Paulo Ricardo de Leão e Raphaela Cerveski**  
**Organização do projeto · Regenera Corporate**

Dossiê público de autoria, integridade e documentação técnica da **Regenera 32B**, um modelo de linguagem de 32 bilhões de parâmetros.

## Autoria do modelo e dos pesos

**Paulo Ricardo de Leão** executou pessoalmente cada etapa do desenvolvimento do modelo e dos pesos. **Paulo Ricardo de Leão e Raphaela Cerveski** conceberam juntos o projeto Regenera 32B.

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

Fontes da ficha técnica · [Configuração do modelo](config.json) e [índice dos pesos](model.safetensors.index.json).

## Evidências e verificação

O dossiê está versionado no Git desde o [commit inicial](https://github.com/regenera-enterprise/MODELO-32B-COPYRIGHT/commit/e5c4245723864acf83726853e726fca5af2ec439). O manifesto e o comprovante abaixo identificam a versão histórica do pacote. A declaração vigente é a versão publicada na branch `main`.

| Documento | Conteúdo |
| --- | --- |
| [Declaração de autoria vigente](evidencias/DECLARACAO-AUTORIA-PAULO-RICARDO-DE-LEAO.md) | Concepção do projeto e autoria técnica do modelo e dos pesos. |
| [Manifesto SHA-256](evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256) | Hashes dos arquivos da versão registrada, incluindo os sete shards. |
| [Comprovante OpenTimestamps](evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256.ots) | Comprovante de carimbo de tempo vinculado ao manifesto. |
| [README da versão registrada](https://github.com/regenera-enterprise/MODELO-32B-COPYRIGHT/blob/e5c4245723864acf83726853e726fca5af2ec439/README.md) | Versão do README cujo SHA-256 está no manifesto. |

Para obter o SHA-256 do manifesto e consultar o estado do comprovante:

```bash
shasum -a 256 'evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256'
ots info 'evidencias/REGISTRO-69a6ff47607fd85c87386509458764c25774618c3351e7ed24169337a6aa7cf1.sha256.ots'
```

O SHA-256 calculado para o manifesto deve coincidir com o valor do campo `File sha256 hash` no comprovante. Para verificar os pesos, compare o SHA-256 de cada um dos sete shards originais com a linha correspondente no manifesto. A confirmação do carimbo vincula a existência do manifesto à data do bloco de ancoragem.

## Licença

© 2026 Regenera Corporate. Todos os direitos reservados quanto ao material de sua titularidade. Os termos aplicáveis estão em [LICENSE](LICENSE) e [NOTICE](NOTICE). Componentes de terceiros seguem seus respectivos termos.

## Como citar

Leão, Paulo Ricardo de. *Regenera 32B. Dossiê de autoria e integridade.* Regenera Corporate, 2026. [Repositório do projeto](https://github.com/regenera-enterprise/MODELO-32B-COPYRIGHT).

## Hashtags

`#Regenera32B` `#RegeneraCorporate` `#PauloRicardoDeLeao` `#InteligenciaArtificial` `#IAProprietaria` `#LLM` `#ModelosDeLinguagem` `#SafeTensors` `#Quantizacao8Bits` `#TokenizerBPE` `#Autoria` `#PropriedadeIntelectual` `#ProvenienciaDigital` `#IntegridadeDigital` `#SHA256` `#OpenTimestamps` `#DocumentacaoTecnica` `#RaphaelaCerveski`
