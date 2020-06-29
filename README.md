# Introdução a Programação Funcional em Haskell
## Características
 * `Código Declarativo`
   * Leitura de forma natural
   * entendo oq ta fazendo e nn como
   * Programas em haskell chegam a ser dezenas de vezes menores
 * Imutabilidade (nn existe conceito de variável)
   * Apenas nome e declarações
 * Tipos Polimórficos
   * Permite definir funções genéricas que funcionam para diferentes classes de tipos(string, number)
 * Avaliações Preguiçosas
   * ao aplicar uma função, o resultado será computado apenas qnd requisitado, Isso Permite evitar computações desnecessárias, estimula uma programaçãp modular e permite estruturas de dados infinitos.
> Toda a declaração de função é o `nome = oq q ela faz`.

## Hello World
```haskell
module Main Where  -- indica que é o módulo principal

main :: IO ()
main = do          -- início da função principal
    putStrLn "hello world"
```

 
 * A aplicação de função é definida como:
   * o nome da função
   * seguido dos parâmetros separados por espaço
   * A aplicação de funções tem maior precedência

```haskell
f a b     -- f(a,b)
f a b + c d  -- f(a,b) + (c,d)
```

## Convenções
  * Os nomes das funções e seus argumentos devem começar com uma letra minúscula e seguida por 0 ou mais letras, maiúsculas ou minúsculas, dígitos, underscore, e aspas simple
  * Ex:
    * `funcao, ordenaLista, soma1, x'`

## Tipos de Dados
  * um *tipo* é uma coleção de valores relacionados entre si.
  * Todo tipo começa com a letra maiúscula no Haskell
  * Em Haskell os tipos são definidos por:
    * `v::T`
    * v define um valor tipo T.
  * Os tipos são:
    * Bool
    * Char
    * String(aspas duplas)
    * Int(limite até 64bits)
    * Integer
    * Float(Precisão simples)
    * Double(Precisão Dupla)

## Listas
 * Listas são sequências de **elementos dos mesmos tipos**
```haskell
[1, 2, 3, 4] :: [Int]
[False, True, True] :: [Boll]

-- Listas de listas

[[1, 2, 3], [3, 4]] :: [[Int]]
[["o", "l", "a"], ["mundo"]] :: [[Char]]
```
## Tuplas
 * São sequências finitas de componentes, contendo zero ou mais tipos diferentes
```Haskell
(True, False) :: (Boll, Boll)
(1, "G") :: (Int, Char)
```

## Funções
 * São mapas de argumentos de um tipo para resultado em outr tipo.
 * Para escrever uma função com múltiplos argumentos, basta separar os argumentos pela `->` sendo o último valor oq ela retorna
```Haskell
not  :: Bool -> Boll
even :: Int  -> Boll

soma :: Int -> Int -> Int
soma x y = x + y
```

## Tipos Polimórficos
 * `length :: [a] -> Int`
 * O `[a]` representa que a função pode receber qualquer tipo


