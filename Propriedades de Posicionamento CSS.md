# Display:

# `display: inline`

```
1. Deixa elementos na mesma linha. 
2. As propriedade width e heigth não funcionam em display inline. Seu tamanho e altura são definidos pelo conteúdo que eles contém.
3. Ganham um comportamento de uma palavra. 
```

# `display: block`

 ```
1. O elemento passa a ocupar a linha toda, dessa forma não podendo ter outros elementos ao lado.
2. Permite definir width e height.
3. A maioria dos elementos vem por padrão com o display: block.
```

# `display: inline-block`

 ```
1. Permite definir largura e altura (essa é o único comportamento que é herdado do display:block).
2. Permite um elemento ao lado do outro (igual ao display:inline).
3. Ele também herda o comportamento de uma palavra (igual ao display:inline, por isso o espaço entre os elementos)
4. Por se comportarem como palavras podem ser afetadas pelo text-align.
5. Seu for usado o justify no text-align, para separar os elemento pro igual na tela, lembrar q ele não justifica a ultima linha. Para resolver isso deve criar um :after no css q vai adicionar um texto na tela, ai vc faz ele ficar na ultima linha sozinho e o deixa sem conteudo.

```

-------------------------
-------------------------

# FLOAT

- Quando se usa essa propriedade criasse um novo contexto, como se fosse uma camada a frente da normal. O elemento passa a flutuar por cima.
- Se tivermos um <img> ou um display:inline ou um display:inline-block logo em seguida de um elemento com float, esse elemento vai se encaixar ao lado daqueles q estão flutuando. Se não couber ele fica logo abaixo.


`overflow: hidden`: tem o poder de esconder qualquer elemento filho que ultrapasse o tamanho do pai. Quando o pai não tem altura e largura definidas ele considera as dos filhos, mesmo q estejam em outro contexto.


`clear`: é usada para limpar o contexto caso tenho um elemento flutuando ao lado esquerdo(left), direito(right) ou ambos(both).

---------------------------
---------------------------

# POSITION

# `position: static`
    1. Static é o valor padrão dos elementos.
    2. Ela não se move.
    3. 


# `position: relative`
    1. Permite o uso de top e left.
    2. Usado na div pai para poder ser respeitada quando os filhos tiverem usando absolute. 


- `z-index`: move o lemento do eixo z (pode deixar algo a frente ou atraz um do outro). Seu valor padrão é 0. 

# `position: absolute`
    1. Quando usado cria um novo contexto levando o elemento para frente e o resto ocupa seu antigo espaço sumindo atraz dele.
    2. Usa como referencia de posicionamento o browser.


- `right, top, bottom e left`: podem ser usadas com o position, o unico q não vai usa-las é o absolute q não se move. Usando um `position: absolute` e um `right: 0;` vc posiciona o elemento grudado a direita da tela, isso serve para os outros tb.

- `transform: translateX(-50%)`: usado junto com o `left: 50%` para centralizar uma div pelo seu centro.

# `position: fixed`
    1. Fixa a posição do elemento na tela, mesmo q o usuario role o scroll o elemento vai ficar no mesmo local em relação a tela.
    2. Seu alinhamento passa a usar como referencia o browser, logo se for usado um right:0 o elemento vai grudar a direita.


- `box-sizing: border-box`: quando usado um width: 100% significa q a largura vai ser o tamanho da largura do browser, porém caso vc tenha usado um padding(respiro interno) esse valor vai ser adicionado ao total (100% + 20px do padding). Para resolver isso deve se adicionar a propriedade `border-box` que vai limitar o elemento ao tamanho maximo do browser, quando usado o padding agora ele fara a conta diminuindo o tamanho do elemento e agrecentando o tamanho do padding para dessa forma ter o tamanho total serpre o mesmo.