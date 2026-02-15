<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glacial Store - Produtos Digitais Premium</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">

    <style>
        :root {
            --cor-primaria: #25D366; 
            --cor-secundaria: #1e293b; 
            --cor-destaque: #0ea5e9; 
            --cor-fundo: #f8fafc; 
            --cor-texto: #334155;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--cor-fundo);
            color: var(--cor-texto);
        }

        /* Navbar Premium */
        .navbar {
            background-color: rgba(255, 255, 255, 0.95) !important;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }
        .navbar-brand {
            color: var(--cor-secundaria) !important;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        /* Hero Section (Banner) */
        .hero-section {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: white;
            padding: 120px 0 100px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        .hero-wave {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            overflow: hidden;
            line-height: 0;
            transform: rotate(180deg);
        }
        .hero-wave svg {
            position: relative;
            display: block;
            width: calc(133% + 1.3px);
            height: 76px;
        }
        .hero-wave .shape-fill {
            fill: var(--cor-fundo);
        }

        .hero-title {
            font-weight: 700;
            font-size: 2.8rem;
            margin-bottom: 20px;
        }

        /* Barra de Confiança */
        .trust-bar {
            background: white;
            padding: 30px 0;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
            position: relative;
            z-index: 10;
            margin-top: -50px; 
            border-radius: 12px;
            max-width: 900px;
            margin-left: auto;
            margin-right: auto;
        }
        .trust-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            color: var(--cor-secundaria);
        }
        .trust-icon {
            font-size: 2rem;
            color: var(--cor-destaque);
        }

        /* Cards de Produtos */
        .product-card {
            background: white;
            border: 1px solid rgba(0,0,0,0.05);
            border-radius: 16px;
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            height: 100%;
            display: flex;
            flex-direction: column;
            overflow: hidden;
        }
        .product-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
            border-color: var(--cor-destaque);
        }
        .product-card img {
            height: 220px;
            object-fit: cover;
        }
        .card-body {
            padding: 1.8rem;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }
        .card-title {
            color: var(--cor-secundaria);
            font-weight: 700;
            font-size: 1.1rem;
        }
        .price-tag {
            font-size: 1.6rem;
            font-weight: 700;
            color: var(--cor-destaque);
            margin: 15px 0;
        }

        /* Botões */
        .btn-detalhes {
            background-color: var(--cor-fundo);
            color: var(--cor-secundaria);
            border: 2px solid #e2e8f0;
            font-weight: 600;
            border-radius: 10px;
            padding: 12px;
            margin-top: auto;
            transition: all 0.3s ease;
        }
        .btn-detalhes:hover {
            background-color: var(--cor-secundaria);
            color: white;
            border-color: var(--cor-secundaria);
        }
        .btn-whatsapp {
            background-color: var(--cor-primaria);
            color: white;
            font-weight: 600;
            border: none;
            padding: 14px;
            border-radius: 10px;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }
        .btn-whatsapp:hover {
            background-color: #1da851;
            color: white;
            transform: scale(1.02);
            box-shadow: 0 10px 20px -10px rgba(37, 211, 102, 0.5);
        }

        /* Depoimentos e Formulário */
        .testimonials-section {
            background-color: white;
            padding: 80px 0;
        }
        .testimonial-card {
            background: var(--cor-fundo);
            padding: 30px;
            border-radius: 16px;
            border-bottom: 4px solid var(--cor-destaque);
            height: 100%;
        }
        .review-form-box {
            background: #f1f5f9;
            padding: 40px;
            border-radius: 20px;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.05);
        }
        .form-control, .form-select {
            border-radius: 10px;
            padding: 12px;
            border: 1px solid #cbd5e1;
        }

        /* FAQ */
        .faq-section {
            padding: 80px 0;
        }
        .accordion-item {
            border: none;
            margin-bottom: 15px;
            border-radius: 12px !important;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .accordion-button {
            font-weight: 600;
            color: var(--cor-secundaria);
            background-color: white;
            padding: 20px;
        }
        .accordion-button:not(.collapsed) {
            background-color: #f0f9ff;
            color: var(--cor-destaque);
            box-shadow: none;
        }
        .accordion-body {
            padding: 20px;
            line-height: 1.6;
        }

        /* Modal PIX Segura */
        .pix-box {
            background-color: #f8fafc;
            border: 2px dashed #cbd5e1;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 15px;
        }

        /* Footer */
        footer {
            background: var(--cor-secundaria);
            color: rgba(255,255,255,0.7);
            padding: 60px 0 30px;
        }
        .footer-link {
            color: rgba(255,255,255,0.6);
            text-decoration: none;
            transition: color 0.3s;
        }
        .footer-link:hover {
            color: var(--cor-destaque);
        }

        .floating-wpp {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background-color: var(--cor-primaria);
            color: white;
            width: 65px;
            height: 65px;
            border-radius: 50%;
            text-align: center;
            font-size: 34px;
            box-shadow: 0 8px 20px -5px rgba(37, 211, 102, 0.5);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: transform 0.3s;
        }
        .floating-wpp:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg fixed-top shadow-sm">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#">
                <i class="bi bi-hexagon-fill text-info me-2 fs-4"></i> Glacial Store
            </a>
            <button class="navbar-toggler border-0 shadow-none" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                <ul class="navbar-nav align-items-center">
                    <li class="nav-item"><a class="nav-link fw-semibold px-3" href="#produtos">Produtos</a></li>
                    <li class="nav-item"><a class="nav-link fw-semibold px-3" href="#avaliacoes">Depoimentos</a></li>
                    <li class="nav-item"><a class="nav-link fw-semibold px-3" href="#faq">Dúvidas</a></li>
                    <li class="nav-item ms-lg-3 mt-2 mt-lg-0">
                        <a href="#produtos" class="btn btn-sm btn-info text-white fw-bold px-3 rounded-pill">Comprar Agora</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <section class="hero-section">
        <div class="container position-relative z-2">
            <span class="badge bg-info bg-opacity-25 text-info border border-info mb-4 px-3 py-2 rounded-pill fw-bold ls-1">
                <i class="bi bi-award me-1"></i> GARANTIA DE SATISFAÇÃO
            </span>
            <h1 class="hero-title display-4">Acelere seus Resultados<br>no Mundo Digital</h1>
            <p class="lead fs-5 mb-5 opacity-75 mx-auto" style="max-width: 700px;">Conhecimento prático, materiais editáveis e serviços diretos ao ponto. Pagamento seguro e entrega imediata via WhatsApp.</p>
            <a href="#produtos" class="btn btn-info text-white fw-bold btn-lg px-5 shadow-lg py-3" style="border-radius: 50px; letter-spacing: 0.5px;">
                EXPLORAR CATÁLOGO <i class="bi bi-arrow-right ms-2"></i>
            </a>
        </div>
        <div class="hero-wave">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="shape-fill"></path>
            </svg>
        </div>
    </section>

    <div class="container relative">
        <section class="trust-bar rounded-4 border">
            <div class="row g-4 text-center">
                <div class="col-md-4 trust-item border-end-md">
                    <div class="p-3 bg-info bg-opacity-10 rounded-circle">
                         <i class="bi bi-shield-check trust-icon text-info"></i>
                    </div>
                    <div class="text-start">
                        <h6 class="fw-bold mb-0">Compra 100% Segura</h6>
                        <small class="text-muted">Transação protegida via PIX</small>
                    </div>
                </div>
                <div class="col-md-4 trust-item border-end-md">
                     <div class="p-3 bg-info bg-opacity-10 rounded-circle">
                        <i class="bi bi-lightning-charge trust-icon text-info"></i>
                    </div>
                    <div class="text-start">
                        <h6 class="fw-bold mb-0">Entrega Imediata</h6>
                        <small class="text-muted">Receba o acesso na hora</small>
                    </div>
                </div>
                <div class="col-md-4 trust-item">
                     <div class="p-3 bg-info bg-opacity-10 rounded-circle">
                        <i class="bi bi-chat-heart trust-icon text-info"></i>
                    </div>
                    <div class="text-start">
                        <h6 class="fw-bold mb-0">Suporte Humano</h6>
                        <small class="text-muted">Atendimento direto pelo Whats</small>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <section id="produtos" class="container py-5 mt-5">
        <div class="text-center mb-5">
            <h6 class="text-info fw-bold text-uppercase ls-1">Nosso Catálogo</h6>
            <h2 class="fw-bold display-6" style="color: var(--cor-secundaria);">Produtos e Serviços em Destaque</h2>
            <p class="text-muted mx-auto" style="max-width: 600px;">Selecione o item desejado para ver todos os detalhes, a garantia e as formas de pagamento.</p>
        </div>
        
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-4 g-4 justify-content-center">
            
            <div class="col">
                <div class="product-card h-100">
                    <img src="https://images.unsplash.com/photo-1579621970563-ebec7560ff3e?auto=format&fit=crop&w=500&q=80" alt="E-book Finanças" alt="E-book Finanças">
                    <div class="card-body">
                        <div class="d-flex align-items-center mb-2">
                            <div class="text-warning small">
                                <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-half"></i>
                            </div>
                            <span class="ms-2 text-muted fw-semibold small">4.9 (142 Vendas)</span>
                        </div>
                        <h5 class="card-title">Para Onde Está Indo Meu Dinheiro?
                        (E-book de finanças)</h5>
                        <p class="price-tag">R$ 26,90 <span class="text-muted text-decoration-line-through fs-6 fw-normal ms-2">R$ 49,90</span></p>
                        
                        <button class="btn btn-detalhes w-100" 
                            onclick="abrirModal(
                                'E-book: Para onde está indo meu dinheiro?', 
                                'R$ 26,90', 
                                'Guia prático e definitivo para organizar as suas finanças. Descubra os gastos invisíveis, monte um orçamento realista e faça o dinheiro sobrar no final do mês.' ,
'https://images.unsplash.com/photo-1579621970563-ebec7560ff3e?auto=format&fit=crop&w=500&q=80'
                            )">
                             <i class="bi bi-eye me-2"></i>Ver Detalhes
                        </button>
                    </div>
                </div>
            </div>

            <div class="col">
                <div class="product-card h-100">
                    <img src="https://images.unsplash.com/photo-1461749280684-dccba630e2f6?auto=format&fit=crop&w=500&q=80" alt="Criação de Sites">
                    <div class="card-body">
                        <div class="d-flex align-items-center mb-2">
                             <div class="text-warning small">
                                <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i>
                            </div>
                             <span class="ms-2 text-muted fw-semibold small">5.0 (58 Vendas)</span>
                        </div>
                        <h5 class="card-title">Criação de Site Simples e Clean</h5>
                        <p class="price-tag">R$ 50,00</p>
                        <button class="btn btn-detalhes w-100" 
                            onclick="abrirModal(
                                'Serviço: Site Simples e Clean', 
                                'R$ 50,00', 
                                'Tenha a sua própria página de vendas na internet! Crio um site moderno, bonito e responsivo (funciona perfeitamente no celular), totalmente focado em atrair clientes direto para o seu WhatsApp.', 
                                'https://images.unsplash.com/photo-1461749280684-dccba630e2f6?auto=format&fit=crop&w=500&q=80'
                            )">
                             <i class="bi bi-eye me-2"></i>Ver Detalhes
                        </button>
                    </div>
                </div>
            </div>

            <div class="col">
                <div class="product-card h-100">
                    <img src="https://images.unsplash.com/photo-1611162617474-5b21e879e113?auto=format&fit=crop&w=500&q=80" alt="Pack Templates">
                    <div class="card-body">
                         <div class="d-flex align-items-center mb-2">
                             <div class="text-warning small">
                                <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-half"></i>
                            </div>
                             <span class="ms-2 text-muted fw-semibold small">4.8 (115 Vendas)</span>
                        </div>
                        <h5 class="card-title">Pack 50 Templates Canva Premium</h5>
                        <p class="price-tag">R$ 15,00</p>
                        <button class="btn btn-detalhes w-100" 
                            onclick="abrirModal(
                                'Pack 50 Templates Premium Canva', 
                                'R$ 15,00', 
                                'Profissionalize o seu Instagram em minutos! Você recebe 50 artes 100% editáveis no Canva (na versão gratuita) para feed e stories. Acesso vitalício.', 
                                'https://images.unsplash.com/photo-1611162617474-5b21e879e113?auto=format&fit=crop&w=500&q=80'
                            )">
                             <i class="bi bi-eye me-2"></i>Ver Detalhes
                        </button>
                    </div>
                </div>
            </div>

            <div class="col">
                <div class="product-card h-100">
                    <img src="https://images.unsplash.com/photo-1434030216411-0b793f4b4173?auto=format&fit=crop&w=500&q=80" alt="Curso Produtividade">
                    <div class="card-body">
                         <div class="d-flex align-items-center mb-2">
                             <div class="text-warning small">
                                <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-half"></i>
                            </div>
                             <span class="ms-2 text-muted fw-semibold small">4.9 (89 Vendas)</span>
                        </div>
                        <h5 class="card-title">Mini-curso: Produtividade Digital</h5>
                        <p class="price-tag">R$ 22,99</p>
                        <button class="btn btn-detalhes w-100" 
                            onclick="abrirModal(
                                'Mini-curso: Produtividade Digital', 
                                'R$ 22,99', 
                                'São 3 aulas práticas em vídeo direto ao ponto. Aprenda a organizar a sua rotina digital e produzir mais em menos tempo usando apenas ferramentas gratuitas do Google.', 
                                'https://images.unsplash.com/photo-1434030216411-0b793f4b4173?auto=format&fit=crop&w=500&q=80'
                            )">
                             <i class="bi bi-eye me-2"></i>Ver Detalhes
                        </button>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <section id="avaliacoes" class="testimonials-section mt-5">
        <div class="container">
            <div class="text-center mb-5">
                <h6 class="text-info fw-bold text-uppercase ls-1">Prova Social</h6>
                <h2 class="fw-bold" style="color: var(--cor-secundaria);">O que dizem nossos clientes</h2>
            </div>
            <div class="row g-4 mb-5">
                <div class="col-md-4">
                    <div class="testimonial-card shadow-sm">
                        <div class="d-flex text-warning mb-3">
                            <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i>
                        </div>
                        <p class="fst-italic text-muted mb-4"> Gente, confesso que fiquei com um pé atrás de comprar por PIX direto no zap, mas arrisquei. Melhor coisa que fiz! O e-book abriu muito minha mente, consegui achar onde meu dinheiro tava sumindo kkk. Recebi o pdf na mesma hora que mandei o comprovante 🙏</p>
                        <div class="d-flex align-items-center">
                            <div class="bg-info text-white rounded-circle d-flex align-items-center justify-content-center fw-bold me-3" style="width: 45px; height: 45px;">MS</div>
                            <div>
                                <h6 class="fw-bold mb-0">Mariana Silva</h6>
                                <small class="text-muted">Comprou E-book Finanças</small>
                            </div>
                        </div>
                    </div>
                </div>
                 <div class="col-md-4">
                    <div class="testimonial-card shadow-sm">
                        <div class="d-flex text-warning mb-3">
                            <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i>
                        </div>
                        <p class="fst-italic text-muted mb-4"> Trabalho impecável! Precisava de um site simples pra minha lojinha e entregaram super rápido. Ficou muito profissional e o pessoal já tá elogiando bastante. O atendimento tira todas as dúvidas, recomendo de olhos fechados.</p>
                        <div class="d-flex align-items-center">
                            <div class="bg-primary text-white rounded-circle d-flex align-items-center justify-content-center fw-bold me-3" style="width: 45px; height: 45px;">RB</div>
                            <div>
                                <h6 class="fw-bold mb-0">Roberto</h6>
                                <small class="text-muted">Comprou Criação de Site</small>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="testimonial-card shadow-sm">
                        <div class="d-flex text-warning mb-3">
                            <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-half"></i>
                        </div>
                        <p class="fst-italic text-muted mb-4"> Comprei o pack de templates do canva pq eu não sabia nada de design kkkk. Salvou demais o meu tempo, os posts ficam lindos em dois palitos. Valeu cada centavo, muito fácil de editar.</p>
                        <div class="d-flex align-items-center">
                            <div class="bg-success text-white rounded-circle d-flex align-items-center justify-content-center fw-bold me-3" style="width: 45px; height: 45px;">AF</div>
                            <div>
                                <h6 class="fw-bold mb-0">Aline F.</h6>
                                <small class="text-muted">Comprou Pack Templates</small>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="row justify-content-center mt-5 pt-4">
                <div class="col-lg-8">
                    <div class="review-form-box text-center">
                        <h3 class="fw-bold mb-3" style="color: var(--cor-secundaria);">Já é cliente? Deixe sua avaliação!</h3>
                        <p class="text-muted mb-4">Sua opinião é muito importante. Preencha abaixo e envie para nossa equipe.</p>
                        
                        <div class="row g-3">
                            <div class="col-md-6">
                                <input type="text" id="nomeAvaliacao" class="form-control" placeholder="Seu Nome/Apelido">
                            </div>
                             <div class="col-md-6">
                                <select id="notaAvaliacao" class="form-select">
                                    <option value="5" selected>⭐⭐⭐⭐⭐ Excelente</option>
                                    <option value="4">⭐⭐⭐⭐ Muito Bom</option>
                                    <option value="3">⭐⭐⭐ Bom</option>
                                    <option value="2">⭐⭐ Razoável</option>
                                    <option value="1">⭐ Ruim</option>
                                </select>
                            </div>
                            <div class="col-12">
                                <textarea id="textoAvaliacao" class="form-control" rows="4" placeholder="Escreva aqui de forma sincera o que achou da sua compra..."></textarea>
                            </div>
                            <div class="col-12 mt-4">
                                <button class="btn btn-info text-white fw-bold btn-lg w-100 px-5" onclick="enviarAvaliacaoWpp()">
                                    <i class="bi bi-send me-2"></i>Enviar Minha Avaliação
                                </button>
                                <small class="text-muted d-block mt-2">Você será redirecionado para o WhatsApp para confirmar o envio.</small>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="faq" class="faq-section bg-white">
        <div class="container">
            <div class="text-center mb-5">
                <h6 class="text-info fw-bold text-uppercase ls-1">Tire suas Dúvidas</h6>
                <h2 class="fw-bold" style="color: var(--cor-secundaria);">Perguntas Frequentes</h2>
            </div>
            <div class="row justify-content-center">
                <div class="col-lg-8">
                    <div class="accordion shadow-sm border-0" id="accordionFAQ">
                        <div class="accordion-item mb-3 border">
                            <h2 class="accordion-header">
                                <button class="accordion-button fw-semibold" type="button" data-bs-toggle="collapse" data-bs-target="#faq1">
                                    <i class="bi bi-shield-check text-info me-2 fs-5"></i> É seguro comprar aqui? Não é golpe?
                                </button>
                            </h2>
                            <div id="faq1" class="accordion-collapse collapse show" data-bs-parent="#accordionFAQ">
                                <div class="accordion-body text-muted">
                                    Sim, é 100% seguro! Nossa loja preza pela transparência. O pagamento é feito via PIX direto para a conta oficial e todo o envio é tratado por atendimento humano no WhatsApp. Você fala com pessoas reais, não robôs.
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item mb-3 border">
                            <h2 class="accordion-header">
                                <button class="accordion-button collapsed fw-semibold" type="button" data-bs-toggle="collapse" data-bs-target="#faq2">
                                    <i class="bi bi-box-seam text-info me-2 fs-5"></i> Como e quando recebo o meu produto?
                                </button>
                            </h2>
                            <div id="faq2" class="accordion-collapse collapse" data-bs-parent="#accordionFAQ">
                                <div class="accordion-body text-muted">
                                    A entrega é imediata após a confirmação! Assim que você enviar o comprovante do PIX no nosso WhatsApp, nossa equipe envia o link de acesso ou arquivo PDF na mesma hora, na própria conversa.
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="modal fade" id="modalProduto" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content border-0 shadow-lg" style="border-radius: 20px; overflow: hidden;">
                <div class="modal-header border-0 pb-0 pt-4 px-4">
                    <h5 class="modal-title fw-bold fs-4" id="modalNome" style="color: var(--cor-secundaria);">Nome do Produto</h5>
                    <button type="button" class="btn-close bg-light p-2 rounded-circle" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                
                <div class="modal-body text-center pt-3 px-4">
                    <img id="modalImg" src="" alt="Imagem" class="img-fluid mb-4 shadow-sm rounded-4" style="width: 100%; max-height: 240px; object-fit: cover;">
                    
                    <h2 id="modalPreco" class="fw-bold mb-3 display-6 text-info">R$ 0,00</h2>
                    
                    <p id="modalDesc" class="text-muted text-start mb-4" style="font-size: 1rem; line-height: 1.7;"></p>
                    
                    <div class="d-flex align-items-center justify-content-center bg-success bg-opacity-10 rounded-3 p-3 mb-4 border border-success border-opacity-25">
                        <i class="bi bi-shield-lock-fill text-success fs-3 me-3"></i>
                        <div class="text-start">
                            <h6 class="fw-bold text-success mb-0">Compra Garantida</h6>
                            <small class="text-success text-opacity-75 fw-semibold">Receba o produto de imediato no WhatsApp.</small>
                        </div>
                    </div>

                    <div class="pix-box bg-white border shadow-sm">
                        <p class="mb-2 text-dark fw-bold d-flex align-items-center justify-content-center">
                            <i class="bi bi-qr-code me-2 text-info fs-5"></i> Dados para Pagamento via PIX
                        </p>
                        <p class="small text-muted mb-1">Chave E-mail Oficial:</p>
                        <div class="d-flex align-items-center justify-content-between bg-light p-3 rounded-3 border mb-3">
                            <p class="fw-bold fs-5 mb-0 user-select-all text-break me-2" id="chavePix" style="color: var(--cor-secundaria);">aglorentin97@gmail.com</p>
                            <button class="btn btn-white border shadow-sm text-info fw-bold p-2 rounded-3" id="btnCopiarIcon" onclick="copiarChavePix()" title="Copiar">
                                <i class="bi bi-files fs-5"></i>
                            </button>
                        </div>
                        
                        <button class="btn btn-dark w-100 fw-bold py-3 rounded-3" id="btnCopiar" onclick="copiarChavePix()">
                            <i class="bi bi-copy me-2"></i>CLIQUE PARA COPIAR A CHAVE
                        </button>
                    </div>
                </div>

                <div class="modal-footer border-0 pt-0 pb-4 flex-column px-4 bg-light">
                    <div class="w-100 text-center mb-3">
                        <span class="badge bg-warning text-dark mb-2">Passo 2</span>
                        <p class="small text-muted fw-bold mb-0">Já fez o PIX? Envie o comprovante agora:</p>
                    </div>
                    <button type="button" class="btn btn-whatsapp w-100 shadow fw-bold py-3 rounded-3" id="btnComprarConfirmado">
                        <i class="bi bi-whatsapp me-2 fs-5"></i>ENVIAR COMPROVANTE
                    </button>
                </div>
            </div>
        </div>
    </div>

    <footer class="pt-5 pb-3">
        <div class="container">
            <div class="row gy-4 mb-5">
                <div class="col-lg-4 col-md-6">
                    <h4 class="fw-bold text-white mb-3 d-flex align-items-center">
                        <i class="bi bi-hexagon-fill text-info me-2"></i>Glacial Store
                    </h4>
                    <p class="small opacity-75 mb-4">Nossa missão é fornecer materiais digitais e serviços de alta qualidade que geram resultados reais para nossos clientes, com atendimento rápido e transparente.</p>
                </div>
                <div class="col-lg-2 col-md-6 offset-lg-1">
                    <h5 class="text-white fw-bold mb-3">Links Rápidos</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#produtos" class="footer-link small">Catálogo</a></li>
                        <li class="mb-2"><a href="#avaliacoes" class="footer-link small">Depoimentos</a></li>
                        <li class="mb-2"><a href="#faq" class="footer-link small"></a></li>
                    </ul>
                </div>
                <div class="col-lg-3 col-md-6 offset-lg-2">
                    <h5 class="text-white fw-bold mb-3">Contato</h5>
                    <ul class="list-unstyled small opacity-75">
                        <li class="mb-3 d-flex"><i class="bi bi-whatsapp me-2 text-info"></i> (21) 96982-2509</li>
                        <li class="mb-3 d-flex"><i class="bi bi-envelope me-2 text-info"></i> aglorentin97@gmail.com</li>
                    </ul>
                </div>
            </div>
            <hr class="border-secondary opacity-25">
            <div class="row align-items-center mt-3">
                <div class="col-md-6 text-center text-md-start">
                     <p class="small opacity-50 mb-0">© 2026 Glacial Store. Todos os direitos reservados.</p>
                </div>
            </div>
        </div>
    </footer>

    <a href="https://wa.me/5521969822509?text=Olá! Estava navegando no site da Glacial Store e tenho uma dúvida." class="floating-wpp shadow-lg" target="_blank">
        <i class="bi bi-whatsapp"></i>
    </a>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        const SEU_NUMERO_WHATSAPP = "5521969822509"; 
        
        let produtoSelecionado = "";
        let precoSelecionado = "";

        const modalElemento = document.getElementById('modalProduto');
        const modalBootstrap = new bootstrap.Modal(modalElemento);

        function abrirModal(nome, preco, descricao, imagem) {
            document.getElementById('modalNome').innerText = nome;
            document.getElementById('modalPreco').innerText = preco;
            document.getElementById('modalDesc').innerText = descricao;
            document.getElementById('modalImg').src = imagem;
            
            produtoSelecionado = nome;
            precoSelecionado = preco;

            resetarBotaoCopiar();
            modalBootstrap.show();
        }

        function resetarBotaoCopiar() {
            const btnCopiar = document.getElementById('btnCopiar');
            const btnCopiarIcon = document.getElementById('btnCopiarIcon');
            btnCopiar.innerHTML = '<i class="bi bi-copy me-2"></i> CLIQUE PARA COPIAR A CHAVE';
            btnCopiar.classList.remove('btn-success');
            btnCopiar.classList.add('btn-dark');
            btnCopiarIcon.innerHTML = '<i class="bi bi-files fs-5"></i>';
            btnCopiarIcon.classList.remove('text-success', 'bg-success', 'bg-opacity-10');
             btnCopiarIcon.classList.add('text-info', 'btn-white');
        }

        function copiarChavePix() {
            const chave = document.getElementById('chavePix').innerText;
            
            navigator.clipboard.writeText(chave).then(() => {
                const btnCopiar = document.getElementById('btnCopiar');
                const btnCopiarIcon = document.getElementById('btnCopiarIcon');
                
                btnCopiar.innerHTML = '<i class="bi bi-check2-circle me-2"></i> CHAVE COPIADA COM SUCESSO!';
                btnCopiar.classList.remove('btn-dark');
                btnCopiar.classList.add('btn-success');
                
                btnCopiarIcon.innerHTML = '<i class="bi bi-check-lg fs-5"></i>';
                 btnCopiarIcon.classList.remove('text-info', 'btn-white');
                btnCopiarIcon.classList.add('text-success', 'bg-success', 'bg-opacity-10');

                setTimeout(resetarBotaoCopiar, 3000); 
            }).catch(err => {
                alert("Não foi possível copiar automaticamente. Por favor, selecione e copie o e-mail manualmente.");
            });
        }

        document.getElementById('btnComprarConfirmado').addEventListener('click', function() {
            const mensagem = `Olá! Vi os detalhes do *${produtoSelecionado}* (${precoSelecionado}) na Glacial Store. Já copiei a chave PIX e fiz o pagamento. Segue o meu comprovante para liberação do acesso:`;
            
            const mensagemCodificada = encodeURIComponent(mensagem);
            const linkWhatsapp = `https://wa.me/${SEU_NUMERO_WHATSAPP}?text=${mensagemCodificada}`;

            window.open(linkWhatsapp, '_blank');
            modalBootstrap.hide();
        });

        function enviarAvaliacaoWpp() {
            const nome = document.getElementById('nomeAvaliacao').value;
            const notaSelect = document.getElementById('notaAvaliacao');
            const notaTexto = notaSelect.options[notaSelect.selectedIndex].text;
            const texto = document.getElementById('textoAvaliacao').value;

            if (!nome || !texto) {
                alert("Por favor, preencha seu nome e sua avaliação antes de enviar.");
                return;
            }

            const mensagemAvaliacao = `Olá, equipe Glacial Store! Gostaria de deixar minha avaliação:\n\n*Nome:* ${nome}\n*Nota:* ${notaTexto}\n*Depoimento:* "${texto}"\n\nAutorizo o uso no site.`;
            
            const mensagemCodificada = encodeURIComponent(mensagemAvaliacao);
            const linkWhatsapp = `https://wa.me/${SEU_NUMERO_WHATSAPP}?text=${mensagemCodificada}`;

            window.open(linkWhatsapp, '_blank');
            document.getElementById('nomeAvaliacao').value = '';
            document.getElementById('textoAvaliacao').value = '';
        }
    </script>
</body>
</html>
