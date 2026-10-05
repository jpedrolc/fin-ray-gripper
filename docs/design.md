# Garra Fin Ray — Escopo técnico

Síntese do documento de projeto de 12/04/2026 e da atualização de status de 29/08/2026 no Notion. O projeto está pausado; as partes descritas abaixo ainda precisam ser construídas e testadas.

## Primeiro experimento

O kit mínimo previsto reúne ESP32 DevKit V1, servo MG90S e fonte externa de 5 V com capacidade inicialmente proposta de pelo menos 2 A. Servo e controlador precisam compartilhar a referência de GND; a alimentação final depende da placa escolhida e da corrente medida.

O primeiro ensaio deve comprovar comando PWM e abertura/fechamento em bancada, sem presumir a integração com câmera ou movimento de objetos.

## Mecânica

O planejamento propõe dedos em TPU 95A e estrutura rígida em PETG/PLA. Os nomes de arquivos STL no documento original são entregáveis previstos; não há CAD anexado a este repositório.

A geometria, transmissão do servo, força de apreensão, desgaste e tolerância ao erro precisam ser avaliados experimentalmente. O valor de ±30 mm do planejamento não é uma tolerância medida.

## Percepção e controle

A proposta futura usa câmera USB conectada ao PC, OpenCV para segmentação por cor e contornos, e calibração para relacionar imagem e espaço de trabalho. O PC enviaria comandos ao ESP32 por serial.

Uma máquina de estados organizaria percepção e apreensão. A movimentação até uma área de destino exige uma mecânica de posicionamento ainda não especificada. Um único servo de fechamento não comprova um sistema completo de pick-and-place.

Não há sensor de força definido para o primeiro kit. Portanto, feedback de força e controle fechado de apreensão não devem ser tratados como implementados.

## Validação pendente

- Registrar objetos, geometria, material e condições de cada ensaio.
- Medir sucesso/falha da apreensão e observar escorregamento ou deformação excessiva.
- Verificar estabilidade elétrica durante acionamento do servo.
- Avaliar visão e comunicação separadamente antes da integração.

As metas do documento original — sucesso acima de 90%, ciclo abaixo de 30 s e latência abaixo de 500 ms — continuam sem medições publicadas.

## Limite da apresentação

O projeto aparece no acervo de robótica do autor. Não há confirmação de vínculo institucional específico desta garra com o FATA; por isso o nome do repositório não usa esse vínculo como atributo do projeto.
