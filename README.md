As integrantes da dupla são: Vívian e Lívia.

DIAGRAMA DE CLASSE (UML)
```
+------------------+
|      Sala        |
+------------------+
| - id: int        |
| - nome: string   |
| - capacidade: int|
+------------------+
| + reservar(): void|
| + cancelar(): void|
+------------------+
        |
        | (associado a)
        v
+-----------------+
|     Usuário     |
+-----------------+
| - id: int       |
| - nome: string  |
| - email: string |
+-----------------+
| + criarReserva(): void |
| + cancelarReserva(): void|
+-----------------+
        |
        | (associado a)
        v
+------------------+
|      Reserva     |
+------------------+
| - id: int        |
| - data: datetime |
| - status: string |
+------------------+
| + confirmar(): void|
| + cancelar(): void |
+------------------+
```

**EXPLICAÇÃO**
                     
1. **Início**: Usuário decide fazer a reserva.
2. **Escolher Sala**: Usuário escolhe a sala.
3. **Inserir Dados**: Usuário informa a data.
4. **Verificar Disponibilidade**: Sistema checa se está disponível.
6. **Confirmar ou Escolher Outra**: Se disponível, reserva é confirmada. Se não, escolhe outra sala.
7. **Fim**: Processo finaliza.

**Explicação para que serve os nomes que não são tão conhecidos.**

**void**: Indica que o método não retorna nada.

**int**: Tipo para números inteiros (sem decimais).

**string**: Tipo para texto (como palavras ou frases).

**id**: Um identificador único para diferenciar objetos (como uma sala ou usuário).

**datetime**: Tipo para data e hora.

-------------------------------------------------------------------------------------------------

DIAGRAMA DE CLASSE (BPMN)
```
+-------------------+
| Início do Processo|
+-------------------+
        |
        v
+---------------------+
| Escolher a Sala     |
+---------------------+
        |
        v
+------------------+
| Inserir Dados    |
+------------------+
        |
        v
+-------------------+
| Verificar        |
| Disponibilidade  |
+-------------------+
        |
        v
+------------------+       +-------------------+
| Sala Disponível  | ----> | Confirmar Reserva |
+------------------+       +-------------------+
        |                           |
        v                           v
+------------------+       +-------------------+
| Sala Indisponível|       | Fim do Processo   |
+------------------+       +-------------------+
```


explicação do Diagrama BPMN:

1. **Início**: O usuário decide fazer a reserva.

2. **Escolher Sala**: O usuário seleciona a sala.

3. **Inserir Dados**: O usuário informa a data da reserva.

3. **Verificar Disponibilidade**: O sistema checa se a sala está disponível.

4. **Sala Disponível**: Se a sala estiver disponível, o usuário confirma a reserva.

5. **Confirmar Reserva**: A reserva é finalizada.

6. **Sala Indisponível**: Se a sala não estiver disponível, o usuário escolhe outra sala.

7. **Fim**: O processo termina.

