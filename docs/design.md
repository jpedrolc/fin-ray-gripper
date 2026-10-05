# Garra Fin Ray — Escopo técnico

Projeto pausado desde abril de 2026. A arquitetura está documentada; hardware, firmware, CAD final e ensaios permanecem pendentes.

## Primeiro experimento

O kit mínimo previsto reúne ESP32 DevKit V1, servo MG90S e fonte externa de 5 V com capacidade inicialmente proposta de pelo menos 2 A. Servo e controlador precisam compartilhar a referência de GND; a alimentação final depende da placa escolhida e da corrente medida.

O primeiro ensaio deve comprovar comando PWM e abertura/fechamento em bancada, sem presumir a integração com câmera ou movimento de objetos.

## Mecânica

A proposta usa dedos em TPU 95A e estrutura rígida em PETG/PLA. O CAD final ainda precisa ser desenvolvido.

A geometria, transmissão do servo, força de apreensão, desgaste e tolerância ao erro precisam ser avaliados experimentalmente. O valor de ±30 mm do planejamento não é uma tolerância medida.

## Percepção e controle

A proposta futura usa câmera USB conectada ao PC, OpenCV para segmentação por cor e contornos, e calibração para relacionar imagem e espaço de trabalho. O PC enviaria comandos ao ESP32 por serial.

Uma máquina de estados organizaria percepção e apreensão. A movimentação até uma área de destino exige uma mecânica de posicionamento ainda não especificada. Um único servo de fechamento não comprova um sistema completo de pick-and-place.

O primeiro kit não inclui sensor de força definido; controle fechado de força fica fora do escopo inicial.

## Validação pendente

- Registrar objetos, geometria, material e condições de cada ensaio.
- Medir sucesso/falha da apreensão e observar escorregamento ou deformação excessiva.
- Verificar estabilidade elétrica durante acionamento do servo.
- Avaliar visão e comunicação separadamente antes da integração.

Sucesso acima de 90%, ciclo abaixo de 30 s e latência abaixo de 500 ms são metas propostas, ainda sem medições. O escopo e as condições de cada métrica precisam ser definidos antes dos ensaios.
