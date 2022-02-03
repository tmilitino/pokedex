# pokedex

## Objetivo
O projeto teve como objetivo predizer utilizando redes neurais (resnet) os pokémons iniciais (Bulbasaur, Charmander, Squirtle) através de suas fotos. Foi feito também uma predição de dois pokémons (Pikachu e Raichu).

## Coleta das imagens

Foram coletadas diversas imagens da internet (google), ao todo foram coletadas 7000 imagens divididas entre os 150 pokemons da primeira geração. \
pokedex_alfa - pokemons inicias \
evolução - pokemons sequencia de evolução

## Execução

Para executar o notebook as células devem ser executadas em sequência para não ter problemas de referências de variáveis.\
O download do dataset já está incluso no notebook.

## Arquivos

* pokedex_rgb.pt - modelo treinado com pokemon cores
* pokedex_gray.pt - modelo treinado com pokemon em escala de cinza
* pokedex_evo_rgb.pt - modelo treinado com evolução dos pokemons utilizando cores
* pokedex_evo_gray.pt - modelo treinado com evolução dos pokemons escala de cinza


## Método

### Experimento 1
No primeiro experimento foram observados os pokémons iniciais, com as fotos coloridas, foram analisadas 141 fotos, foi dado um split entre treino e teste de 80/20. Foram utilizados 5 epochs e obteve uma acurácia de 1.0, porém o modelo se baseou com a cor do pokémon, caso incluísse um pokémon de cor verde o modelo iria classificar como bulbasaur, comprovado  através do salvamento do modelo. O pokémons metapod (verde) foi classificado como bulbasaur e goldduck (azul) como Squirtle. Convertendo as imagens para escala de cinza e o modelo não ficar enviazado por conta das cores, optivie uma acurácia 0.935484 para 10 epochs, com isso eliminei um vies de classificar pela cor. 
![WhatsApp Image 2022-02-01 at 02 00 08](https://user-images.githubusercontent.com/23370997/152085243-b2654421-3a9a-4667-bf46-eb7504448032.jpeg)

### Experimento 2
No segundo experimento foram escolhidos dois pokemons parecido e que fossem evoluções, para observar o impacito das cores para eles. Com as cores o modelo tem uma acurácia de 1.0 para 3 epoch, mas vies da cor estava presente, para validar usei o Charizard (laranja) que foi classificado como raichu e psyduck (amarelo) pikachu. Convertendo as imagens para escala de cinza e o modelo não ficar enviazado por conta das cores, optivie uma acurácia 0.958333 para 10 epochs, com isso eliminei um vies de classificar pela cor.
