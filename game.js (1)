/* =================================
   DIA DOS PAIS - XANDA
   ALIXANDRE RAMOS
================================= */


/* =================================
   ABRIR HOMENAGEM
================================= */

function abrirHomenagem() {

    var homenagem = document.getElementById("homenagem");

    if (homenagem) {
        homenagem.scrollIntoView({
            behavior: "smooth",
            block: "start"
        });
    }

    criarCoracoes();
}


/* =================================
   MOSTRAR SURPRESA
================================= */

function mostrarSurpresa() {

    var surpresa = document.getElementById("surpresa");
    var botao = document.querySelector(".botao-surpresa");

    if (!surpresa) {
        return;
    }

    if (surpresa.classList.contains("ativa")) {

        surpresa.classList.remove("ativa");

        if (botao) {
            botao.innerHTML = "🎁 Clique aqui";
        }

        return;
    }

    surpresa.classList.add("ativa");

    if (botao) {
        botao.innerHTML = "🖤 Feliz Aniversário!";
    }

    criarConfetes();
}


/* =================================
   CORACOES E SIMBOLOS
================================= */

function criarCoracoes() {

    var simbolos = [
        "🖤",
        "🤍",
        "⚽",
        "🏆"
    ];

    for (var i = 0; i < 20; i++) {

        var elemento = document.createElement("div");

        elemento.innerHTML =
            simbolos[
                Math.floor(
                    Math.random() * simbolos.length
                )
            ];

        elemento.style.position = "fixed";
        elemento.style.left =
            Math.random() * 100 + "vw";

        elemento.style.bottom = "-50px";

        elemento.style.fontSize =
            (18 + Math.random() * 18) + "px";

        elemento.style.zIndex = "9999";

        elemento.style.pointerEvents = "none";

        elemento.style.transition =
            "transform 4s linear, opacity 4s linear";

        document.body.appendChild(elemento);

        setTimeout(function() {

            elemento.style.transform =
                "translateY(-" +
                (window.innerHeight + 100) +
                "px) rotate(360deg)";

            elemento.style.opacity = "0";

        }, 50);

        setTimeout(function() {

            elemento.remove();

        }, 4200);
    }
}


/* =================================
   CONFETES
================================= */

function criarConfetes() {

    var simbolos = [
        "🖤",
        "🤍",
        "🏆",
        "⚽",
        "⭐"
    ];

    for (var i = 0; i < 40; i++) {

        var confete = document.createElement("div");

        confete.innerHTML =
            simbolos[
                Math.floor(
                    Math.random() * simbolos.length
                )
            ];

        confete.style.position = "fixed";

        confete.style.left =
            Math.random() * 100 + "vw";

        confete.style.top = "-40px";

        confete.style.fontSize =
            (14 + Math.random() * 18) + "px";

        confete.style.zIndex = "9999";

        confete.style.pointerEvents = "none";

        confete.style.transition =
            "top 3s linear, transform 3s linear, opacity 3s";

        document.body.appendChild(confete);

        setTimeout(function() {

            confete.style.top = "110vh";

            confete.style.transform =
                "rotate(720deg)";

            confete.style.opacity = "0";

        }, 50);

        setTimeout(function() {

            confete.remove();

        }, 4000);
    }
}


/* =================================
   ANIMACAO DAS SECOES
================================= */

var elementos = document.querySelectorAll(
    ".homenagem, .fotos, .campeao, .surpresa"
);

if ("IntersectionObserver" in window) {

    var observador =
        new IntersectionObserver(
            function(entradas) {

                entradas.forEach(
                    function(entrada) {

                        if (
                            entrada.isIntersecting
                        ) {

                            entrada.target.style.opacity =
                                "1";

                            entrada.target.style.transform =
                                "translateY(0)";

                        }
                    }
                );

            },
            {
                threshold: 0.15
            }
        );

    elementos.forEach(
        function(elemento) {

            elemento.style.opacity = "0";

            elemento.style.transform =
                "translateY(40px)";

            elemento.style.transition =
                "opacity 0.8s ease, transform 0.8s ease";

            observador.observe(elemento);
        }
    );
}


/* =================================
   CLIQUE NAS FOTOS
================================= */

var fotos = document.querySelectorAll(
    ".foto-card img"
);

fotos.forEach(
    function(foto) {

        foto.addEventListener(
            "click",
            function() {

                foto.style.transform =
                    "scale(1.08)";

                setTimeout(
                    function() {

                        foto.style.transform =
                            "scale(1)";

                    },
                    300
                );
            }
        );
    }
);


/* =================================
   CONSOLE
================================= */

console.log(
    "Site do Aniversário - Xanda"
);

console.log(
    "Alixandre Ramos"
);