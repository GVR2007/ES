# STM32 Practice Lab

Interactive bare-metal C code analyzer and hardware simulator for **STM32F401CCU6 (Black Pill)** board.

## Features

- **Code Analysis** — Paste any STM32 bare-metal C code and get instant register-level analysis
- **Register Simulation** — Bit-accurate computation of all peripheral registers (GPIO, RCC, USART, ADC, EXTI, SysTick, I2C, NVIC)
- **Interactive Hardware Dashboard** — Toggle switches, LEDs with glow effects, ADC slider, USART TX output
- **EXTI Interrupt Simulation** — Edge detection with PR flag management and ISR execution
- **Clock Verification** — Checks AHB1ENR, APB1ENR, APB2ENR enable bits
- **Practice Questions** — 17+ exercises from basic GPIO to EXTI+USART combos
- **Dark/Light Mode** — Follows system theme

## How to Get Access

1. **Star** this repository
2. **Fork** it
3. Open `index.html` and enter your GitHub username to verify
4. You'll receive a unique access code

## Quick Start

```bash
git clone https://github.com/GVR2007/ES.git
cd ES
# Open index.html in any browser
```

Or use a local server:
```bash
python -m http.server 8080
# Visit http://localhost:8080
```

## Setup for Repository Owner

After cloning, update the config variables at the top of the `<script>` section in `index.html`:

```javascript
var REPO_OWNER = 'GVR2007';   // Your GitHub username
var REPO_NAME = 'ES';          // This repo name
```

## Supported Peripherals

| Peripheral | Registers |
|-----------|-----------|
| RCC | AHB1ENR, APB1ENR, APB2ENR |
| GPIO A/B/C | MODER, PUPDR, ODR, IDR, BSRR, OTYPER, OSPEEDR, AFR[0/1] |
| USART2 | BRR, CR1, CR2, CR3, SR, DR |
| ADC1 | CR1, CR2, SR, DR, SQR1, SQR3, SMPR2 |
| EXTI | IMR, EMR, FTSR, RTSR, PR |
| SYSCFG | EXTICR[0-3] |
| SysTick | LOAD, VAL, CTRL |
| I2C1 | CR1, CR2, CCR, TRISE, OAR1, SR1, SR2 |
| NVIC | ISER[0-2] |

## Board Pin Map

| Pin | Function |
|-----|----------|
| PA0 | User KEY / ADC_IN0 |
| PA2 | USART2_TX (AF7) |
| PA3 | USART2_RX (AF7) |
| PA6 | Switch S2 / EXTI6 |
| PB6 | I2C1_SCL (AF4) |
| PB7 | I2C1_SDA (AF4) |
| PB9 | LED 2 |
| PB10 | Switch S1 / EXTI10 |
| PC13 | User LED (on-board, active-low) |
| PC14 | LED 1 |

## License

MIT License - Feel free to use and modify.
