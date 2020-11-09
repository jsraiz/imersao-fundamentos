## Desenvolvendo a lógica
Agora que nós já situamos sobre JavaScript, navegador e ecossistema front-end, precisamos pegar tudo isso e começar a desenvolver.

Mas se você ainda está desenvolvendo lógica e ao mesmo tempo estudando front-end. Aqui vão algumas dicas.

### Continentes
Você pode praticar lógica unicamente utilizando o continente JavaScript. Entretanto, muitos exemplos e aulas que você vai encontrar na internet, vão ter continentes se misturando.

Para isso, é muito importante dissernir eles e saber misturá-los bem, sabendo como atuar em cada continente.

O mais comum é a mescla entre continente navegador e continente JavaScript, onde capturamos dados do usuário, processamos e depois mandamos novamente a informação para a tela.

![Navegador e JavaScript juntos](imgs/navegador-e-js.svg)

Para você acessar as funcionalidades do navegador via JavaScript, é como se fosse uma estrada entre os dois continentes. Uma estrada chamado `window`. 

O navegador vai injetar um objeto global chamado `window` no seu JavaScript. Através do `window`, conseguimos fazer tudo que o navegador disponibiliza para nós, como devs, fazer.

```js
window.document.addEventListener('click', manipulaClique);

const contador = window.localStorage.getItem('contador');
```

ou melhor (sem precisar digitar window)

```js
document.addEventListener('click', manipulaClique);

const contador = localStorage.getItem('contador');
```

No geral, quando trabalhamos no navegador com JavaScript, fazemos acesso direto ao `document`, `location`, `navigator`, `localStorage` e muitos outros sem precisar chamar o objeto `window`. Por quê?

A primeira coisa a frizar, é que todos esses objetos (document, localStorage, etc.) estão dentro de window.

A segunda, se deve ao [escopo lexico](https://youtu.be/D-qxe4Pem0Y) e objeto global. Quando o JavaScript não encontra a definição daquela variável/constante/função naquele escopo, ele busca no escopo maior. Caso também não encontre, ele continua procurando.

Só a nível de curiosidade, existe um termo chamado Variable shadowing, que é quando uma variável no escopo local de mesmo nome de uma do escopo externo. Essa do escopo externo se torna inacessível, a variável de fora está sendo 'sombreada/shadowed' pela de dentro, enquanto a de dentro está sendo uma máscara para a de fora

O escopo maior de um JavaScript no navegador é o escopo global, sendo que o escopo global e `window` são as mesmas coisas. Por isso que você consegue acessar `document` em qualquer parte do seu código, pois o último lugar que o JavaScript vai procurar a definição de `document` vai ser no escopo global.



## Quebre o problema em pequenas tarefas
A primeira forma de quebrar as tarefas, é pensar em seus continentes separadamente.

Se o que vai desenvolver, precisa de algo relacionado ao navegador, tente pensar nele separado do JavaScript em si.

Pense em como vai fazer essa captura da informação ou interação com o navegador de alguma forma e como vai passar isso para ser processado no JavaScript.

Fluxo natural: Entrada -> Processamento -> Saída.

Claro que nem sempre vai ser natural assim, porém sempre tente isolar essas camadas.

## Desafios

Aqui tem alguns desafios para você praticar todas as dicas aqui dadas.

Acesse agora e comece para exercitar a lógica:
- [Lista de desafios](https://github.com/jsraiz/desafios)