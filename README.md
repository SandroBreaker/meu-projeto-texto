<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página de Texto</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <button id="mostrarTexto">Mostrar Texto</button>
        <div id="conteudo"></div>
    </div>

    <script>
        const botao = document.getElementById("mostrarTexto");
        const conteudo = document.getElementById("conteudo");
        const texto1 = `
            Percebeu que eu fui embora sem lhe avisar e que não sinto remorso por isso? 
            Percebeu agora que pus em prática o que lhe pedi diversas vezes? 
            Acha mesmo que eu não iria seguir o caminho que eu queria? 
            Acha mesmo que mandaria em mim para o restante de minha vida? 
            Acha mesmo que eu suportaria os desprezos que sofria pelo meu próprio pai? 
            Realmente pensou que me humilhar e maltratar seria o melhor método de criação? 
            O que fez comigo ninguém da minha família faria, a família Gomes. Contei tudo que dissestes de minha mãe, contei o que falastes de minha avó e sua criação, contei o que falastes de meu avô em relação a sua fase terrível de vida. Já parou pra pensar que eu sempre tive um caminho pré estabelecido em minha vida? Já parou para pensar que eu sempre me senti mais feliz próxima a família Gomes? 
            Já parou para pensar que todos estes anos eu fui OBRIGADA a amadurecer antes da hora? Fui obrigada a recorrer a um vício (dança) pois ficava sozinha em casa, trancada, sem poder sair, sem poder ser visitada 
            Tu queres que eu seja grata? Então aí vai: 
            • OBRIGADA por ter sido ausente em minha vida mesmo eu não tendo morado com minha mãe. 
            • OBRIGADA por ser ríspido sempre que eu tentava chamar sua atenção, pois queria carinho. 
            • OBRIGADA por jogar dois copos de água gelada em meu rosto, em um dia frio, somente porque quando acordei fiquei sentada na cama ao invés de levantar. 
            • OBRIGADA por me chamar de idiota, filha da puta, puta, retardada, etc. 
            • OBRIGADA por ter me enforcado. 
            • OBRIGADA por ter comprado calcinhas para a sua mulher quando a última vez que comprou calcinhas para mim foi a 4 anos atrás. 
            • OBRIGADA por ter me feito usar o chinelo da sua mulher e ter comprado um novo para ela, quando o meu estourou. 
            • OBRIGADA por brigar comigo sem pensar nos motivos pela a qual eu estava apenas no meu quarto. Nunca pensou que eu tinha ansiedade, não é? 
            • OBRIGADA por me humilhar sempre que eu fazia as coisas de "qualquer jeito", mesmo tendo diversas tarefas antes de ir para a escola. 
            • OBRIGADA por ter apenas me dito "coisa da escola, você deixa na escola" quando eu estava triste por minhas notas estarem despencando pela ansiedade e não estar conseguindo compreender os conteúdos da escola. 
            • OBRIGADA por toda vez que estive mal tu não teres me escutado. Foi extremamente benéfico para mim. 
            E caso esteja pensando que minha mãe tá colocando coisa na minha cabeça, já lhe digo que não. Isto tudo veio do fundo de meu coração. Tu nem me mandastes se quer uma única mensagem, então de ti eu não tenho pena, eu tenho asco.  
            Obrigada, Genitor.
        `;
        const texto2 = `
            Ela, a menina-mulher que floresceu antes do tempo, partiu sem olhar para trás, sem um adeus. Uma partida corajosa, um ato de liberdade de quem escolhe trilhar seu próprio caminho, sem correntes, sem o peso da amargura.
            Seu coração, ferido por palavras cruéis e desprezos, encontrou abrigo na família Gomes, um oásis de afeto onde a menina-mulher pode, enfim, ser apenas menina.
            A dança, seu refúgio, a protegeu da solidão, embalou seus sonhos e a fez voar mais alto. As dores, transformadas em arte, a impulsionaram para um futuro mais leve.
            E apesar das cicatrizes, ela se ergueu forte, com a voz firme e o olhar determinado. A menina-mulher que ousou dizer "não" à dor, que se recusou a ser silenciada, que encontrou em si a força para romper as amarras e voar em direção à liberdade.
            Em cada passo, em cada palavra, em cada lágrima, ela tece a sua história, uma história de superação, de resiliência, de recomeço. Uma história que inspira e nos convida a acreditar na força do espírito humano, na capacidade de renascer das cinzas e encontrar a luz, mesmo na mais profunda escuridão.
            Que sua jornada seja repleta de flores, de sorrisos, de abraços que aqueçam a alma. Que ela encontre em seu caminho a paz, o amor e a felicidade que tanto merece.
            Voa, menina-mulher, voa! O mundo te espera de braços abertos.
        `;

        botao.addEventListener("click", () => {
            conteudo.textContent = texto1;
            botao.style.display = "none";

            setTimeout(() => {
                if (confirm("Quer ver o lado positivo dessa história?")) {
                    conteudo.classList.add("fadeOut");

                    setTimeout(() => {
                        conteudo.textContent = texto2;
                        conteudo.classList.remove("fadeOut");
                        conteudo.classList.add("fadeIn");
                    }, 1000); // Tempo da animação de fadeOut
                }
            }, 5000); // Tempo para o popup aparecer
        });
    </script>
</body>
</html>
