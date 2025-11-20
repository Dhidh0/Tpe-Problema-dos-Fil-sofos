# Tpe-Problema-dos-Filosofos
TPE Problema dos Filósofos 2025/02, Unochapecó

Explicação rápida do código

forks: lista de threading.Lock() representando os hashis entre pratos.

Philosopher é uma thread. Cada filósofo pensa, pede permissão ao garçom (waiter), então tenta pegar os dois hashis e comer.

waiter = Semaphore(N-1): técnica clássica para evitar deadlock — impede que todos os N filósofos tentem pegar um hashi ao mesmo tempo. Com no máximo N-1 tentando, pelo menos um pode comer e liberar recursos.

print_lock evita que prints de várias threads se misturem.

ITERATIONS controla quantas vezes cada filósofo tenta comer; ajuste para testes.
