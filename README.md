# Projeto Final de Microcontroladores

Este projeto tem como objetivo automatizar o controle de ventilação e iluminação em uma sala de aula utilizando a plataforma STM32 e sensores ambientais. O sistema monitora temperatura, umidade e luminosidade, e toma decisões para ligar/desligar luzes ou ventiladores automaticamente.

## Tecnologias e Componentes Utilizados

- Microcontrolador: STM32 (modelo utilizado: STM32F103C8T6)
- Sensor de temperatura e umidade: AHT10 (via I2C)
- Sensor de luminosidade: LDR (via ADC)
- Ventoinha representada por LED (GPIO)
- STM32CubeMX + STM32CubeIDE
- Protoboard, resistores, jumpers

## Funcionalidades

- Leitura de temperatura e umidade com o sensor AHT10
- Leitura da luminosidade ambiente com LDR
- Controle automático da iluminação da sala (liga se ambiente estiver escuro)
- Acionamento da ventilação quando a temperatura ultrapassa um valor limite (ex: 28 °C)
- Modularização do código e escrita em C usando HAL Drivers

## Estrutura do Projeto

```
📁 Projeto_Automatizacao_Sala
├── Core/
│   ├── Inc/                # Arquivos de cabeçalho (headers)
│   └── Src/                # Código-fonte principal (main.c, sensores, controle)
├── Drivers/                # Drivers HAL
├── README.md               # Este arquivo
├── Projeto.ioc             # Arquivo de configuração STM32CubeMX
└── Apresentacao_Slides/    # Slides da apresentação
```

## Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/nathalia0902/Projeto-Final-de-Microcontroladores
```

2. Abra o projeto no STM32CubeIDE

3. Compile e faça upload para sua placa STM32 (via ST-Link)

4. Conecte os sensores conforme o esquemático incluído

## Equipe e Contribuições

- Maria Eduarda – Modularização do código
- Nathalia – Documentação, slides, datasheets, organização do GitHub
- Vitória – Montagem e testes de hardware
- Todas as integrantes participaram juntas do desenvolvimento do código principal e elaboração do esquemático

## Links Úteis

- [Datasheet AHT10 (PDF)](https://server4.eca.ir/eshop/AHT10/Aosong_AHT10_en_draft_0c.pdf)
- [Documentação STM32 HAL](https://www.st.com/en/embedded-software/stm32cube-mcu-packages.html)
- [STM32CubeIDE Download](https://www.st.com/en/development-tools/stm32cubeide.html)
