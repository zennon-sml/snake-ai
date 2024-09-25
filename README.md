Guia rapido:

Dependencias:
1. pip
2. pipenv
3. TK


```python
cd snake-ai
pipenv shell
pipenv install
python agent.py
```

# Reinforcement Learning IA presentation

Reinforcement learning (RL) é uma técnica de machine learning (ML) que treina software para tomar decisões para atingir os resultados mais otimizados. Ela imita o processo de aprendizado por tentativa e erro.

RL vai ensinar ao agente de software como se comportar em um ambiente dizendo o quão bem ele está indo se saindo nesse ambiente que no nosso caso é a quantidade de comidas que a nossa snake consegue comer.

Usando Deep Q Learning(DQN), essa maneira extende RL usando uma profunda rede neural  para prever ações.

As três partes necessarias são:

O jogo - Ambiente

O agente - Snake

O model - Pythorch

Recompensa:
1. Come: +10
2. Morre: -10
3. Else: 0

Estados | Inputs:

11 estados:
[PerigoReto, pEsquerda, pDireita, DireçãoAtualEsquerda, dDireita, dCima, dBaixo, ComidaEsquerda, cDireita, cCima, cBaixo]

Acões | Outputs:

[1, 0, 0] = Reto

[0, 1, 0] = Direita

[0, 0, 1] = Esquerda

Model:
![snakeai](https://github.com/user-attachments/assets/b0775332-1e00-43ca-bb15-472c83da6ca2)

Lógica:

Usando o Deep Q Learning

onde ValorQ = Qualidade da ação

0. Inicializa ValorQ (= init model)
1. Escolhe a ação (model.predict(states))
2. Realiza a ação
3. Mede as recompensas
4. Atualiza o ValorQ(& train model)

Fazer um loop dos passos 1 a 4  

E para atualizar o ValorQ é usado a equação de Bellman

Simplificadamente, ela busca encontrar o valor ótimo de uma política, isto é, a sequência de ações que maximiza o retorno esperado a longo prazo.

A equação de Bellman faz isso decompondo o valor de uma ação em dois componentes:
1. **Recompensa imediata** recebida ao realizar a ação naquele estado.
2. **Valor esperado** das recompensas futuras a partir do próximo estado.

### References:
https://www.youtube.com/watch?v=L8ypSXwyBds
