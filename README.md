# 🚗😻 Pussycat – O Carro da Penelope Charmosa

Projeto de robô seguidor de linha baseado em Arduino, batizado de **Pussycat** em homenagem ao icônico carro da Penelope Charmosa. Este carrinho é capaz de detectar e seguir linhas pretas no chão usando sensores infravermelhos, e pode corrigir sua trajetória automaticamente com curvas suaves.

---

## 🧠 Funcionalidades

- Leitura analógica de 3 sensores IR (esquerda, centro e direita)
- Decisão de movimento baseada em leitura de intensidade da linha
- Curvas automáticas para direita e esquerda com controle individual de motores
- Controle de velocidade por PWM
- Comandos simples: frente, virar direita, virar esquerda e parar

---

## ⚙️ Componentes Utilizados

- Arduino Uno (ou similar)
- Ponte H L298N
- 2 Motores DC com rodas
- 3 Sensores Infravermelhos reflexivos
- Protoboard e jumpers
- Fonte de alimentação (ex: Li-Ion 2S ou pack de pilhas)

---

## 🔌 Esquema de Ligação

| Pino Arduino | Componente            |
|--------------|------------------------|
| A0           | Sensor direito         |
| A1           | Sensor central         |
| A2           | Sensor esquerdo        |
| 6            | IN1 (motor A)          |
| 3            | IN2 (motor A)          |
| 5            | IN3 (motor B)          |
| 9            | IN4 (motor B)          |

> O controle de velocidade é feito diretamente via `analogWrite()` nos pinos dos motores.

---

## 🛠️ Instalação e Uso

1. Monte os componentes conforme o esquema acima.
2. Abra o código `.ino` no Arduino IDE.
3. Selecione a placa correta (ex: **Arduino Uno**) e a porta COM.
4. Carregue o código na placa.
5. Posicione o carrinho sobre uma linha preta com fundo branco.
6. Ligue a fonte e **divirta-se observando o carrinho seguir a linha!**

---

## 💡 Lógica de Decisão

```cpp
Se centro detectar a linha e laterais não → andar pra frente
Se direita detectar linha → virar à direita
Se esquerda detectar linha → virar à esquerda
```

---

## 🐾 Inspiração

Este projeto é uma homenagem ao icônico carro **Pussycat** da personagem **Penelope Charmosa**, da série "Corrida Maluca". Assim como ela, o carrinho busca ser elegante, inteligente e... sempre na frente! 💅

---


## 📄 Licença

Este projeto é open-source e pode ser utilizado livremente para fins educacionais e pessoais. Sugestões, melhorias e forks são super bem-vindos!

---
