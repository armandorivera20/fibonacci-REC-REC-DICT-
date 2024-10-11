# fibonacci-REC-REC-DICT
Tarea codigo python de fibonacci:

Fibonacci (diccionario)
  def fib_memo(n, memo={}):
    """
    Calcula el n-ésimo número de Fibonacci usando recursión con memoización.
    """
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib_memo(n-1, memo) + fib_memo(n-2, memo)
    return memo[n]

 Ejemplo de uso
 n = 10
print(f"El {n}-ésimo número de Fibonacci (con memoización) es: {fib_memo(n)}")

# Fibonacci Iteracion con arreglos:
def fib_iter(n):
    """
    Calcula el n-ésimo número de Fibonacci usando un enfoque iterativo con arreglos.
    """
    if n <= 1:
        return n
    fib_array = [0, 1]
    for i in range(2, n + 1):
        fib_array.append(fib_array[i-1] + fib_array[i-2])
    return fib_array[n]

#Ejemplo de uso
n = 10
print(f"El {n}-ésimo número de Fibonacci (iterativo) es: {fib_iter(n)}")
