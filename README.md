<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Чашка дня · кофе, чай, матча</title>
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300..700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /*==========БАЗОВЫЕ СТИЛИ, ЗЕЛЕНАЯ ГАММА==========*/
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eaf4e4;
            color: #1a3b2e;
            line-height: 1.5;
            font-family: 'Inter', sans-serif;
        }

        h1, h2, h3, h4, .logo h1, .hero-text h2, .section-title {
            font-family: 'Playfair Display', serif;
            font-weight: 600;
            letter-spacing: -0.02em;
            color: #0f3b1f;
        }
        /*==========ЛЕТЯЩИЕ ЧАШЕЧКИ (без отдельного пара, чуть ярче)==========*/
        .floating-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            overflow: hidden;
        }

        .float-item {
            position: absolute;
            color: rgba(60, 100, 60, 0.2); /* стало ярче (было 0.1) */
            font-size: 3.5rem;
            animation: floatUp 22s linear infinite;
            bottom: -15%;
            transform: rotate(0deg);
            filter: blur(1px);
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }

            10% {
                opacity: 0.35;
            }
            /* чуть выше */
            85% {
                opacity: 0.25;
            }

            100% {
                transform: translateY(-130vh) rotate(360deg);
                opacity: 0;
            }
        }
        /* разные размеры, углы и задержки */
        .float-item:nth-child(1) {
            left: 2%;
            animation-delay: 0s;
            transform: rotate(-15deg);
            font-size: 3rem;
        }

        .float-item:nth-child(2) {
            left: 18%;
            animation-delay: 2.5s;
            transform: rotate(10deg);
            font-size: 4rem;
        }

        .float-item:nth-child(3) {
            left: 32%;
            animation-delay: 1.2s;
            transform: rotate(-5deg);
            font-size: 3.2rem;
        }

        .float-item:nth-child(4) {
            left: 47%;
            animation-delay: 3.8s;
            transform: rotate(20deg);
            font-size: 4.2rem;
        }

        .float-item:nth-child(5) {
            left: 62%;
            animation-delay: 5s;
            transform: rotate(-20deg);
            font-size: 3.8rem;
        }

        .float-item:nth-child(6) {
            left: 78%;
            animation-delay: 4s;
            transform: rotate(15deg);
            font-size: 3rem;
        }

        .float-item:nth-child(7) {
            left: 90%;
            animation-delay: 6.5s;
            transform: rotate(-10deg);
            font-size: 4rem;
        }

        .float-item:nth-child(8) {
            left: 10%;
            animation-delay: 7s;
            transform: rotate(25deg);
            font-size: 3.3rem;
        }

        .float-item:nth-child(9) {
            left: 45%;
            animation-delay: 8s;
            transform: rotate(-25deg);
            font-size: 4.5rem;
        }

        .float-item:nth-child(10) {
            left: 70%;
            animation-delay: 9s;
            transform: rotate(5deg);
            font-size: 3.6rem;
        }

        .float-item:nth-child(11) {
            left: 25%;
            animation-delay: 10s;
            transform: rotate(-12deg);
            font-size: 3.2rem;
        }

        .float-item:nth-child(12) {
            left: 55%;
            animation-delay: 11s;
            transform: rotate(18deg);
            font-size: 4.1rem;
        }

        .float-item:nth-child(13) {
            left: 82%;
            animation-delay: 12s;
            transform: rotate(-8deg);
            font-size: 3.7rem;
        }

        .float-item:nth-child(14) {
            left: 38%;
            animation-delay: 13s;
            transform: rotate(22deg);
            font-size: 4.3rem;
        }

        .float-item:nth-child(15) {
            left: 93%;
            animation-delay: 14s;
            transform: rotate(-18deg);
            font-size: 3.9rem;
        }

        .float-item:nth-child(16) {
            left: 5%;
            animation-delay: 15s;
            transform: rotate(30deg);
            font-size: 3.4rem;
        }

        .float-item:nth-child(17) {
            left: 68%;
            animation-delay: 16s;
            transform: rotate(-30deg);
            font-size: 4.0rem;
        }

        .float-item:nth-child(18) {
            left: 15%;
            animation-delay: 17s;
            transform: rotate(12deg);
            font-size: 3.5rem;
        }

        .float-item:nth-child(19) {
            left: 88%;
            animation-delay: 18s;
            transform: rotate(-22deg);
            font-size: 4.2rem;
        }

        .float-item:nth-child(20) {
            left: 42%;
            animation-delay: 19s;
            transform: rotate(35deg);
            font-size: 3.8rem;
        }

        .site-wrapper {
            position: relative;
            z-index: 30;
            max-width: 1350px;
            margin: 0 auto;
            padding: 20px 30px 40px;
        }

        /*==========ШАПКА==========*/
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(255, 255, 255, 0.9);
            padding: 14px 32px;
            border-radius: 80px;
            border: 1px solid #a8d0a8;
            backdrop-filter: blur(8px);
            margin-bottom: 35px;
            flex-wrap: wrap;
            box-shadow: 0 10px 30px rgba(30, 70, 30, 0.1);
        }

        .logo {
            cursor: pointer;
        }

            .logo h1 {
                font-size: 2.2rem;
                color: #1e562e;
            }

            .logo span {
                color: #5d8c5d;
                font-size: 1.1rem;
                margin-left: 8px;
                font-family: 'Inter', sans-serif;
                font-weight: 400;
            }

        .right-actions {
            display: flex;
            align-items: center;
            gap: 25px;
            flex-wrap: wrap;
        }

        .nav-menu {
            display: flex;
            gap: 8px;
            background: #d5e8d5;
            padding: 6px 14px;
            border-radius: 60px;
        }

        .nav-btn {
            background: transparent;
            border: none;
            padding: 8px 20px;
            font-weight: 500;
            color: #1b4a1b;
            border-radius: 40px;
            cursor: pointer;
            transition: 0.2s;
            font-size: 1rem;
        }

            .nav-btn.active {
                background: #2f6b2f;
                color: white;
            }

            .nav-btn:hover {
                background: #c0ddc0;
            }

            .nav-btn.active:hover {
                background: #235623;
            }

        .cart-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .cart-icon {
            font-size: 1.9rem;
            color: #2f6b2f;
            cursor: pointer;
            position: relative;
        }

        #cart-count {
            background: #2f6b2f;
            color: white;
            border-radius: 50px;
            padding: 2px 12px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-left: 6px;
        }

        .open-cart-btn {
            background: #d5e8d5;
            border: 1px solid #9ac09a;
            padding: 10px 22px;
            border-radius: 60px;
            font-weight: 600;
            color: #1b4a1b;
            cursor: pointer;
            transition: 0.2s;
        }

            .open-cart-btn:hover {
                background: #c0ddc0;
            }

        /*==========СТРАНИЦЫ (ХЭШ-НАВИГАЦИЯ)==========*/
        .page {
            display: none;
        }

            .page.active {
                display: block;
            }

        /*==========ГЛАВНАЯ==========*/
        .hero {
            background: linear-gradient(135deg, #f0f8f0, #e0f0e0);
            border-radius: 80px;
            padding: 60px 50px;
            margin-bottom: 50px;
            border: 1px solid #a8d0a8;
            box-shadow: 0 20px 40px rgba(30, 80, 30, 0.1);
        }

        .hero-text h2 {
            font-size: 3.5rem;
            color: #1b4a1b;
            line-height: 1.1;
            margin-bottom: 20px;
        }

        .hero-text p {
            font-size: 1.3rem;
            color: #2b4a2b;
            margin: 25px 0 20px;
            font-weight: 300;
        }

        .hero-btn {
            background: #2f6b2f;
            color: white;
            padding: 16px 42px;
            border-radius: 60px;
            font-weight: 600;
            font-size: 1.1rem;
            border: none;
            cursor: pointer;
            transition: 0.2s;
            box-shadow: 0 8px 18px rgba(30, 80, 30, 0.2);
        }

            .hero-btn:hover {
                background: #1d4f1d;
            }

        .section-title {
            font-size: 2.4rem;
            margin: 45px 0 25px;
            border-left: 12px solid #2f6b2f;
            padding-left: 20px;
            color: #1b4a1b;
        }

        .cats-grid {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }

        .cat-card {
            background: white;
            flex: 1 1 180px;
            border-radius: 60px;
            padding: 30px 20px;
            text-align: center;
            border: 1px solid #a8d0a8;
            cursor: pointer;
            transition: 0.2s;
            box-shadow: 0 10px 20px rgba(0,0,0,0.02);
        }

            .cat-card:hover {
                background: #eff8ef;
                transform: translateY(-5px);
                border-color: #2f6b2f;
            }

            .cat-card i {
                font-size: 3rem;
                color: #2f6b2f;
            }

        .hits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 25px;
            margin: 20px 0;
        }

        .hit-item {
            background: white;
            border-radius: 48px;
            padding: 18px;
            border: 1px solid #a8d0a8;
            cursor: pointer;
            transition: 0.2s;
        }

            .hit-item:hover {
                transform: translateY(-5px);
                border-color: #2f6b2f;
                box-shadow: 0 15px 25px rgba(30,80,30,0.1);
            }

            .hit-item img {
                width: 100%;
                height: 160px;
                object-fit: cover;
                border-radius: 32px;
                background: #e0e8e0;
            }

        .hit-price {
            font-size: 1.5rem;
            font-weight: 700;
            color: #1e562e;
        }

        .reviews {
            display: flex;
            gap: 25px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .review-card {
            background: #f0faf0;
            border-radius: 60px;
            padding: 30px;
            flex: 1 1 250px;
            border: 1px solid #a8d0a8;
        }

        /*==========КАТАЛОГ==========*/
        .catalog-layout {
            display: flex;
            gap: 30px;
        }

        .filters {
            width: 260px;
            background: white;
            border-radius: 60px;
            padding: 25px;
            border: 1px solid #a8d0a8;
            height: fit-content;
        }

        .filter-group h4 {
            color: #1b4a1b;
            margin-bottom: 10px;
        }

        .filter-group label {
            display: block;
            margin: 8px 0;
            color: #1a3b2e;
        }

        .catalog-right {
            flex: 1;
        }

        .catalog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 25px;
        }

        .catalog-card {
            background: white;
            border-radius: 48px;
            border: 1px solid #a8d0a8;
            cursor: pointer;
            transition: 0.2s;
            overflow: hidden;
        }

            .catalog-card:hover {
                transform: translateY(-5px);
                border-color: #2f6b2f;
            }

            .catalog-card img {
                width: 100%;
                height: 170px;
                object-fit: cover;
                background: #e0e8e0;
            }

        .card-content {
            padding: 15px 18px;
        }

        .card-price {
            font-weight: 700;
            font-size: 1.4rem;
            color: #1e562e;
        }

        .card-add, .card-quantity {
            background: #2f6b2f;
            color: white;
            border: none;
            padding: 10px 16px;
            border-radius: 60px;
            margin: 0 18px 18px 18px;
            font-weight: 600;
            cursor: pointer;
            width: calc(100% - 36px);
            transition: 0.2s;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

            .card-add:hover {
                background: #1d4f1d;
            }

            .card-quantity span {
                font-size: 1rem;
            }

            .card-quantity button {
                background: transparent;
                border: none;
                color: white;
                font-size: 1.2rem;
                cursor: pointer;
                padding: 0 8px;
            }

                .card-quantity button:hover {
                    opacity: 0.8;
                }

        /*==========СТРАНИЦА ТОВАРА==========*/
        .product-page {
            background: white;
            border-radius: 80px;
            padding: 40px;
            border: 1px solid #a8d0a8;
        }

        .product-main {
            display: flex;
            gap: 40px;
            flex-wrap: wrap;
        }

        .product-images {
            flex: 1 1 280px;
        }

            .product-images img {
                width: 100%;
                border-radius: 48px;
                background: #e0e8e0;
            }

        .product-info {
            flex: 2 1 350px;
        }

            .product-info h2 {
                font-size: 2.8rem;
                color: #1b4a1b;
            }

        .product-price {
            font-size: 2.4rem;
            font-weight: 700;
            color: #2f6b2f;
            margin: 15px 0;
        }

        .product-buy {
            background: #2f6b2f;
            color: white;
            border: none;
            padding: 18px 40px;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
        }

            .product-buy:hover {
                background: #1d4f1d;
            }

        .similar-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(170px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        /*==========ЛИЧНЫЙ КАБИНЕТ==========*/
        .cabinet-auth-container {
            background: white;
            border-radius: 80px;
            padding: 50px 40px;
            border: 1px solid #a8d0a8;
            max-width: 600px;
            margin: 0 auto;
            box-shadow: 0 25px 45px rgba(30,80,30,0.1);
        }

        .auth-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-bottom: 30px;
        }

        .auth-btn {
            background: #e0f0e0;
            border: 1px solid #9ac09a;
            padding: 15px 40px;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 600;
            color: #1b4a1b;
            cursor: pointer;
            transition: 0.2s;
            flex: 1;
        }

            .auth-btn.active {
                background: #2f6b2f;
                color: white;
                border-color: #2f6b2f;
            }

        .auth-form {
            display: none;
        }

            .auth-form.active {
                display: block;
            }

        .form-group {
            margin-bottom: 20px;
        }

            .form-group label {
                display: block;
                font-weight: 600;
                color: #1b4a1b;
                margin-bottom: 8px;
            }

            .form-group input, .form-group select {
                width: 100%;
                padding: 14px 20px;
                border-radius: 50px;
                border: 1px solid #9ac09a;
                font-size: 1rem;
                outline: none;
                background: white;
            }

                .form-group input:focus, .form-group select:focus {
                    border-color: #2f6b2f;
                }

        .card-row {
            display: flex;
            gap: 10px;
            align-items: center;
        }

            .card-row input {
                flex: 1;
            }

        .card-brand-icon {
            font-size: 2rem;
            color: #2f6b2f;
            min-width: 40px;
            text-align: center;
        }

        .phone-row {
            display: flex;
            gap: 10px;
        }

            .phone-row select {
                width: 120px;
                flex-shrink: 0;
            }

            .phone-row input {
                flex: 1;
            }

        .password-hint {
            font-size: 0.85rem;
            margin-top: 5px;
        }

            .password-hint.strong {
                color: #1d7a1d;
            }

            .password-hint.weak {
                color: #a14b4b;
            }

        .reg-code-section {
            background: #e0f0e0;
            border-radius: 50px;
            padding: 20px;
            margin: 20px 0;
            display: none;
        }

            .reg-code-section.active {
                display: block;
            }

        .code-input {
            display: flex;
            gap: 10px;
            align-items: center;
            flex-wrap: wrap;
        }

            .code-input input {
                width: 120px;
                text-align: center;
                font-size: 1.5rem;
                letter-spacing: 4px;
                padding: 10px;
            }

        .generated-code {
            background: #c0ddc0;
            padding: 8px 20px;
            border-radius: 40px;
            font-weight: 700;
            font-size: 1.4rem;
        }

        .cabinet-profile {
            background: white;
            border-radius: 60px;
            padding: 40px;
            border: 1px solid #a8d0a8;
        }

        .profile-info p {
            font-size: 1.2rem;
            margin: 10px 0;
        }

        .logout-btn {
            background: #e0f0e0;
            border: 1px solid #9ac09a;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 600;
            color: #1b4a1b;
            cursor: pointer;
            margin-top: 20px;
        }

            .logout-btn:hover {
                background: #c0ddc0;
            }

        /*==========КОРЗИНА (сайдбар)==========*/
        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -500px;
            width: 420px;
            max-width: 95%;
            height: 100vh;
            background: white;
            box-shadow: -8px 0 40px rgba(30,70,30,0.15);
            transition: right 0.35s;
            z-index: 300;
            padding: 30px 25px;
            display: flex;
            flex-direction: column;
            border-left: 6px solid #2f6b2f;
        }

            .cart-sidebar.active {
                right: 0;
            }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .close-cart {
            background: none;
            border: none;
            font-size: 2rem;
            color: #2f6b2f;
            cursor: pointer;
        }

        .cart-items {
            flex: 1;
            overflow-y: auto;
        }

        .cart-item {
            display: flex;
            flex-direction: column;
            background: #eaf4ea;
            padding: 14px;
            border-radius: 28px;
            margin-bottom: 10px;
        }

        .cart-item-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .cart-item-name {
            font-weight: 600;
        }

        .cart-item-price {
            font-weight: 700;
            color: #1e562e;
        }

        .cart-item-controls {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 8px;
        }

            .cart-item-controls button {
                background: #d5e8d5;
                border: none;
                width: 32px;
                height: 32px;
                border-radius: 50%;
                font-size: 1.2rem;
                font-weight: 700;
                cursor: pointer;
                color: #1b4a1b;
                border: 1px solid #9ac09a;
            }

            .cart-item-controls span {
                font-size: 1.1rem;
                font-weight: 600;
                min-width: 30px;
                text-align: center;
            }

        .cart-total {
            font-size: 1.8rem;
            font-weight: 700;
            margin-top: 20px;
            border-top: 2px solid #9ac09a;
            padding-top: 15px;
            color: #1b4a1b;
        }

        .checkout-btn {
            background: #2f6b2f;
            color: white;
            border: none;
            padding: 18px;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 700;
            margin-top: 15px;
            cursor: pointer;
            transition: 0.2s;
        }

            .checkout-btn:hover {
                background: #1d4f1d;
            }

        /*==========МОДАЛКА ДОСТАВКИ==========*/
        .delivery-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(20,50,20,0.6);
            backdrop-filter: blur(5px);
            z-index: 400;
            align-items: center;
            justify-content: center;
        }

            .delivery-modal.active {
                display: flex;
            }

        .delivery-content {
            background: white;
            border-radius: 60px;
            padding: 40px;
            max-width: 600px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
            border: 2px solid #2f6b2f;
        }

            .delivery-content h3 {
                color: #1b4a1b;
                margin-bottom: 20px;
            }

        .address-row {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }

            .address-row input {
                flex: 1;
                min-width: 120px;
                padding: 14px 20px;
                border-radius: 50px;
                border: 1px solid #9ac09a;
                font-size: 1rem;
            }

        .address-group {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }

            .address-group input {
                flex: 1;
                padding: 14px 20px;
                border-radius: 50px;
                border: 1px solid #9ac09a;
                font-size: 1rem;
            }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 15px;
        }

            .checkbox-group input[type="checkbox"] {
                width: auto;
            }

        .delivery-content input, .delivery-content select {
            width: 100%;
            padding: 14px 20px;
            border-radius: 50px;
            border: 1px solid #9ac09a;
            margin-bottom: 15px;
            font-size: 1rem;
        }

        .delivery-btns {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

            .delivery-btns button {
                flex: 1;
                padding: 14px;
                border-radius: 50px;
                border: none;
                font-weight: 600;
                cursor: pointer;
            }

        .delivery-confirm {
            background: #2f6b2f;
            color: white;
        }

            .delivery-confirm:disabled {
                background: #9ac09a;
                cursor: not-allowed;
            }

        .delivery-cancel {
            background: #e0f0e0;
            color: #1b4a1b;
            border: 1px solid #9ac09a;
        }

        /*==========ТОСТЫ==========*/
        .custom-toast {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            background: #ffffff;
            border-left: 12px solid #2f6b2f;
            padding: 18px 32px;
            border-radius: 80px;
            display: flex;
            gap: 18px;
            font-weight: 600;
            color: #1b4a1b;
            z-index: 350;
            transition: 0.3s;
            opacity: 0;
            visibility: hidden;
            align-items: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

            .custom-toast.show {
                opacity: 1;
                visibility: visible;
                bottom: 50px;
            }

            .custom-toast.error {
                border-left-color: #b34a4a;
                background: #ffeae5;
                color: #882e2e;
            }

        footer {
            margin-top: 60px;
            text-align: center;
            color: #2b4a2b;
            padding: 25px;
            border-top: 2px solid #9ac09a;
        }
    </style>
</head>
<body>
    <!-- ТОЛЬКО ЛЕТЯЩИЕ ЧАШЕЧКИ (без отдельного пара, чуть ярче) -->
    <div class="floating-bg">
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
        <div class="float-item"><i class="fas fa-mug-hot"></i></div>
        <div class="float-item"><i class="fas fa-mug-saucer"></i></div>
    </div>

    <div class="site-wrapper">
        <header>
            <div class="logo" onclick="navigateTo('home')">
                <h1>Чашка дня ✦</h1>
                <span>кофе · чай · матча</span>
            </div>
            <div class="right-actions">
                <div class="nav-menu">
                    <button class="nav-btn" id="nav-home" onclick="navigateTo('home')">Главная</button>
                    <button class="nav-btn" id="nav-catalog" onclick="navigateTo('catalog')">Каталог</button>
                    <button class="nav-btn" id="nav-cabinet" onclick="navigateTo('cabinet')">Кабинет</button>
                </div>
                <div class="cart-area">
                    <span class="cart-icon" onclick="toggleCart()">
                        <i class="fas fa-basket-shopping"></i><span id="cart-count">0</span>
                    </span>
                    <button class="open-cart-btn" onclick="toggleCart()">Корзина</button>
                </div>
            </div>
        </header>

        <!--ГЛАВНАЯ-->
        <div id="home-page" class="page">
            <div class="hero">
                <div class="hero-text">
                    <h2>Кофе, чай, матча<br>с заботой о природе</h2>
                    <p>Натуральные листья и зёрна, ручной отбор, свежая обжарка.</p>
                    <button class="hero-btn" onclick="navigateTo('catalog')">Перейти в каталог →</button>
                </div>
            </div>
            <div style="margin: 40px 0; background: white; border-radius: 60px; padding: 30px; border:1px solid #a8d0a8;">
                <p style="font-size:1.3rem;">🌱 Мы собираем чай вручную в высокогорных районах, контролируем каждый этап обжарки. Более 10 лет выбираем только спешелти кофе и матчу трёх цветов.</p>
            </div>
            <div class="section-title">Категории</div>
            <div class="cats-grid">
                <div class="cat-card" onclick="applyCategoryFilter('tea')"><i class="fas fa-leaf"></i><h3>Чай</h3><p>белый, зелёный, улун</p></div>
                <div class="cat-card" onclick="applyCategoryFilter('coffee')"><i class="fas fa-mug-hot"></i><h3>Кофе</h3><p>моносорта, бленды</p></div>
                <div class="cat-card" onclick="applyCategoryFilter('matcha')"><i class="fas fa-whiskey-glass"></i><h3>Матча</h3><p>зелёная, синяя, розовая</p></div>
            </div>
            <div class="section-title">🔥 Хиты продаж</div>
            <div class="hits-grid" id="hits-grid"></div>
            <div class="section-title">💬 Отзывы</div>
            <div class="reviews">
                <div class="review-card"><i class="fas fa-star"></i><p>«Обожаю синюю матчу, необычный цвет и мягкий вкус!» — Анна</p></div>
                <div class="review-card"><i class="fas fa-star"></i><p>«Кофе Эфиопия просто космос, свежий, цитрусовый.» — Михаил</p></div>
                <div class="review-card"><i class="fas fa-star"></i><p>«Чай с лавандой — вечерний ритуал, спасибо за заботу.» — Елена</p></div>
            </div>
        </div>

        <!--КАТАЛОГ-->
        <div id="catalog-page" class="page">
            <div class="catalog-layout">
                <div class="filters">
                    <h3 style="color:#1b4a1b;">Фильтры</h3>
                    <div class="filter-group">
                        <h4>Тип</h4>
                        <label><input type="checkbox" id="filter-coffee" value="coffee" onchange="applyFilters()"> ☕ Кофе</label>
                        <label><input type="checkbox" id="filter-tea" value="tea" onchange="applyFilters()"> 🍵 Чай</label>
                        <label><input type="checkbox" id="filter-matcha" value="matcha" onchange="applyFilters()"> 🍃 Матча</label>
                    </div>
                    <div class="filter-group">
                        <h4>Цена</h4>
                        <label><input type="radio" name="price" value="all" checked onchange="applyFilters()"> Все</label>
                        <label><input type="radio" name="price" value="0-800" onchange="applyFilters()"> до 800 ₽</label>
                        <label><input type="radio" name="price" value="800-1200" onchange="applyFilters()"> 800–1200 ₽</label>
                        <label><input type="radio" name="price" value="1200-99999" onchange="applyFilters()"> от 1200</label>
                    </div>
                    <div class="filter-group">
                        <h4>Крепость (кофе)</h4>
                        <label><input type="checkbox" id="strength-soft" value="мягкий" onchange="applyFilters()"> мягкий</label>
                        <label><input type="checkbox" id="strength-medium" value="средняя" onchange="applyFilters()"> средняя</label>
                        <label><input type="checkbox" id="strength-strong" value="крепкий" onchange="applyFilters()"> крепкий</label>
                    </div>
                    <div class="filter-group">
                        <h4>Страна</h4>
                        <label><input type="checkbox" id="origin-ethiopia" value="Эфиопия" onchange="applyFilters()"> Эфиопия</label>
                        <label><input type="checkbox" id="origin-kenya" value="Кения" onchange="applyFilters()"> Кения</label>
                        <label><input type="checkbox" id="origin-colombia" value="Колумбия" onchange="applyFilters()"> Колумбия</label>
                        <label><input type="checkbox" id="origin-guatemala" value="Гватемала" onchange="applyFilters()"> Гватемала</label>
                        <label><input type="checkbox" id="origin-brazil" value="Бразилия" onchange="applyFilters()"> Бразилия</label>
                        <label><input type="checkbox" id="origin-china" value="Китай" onchange="applyFilters()"> Китай</label>
                        <label><input type="checkbox" id="origin-japan" value="Япония" onchange="applyFilters()"> Япония</label>
                    </div>
                </div>
                <div class="catalog-right">
                    <div class="catalog-grid" id="catalog-grid"></div>
                </div>
            </div>
        </div>

        <!--СТРАНИЦА ТОВАРА-->
        <div id="product-page" class="page">
            <div class="product-page" id="product-detail-container"></div>
        </div>

        <!--ЛИЧНЫЙ КАБИНЕТ-->
        <div id="cabinet-page" class="page">
            <div id="cabinet-content"></div>
        </div>

        <!--КОРЗИНА (сайдбар)-->
        <div id="cartSidebar" class="cart-sidebar">
            <div class="cart-header"><h2>Корзина</h2><button class="close-cart" onclick="toggleCart()"><i class="fas fa-times"></i></button></div>
            <div id="cart-items-container" class="cart-items"></div>
            <div class="cart-total" id="cart-total">Итого: 0 ₽</div>
            <button class="checkout-btn" onclick="openDeliveryModal()">Оформить заказ</button>
        </div>

        <!--МОДАЛКА ДОСТАВКИ-->
        <div id="deliveryModal" class="delivery-modal">
            <div class="delivery-content">
                <h3>Доставка</h3>
                <div class="address-row">
                    <input type="text" id="delivery-city" placeholder="Город *" required oninput="this.value = this.value.replace(/[a-zA-Z]/g, ''); validateDeliveryForm()">
                    <input type="text" id="delivery-street" placeholder="Улица *" required oninput="this.value = this.value.replace(/[a-zA-Z]/g, ''); validateDeliveryForm()">
                </div>
                <div class="address-group">
                    <input type="text" id="delivery-house" placeholder="Дом *" required oninput="this.value = this.value.replace(/[a-zA-Z]/g, ''); validateDeliveryForm()">
                    <input type="text" id="delivery-apartment" placeholder="Квартира" oninput="this.value = this.value.replace(/[a-zA-Z]/g, ''); validateDeliveryForm()">
                </div>
                <div class="checkbox-group">
                    <input type="checkbox" id="delivery-private-house" onchange="toggleApartment()">
                    <label for="delivery-private-house">Частный дом</label>
                </div>
                <input type="date" id="delivery-date" placeholder="Дата" onchange="validateDeliveryForm()">
                <select id="delivery-time" onchange="validateDeliveryForm()">
                    <option value="">Выберите время</option>
                    <option value="10-12">10:00 – 12:00</option>
                    <option value="12-14">12:00 – 14:00</option>
                    <option value="14-16">14:00 – 16:00</option>
                    <option value="16-18">16:00 – 18:00</option>
                    <option value="18-20">18:00 – 20:00</option>
                </select>
                <div class="delivery-btns">
                    <button class="delivery-confirm" id="delivery-confirm-btn" onclick="confirmOrder()" disabled>Подтвердить</button>
                    <button class="delivery-cancel" onclick="closeDeliveryModal()">Отмена</button>
                </div>
            </div>
        </div>

        <!--ТОСТ-->
        <div id="successToast" class="custom-toast"><i class="fas fa-circle-check"></i><span id="toast-message">✓ Заказ оформлен</span></div>

        <footer>🍃 Чашка дня · ручной отбор · свежая обжарка</footer>
    </div>

    <script>
        (function () {
            //==========ТОВАРЫ==========
            const products = [
                { id: 1, cat: 'coffee', name: 'Эфиопия Гедэб', img: 'images/coffee1.jpg', desc: 'Цитрус, бергамот, цветочный', weight: '250г', taste: 'жасмин, личи', price: 890, origin: 'Эфиопия', strength: 'средняя', description: 'Яркий цветочно-цитрусовый кофе с нотами бергамота и жасмина. Послевкусие сладкое, чайное.' },
                { id: 2, cat: 'coffee', name: 'Кения Аб', img: 'images/coffee2.jpg', desc: 'Клюква, вино, томат', weight: '250г', taste: 'красные ягоды, карамель', price: 1040, origin: 'Кения', strength: 'крепкий', description: 'Насыщенный фруктовый вкус с оттенками клюквы и вина. Плотное тело, долгое ягодное послевкусие.' },
                { id: 3, cat: 'coffee', name: 'Колумбия Супремо', img: 'images/coffee3.jpg', desc: 'Шоколад, орех, яблоко', weight: '500г', taste: 'какао, миндаль', price: 750, origin: 'Колумбия', strength: 'средняя', description: 'Сбалансированный кофе с нотами тёмного шоколада, миндаля и зелёного яблока. Приятная кислинка.' },
                { id: 4, cat: 'coffee', name: 'Гватемала', img: 'images/coffee4.jpg', desc: 'Карамель, апельсин', weight: '250г', taste: 'шоколад, корица', price: 930, origin: 'Гватемала', strength: 'мягкий', description: 'Мягкий сладкий кофе с карамелью и цитрусовой свежестью. Утончённый аромат корицы.' },
                { id: 5, cat: 'coffee', name: 'Бразилия Серрадо', img: 'images/coffee5.jpg', desc: 'Арахис, молочный шоколад', weight: '500г', taste: 'сливочный, орехи', price: 640, origin: 'Бразилия', strength: 'средняя', description: 'Классический бразильский профиль: арахис, молочный шоколад, низкая кислинка, плотное тело.' },
                { id: 6, cat: 'matcha', name: 'Матча зелёная', img: 'images/matcha1.jpg', desc: 'Уджи, церемониальная', weight: '40г', taste: 'умами, сливочный', price: 1290, origin: 'Япония', description: 'Высший сорт матчи из Удзи. Травяной вкус с глубоким умами, кремовая текстура, ярко-зелёный цвет.' },
                { id: 7, cat: 'matcha', name: 'Матча синяя', img: 'images/matcha2.jpg', desc: 'Клатория, ваниль', weight: '30г', taste: 'цветочный, тропики', price: 1490, origin: 'Таиланд', description: 'Голубая матча из цветов клитории. Ванильный вкус, цветочный аромат, меняет цвет от лимона.' },
                { id: 8, cat: 'matcha', name: 'Матча розовая', img: 'images/matcha3.jpg', desc: 'Гибискус, малина', weight: '35г', taste: 'клубника, шиповник', price: 1390, origin: 'Китай', description: 'Ягодная матча с гибискусом. Яркая кислинка малины, розовый цвет, богата антиоксидантами.' },
                { id: 9, cat: 'tea', name: 'Бай Му Дань', img: 'images/tea1.jpg', desc: 'Белый пион', weight: '50г', taste: 'дыня, орех, мёд', price: 650, origin: 'Китай', description: 'Белый чай с пушистыми почками. Лёгкий настой с оттенками дыни и орехов, медовое послевкусие.' },
                { id: 10, cat: 'tea', name: 'Те Гуань Инь', img: 'images/tea2.jpg', desc: 'Молочный улун', weight: '100г', taste: 'орхидея, сливки', price: 840, origin: 'Китай', description: 'Полуферментированный улун с молочными нотками. Цветочный аромат, сливочная текстура, долгое сладкое послевкусие.' },
                { id: 11, cat: 'tea', name: 'Лапсанг Сушонг', img: 'images/tea3.jpg', desc: 'Копчёный чай', weight: '100г', taste: 'дым, сосна', price: 720, origin: 'Китай', description: 'Чай, копчённый на сосновых дровах. Насыщенный дымный аромат, терпкий вкус, подходит для церемоний.' },
                { id: 12, cat: 'tea', name: 'Сенча', img: 'images/tea4.jpg', desc: 'Японский зелёный', weight: '100г', taste: 'морской бриз, трава', price: 590, origin: 'Япония', description: 'Классическая японская сенча. Свежий травяной вкус, нотки морских водорослей, лёгкая терпкость.' },
            ];

            //==========ГЛОБАЛЬНЫЕ ПЕРЕМЕННЫЕ==========
            let cart = []; // массив { product, quantity }
            let currentUser = null;
            let regCode = '';
            let tempUserData = null;

            //==========ПРОСТОЕ ШИФРОВАНИЕ (XOR с фиксированным ключом) ДЛЯ ДЕМОНСТРАЦИИ==========
            const ENC_KEY = 0x5A;
            function encryptPassword(pwd) {
                return pwd.split('').map(ch => String.fromCharCode(ch.charCodeAt(0) ^ ENC_KEY)).join('');
            }
            function decryptPassword(enc) {
                return enc.split('').map(ch => String.fromCharCode(ch.charCodeAt(0) ^ ENC_KEY)).join('');
            }

            //==========ГЕНЕРАЦИЯ CSRF-ТОКЕНА==========
            function generateCsrfToken() {
                return Math.random().toString(36).substring(2, 15) + Math.random().toString(36).substring(2, 15);
            }

            //==========ОПРЕДЕЛЕНИЕ БРЕНДА КАРТЫ И БАНКА==========
            function getCardInfo(cardNumber) {
                let clean = cardNumber.replace(/\D/g, '');
                let brand = { name: 'Card', icon: 'fas fa-credit-card' };
                let bank = '';

                if (clean.startsWith('4')) {
                    brand = { name: 'Visa', icon: 'fab fa-cc-visa' };
                } else if (clean.startsWith('5')) {
                    brand = { name: 'Mastercard', icon: 'fab fa-cc-mastercard' };
                } else if (clean.startsWith('34') || clean.startsWith('37')) {
                    brand = { name: 'Amex', icon: 'fab fa-cc-amex' };
                } else if (clean.startsWith('2') || clean.startsWith('60')) {
                    brand = { name: 'Мир', icon: 'fas fa-credit-card' };
                }

                if (clean.length >= 6) {
                    let bin = clean.substring(0, 6);
                    if (bin.startsWith('5469') || bin.startsWith('4276') || bin.startsWith('4817')) {
                        bank = 'Сбербанк';
                    } else if (bin.startsWith('4622') || bin.startsWith('4024')) {
                        bank = 'ВТБ';
                    } else if (bin.startsWith('2200') || bin.startsWith('2201') || bin.startsWith('2202')) {
                        bank = 'Мир (Сбербанк)';
                    } else if (bin.startsWith('5213')) {
                        bank = 'Тинькофф';
                    }
                }
                return { brand, bank };
            }

            //==========НАВИГАЦИЯ (ХЭШИ)==========
            window.navigateTo = function (page, productId = null) {
                if (page === 'home') location.hash = '#home';
                else if (page === 'catalog') location.hash = '#catalog';
                else if (page === 'product' && productId) location.hash = `#product/${productId}`;
                else if (page === 'cabinet') location.hash = '#cabinet';
            };

            function handleHash() {
                const hash = location.hash.slice(1) || 'home';
                const parts = hash.split('/');
                const page = parts[0];
                const productId = parts[1] ? parseInt(parts[1]) : null;

                document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));

                if (page === 'home') {
                    document.getElementById('home-page').classList.add('active');
                } else if (page === 'catalog') {
                    document.getElementById('catalog-page').classList.add('active');
                    renderCatalog(products);
                } else if (page === 'product' && productId) {
                    document.getElementById('product-page').classList.add('active');
                    openProductPage(productId);
                } else if (page === 'cabinet') {
                    document.getElementById('cabinet-page').classList.add('active');
                    renderCabinet();
                } else {
                    document.getElementById('home-page').classList.add('active');
                }

                document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('active'));
                if (page === 'home') document.getElementById('nav-home').classList.add('active');
                else if (page === 'catalog') document.getElementById('nav-catalog').classList.add('active');
                else if (page === 'cabinet') document.getElementById('nav-cabinet').classList.add('active');
                if (page === 'product') document.getElementById('nav-catalog').classList.add('active');
            }

            window.addEventListener('hashchange', handleHash);
            if (!location.hash) location.hash = '#home';
            else handleHash();

            //==========КАТАЛОГ==========
            window.renderCatalog = function (array) {
                const grid = document.getElementById('catalog-grid');
                grid.innerHTML = '';
                array.forEach(p => {
                    const card = document.createElement('div');
                    card.className = 'catalog-card';
                    card.onclick = (e) => {
                        // Если клик по кнопкам счётчика, не переходим на товар
                        if (e.target.closest('.card-quantity') || e.target.closest('.card-add')) return;
                        navigateTo('product', p.id);
                    };
                    // Определяем текущее количество в корзине для этого товара
                    const cartItem = cart.find(item => item.product.id === p.id);
                    const qty = cartItem ? cartItem.quantity : 0;
                    let buttonHtml = '';
                    if (qty === 0) {
                        buttonHtml = `<button class="card-add" onclick="event.stopPropagation(); addToCart(${p.id});">➕ В корзину</button>`;
                    } else {
                        buttonHtml = `
                  <div class="card-quantity">
                    <button onclick="event.stopPropagation(); decreaseFromCard(${p.id});">−</button>
                    <span>${qty}</span>
                    <button onclick="event.stopPropagation(); increaseFromCard(${p.id});">+</button>
                  </div>
                `;
                    }
                    card.innerHTML = `
                <img src="${p.img}" alt="${p.name}" loading="lazy" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' viewBox=\'0 0 200 200\'%3E%3Crect width=\'200\' height=\'200\' fill=\'%23ccc\'/%3E%3Ctext x=\'30\' y=\'130\' fill=\'%23333\' font-size=\'60\'%3E🖼️%3C/text%3E%3C/svg%3E'">
                <div class="card-content">
                  <div><strong>${p.name}</strong></div>
                  <div class="card-price">${p.price} ₽</div>
                </div>
                ${buttonHtml}
              `;
                    grid.appendChild(card);
                });
            };

            // Функции для управления количеством прямо из карточки
            window.increaseFromCard = function (id) {
                const product = products.find(p => p.id === id);
                if (!product) return;
                const existing = cart.find(item => item.product.id === id);
                if (existing) {
                    existing.quantity += 1;
                } else {
                    cart.push({ product, quantity: 1 });
                }
                updateCartUI();
                renderCatalog(products); // перерисовываем каталог для обновления кнопок
                showToast(`${product.name} добавлен в корзину`);
            };

            window.decreaseFromCard = function (id) {
                const existingIndex = cart.findIndex(item => item.product.id === id);
                if (existingIndex === -1) return;
                if (cart[existingIndex].quantity > 1) {
                    cart[existingIndex].quantity -= 1;
                } else {
                    cart.splice(existingIndex, 1);
                }
                updateCartUI();
                renderCatalog(products); // перерисовываем каталог
                const product = products.find(p => p.id === id);
                showToast(`${product.name} удалён из корзины`);
            };

            window.applyFilters = function () {
                let filtered = [...products];
                const coffee = document.getElementById('filter-coffee')?.checked;
                const tea = document.getElementById('filter-tea')?.checked;
                const matcha = document.getElementById('filter-matcha')?.checked;
                const selectedTypes = [];
                if (coffee) selectedTypes.push('coffee');
                if (tea) selectedTypes.push('tea');
                if (matcha) selectedTypes.push('matcha');
                if (selectedTypes.length > 0) filtered = filtered.filter(p => selectedTypes.includes(p.cat));

                const priceRad = document.querySelector('input[name="price"]:checked');
                if (priceRad && priceRad.value !== 'all') {
                    const [min, max] = priceRad.value.split('-').map(Number);
                    filtered = filtered.filter(p => p.price >= min && p.price <= max);
                }

                const strengthSoft = document.getElementById('strength-soft')?.checked;
                const strengthMedium = document.getElementById('strength-medium')?.checked;
                const strengthStrong = document.getElementById('strength-strong')?.checked;
                const selectedStrengths = [];
                if (strengthSoft) selectedStrengths.push('мягкий');
                if (strengthMedium) selectedStrengths.push('средняя');
                if (strengthStrong) selectedStrengths.push('крепкий');
                if (selectedStrengths.length > 0) {
                    filtered = filtered.filter(p => p.cat === 'coffee' ? selectedStrengths.includes(p.strength) : true);
                }

                const originEth = document.getElementById('origin-ethiopia')?.checked;
                const originKen = document.getElementById('origin-kenya')?.checked;
                const originCol = document.getElementById('origin-colombia')?.checked;
                const originGua = document.getElementById('origin-guatemala')?.checked;
                const originBra = document.getElementById('origin-brazil')?.checked;
                const originChi = document.getElementById('origin-china')?.checked;
                const originJap = document.getElementById('origin-japan')?.checked;
                const selectedOrigins = [];
                if (originEth) selectedOrigins.push('Эфиопия');
                if (originKen) selectedOrigins.push('Кения');
                if (originCol) selectedOrigins.push('Колумбия');
                if (originGua) selectedOrigins.push('Гватемала');
                if (originBra) selectedOrigins.push('Бразилия');
                if (originChi) selectedOrigins.push('Китай');
                if (originJap) selectedOrigins.push('Япония');
                if (selectedOrigins.length > 0) filtered = filtered.filter(p => selectedOrigins.includes(p.origin));

                renderCatalog(filtered);
            };

            window.applyCategoryFilter = function (cat) {
                document.getElementById('filter-coffee').checked = (cat === 'coffee');
                document.getElementById('filter-tea').checked = (cat === 'tea');
                document.getElementById('filter-matcha').checked = (cat === 'matcha');
                navigateTo('catalog');
                applyFilters();
            };

            function renderHits() {
                const hits = products.filter(p => [1, 6, 9].includes(p.id));
                const container = document.getElementById('hits-grid');
                container.innerHTML = '';
                hits.forEach(p => {
                    const div = document.createElement('div');
                    div.className = 'hit-item';
                    div.onclick = () => navigateTo('product', p.id);
                    div.innerHTML = `<img src="${p.img}" alt=""><h4>${p.name}</h4><span class="hit-price">${p.price} ₽</span>`;
                    container.appendChild(div);
                });
            }

            window.openProductPage = function (id) {
                const prod = products.find(p => p.id === id);
                if (!prod) return;
                const container = document.getElementById('product-detail-container');
                container.innerHTML = `
              <div class="product-main">
                <div class="product-images"><img src="${prod.img}" alt=""></div>
                <div class="product-info">
                  <h2>${prod.name}</h2>
                  <p><strong>🌱 Вкус:</strong> ${prod.taste} · ${prod.desc}</p>
                  <p><strong>📦 Состав:</strong> 100% натуральный продукт</p>
                  <p><strong>⚖️ Объём:</strong> ${prod.weight}</p>
                  <p><strong>📝 Описание:</strong> ${prod.description || 'Нет дополнительного описания'}</p>
                  <div class="product-price">${prod.price} ₽</div>
                  <button class="product-buy" onclick="addToCart(${prod.id}); navigateTo('catalog');">Купить</button>
                </div>
              </div>
              <div class="similar">
                <h3>Похожие товары</h3>
                <div class="similar-grid" id="similar-grid"></div>
              </div>
            `;
                const similar = products.filter(p => p.cat === prod.cat && p.id !== prod.id).slice(0, 3);
                const simGrid = document.getElementById('similar-grid');
                simGrid.innerHTML = '';
                similar.forEach(s => {
                    simGrid.innerHTML += `<div class="hit-item" onclick="navigateTo('product', ${s.id})"><img src="${s.img}"><h4>${s.name}</h4><span class="hit-price">${s.price} ₽</span></div>`;
                });
            };

            //==========КОРЗИНА==========
            window.toggleCart = function () {
                document.getElementById('cartSidebar').classList.toggle('active');
            };

            window.addToCart = function (id) {
                const product = products.find(p => p.id === id);
                if (!product) return;
                const existing = cart.find(item => item.product.id === id);
                if (existing) {
                    existing.quantity += 1;
                } else {
                    cart.push({ product, quantity: 1 });
                }
                updateCartUI();
                renderCatalog(products); // обновляем кнопки в каталоге
                showToast(`${product.name} добавлен в корзину`);
            };

            window.increaseQuantity = function (index) {
                cart[index].quantity += 1;
                updateCartUI();
                renderCatalog(products);
            };

            window.decreaseQuantity = function (index) {
                if (cart[index].quantity > 1) {
                    cart[index].quantity -= 1;
                } else {
                    cart.splice(index, 1);
                }
                updateCartUI();
                renderCatalog(products);
            };

            function updateCartUI() {
                const container = document.getElementById('cart-items-container');
                const totalSpan = document.getElementById('cart-total');
                const countSpan = document.getElementById('cart-count');
                let html = '';
                let total = 0;
                let totalItems = 0;
                cart.forEach((item, idx) => {
                    total += item.product.price * item.quantity;
                    totalItems += item.quantity;
                    html += `
                <div class="cart-item">
                  <div class="cart-item-row">
                    <span class="cart-item-name">${item.product.name}</span>
                    <span class="cart-item-price">${item.product.price} ₽</span>
                  </div>
                  <div class="cart-item-controls">
                    <button onclick="decreaseQuantity(${idx})">−</button>
                    <span>${item.quantity}</span>
                    <button onclick="increaseQuantity(${idx})">+</button>
                  </div>
                </div>
              `;
                });
                container.innerHTML = html || '<p style="padding:20px;">Корзина пуста</p>';
                totalSpan.innerText = `Итого: ${total} ₽`;
                countSpan.innerText = totalItems;
            }

            //==========ЛИЧНЫЙ КАБИНЕТ==========
            function renderCabinet() {
                const container = document.getElementById('cabinet-content');
                const savedUser = localStorage.getItem('currentUser');
                if (savedUser) {
                    currentUser = JSON.parse(savedUser);
                    showProfile(container);
                } else {
                    showAuthScreen(container);
                }
            }

            function showAuthScreen(container) {
                container.innerHTML = `
              <div class="cabinet-auth-container">
                <div class="auth-buttons">
                  <button class="auth-btn active" id="btn-login" onclick="showLoginForm()">Войти</button>
                  <button class="auth-btn" id="btn-register" onclick="showRegisterForm()">Зарегистрироваться</button>
                </div>
                <div id="login-form" class="auth-form active">
                  <div class="form-group">
                    <label>Email или телефон</label>
                    <input type="text" id="login-credential" placeholder="example@mail.com / +7 (999) 999-99-99">
                  </div>
                  <div class="form-group">
                    <label>Пароль</label>
                    <input type="password" id="login-password">
                  </div>
                  <button class="hero-btn" style="width:100%" onclick="login()">Войти</button>
                </div>
                <div id="register-form" class="auth-form">
                  <div class="form-group">
                    <label>Имя *</label>
                    <input type="text" id="reg-firstname" required maxlength="20" oninput="this.value = this.value.replace(/[^а-яА-ЯёЁ]/g, '')">
                  </div>
                  <div class="form-group">
                    <label>Фамилия *</label>
                    <input type="text" id="reg-lastname" required maxlength="20" oninput="this.value = this.value.replace(/[^а-яА-ЯёЁ]/g, '')">
                  </div>
                  <div class="form-group">
                    <label>Дата рождения</label>
                    <input type="date" id="reg-birthdate">
                  </div>
                  <div class="form-group">
                    <label>Email</label>
                    <input type="text" id="reg-email" placeholder="example@mail.com">
                  </div>
                  <div class="form-group">
                    <label>Телефон *</label>
                    <div class="phone-row">
                      <select id="country-code">
                        <option value="+7" selected>+7 (Россия)</option>
                        <option value="+1">+1 (США/Канада)</option>
                        <option value="+44">+44 (Великобритания)</option>
                        <option value="+49">+49 (Германия)</option>
                        <option value="+33">+33 (Франция)</option>
                        <option value="+39">+39 (Италия)</option>
                        <option value="+34">+34 (Испания)</option>
                        <option value="+86">+86 (Китай)</option>
                        <option value="+81">+81 (Япония)</option>
                      </select>
                      <input type="text" id="reg-phone" required placeholder="(999) 999-99-99" oninput="formatPhoneWithCode(this)">
                    </div>
                  </div>
                  <div class="form-group">
                    <label>Данные карты (обязательно)</label>
                    <div class="card-row">
                      <input type="text" id="reg-card" placeholder="0000 0000 0000 0000" maxlength="19" oninput="formatCardNumber(this); updateCardInfo(this);">
                      <span id="card-brand-icon" class="card-brand-icon"><i class="fas fa-credit-card"></i></span>
                      <input type="text" id="reg-exp" placeholder="ММ/ГГ" maxlength="5" oninput="formatExpiry(this)">
                      <input type="password" id="reg-cvv" placeholder="CVV" maxlength="3" oninput="this.value = this.value.replace(/\D/g, '').substring(0,3)" style="font-family: monospace;">
                    </div>
                    <div id="card-bank-name" style="margin-top:5px; font-size:0.9rem; color:#2f6b2f;"></div>
                  </div>
                  <div class="form-group">
                    <label>Пароль *</label>
                    <input type="password" id="reg-password" maxlength="30" oninput="validatePasswordStrength()">
                    <div class="password-hint" id="password-hint"></div>
                  </div>
                  <button class="hero-btn" style="width:100%" onclick="startRegistration()">Зарегистрироваться</button>
                </div>
                <div id="reg-code-section" class="reg-code-section">
                  <p>На ваш телефон/почту отправлен код из 4 цифр</p>
                  <div class="code-input">
                    <input type="text" id="reg-code-input" maxlength="4" placeholder="____">
                    <span id="generated-code-display" class="generated-code"></span>
                  </div>
                  <button class="hero-btn" style="margin-top:15px;" onclick="confirmRegistration()">Подтвердить код</button>
                </div>
              </div>
            `;
                window.showLoginForm = function () {
                    document.getElementById('btn-login').classList.add('active');
                    document.getElementById('btn-register').classList.remove('active');
                    document.getElementById('login-form').classList.add('active');
                    document.getElementById('register-form').classList.remove('active');
                    document.getElementById('reg-code-section').classList.remove('active');
                };
                window.showRegisterForm = function () {
                    document.getElementById('btn-login').classList.remove('active');
                    document.getElementById('btn-register').classList.add('active');
                    document.getElementById('login-form').classList.remove('active');
                    document.getElementById('register-form').classList.add('active');
                    document.getElementById('reg-code-section').classList.remove('active');
                };
            }

            //==========ФОРМАТИРОВАНИЕ ТЕЛЕФОНА==========
            window.formatPhoneWithCode = function (input) {
                let digits = input.value.replace(/\D/g, '');
                digits = digits.substring(0, 10);
                let formatted = '';
                if (digits.length > 0) {
                    formatted += '(' + digits.substring(0, 3);
                    if (digits.length >= 3) formatted += ') ';
                    if (digits.length >= 4) formatted += digits.substring(3, 6);
                    if (digits.length >= 6) formatted += '-';
                    if (digits.length >= 7) formatted += digits.substring(6, 8);
                    if (digits.length >= 8) formatted += '-';
                    if (digits.length >= 9) formatted += digits.substring(8, 10);
                }
                input.value = formatted;
            };

            window.formatCardNumber = function (input) {
                let value = input.value.replace(/\D/g, '').substring(0, 16);
                let formatted = value.replace(/(\d{4})(?=\d)/g, '$1 ');
                input.value = formatted;
            };

            window.updateCardInfo = function (input) {
                let clean = input.value.replace(/\D/g, '');
                let info = getCardInfo(clean);
                document.getElementById('card-brand-icon').innerHTML = `<i class="${info.brand.icon}"></i>`;
                let bankText = info.bank ? info.bank : '';
                document.getElementById('card-bank-name').innerText = bankText;
            };

            window.formatExpiry = function (input) {
                let digits = input.value.replace(/\D/g, '').substring(0, 4);
                let formatted = '';
                // Заполняем слева направо: если 1 цифра, то просто цифра, после 2 цифр добавляем слеш
                if (digits.length <= 2) {
                    formatted = digits;
                } else {
                    formatted = digits.substring(0, 2) + '/' + digits.substring(2, 4);
                }
                input.value = formatted;
            };

            window.validatePasswordStrength = function () {
                const pwd = document.getElementById('reg-password').value;
                const hint = document.getElementById('password-hint');
                const isValid = /^(?=.*[A-Za-z]).{8,30}$/.test(pwd);
                if (!pwd) {
                    hint.innerText = '';
                    hint.className = 'password-hint';
                } else if (!isValid) {
                    hint.innerText = 'Пароль должен содержать от 8 до 30 символов и хотя бы одну латинскую букву';
                    hint.className = 'password-hint weak';
                } else {
                    hint.innerText = 'надежный пароль';
                    hint.className = 'password-hint strong';
                }
            };

            window.startRegistration = function () {
                const firstName = document.getElementById('reg-firstname').value.trim();
                const lastName = document.getElementById('reg-lastname').value.trim();
                const email = document.getElementById('reg-email').value.trim();
                const countryCode = document.getElementById('country-code').value;
                const phoneRaw = document.getElementById('reg-phone').value.replace(/\D/g, '');
                const phone = countryCode + ' ' + document.getElementById('reg-phone').value;
                const card = document.getElementById('reg-card').value.replace(/\s/g, '');
                const exp = document.getElementById('reg-exp').value.trim();
                const cvv = document.getElementById('reg-cvv').value;
                const password = document.getElementById('reg-password').value;

                if (!firstName || !lastName || !phoneRaw) {
                    showToast('Заполните обязательные поля', true);
                    return;
                }
                if (!email && !phoneRaw) {
                    showToast('Укажите email или телефон', true);
                    return;
                }
                if (firstName.length > 20 || lastName.length > 20) {
                    showToast('Имя и фамилия не более 20 символов', true);
                    return;
                }
                if (!/^[а-яА-ЯёЁ]+$/.test(firstName) || !/^[а-яА-ЯёЁ]+$/.test(lastName)) {
                    showToast('Имя и фамилия должны содержать только буквы кириллицы', true);
                    return;
                }
                if (phoneRaw.length !== 10) {
                    showToast('Телефон должен содержать 10 цифр после кода страны', true);
                    return;
                }
                if (card.length !== 16 || !/^\d+$/.test(card)) {
                    showToast('Номер карты должен содержать 16 цифр', true);
                    return;
                }
                if (!/^\d{2}\/\d{2}$/.test(exp)) {
                    showToast('Дата карты должна быть в формате ММ/ГГ', true);
                    return;
                }
                let month = parseInt(exp.substring(0, 2), 10);
                let year = parseInt(exp.substring(3, 5), 10);
                if (month < 1 || month > 12) {
                    showToast('Месяц должен быть от 01 до 12', true);
                    return;
                }
                if (year > 40) {
                    showToast('Год должен быть не более 40 (2040)', true);
                    return;
                }
                if (!/^\d{3}$/.test(cvv)) {
                    showToast('CVV должен содержать 3 цифры', true);
                    return;
                }
                if (!/^(?=.*[A-Za-z]).{8,30}$/.test(password)) {
                    showToast('Пароль не соответствует требованиям', true);
                    return;
                }

                regCode = Math.floor(1000 + Math.random() * 9000).toString();
                const encryptedPassword = encryptPassword(password);
                const csrfToken = generateCsrfToken();
                tempUserData = { firstName, lastName, email, phone: countryCode + ' ' + document.getElementById('reg-phone').value, card, exp, cvv, password: encryptedPassword, csrfToken };

                document.getElementById('register-form').style.display = 'none';
                document.getElementById('reg-code-section').classList.add('active');
                document.getElementById('generated-code-display').innerText = regCode;
            };

            window.confirmRegistration = function () {
                const enteredCode = document.getElementById('reg-code-input').value;
                if (enteredCode === regCode) {
                    const user = { ...tempUserData, card: tempUserData.card.replace(/\d(?=\d{4})/g, '*') };
                    localStorage.setItem('currentUser', JSON.stringify(user));
                    currentUser = user;
                    showProfile(document.getElementById('cabinet-content'));
                    showToast('Регистрация успешна!');
                } else {
                    showToast('Неверный код', true);
                }
            };

            window.login = function () {
                const credential = document.getElementById('login-credential').value.trim();
                const password = document.getElementById('login-password').value;
                const saved = localStorage.getItem('currentUser');

                if (!saved) {
                    showToast('Нет зарегистрированных пользователей', true);
                    return;
                }

                const user = JSON.parse(saved);
                const isEmail = credential.includes('@');
                let match = false;

                if (isEmail) {
                    match = (user.email && user.email.toLowerCase() === credential.toLowerCase());
                } else {
                    const inputDigits = credential.replace(/\D/g, '');
                    const userPhoneDigits = user.phone.replace(/\D/g, '');
                    match = (userPhoneDigits === inputDigits);
                }

                const decryptedPassword = decryptPassword(user.password);

                if (match && decryptedPassword === password) {
                    currentUser = user;
                    showProfile(document.getElementById('cabinet-content'));
                    showToast('Вход выполнен');
                } else {
                    showToast('Неверный логин или пароль', true);
                }
            };

            function showProfile(container) {
                container.innerHTML = `
              <div class="cabinet-profile">
                <h2 style="color:#1b4a1b;">Здравствуйте, ${currentUser.firstName}!</h2>
                <div class="profile-info">
                  <p><strong>Имя:</strong> ${currentUser.firstName} ${currentUser.lastName}</p>
                  <p><strong>Email:</strong> ${currentUser.email || 'не указан'}</p>
                  <p><strong>Телефон:</strong> ${currentUser.phone}</p>
                  <p><strong>Карта:</strong> ${currentUser.card ? '**** **** **** ' + currentUser.card.slice(-4) : 'не указана'}</p>
                </div>
                <button class="logout-btn" onclick="logout()">Выйти</button>
              </div>
            `;
            }

            window.logout = function () {
                localStorage.removeItem('currentUser');
                currentUser = null;
                renderCabinet();
                showToast('Вы вышли из аккаунта');
            };

            //==========ДОСТАВКА==========
            window.openDeliveryModal = function () {
                if (cart.length === 0) {
                    showToast('Корзина пуста', true);
                    return;
                }
                const today = new Date().toISOString().split('T')[0];
                document.getElementById('delivery-date').min = today;
                document.getElementById('delivery-date').value = '';
                document.getElementById('delivery-time').value = '';
                document.getElementById('delivery-city').value = '';
                document.getElementById('delivery-street').value = '';
                document.getElementById('delivery-house').value = '';
                document.getElementById('delivery-apartment').value = '';
                document.getElementById('delivery-private-house').checked = false;
                document.getElementById('delivery-apartment').disabled = false;
                document.getElementById('delivery-confirm-btn').disabled = true;
                document.getElementById('deliveryModal').classList.add('active');
            };

            window.closeDeliveryModal = function () {
                document.getElementById('deliveryModal').classList.remove('active');
            };

            window.toggleApartment = function () {
                const isPrivate = document.getElementById('delivery-private-house').checked;
                const aptInput = document.getElementById('delivery-apartment');
                aptInput.disabled = isPrivate;
                if (isPrivate) aptInput.value = '';
                validateDeliveryForm();
            };

            window.validateDeliveryForm = function () {
                const city = document.getElementById('delivery-city').value.trim();
                const street = document.getElementById('delivery-street').value.trim();
                const house = document.getElementById('delivery-house').value.trim();
                const apt = document.getElementById('delivery-apartment').value.trim();
                const isPrivate = document.getElementById('delivery-private-house').checked;
                const date = document.getElementById('delivery-date').value;
                const time = document.getElementById('delivery-time').value;
                const confirmBtn = document.getElementById('delivery-confirm-btn');

                let valid = true;
                if (!city || !street || !house) valid = false;
                if (!isPrivate && !apt) valid = false;
                if (!date || !time) valid = false;

                if (date && time) {
                    const selectedDate = new Date(date);
                    const now = new Date();
                    const today = new Date(now.getFullYear(), now.getMonth(), now.getDate());
                    if (selectedDate < today) valid = false;
                    if (selectedDate.toDateString() === today.toDateString()) {
                        const currentHour = now.getHours();
                        const selectedHour = parseInt(time.split('-')[0]);
                        if (selectedHour <= currentHour) valid = false;
                    }
                }

                confirmBtn.disabled = !valid;
            };

            window.confirmOrder = function () {
                if (!document.getElementById('delivery-confirm-btn').disabled) {
                    const city = document.getElementById('delivery-city').value.trim();
                    const street = document.getElementById('delivery-street').value.trim();
                    const house = document.getElementById('delivery-house').value.trim();
                    const apt = document.getElementById('delivery-apartment').value.trim();
                    const isPrivate = document.getElementById('delivery-private-house').checked;
                    const date = document.getElementById('delivery-date').value;
                    const time = document.getElementById('delivery-time').value;
                    const total = cart.reduce((sum, item) => sum + item.product.price * item.quantity, 0);

                    let address = `${city}, ${street}, д. ${house}`;
                    if (!isPrivate && apt) address += `, кв. ${apt}`;
                    else if (isPrivate) address += ' (частный дом)';

                    showToast(`Заказ на сумму ${total} ₽ оформлен! Доставка: ${address}, ${date} ${time.replace('-', ' – ')}`);
                    cart = [];
                    updateCartUI();
                    renderCatalog(products); // обновляем кнопки после очистки корзины
                    closeDeliveryModal();
                }
            };

            //==========ТОСТЫ==========
            function showToast(msg, isError = false) {
                const toast = document.getElementById('successToast');
                document.getElementById('toast-message').innerText = msg;
                toast.classList.remove('error');
                if (isError) toast.classList.add('error');
                toast.classList.add('show');
                setTimeout(() => toast.classList.remove('show'), 4000);
            }

            //==========ИНИЦИАЛИЗАЦИЯ==========
            renderHits();
            updateCartUI();
        })();
        document.addEventListener('DOMContentLoaded', () => {

            // Маска карты
            const card = document.getElementById('card-number');
            if (card) {
                card.addEventListener('input', function () {
                    const d = this.value.replace(/\D/g, '');
                    if (d.length >= 6) {
                        this.value = d.slice(0, 4) + ' **** **** ' + d.slice(-2);
                    }
                });
            }

            // Телефон
            const phone = document.getElementById('phone');
            if (phone) {
                phone.addEventListener('input', function () {
                    this.value = this.value.replace(/[^0-9+]/g, '');
                });
            }

            // Квартира
            const noApt = document.getElementById('no-apartment');
            if (noApt) {
                noApt.addEventListener('change', function () {
                    const apt = document.getElementById('apartment');
                    if (!apt) return;
                    if (this.checked) {
                        apt.value = '';
                        apt.disabled = true;
                    } else {
                        apt.disabled = false;
                    }
                });
            }

            // Пароль
            function validatePassword(p) {
                return /^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&]).{8,}$/.test(p);
            }

            // Срок карты
            function validateExpiry() {
                const el = document.getElementById('card-expiry');
                if (!el) return true;

                const value = el.value;
                if (!value) return false;

                const [y, m] = value.split('-').map(Number);
                const now = new Date();

                if (y < now.getFullYear()) return false;
                if (y === now.getFullYear() && m < now.getMonth() + 1) return false;
                if (y > now.getFullYear() + 15) return false;

                return true;
            }

            // submit (НЕ ломаем существующие)
            document.querySelectorAll('form').forEach(f => {
                f.addEventListener('submit', function (e) {
                    const pass = document.getElementById('password')?.value;

                    if (pass && !validatePassword(pass)) {
                        alert('Слабый пароль');
                        e.preventDefault();
                    }

                    if (!validateExpiry()) {
                        alert('Ошибка даты карты');
                        e.preventDefault();
                    }
                });
            });

        });

    </script>
</body>
</html>
