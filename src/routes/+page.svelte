<script>
import { base } from '$app/paths';
</script>

<svelte:head>
    <title>Página do Projeto</title>
</svelte:head>

<div class="page">
    <div class="title">
        <h1>Análise dos Resultados Olímpicos</h1>
        
        <h3>por Guilherme Buss, Guilherme Carvalho e Luís Felipe Marciano</h3>

        <p>
            Apresentamos a Plataforma de Análise Olímpica! Nosso objetivo com o site é mergulhar na rica história dos Jogos Olímpicos através de dados e visualizações interativas. Queremos oferecer ao usuário uma maneira fascinante de explorar tendências, comparar performances marcantes e compreender a evolução do esporte ao longo das décadas. Navegando por todas as abas, terá uma experiência completa e entenderá diferentes aspectos dos jogos olímpicos.
        </p>
            
        <p>
            A visualização pode ser acessada em:
            <a href="https://fgv-vis-2025.github.io/final-project-analise-resultados-olimpiadas/"
                target="_blank"
                rel="noopener">
                Análise de Resultados - Olimpíadas
            </a>
        </p>   
        
        <p>
            Link para o Artigo:
            <a href="https://filiacao.pt.org.br"
                target="_blank"
                rel="noopener">
                link do artigo
            </a>
        </p>   
    </div>

    <div class="resumo">
        <div class="resumo-item">
            <h3><strong>Resultados ao longo do tempo</strong></h3>
            <p>Nessa visualização destacamos a performance dos medalhistas de ouro em diversas modalidades do atletismo através das diferentes edições dos Jogos Olímpicos. Observe como as marcas vencedoras evoluíram, identifique atletas que dominaram suas provas e perceba o impacto de diferentes eras no auge do desempenho esportivo. Utilize os filtros disponíveis para refinar sua busca e focar em eventos específicos ou faixas de resultados que mais lhe interessam.</p>
            <img src={`${base}/page1.png`} alt="Gráfico de desempenho dos medalhistas ao longo do tempo"/>
        </div>
        <div class="resumo-item">
            <h3><strong>Rede de Competição de Atletas</strong></h3>
            <p>Esta visualização revela a rede de rivalidades e encontros entre atletas olímpicos ao longo da história. Cada nó representa um competidor, posicionado de acordo com sua frequência de confrontos com o atleta central, permitindo identificar adversários recorrentes, duelos icônicos e até padrões de dominância em determinadas modalidades.</p>
            <img src={`${base}/page2.png`} alt="Grafo de rede de competição entre atletas"/>
        </div>
        <div class="resumo-item">
            <h3><strong>Histórico das edições</strong></h3>
            <p>Na terceira página apresentamos uma animação com a evolução do ranking dos 10 países com mais medalhas conquistadas em todas as edições dos Jogos Olímpicos. Descubra as ascensões e quedas das maiores potências esportivas do mundo e acompanhe as mudanças no domínio olímpico ao longo dos anos. Além disso, confira os cards ao lado do ranking para informações detalhadas sobre cada edição, incluindo curiosidades e destaques marcantes.</p>
            <img src={`${base}/page3.png`} alt="Animação do ranking de medalhas por país"/>
        </div>
    </div>

    <div class="video-container">
        <video width="100%" controls poster={`${base}/thumb_video.png`}>
            <source src={`${base}/video_apresentação.mp4`} type="video/mp4">
            Seu navegador não suporta a tag de vídeo.
        </video>
    </div>

    
    <div class="instrucoes">
        <h1>Instruções de Execução</h1>
        Lorem ipsum dolor sit
    </div>
</div>

<style>
.page h1, h3{
    color: #0076bf;
}
.page {
    max-width: 1320px;
    margin: 0 auto;
    padding: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.title h1 {
    font-weight: 700;
    margin: 0 0 0 0;
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 2rem;
    letter-spacing: -0.5px;
    text-align: center;
}

.title h3 {
    font-weight: 300;
    color: #555;
    margin: 0.5em 0 1.5em 0; 
    font-size: 1rem;
    text-align: center;
}
.resumo {
    display: flex;
    gap: 20px;
    margin: 2rem 0; 
}

.resumo-item {
    flex: 1;
    display: flex; 
    flex-direction: column; 
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
}

.resumo-item h3 {
    margin-top: 0;
}

.resumo-item img {
    width: 100%; 
    height: auto;
    margin-top: auto; 
    border-radius: 0px;
}

.video-container {
    margin: 2rem 0;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}
</style>