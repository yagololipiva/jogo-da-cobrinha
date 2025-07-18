# Snake Game em Python 🐍

## 🎮 Código principal:
---

```python
import pygame
import random

from pygame.gfxdraw import pixel
pygame.init()
pygame.display.set_caption("jogo snake em python")
largura, altura = 1200, 700
tela = pygame.display.set_mode((largura, altura))
relogio = pygame.time.Clock()

# cores RGB
preta = (0, 0 ,0)
branca = (255, 255, 255)
vermelho = (255, 0 ,0)
verde = (0, 255, 0)
azul = (0, 0, 255)

# parametros da cobrinha
tamanho_quadrado = 10
velocidade_jogo = 15

def gerar_comida():
    comida_x = round(random.randrange(0, largura - tamanho_quadrado) / float(tamanho_quadrado)) * float(tamanho_quadrado)
    comida_y = round(random.randrange(0, altura - tamanho_quadrado) / float(tamanho_quadrado)) * float(tamanho_quadrado)
    return comida_x, comida_y

def desenhar_comida(tamanho, comida_x, comida_y):
    pygame.draw.rect(tela, verde, [comida_x, comida_y, tamanho, tamanho])
---
