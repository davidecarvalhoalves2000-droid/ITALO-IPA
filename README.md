# TIM — downloads

Repositório **apenas de download** do TIM. O código-fonte fica no repositório privado.

## Instalar

1. Abra a aba [Releases](../../releases/latest) e baixe o `.ipa` mais recente.
2. Instale com sua assinatura (certificado de empresa, AltStore, ESign ou similar).
3. Abra o TIM, entre com a sua key e escolha o jogo.

## Atualizações

O TIM lê o `update.json` deste repositório em toda abertura, a cada 5 minutos
enquanto está aberto e sempre que volta para a frente. Quando a versão publicada
ali for maior que a instalada, o app mostra a tela de atualização obrigatória e
**bloqueia tudo** — não existe opção de adiar: ou atualiza, ou o app não ativa
nada.

## Publicar uma atualização (dono)

1. Gere a build nova no repositório de código.
2. Publique o `.ipa` em Releases com a tag da versão (ex.: `2.6`).
3. Edite o `version` no `update.json` deste repositório para a mesma versão.

Pronto: em minutos todo mundo começa a receber a tela de atualização, sem precisar
de uma build nova. Tire a chave `message` se preferir que o app mostre o texto
traduzido padrão.

> Toda build do app carrega o carimbo SHA-256 do próprio código compilado e recusa
> ativar patches se o binário for alterado depois. Reassinar o IPA não afeta o
> carimbo.
