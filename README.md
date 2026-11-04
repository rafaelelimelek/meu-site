<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rafael Elimelek - Ator e Jornalista</title>
    <style>
        /* Importação de fontes cursivas e limpas */
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Inter:wght@400;600;700&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #ffffff;
            color: #0b2545;
            font-family: 'Inter', Arial, sans-serif;
            width: 100vw;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .page {
            display: none;
            width: 100vw;
            min-height: 100vh;
            padding: 40px;
        }

        .page.active {
            display: block;
        }

        /* RETÂNGULO SUPERIOR DA PÁGINA PRINCIPAL */
        .top-banner {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, #0b2545 70%, #38b000 70%);
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 50px;
            position: relative;
        }

        .top-banner .photo-placeholder {
            width: 150px;
            height: 200px;
            background-color: #e5e5e5;
            border: 2px dashed #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #0b2545;
            font-weight: 600;
            text-align: center;
            font-size: 14px;
        }

        /* CONTATO ABAIXO DO RETÂNGULO */
        .contact-info {
            margin-top: 15px;
            font-size: 14px;
            color: #0b2545;
            display: flex;
            gap: 20px;
            align-items: center;
        }

        .contact-info a {
            color: #0b2545;
            text-decoration: none;
            font-weight: 600;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        /* TÍTULOS PRINCIPAIS */
        .main-title {
            font-family: 'Dancing Script', cursive;
            font-size: 64px;
            margin-top: 20px;
            color: #0b2545;
        }

        .subtitle {
            font-size: 20px;
            font-weight: bold;
            text-transform: uppercase;
            color: #0b2545;
            margin-top: 5px;
            margin-bottom: 25px;
        }

        /* CAIXA SOBRE MIM */
        .about-box {
            background-color: #f4f5f7;
            padding: 30px;
            border-radius: 6px;
            position: relative;
            margin-bottom: 30px;
        }

        .about-box h3 {
            color: #38b000;
            font-size: 18px;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .about-box p {
            font-family: Arial, sans-serif;
            color: #0b2545;
            line-height: 1.6;
            font-size: 15px;
        }

        .more-about-btn {
            position: absolute;
            bottom: 15px;
            right: 20px;
            font-size: 11px;
            color: #0b2545;
            font-weight: bold;
            text-decoration: underline;
            cursor: pointer;
            background: none;
            border: none;
        }

        /* IDIOMAS */
        .languages {
            display: flex;
            gap: 20px;
            align-items: center;
            font-size: 15px;
            margin-bottom: 40px;
        }

        .lang-item {
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .dot {
            display: inline-block;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background-color: #0b2545;
        }

        .dot-half {
            background: linear-gradient(90deg, #0b2545 50%, #ccc 50%);
        }

        .dot-quarter {
            background: linear-gradient(135deg, #0b2545 25%, #ccc 25%);
        }

        /* SEÇÃO DUPLA: ATOR & JORNALISTA */
        .duo-section {
            display: flex;
            justify-content: space-between;
            gap: 30px;
            position: relative;
            margin-bottom: 40px;
        }

        .card-box {
            background-color: #ffffff;
            border: 1px solid #e1e1e1;
            padding: 25px;
            border-radius: 6px;
            width: 42%;
            cursor: pointer;
            transition: box-shadow 0.3s;
        }

        .card-box:hover {
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .card-box h3 {
            color: #0b2545;
            font-size: 22px;
            text-transform: uppercase;
            margin-bottom: 15px;
        }

        .card-box p {
            font-size: 14px;
            line-height: 1.5;
            color: #0b2545;
        }

        /* SETAS E FLUXOGRAMA CENTRAL */
        .arrows-center {
            width: 16%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 8px;
            color: #0b2545;
            font-size: 12px;
            text-align: center;
        }

        .arrow-item {
            font-weight: 600;
        }

        /* CAIXA DE TRABALHO VOLUNTÁRIO CENTRAL */
        .volunteering-box {
            background-color: #f4f5f7;
            border: 1px solid #e1e1e1;
            padding: 20px;
            border-radius: 6px;
            text-align: center;
            margin-top: 10px;
            cursor: pointer;
        }

        .volunteering-box h4 {
            color: #0b2545;
            font-size: 14px;
            text-transform: uppercase;
            margin-bottom: 5px;
        }

        .volunteering-box p {
            font-size: 12px;
            color: #0b2545;
        }

        /* ESTILOS DE SUB-PÁGINAS */
        .subpage-title {
            color: #0b2545;
            font-size: 24px;
            font-weight: bold;
            text-transform: uppercase;
            margin-bottom: 20px;
        }

        .back-btn {
            display: inline-block;
            margin-bottom: 20px;
            background-color: #0b2545;
            color: #fff;
            padding: 8px 16px;
            border-radius: 4px;
            text-decoration: none;
            font-size: 14px;
            cursor: pointer;
        }

        .file-grid {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .file-card {
            width: 180px;
            background: #f4f5f7;
            border: 1px solid #ccc;
            padding: 12px;
            text-align: center;
            border-radius: 4px;
            cursor: pointer;
        }

        .file-preview {
            width: 100%;
            height: 90px;
            background: #fff;
            border: 1px solid #ddd;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            color: #666;
        }

        .file-card span {
            font-size: 11px;
            font-weight: bold;
            color: #0b2545;
            display: block;
            line-height: 1.3;
        }
    </style>
</head>
<body>

    <!-- ================= PÁGINA PRINCIPAL ================= -->
    <div id="home-page" class="page active">
        <div class="top-banner">
            <div style="color: white; font-size: 24px; font-weight: bold;">Rafael Elimelek</div>
            <div class="photo-placeholder">Espaço Foto Corpo Inteiro</div>
        </div>

        <div class="contact-info">
            <span>E-mail: rafaelelimelek@gmail.com</span>
            <span>|</span>
            <span>LinkedIn: <a href="https://www.linkedin.com/in/rafael-elimelek-6123561b2" target="_blank">linkedin</a></span>
        </div>

        <h1 class="main-title">Rafael Elimelek</h1>
        <div class="subtitle">Ator e Jornalista</div>

        <div class="about-box">
            <h3>Sobre Mim</h3>
            <p>Olá. Sou o Rafael Elimelek. Tenho um perfil criativo, dedicado, comunicativo e artístico. Estudante de Jornalismo e de Artes Cênicas e educador. Busco informar, causar reflexões e incentivar a imaginação. Trabalho sério e estou disposto a continuar aprendendo.</p>
            <button class="more-about-btn" onclick="navigateTo('more-about-page')">mais sobre mim</button>
        </div>

        <div class="languages">
            <div class="lang-item"><span class="dot"></span> Português</div>
            <div class="lang-item"><span class="dot"></span> Inglês</div>
            <div class="lang-item"><span class="dot dot-half"></span> Hebraico</div>
            <div class="lang-item"><span class="dot dot-quarter"></span> Espanhol</div>
        </div>

        <div class="duo-section">
            <div class="card-box" onclick="navigateTo('actor-page')">
                <h3>Ator</h3>
                <p><strong>ARTES CÊNICAS na UNESP</strong><br>
                Faço teatro desde quando eu tinha 6 anos. Aprendi a improvisar, atuar e me expressar. Participei de mais 17 peças de teatro, incluindo musicais. Atualmente curso Bacharelado em Artes Cênicas na UNESP, estou no 4° semestre.</p>
            </div>

            <div class="arrows-center">
                <div class="arrow-item">↕ comunicativo</div>
                <div class="arrow-item">← artista</div>
                <div class="arrow-item">→ conhecimento esportivo/textos</div>
                <div class="arrow-item">← criativo</div>
                <hr style="width:100%; border:0; border-top:1px solid #0b2545; margin: 5px 0;">
                <div class="arrow-item">↓ líder</div>
                <div class="arrow-item">↓ educador</div>
                <div class="arrow-item">↓ comunicação não violenta</div>
                
                <div class="volunteering-box" onclick="navigateTo('volunteering-page')">
                    <h4>Trabalho Voluntário</h4>
                    <p>Movimento juvenil Habonim Dror, experiência internacional e outras atividades interessantes.</p>
                </div>
            </div>

            <div class="card-box" onclick="navigateTo('journalism-page')">
                <h3>Jornalista</h3>
                <p><strong>JORNALISMO na FACULDADE CÁSPER LÍBERO</strong><br>
                Informar a realidade, com honestidade e trabalho duro. Esse é o meu compromisso com o Jornalismo. Além de ter conhecimentos prévios principalmente sobre esportes, busco aprender para atuar em outras áreas. Atualmente estou no 4° semestre de Jornalismo na Faculdade Cásper Líbero.</p>
            </div>
        </div>
    </div>


    <!-- ================= PÁGINA: MAIS SOBRE MIM ================= -->
    <div id="more-about-page" class="page">
        <a class="back-btn" onclick="navigateTo('home-page')">← Voltar à Página Principal</a>
        <h2 class="subpage-title">Textos sobre mim</h2>
        <div style="line-height: 1.8; font-size: 15px; max-width: 900px;">
            <p><strong>Mais sobre mim:</strong><br>São Paulo, 7 de abril de 2021</p>
            <p><strong>Para:</strong> Rahamim Elimelek, mais conhecido como nono (meu avô paterno que faleceu em 2003)</p>
            <p>Oi nono, tudo bem?</p>
            <p>Sou eu, o Rafael, seu neto. Nós nunca nos vimos pessoalmente, mas meus pais, tios e amigos dos meus pais me contam muito sobre você e a nona...</p>
            <br>
            <p><strong>Atualizações (11/2026):</strong><br>
            - <strong>2021:</strong> Em Julho participei da peça-filme Berlim, na Escola Lux de Teatro.<br>
            - <strong>2022:</strong> Me tornei madrich (educador) no Habonim Dror; Fiz a monografia “Propostas para solucionar as crises financeiras no futebol brasileiro” e fui premiado na MOSTRATEC; Apresentei as peças <em>O Casamento de Wandinha</em> e <em>Admirável Mundo Novo</em>.<br>
            - <strong>2023:</strong> Me formei na Escola Alef Peretz em dezembro de 2023; Fui madrich na Machané do Habonim Dror no Rio de Janeiro.<br>
            - <strong>2024:</strong> Comecei a graduação em Jornalismo na Faculdade Cásper Líbero e Bacharelado em Artes Cênicas na UNESP; Fui madrich em Machané em Salvador.<br>
            - <strong>2025:</strong> Fiz o programa Shnat Hachshará do Habonim Dror da América Latina (10 meses em Israel, voluntariado no Kibutz Revivim, Escola Ofarim em Haifa, Teatro Cameri em Tel Aviv e Machon Le Madrichim em Jerusalém).<br>
            - <strong>2026:</strong> Estou na metade das minhas duas graduações; Sou Mazkir do Habonim Dror de São Paulo.</p>
            <br>
            <p><strong>FOTOS:</strong> Diploma Escola Alef Peretz</p>
        </div>
    </div>


    <!-- ================= PÁGINA: ATOR ================= -->
    <div id="actor-page" class="page">
        <a class="back-btn" onclick="navigateTo('home-page')">← Voltar à Página Principal</a>
        <div style="display: flex; justify-content: space-between; align-items: center;">
            <h2 class="subpage-title">Peças</h2>
            <h2 class="subpage-title" style="text-align: center;">Vídeos (7 espaços)</h2>
            <h2 class="subpage-title">Fotos</h2>
        </div>

        <div style="display: flex; justify-content: space-between; margin-top: 20px;">
            <div style="width: 30%; font-size: 14px; line-height: 1.6;">
                <p>2013 - O Mágico de Oz (Luciane Strull) (1)</p>
                <p>2014 - Como Tudo Começou (Luciane Strull) (1)</p>
                <p>2015 - E com vocês: Romeu e Julieta (Ozani) (1)</p>
                <p>2016 - Matilda (Luciane Strull) (1)</p>
                <p>2017 - E se Fosse Verdade? (Ozani) (1)</p>
                <p>2018 - Respeitável Público (Camila Cohen) (1)</p>
                <p>2018 - Releituras em Série (Bruno Lochiavo) (2)</p>
                <p>2019 - The Point (Ozani) (1)</p>
                <p>2019 - Encerramento teatro musical (Marcelo Klabin) (1)</p>
                <p>2019 - Montagem Escola Alef Peretz (Natália Albuquerque) (1)</p>
                <p>2020 - Magical Celebrity Show (Marcelo Klabin) (1)</p>
                <p>2021 - Hairspray (Marcelo Klabin) (1)</p>
                <p>2021 - Berlin (Ivan Nóbrega) (1)</p>
                <p>2022 - O Casamento de Wandinha (Marcelo Klabin) (4)</p>
                <p>2022 - Admirável Mundo Novo (João Chanuch) (2)</p>
                <p>2023 - Mamma Mia! (Marcelo Klabin) (6)</p>
                <p>2024 - Delírios Rodriguianos (Wagner Cintra)</p>
                <p style="margin-top: 10px; font-weight: bold;">Total: Montagens: 17; Apresentações: 27</p>
            </div>

            <div style="width: 35%; display: flex; flex-direction: column; gap: 10px; align-items: center;">
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 1</div>
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 2</div>
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 3</div>
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 4</div>
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 5</div>
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 6</div>
                <div style="width: 100%; height: 120px; background: #eee; display: flex; align-items: center; justify-content: center; border: 1px solid #ccc;">Vídeo 7</div>
            </div>

            <div style="width: 25%; display: flex; flex-direction: column; gap: 10px;">
                <div style="width: 100%; height: 150px; background: #eee; border: 1px solid #ccc; display: flex; align-items: center; justify-content: center;">Galeria de Fotos</div>
            </div>
        </div>

        <div style="margin-top: 50px;">
            <h3 style="color: #0b2545; margin-bottom: 10px;">EXPERIÊNCIA INTERNACIONAL</h3>
            <p><strong>Teatro Cameri</strong></p>
            <div style="width: 200px; height: 130px; background: #eee; border: 1px solid #ccc; margin-top: 10px; display: flex; align-items: center; justify-content: center;">Foto Teatro Cameri</div>
        </div>

        <div style="margin-top: 40px;">
            <h3 style="color: #0b2545; margin-bottom: 15px;">Trabalhos feitos no Bacharelado em Artes Cênicas na UNESP:</h3>
            <div class="file-grid">
                <div class="file-card" onclick="alert('Abrindo Relatório da exposição A Costura do Sagrado')">
                    <div class="file-preview">📄 PDF</div>
                    <span>Relatório da exposição A COSTURA DO SAGRADO</span>
                </div>
                <div class="file-card" onclick="alert('Abrindo Autoavaliação - Rafael Elimelek')">
                    <div class="file-preview">📄 PDF</div>
                    <span>Autoavaliação - Rafael Elimelek</span>
                </div>
                <div class="file-card" onclick="alert('Abrindo Relato sobre as Performances')">
                    <div class="file-preview">📄 DOCX</div>
                    <span>RELATO SOBRE AS PERFORMANCES</span>
                </div>
            </div>
        </div>
    </div>


    <!-- ================= PÁGINA: JORNALISMO ================= -->
    <div id="journalism-page" class="page">
        <a class="back-btn" onclick="navigateTo('home-page')">← Voltar à Página Principal</a>
        <h2 class="subpage-title">JORNALISMO</h2>
        <h3 style="color: #0b2545; margin-bottom: 20px;">Textos</h3>

        <div class="file-grid">
            <div class="file-card" onclick="alert('Abrindo arquivo Não há neutralidade no Jornalismo Esportivo')">
                <div class="file-preview">📄 DOCX</div>
                <span>Não há neutralidade no Jornalismo Esportivo</span>
            </div>
            <div class="file-card" onclick="alert('Abrindo arquivo As mulheres no Egito e no Irã')">
                <div class="file-preview">📄 DOCX</div>
                <span>As mulheres no Egito e no Irã</span>
            </div>
            <div class="file-card" onclick="alert('Abrindo arquivo Síntese Rafael')">
                <div class="file-preview">📄 PDF</div>
                <span>Síntese Rafael</span>
            </div>
            <div class="file-card" onclick="alert('Abrindo arquivo Ensinando o Holocausto')">
                <div class="file-preview">📄 DOCX</div>
                <span>Ensinando o Holocausto nas Escolas</span>
            </div>
            <div class="file-card" onclick="alert('Abrindo arquivo Processo Seletivo Fast Company')">
                <div class="file-preview">📄 DOCX</div>
                <span>Processo Seletivo Fast Company</span>
            </div>
            <div class="file-card" onclick="alert('Abrindo arquivo Síntese Monografia 2022')">
                <div class="file-preview">📄 PDF</div>
                <span>Síntese Monografia 2022</span>
            </div>
        </div>

        <div style="margin-top: 40px;">
            <a href="https://medium.com/@rafaelelimelek" target="_blank" style="display: inline-block; background: #0b2545; color: white; padding: 10px 20px; border-radius: 4px; text-decoration: none; font-weight: bold;">
                Acessar Perfil do Medium (@rafaelelimelek)
            </a>
        </div>

        <div style="margin-top: 40px;">
            <h3 style="color: #0b2545; margin-bottom: 15px;">Fotos Adicionais</h3>
            <div style="width: 200px; height: 150px; background: #eee; border: 1px solid #ccc; display: flex; align-items: center; justify-content: center;">Espaço para Fotos</div>
        </div>
    </div>


    <!-- ================= PÁGINA: TRABALHOS VOLUNTÁRIOS ================= -->
    <div id="volunteering-page" class="page">
        <a class="back-btn" onclick="navigateTo('home-page')">← Voltar à Página Principal</a>
        <h2 class="subpage-title" style="text-align: center;">TRABALHOS VOLUNTÁRIOS E OUTRAS ATIVIDADES INTERESSANTES</h2>

        <div style="display: flex; gap: 20px; margin-top: 30px;">
            <div style="width: 25%; background: #f4f5f7; border: 1px solid #ccc; padding: 20px; border-radius: 6px; cursor: pointer; text-align: center;" onclick="alert('Abrindo Outras Atividades Interessantes e fotos')">
                <h3 style="color: #0b2545; font-size: 16px; margin-bottom: 10px;">Outras Atividades Interessantes</h3>
                <p style="font-size: 13px;">Clique para ver fotos e detalhes.</p>
            </div>

            <div style="width: 50%; background: #f4f5f7; border: 1px solid #ccc; padding: 20px; border-radius: 6px;">
                <h3 style="color: #0b2545; font-size: 16px; text-align: center; margin-bottom: 15px;">MOVIMENTO JUVENIL JUDAICO HABONIM DROR</h3>
                <p style="font-size: 13px; line-height: 1.6; text-align: justify;">
                    Em 2012 ingressei para o que se tornaria uma das maiores jornadas da minha vida, a participação ativa em um movimento juvenil judaico mundial, com uma sede localizada na cidade de São Paulo. A partir de brincadeiras e pequenas conversas, aos sábados e em acampamentos em julho e em dezembro, fui aprendendo sem perceber, sobre diversos assuntos como judaísmo, história de Israel e sociedade.<br><br>
                    Com 1 ano e meio de preparação, iniciado no começo de 2021 e terminando em julho de 2022, me tornei educador no Movimento. Assim, me tornei responsável pela educação de crianças de 6 a 14 anos. Preparei diversas atividades, que traziam assuntos difíceis de maneiras lúdicas para os chanichim (educandos). Em 2023 fui madrich em uma machané (acampamento) do Habonim Dror do Rio de Janeiro e em 2024 em Salvador.<br><br>
                    Após um ano de preparação em Israel, em 2025, e 2026 me tornei Mazkir do Habonim Dror de São Paulo, tendo como responsabilidade a centralização do movimento, dividir as funções da equipe, identificar os problemas e procurar possíveis soluções, representar o movimento para outras instituições e cuidar das relações entre educandos e educadores e pais de chanichim com madrichim.
                </p>
                <div style="margin-top: 15px; text-align: center; font-size: 12px; color: #666;">[Espaço para fotos futuras do Habonim Dror]</div>
            </div>

            <div style="width: 25%; background: #f4f5f7; border: 1px solid #ccc; padding: 20px; border-radius: 6px; cursor: pointer;" onclick="alert('Abrindo galeria de Fotos da Experiência Internacional')">
                <h3 style="color: #0b2545; font-size: 16px; text-align: center; margin-bottom: 10px;">EXPERIÊNCIA INTERNACIONAL</h3>
                <p style="font-size: 13px; line-height: 1.5; text-align: justify;">
                    <strong>Shnat Hachshará Habonim Dror AMLAT - ano de preparação em Israel</strong><br><br>
                    Em 2025, deixei minha casa em São Paulo para conhecer uma nova cultura, vivenciar na prática um país com a minha religião como predominante, morar em uma sociedade completamente diferente... (Clique para ver o texto completo e fotos).
                </p>
            </div>
        </div>
    </div>

    <!-- Script JavaScript para alternar entre as páginas -->
    <script>
        function navigateTo(pageId) {
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById(pageId).classList.add('active');
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>

