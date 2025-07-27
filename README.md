<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DocWrite - Services de Rédaction & Mise en Forme</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0056b3;
            --secondary: #ffd700;
            --accent: #e63946;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #28a745;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), #003d82);
            color: white;
            padding: 15px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
            text-decoration: none;
        }
        
        .logo-img {
            width: 60px;
            height: 60px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .logo-img .logo-inner {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--secondary);
            font-weight: bold;
            font-size: 1.4rem;
            border: 2px solid var(--secondary);
        }
        
        .logo-text {
            display: flex;
            flex-direction: column;
        }
        
        .logo-text h1 {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
        }
        
        .logo-text p {
            font-size: 0.9rem;
            opacity: 0.95;
            color: #f0f0f0;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 12px;
            border-radius: 4px;
            transition: var(--transition);
        }
        
        nav a:hover {
            background: rgba(255, 255, 255, 0.15);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 100px 0;
            margin-bottom: 60px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 2.8rem;

margin-bottom: 20px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: var(--dark);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: 2px solid var(--secondary);
        }
        
        .btn:hover {
            background: transparent;
            color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }
        
        .btn-outline {
            background: transparent;
            color: var(--secondary);
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background: var(--secondary);
            color: var(--dark);
        }
        
        /* Security Badge */
        .security-badge {
            display: inline-block;
            background: var(--success);
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            margin-top: 20px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(40, 167, 69, 0.7); }
            70% { box-shadow: 0 0 0 10px rgba(40, 167, 69, 0); }
            100% { box-shadow: 0 0 0 0 rgba(40, 167, 69, 0); }
        }
        
        /* Services Section */
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 80px;
        }
        
        .service-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: var(--transition);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .service-card::after {
            content: "Voir détails";
            position: absolute;
            bottom: -40px;
            left: 0;
            right: 0;
            background: var(--secondary);
            color: var(--dark);
            text-align: center;
            padding: 10px;
            font-weight: 600;
            transition: var(--transition);
        }
        
        .service-card:hover::after {
            bottom: 0;
        }
        
        .service-icon {
            background: var(--primary);
            color: white;
            font-size: 2.5rem;
            padding: 30px;
            text-align: center;
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            color: var(--primary);
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .service-content p {
            color: #666;
            margin-bottom: 20px;
        }
        
        /* Styles pour les pages de service */
        .service-detail-container {

max-width: 1200px;
            margin: 50px auto;
            padding: 0 20px;
            display: none; /* Caché par défaut */
        }
        
        .service-detail-header {
            background: linear-gradient(135deg, var(--primary), #003d82);
            color: white;
            padding: 40px 0;
            border-radius: 0 0 30px 30px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .service-detail-header h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            position: relative;
        }
        
        .service-detail-header p {
            max-width: 700px;
            margin: 0 auto;
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .back-to-services {
            position: absolute;
            top: 20px;
            left: 20px;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .back-to-services:hover {
            color: var(--secondary);
            transform: translateX(-5px);
        }
        
        .service-detail-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-top: 50px;
        }
        
        .service-visuals {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        
        .service-visual {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            transition: var(--transition);
            height: 200px;
            background-color: #f0f0f0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-weight: bold;
            font-size: 1.2rem;
            background-size: cover;
            background-position: center;
            position: relative;
        }
        
        .visual-overlay {
            background: rgba(0, 86, 179, 0.7);
            color: white;
            padding: 10px;
            text-align: center;
            width: 100%;
            position: absolute;
            bottom: 0;
            font-weight: 600;
        }
        
        .service-visual:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .service-visual.large {
            grid-column: span 2;
            height: 250px;
        }
        
        .service-info {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }
        
        .service-info h2 {
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--secondary);
        }
        
        .benefits-list {
            margin: 25px 0;
        }
        
        .benefits-list li {
            margin-bottom: 15px;
            padding-left: 30px;
            position: relative;
            list-style: none;
        }
        
        .benefits-list li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--success);
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin: 25px 0;
        }
        
        .feature-card {
            background: rgba(0, 86, 179, 0.05);
            border-radius: 8px;
            padding: 15px;
            transition: var(--transition);
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .feature-card i {

color: var(--primary);
            font-size: 1.8rem;
            margin-bottom: 10px;
        }
        
        .use-cases {
            background: #f8f9fa;
            border-left: 4px solid var(--secondary);
            padding: 20px;
            margin: 25px 0;
            border-radius: 0 8px 8px 0;
        }
        
        .use-cases li {
            margin-bottom: 10px;
            position: relative;
            padding-left: 25px;
        }
        
        .use-cases li:before {
            content: "•";
            color: var(--primary);
            font-weight: bold;
            position: absolute;
            left: 10px;
        }
        
        .testimonial {
            background: white;
            border-radius: 8px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin: 30px 0;
            position: relative;
        }
        
        .testimonial:before {
            content: """;
            position: absolute;
            top: -20px;
            left: 20px;
            font-size: 5rem;
            color: rgba(0, 86, 179, 0.1);
            font-family: Georgia, serif;
        }
        
        .testimonial blockquote {
            font-style: italic;
            margin-bottom: 15px;
            position: relative;
            z-index: 1;
        }
        
        .testimonial cite {
            font-weight: 600;
            font-style: normal;
            color: var(--primary);
        }
        
        .service-cta {
            background: linear-gradient(135deg, var(--primary), #003d82);
            color: white;
            padding: 40px;
            border-radius: 15px;
            margin-top: 50px;
            text-align: center;
        }
        
        .service-cta h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }
        
        /* Animation pour le changement de page */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .service-detail-container.active {
            display: block;
            animation: fadeIn 0.5s ease forwards;
        }
        
        /* Pricing Section */
        .pricing {
            background: var(--light);
            padding: 80px 0;
        }
        
        .pricing-table {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            max-width: 1000px;
            margin: 0 auto;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        thead {
            background: var(--primary);
            color: white;
        }
        
        th, td {
            padding: 15px 20px;
            text-align: left;
        }
        
        th {
            font-weight: 600;
        }
        
        tbody tr:nth-child(even) {
            background: rgba(0, 86, 179, 0.05);
        }
        
        tbody tr:hover {
            background: rgba(0, 86, 179, 0.1);
        }
        
        .price-tag {
            font-weight: 700;
            color: var(--primary);
        }
        
        /* Payment Section */
        .payment-section {
            padding: 80px 0;
        }
        
        .payment-methods {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 30px;
        }
        
        .payment-card {
            background: white;
            border-radius: 10px;
            padding: 25px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            width: 200px;
        }
        
        .payment-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .payment-card p {
            font-weight: 600;
            color: var(--dark);
        }
        
        /* Security Section */

.security-section {
            background: linear-gradient(135deg, #2c3e50, #4a6491);
            color: white;
            padding: 80px 0;
            text-align: center;
        }
        
        .security-features {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin-top: 50px;
        }
        
        .security-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 30px;
            width: 250px;
            transition: var(--transition);
        }
        
        .security-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.15);
        }
        
        .security-icon {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        .security-card h3 {
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .security-card p {
            font-size: 0.95rem;
            opacity: 0.9;
        }
        
        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, var(--primary), #003d82);
            color: white;
            padding: 80px 0;
            text-align: center;
        }
        
        .contact-title {
            margin-bottom: 40px;
        }
        
        .contact-title h2 {
            font-size: 2.2rem;
            margin-bottom: 15px;
        }
        
        .contact-methods {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin-top: 30px;
        }
        
        .contact-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 30px;
            width: 280px;
            transition: var(--transition);
        }
        
        .contact-card:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-5px);
        }
        
        .contact-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .contact-card h3 {
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .contact-card a {
            color: white;
            text-decoration: none;
            display: block;
            margin-top: 10px;
            transition: var(--transition);
        }
        
        .contact-card a:hover {
            color: var(--secondary);
            text-decoration: underline;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 30px 0;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }
        
        .footer-logo {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .footer-logo .logo-img {
            width: 50px;
            height: 50px;
        }
        
        .footer-logo .logo-img .logo-inner {
            width: 42px;
            height: 42px;
            font-size: 1.2rem;
        }
        
        .footer-logo h2 {
            color: white;
            font-size: 1.5rem;
        }
        
        .social-icons {
            display: flex;
            gap: 20px;
            margin-top: 15px;
        }
        
 