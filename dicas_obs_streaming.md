> Este arquivo ainda está em construção, mas espero que já possa ser de ajuda.

# Introdução

Neste documento você irei falar sobre algumas coisas que eu sei e utilizo para configurar as lives. Não sou expert, nem nada, comecei a fazer live em 2020, mas das coisas que sei já chegaram a ajudar algumas pessoas próximas a mim e a deixar suas lives da forma que agradavam a elas. Então, espero que possa ajudar você também.

> Nota: Tudo aqui pode ser alterado de acordo com sua necessidade. Eu não estou ditando regras, nem falando uma verdade absoluta. É puramente minha singela esperiência de como uso o OBS.

## Aqui você verá

1. Configurações que considero importante
    1. Organização de cenas
    2. Configuração de som
    3. Configuração de video
    4. Configuração de atalhos atalhos
2. Plataformas gratuitas, que utilizo:
    1. [Streamlabs](streamlabs.com/)
    2. [Stream Elements](streamelements.com)
    3. [Stream Holics](streamholics.live)
    4. [wdflat](https://wdflat.com/)
3. Dicas
    1. Economizando CPU
    2. Economizando memória

# 1. Configurações que considero importante

## 1.1 Organização de cenas

As organizações de cenas eu costumo fazer camadas genéricas que possam ser reutilizadas. Eu chamo elas de template, mas você pode dar que desejar.

![image](https://user-images.githubusercontent.com/6399202/101716606-63397e00-3a7c-11eb-8fac-54c12638bb40.png)

Essas cadas eu utilizo para o Overlay de uma forma geral. O overlay é como chamamos os desenhos que colocamos na live, por exemplo:

1. Quadro onde fica a webcam (frame cam)
2. Barras de metas: Seguidores, inscritos, doações
3. Textos do chat
4. Notificações
5. etc

A organização das fontes em uma cena no OBS funcionam em forma de camadas. Então imagina você ter várias figurinhas recortadas e quisesse montar um quadrinho. Então você empilha os pedaços montando a sua cena.

Dessa forma, você pode tentar imaginar como organizar suas cenas de forma que elas podem ser usadas em outras, evitando trabalhos em excesso.

Na imagem acima eu utilizo 4 templates:

1. Template Status:  
    É onde eu coloco as cenas de status: Começando, Volto logo, Encerrando  
    Assim eu simplemente mudo o plano de fundo e o texto.
2. Template Minimal e minimal bot:  
    Este template eu utilizo na hora do live code e dos jogos. Basicamente ele tem toda a diagramação dos objetos, e na cena LIVEON eu monto os detalhes
3. Template Alerta:  
    Este é o que com certeza irá gostar de criar para reutilizar. Aqui eu coloco todos os alertas da live, e assim reutilizo em todas as outras cenas e não preciso configurar em todos.  
    Aqui vai alertas de seguidores, inscritos, doações, strealholics e tudo mais

> O principal aqui, é você ter a ideia que cenas e fontes funcionam como camadas uma em cima da outra.

## 1.2 Configuração de som

Este é o principal ponto da sua live. O som é a principal arma de comunicação. Particularmente, ouvi o som do teclado e de carros passando na rua não é nada legal durante uma live, há quem goste né? Vou comentar sobre como podemos remover isso, ou deixar levemente legal. Mas, novamente, tudo que falo aqui é gosto pessoal e experiência minha, você pode definir como desejar a sua live. :)

### Barra de áudio

![image](https://user-images.githubusercontent.com/6399202/101718031-28851500-3a7f-11eb-9c07-eda3730849ad.png)

"Me disse" que a twitch recomenda que o audio do microfone (Mic/Aux) fique no máximo no amarelo, e que o audio do computador (Desktop Áudio) no máximo no inicio do amarelo.

Isso faz um sentido se você considerar que sua voz é relativamente mais importante que o som das computador, pois se sua voz ficar mais baixa, pode acontecer de não lhe ouvirem e dando uma experiência ruim.

Eu costumo deixar todos os audios do computador no máximo, e abaixo dentro da aplicação o áudio delas, tipo o Spotify, deixo em cerca de 20% somente.

Na imagem objserve que o meu Desktop Áudio está com -18.5dB, isso é porque os programas com full audio e o discord alcançam o limite que eu desejo, alí por volta dos -20 (comecinho da barra amarela). Já o meu mic está no máximo, pois eu limito só o fim. E essa limitação fazemos com os filtos

### Filtros

Os filtros são fatores muito importante na configuração do seu áudio. E utilizo alguns diferentes para o desktop e para o mic/aux. Eu só comento estas duas barras de audio, pois são os mais importantes. Os demais você configura com a mesma lógica para ambos.

Aqui pode ser a questão mais chata, pois você precisará ir testando até achar o que fica melhor no seu ambiente.

![image](https://user-images.githubusercontent.com/6399202/101718486-0d66d500-3a80-11eb-8451-d7442f23fdb4.png)

A imagem acima são os filtros que uso no microfone. 

1. Compressor:  
    Interessante para trazer o áudio mais baixo para um tom médio e o audio mais alto para um tom médio, ou seja, ele comprime os volumes para deixar igual, tanto falando baixinho, como gritando.   
    Entretanto, sem mexer na configuração você ainda mantem a entonação de voz.
2. Redução de ruídos:
    No Windows (onde uso), ele possui uma configuração automática, que particularmente é o suficiente.  
    A ideia deste filtro é deixar quase no mínimo a oscilação do audio quando você está em silêncio. **SIM EM SILÊNCIO**. Você configura este filtro sem falar no microfone. Aqui você tenta minimizar os audios que "sujam" sua voz.  
    **NOTA**: Vale a pena testar aqui o som da digitação e o som do clique do mouse. Eu sempre reduzo o máximo possível, se zerar ótimo, se não poder, deixe no menor.
3. Limitador:  
    Aqui é o colega que vai impedir que seu audio "papoque" os ouvidos de quem lhe ouve. Basicamente, você poe até antes de chegar no vermelho. No meu, com audio no máximo, eu coloquei -10db (exemplo da imagem). É bastante interessante utilizá-lo
4. Filtro de ruídos:  
    Este eu parei de usar quando ganhei um microfone (S2 Kildin), e comprei o braço articulado, assim o microfone ficou mais longe do teclado e do mouse. Mas, quando usava headset era obrigatório. A redução de ruído remove muito do som ambiente, mas foi com este filtro que eu consegui remover o audio do clique no mouse e 99% do teclado (pois, aquele 1% safadão... saia).  
    **NOTA**: Este filtro possui duas opções, e elas sempre, **SEMPRE**, devem ter uma diferença de 6 entre elas. Ao adicionar elas ja vem com essa diferença de 6, mantenha ela ao mover ambos.  
    **NOTA²**: Movendo para a esquerda você dificulta a entrada de som, diminuindo o ruído, entretanto você precisará falar mais alto.

Se divitar com a configuração de som e filtros, eu realmente considero o ponto mais importante numa transmissão.

Vou deixar o link aqui de um video muito bom que me ensinou muito sobre os filtros:  
[Como Configurar o Microfone no OBS Studio / Streamlabs OBS - canal Tunyzin
](https://www.youtube.com/watch?v=Sy6WXuwgCJI)

## 1.3 Configuração de video

As configurações de vídeo é realmente algo muito delicado, vai depender completamente da sua máquina, se você tem placa de vídeo ou não. Para o live coding, eu não recomendaria mais que 720p, pois com 480p já é possível ler muitos dos códigos, e com 720p você lê tudo. MAS, se você tem computador suficiente e internet também, você pode por na resolução que quiser.

Uma dica que eu dou é você gravar sua live ao invés de transmitir, para configurar resolução e FPS de acordo com suas limitações, dessa forma você testa trabalho de renderização do seu computador e consegue deixar as mehores taxas.

A quantidade de Bitrate é muito dependente da sua banda. Eu tenho 50mb de internet, uso no wifi, fica com 25mb a 30mb me dando 2mb a 3mb de upload, assim eu deixo meu bitrate em 2500.

Uma forma de você testar seu bitrate é executando uma transmissão de tese. **SIM** você tem como fazer uma transmissão de teste sem ficar online.

![image](https://user-images.githubusercontent.com/6399202/101719587-60da2280-3a82-11eb-9f8a-aef3c7df3325.png)

Utilize deste recurso sempre que poder, se possível tempos antes de abrir live. Assim, você pode verificar se precisa por exemplo reiniciar o modem para melhorar o sinal.


Como eu possuo uma placa de vídeo singela no meu notebook de 2GB (geforce mtx 110), ela me ajuda a renderizar o video da live, assim meu encoder e este da imagem abaixo. A saída é 720p (1280x720) e as configurações são essas, para melhorar o máximo que posso. 

![image](https://user-images.githubusercontent.com/6399202/101719671-94b54800-3a82-11eb-957d-38af9136bad6.png)

Essas configurações não sairam do nada e foram tiradas da própria twitch: [Broadcasting Guidelines](https://stream.twitch.tv/encoding/). Foram feitas algumas leves alterações para não explodir meu notebook :D

## 1.4 Configurações de atalhos

Aqui temos nossa `streampadkeyboardsuperdahoragambiarraquefunciona`.

Basicamente aqui eu gostaria de falar sobre atalhos que considero muito importante:

1. Mudança de cena
2. Silenciar audio do computador (desktop)
3. Silenciar audio do microfone 
4. Desligar webcam

Como eu não tenho uma `Streampad` eu utilizo atalhos loucos do teclado para efetuar tudo isso. Aqui você pode usar o que desejar.

Vou mostra algumas imagens para exemplificar, eu utilizo o ALT+GR do teclado, que cria um `ctrl+alt` nos atalhos.

Eu mudo as cenas usando ALT+GR+F... assim coloco do F! ao F5 e mudo as cenas sem menor problema.

![image](https://user-images.githubusercontent.com/6399202/101720018-4fdde100-3a83-11eb-9161-afe583478901.png)

Em todas as cenas que possuem webcam eu adiciono o mesmo atalho. O mesmo atalho irá funcionar para todas as cenas, então quando eu mudar de cena, caso remova a cam, ela continuará desligada.

![image](https://user-images.githubusercontent.com/6399202/101720164-a2b79880-3a83-11eb-9b19-8083460ce53b.png)

> Lembre-se de colocar o mesmo atalho para ligar e desligar, assim facilita a vida :D

Para o audio a mesma coisa.

![image](https://user-images.githubusercontent.com/6399202/101720221-c844a200-3a83-11eb-86b1-51ee75ff3ad3.png)

Aqui eu quis demonstrar os meus atalhos que facilitam muito muita vida durante as lives, não precisando que eu mecha diretamente no OBS e agilizando muito a minha dinâmica. Sobretudo, os de audio e webcam. :)
