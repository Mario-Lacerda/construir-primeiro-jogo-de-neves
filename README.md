# Desafio dio - Construindo o seu Primeiro Jogo de Naves 
Neste projeto o objetivo é criar um jogo de naves abrangente e bem estruturado, seguindo os princípios de engenharia de software.  Para isso, ouso construir um jogo de naves simples usando Kotlin. O jogo contará com uma nave controlada pelo jogador e inimigos que se movem pela tela. O objetivo do jogador é destruir os inimigos e evitar ser atingido.

## **Estrutura do Projeto**

- **Modelos:** Classes que representam os objetos do jogo, como `Nave`, `Inimigo` e `Tiro`.
- **Serviços:** Funções que controlam a lógica do jogo, como movimento, disparo e verificação de colisões.
- **Lógica de Negócios:** Regras e comportamentos do jogo, como como os inimigos se movem e como os tiros causam dano.
- **Testes:** Testes unitários para verificar a funcionalidade de cada componente.
- **Documentação:** Documentação abrangente para explicar o código e o design do jogo.

## **Definição de Modelos**

As classes de modelo representam os objetos do jogo:

- **Nave:** A nave controlada pelo jogador, com propriedades como posição, velocidade e vida.
- **Inimigo:** Um inimigo que se move pela tela, com propriedades semelhantes à nave.
- **Tiro:** Um tiro disparado pela nave ou por um inimigo, com propriedades como posição, velocidade e dano.

## **Serviços**

Os serviços controlam a lógica do jogo:

- **Gerenciador de Nave:** Controla o movimento e o disparo da nave do jogador.
- **Gerenciador de Inimigos:** Controla o movimento e o comportamento dos inimigos.
- **Gerenciador de Tiros:** Controla o movimento e as colisões dos tiros.
- **Verificador de Colisões:** Verifica se há colisões entre a nave do jogador, inimigos e tiros.

## **Lógica de Negócios**

A lógica de negócios define as regras e comportamentos do jogo:

- **Movimento dos Inimigos:** Os inimigos se movem em padrões aleatórios ou predefinidos dentro dos limites da tela.
- **Dano dos Tiros:** Os tiros causam dano aos inimigos e à nave do jogador, reduzindo sua vida.
- **Condições de Vitória/Derrota:** O jogador vence se destruir todos os inimigos. O jogador perde se sua nave perder toda a vida.
- **Níveis e Pontuação:** O jogo pode ter vários níveis com dificuldade crescente. Os jogadores ganham pontos por destruir inimigos.



### O objetivo do jogador é destruir os inimigos e evitar ser atingido.

## **Classes**

- **Nave:** Representa a nave controlada pelo jogador, com propriedades como posição, velocidade e vida.
- **Inimigo:** Representa um inimigo que se move pela tela, com propriedades como posição, velocidade e vida.
- **Tiro:** Representa um tiro disparado pela nave ou por um inimigo, com propriedades como posição, velocidade e dano.

## **Funções**

- **Mover Nave:** Move a nave do jogador na direção especificada.
- **Disparar Tiro:** Dispara um tiro da nave do jogador.
- **Mover Inimigos:** Move todos os inimigos na tela.
- **Verificar Colisões:** Verifica se há colisões entre a nave do jogador, inimigos e tiros.
- **Atualizar Jogo:** Atualiza o estado do jogo, movendo objetos e verificando colisões.

## **Cenários de Uso**

- **Controle da Nave:** O jogador usa as teclas de seta para controlar a nave.
- **Disparo de Tiros:** O jogador pressiona a barra de espaço para disparar tiros.
- **Movimento dos Inimigos:** Os inimigos se movem pela tela em padrões aleatórios.
- **Colisões:** Se a nave do jogador colidir com um inimigo ou tiro inimigo, ela perde vida. Se todos os inimigos forem destruídos, o jogador vence.

#### **Exemplo de Código**

kotlin

```kotlin
class Nave(var x: Int, var y: Int, val velocidade: Int, val vida: Int) {
    fun mover(direcao: Direcao) {
        when (direcao) {
            Direcao.CIMA -> y -= velocidade
            Direcao.BAIXO -> y += velocidade
            Direcao.ESQUERDA -> x -= velocidade
            Direcao.DIREITA -> x += velocidade
        }
    }

    fun dispararTiro(): Tiro {
        return Tiro(x, y, velocidade = 10, dano = 1)
    }
}

class Inimigo(x: Int, y: Int, velocidade: Int, vida: Int) : Nave(x, y, velocidade, vida)

class Tiro(x: Int, y: Int, velocidade: Int, dano: Int) {
    var x = x
    var y = y
    val velocidade = velocidade
    val dano = dano

    fun mover() {
        y += velocidade
    }
}
```

## **Integração e Testes**

- A integração é realizada conectando os modelos, serviços e lógica de negócios em uma classe principal que gerencia o loop principal do jogo.
- Os testes unitários são escritos usando um framework de teste para verificar se as diferentes partes do jogo estão funcionando corretamente.
- Os testes são escritos usando o framework JUnit para verificar se as diferentes partes do jogo estão funcionando corretamente.

## **Documentação**

- A documentação do código é escrita usando comentários e um documento de design separado.
- O documento de design descreve a arquitetura do jogo, os requisitos funcionais e as decisões de design.



## **Conclusão**

Este projeto de jogo de naves abrangente e bem estruturado é altamente modular, testável e bem documentado. Ele fornece uma base sólida para o desenvolvimento de jogos mais complexos e envolventes.  O jogo de naves fornece uma base para os entusiastas jogadores,oportunidade de  controlar uma nave, disparem tiros e interajam com inimigos. Com mais poder de  transformação numa atividade divertida e bastante desafiadora.

## **Aplicabilidade Prática**

Este projeto pode ser usado como um modelo para criar uma ampla gama de jogos de naves, desde jogos simples para iniciantes até jogos profissionais com recursos avançados.
