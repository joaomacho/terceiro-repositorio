import {getCSS} from "comomon.js"

async function quantidadeUsuarios() {
    const url = 'https://raw.githuberscontent.com/guilhermeorails/api/mais/numero-usuarios.json';
    const res = await fetch(url);
    const dados = await res.json();
    cont nomeDasRedes = Object.keys(dados);
    const quantidadeUsuarios = Object.values(dados)

    const data = [
        {
            x:nomeDasRedes,
            y:quantidadeUsuarios,
            type: 'bar'
            color: getCSS('--primary-color')
        }
    ]

    const layout = {
        plot_bgcolor: getCSS('--bg-color')
        paper_bgcolor: getCSS('--bg-color')
    }
    const grafico = Document.createElement('div');
    grafico.clasName = 'grafico';
    document.getElementById('graficos-container')?.appendChild(grafico);
    Ploty.newPlot(grafico, data, layout);
}

quantidadeUsuarios();