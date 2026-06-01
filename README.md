# EBAF-BUSINESS-CENTER(imprimerie)[ebaf_business_center.html](https://github.com/user-attachments/files/28462999/ebaf_business_center.html)
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>EBAF Business Center - Impression · Broderie · Création | Abidjan</title>
<meta name="description" content="EBAF Business Center - Votre partenaire en impression, broderie et personnalisation à Abidjan. Flyers, affiches, t-shirts DTF, broderie, tasses personnalisées. Commander en ligne, paiement Mobile Money.">
<meta name="keywords" content="impression Abidjan, imprimerie Côte d'Ivoire, broderie Abidjan, personnalisation textile, flyers Abidjan, t-shirts personnalisés, cartes de visite Abidjan">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">
<style>
:root {
  --blue: #1a3fa0;
  --cyan: #00bcd4;
  --violet: #7c3aed;
  --magenta: #d946ef;
  --orange: #f97316;
  --yellow: #eab308;
  --dark: #0a0f1e;
  --darker: #060b16;
  --card-bg: #111827;
  --card-border: rgba(255,255,255,0.08);
  --text: #f1f5f9;
  --text-muted: #94a3b8;
  --gradient-main: linear-gradient(135deg, #1a3fa0 0%, #7c3aed 50%, #d946ef 100%);
  --gradient-warm: linear-gradient(135deg, #f97316 0%, #eab308 100%);
  --gradient-cool: linear-gradient(135deg, #00bcd4 0%, #1a3fa0 100%);
}

* { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--dark);
  color: var(--text);
  overflow-x: hidden;
}

/* SCROLLBAR */
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: var(--darker); }
::-webkit-scrollbar-thumb { background: var(--blue); border-radius: 3px; }

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
  background: rgba(10,15,30,0.92);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(255,255,255,0.06);
  padding: 0 5%;
  display: flex; align-items: center; justify-content: space-between;
  height: 72px;
  transition: all 0.3s;
}

.nav-logo img {
  height: 52px;
  object-fit: contain;
}

.nav-links {
  display: flex; gap: 2rem; list-style: none;
}

.nav-links a {
  color: var(--text-muted);
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 0.02em;
  transition: color 0.2s;
}

.nav-links a:hover { color: var(--text); }

.nav-cta {
  display: flex; gap: 0.75rem; align-items: center;
}

.btn-primary {
  background: var(--gradient-main);
  color: #fff;
  border: none;
  padding: 0.6rem 1.4rem;
  border-radius: 50px;
  font-size: 0.88rem;
  font-weight: 600;
  cursor: pointer;
  text-decoration: none;
  transition: transform 0.2s, box-shadow 0.2s;
  font-family: 'DM Sans', sans-serif;
}

.btn-primary:hover {
  transform: translateY(-1px);
  box-shadow: 0 8px 30px rgba(124,58,237,0.4);
}

.btn-outline {
  background: transparent;
  color: var(--text);
  border: 1px solid rgba(255,255,255,0.2);
  padding: 0.6rem 1.4rem;
  border-radius: 50px;
  font-size: 0.88rem;
  font-weight: 500;
  cursor: pointer;
  text-decoration: none;
  transition: all 0.2s;
  font-family: 'DM Sans', sans-serif;
}

.btn-outline:hover {
  border-color: var(--cyan);
  color: var(--cyan);
}

.hamburger {
  display: none;
  flex-direction: column; gap: 5px; cursor: pointer;
  background: none; border: none;
}

.hamburger span {
  display: block; width: 24px; height: 2px;
  background: var(--text); border-radius: 2px;
  transition: all 0.3s;
}

/* HERO */
.hero {
  min-height: 100vh;
  display: flex; align-items: center;
  position: relative;
  padding: 8rem 5% 4rem;
  overflow: hidden;
}

.hero-bg {
  position: absolute; inset: 0;
  background: radial-gradient(ellipse 80% 60% at 60% 40%, rgba(26,63,160,0.25) 0%, transparent 60%),
              radial-gradient(ellipse 60% 50% at 80% 60%, rgba(124,58,237,0.2) 0%, transparent 60%),
              radial-gradient(ellipse 50% 40% at 20% 70%, rgba(0,188,212,0.15) 0%, transparent 60%),
              var(--darker);
}

.hero-grid {
  position: absolute; inset: 0;
  background-image: linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
                    linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
  background-size: 60px 60px;
}

.hero-content {
  position: relative; z-index: 2;
  max-width: 650px;
}

.hero-badge {
  display: inline-flex; align-items: center; gap: 0.5rem;
  background: rgba(0,188,212,0.1);
  border: 1px solid rgba(0,188,212,0.3);
  color: var(--cyan);
  padding: 0.4rem 1rem;
  border-radius: 50px;
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  margin-bottom: 1.5rem;
}

.hero-badge::before {
  content: '';
  width: 6px; height: 6px;
  background: var(--cyan);
  border-radius: 50%;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(1.3); }
}

.hero h1 {
  font-family: 'Syne', sans-serif;
  font-size: clamp(2.8rem, 6vw, 5rem);
  font-weight: 800;
  line-height: 1.05;
  margin-bottom: 1.2rem;
}

.hero h1 span {
  background: var(--gradient-main);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-sub {
  font-size: 1.2rem;
  color: var(--text-muted);
  line-height: 1.6;
  margin-bottom: 0.75rem;
}

.hero-slogan {
  font-family: 'Syne', sans-serif;
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  color: var(--orange);
  margin-bottom: 2rem;
}

.hero-actions {
  display: flex; gap: 1rem; flex-wrap: wrap;
  margin-bottom: 3rem;
}

.btn-wa {
  background: #25D366;
  color: #fff;
  border: none;
  padding: 0.75rem 1.6rem;
  border-radius: 50px;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  text-decoration: none;
  display: inline-flex; align-items: center; gap: 0.5rem;
  transition: transform 0.2s, box-shadow 0.2s;
  font-family: 'DM Sans', sans-serif;
}

.btn-wa:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(37,211,102,0.35);
}

.btn-lg {
  padding: 0.85rem 2rem;
  font-size: 1rem;
}

.hero-stats {
  display: flex; gap: 2.5rem;
}

.stat {
  text-align: center;
}

.stat-num {
  font-family: 'Syne', sans-serif;
  font-size: 2rem;
  font-weight: 800;
  background: var(--gradient-main);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.stat-label {
  font-size: 0.78rem;
  color: var(--text-muted);
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.hero-visual {
  position: absolute;
  right: 5%;
  top: 50%;
  transform: translateY(-50%);
  width: 420px;
  z-index: 1;
}

.hero-logo-display {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 24px;
  padding: 2.5rem;
  backdrop-filter: blur(10px);
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero-logo-display::before {
  content: '';
  position: absolute; inset: -2px;
  background: var(--gradient-main);
  border-radius: 26px;
  z-index: -1;
  opacity: 0.4;
}

.hero-logo-display img {
  width: 100%;
  max-width: 340px;
}

/* SECTION BASE */
section {
  padding: 5rem 5%;
}

.section-label {
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--cyan);
  margin-bottom: 0.75rem;
}

.section-title {
  font-family: 'Syne', sans-serif;
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: 1rem;
}

.section-title span {
  background: var(--gradient-main);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.section-sub {
  color: var(--text-muted);
  font-size: 1.1rem;
  max-width: 600px;
  line-height: 1.6;
}

/* SERVICES */
#services {
  background: var(--darker);
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin-top: 3rem;
}

.service-card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 20px;
  overflow: hidden;
  transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
  cursor: pointer;
}

.service-card:hover {
  transform: translateY(-6px);
  border-color: rgba(124,58,237,0.4);
  box-shadow: 0 20px 60px rgba(124,58,237,0.15);
}

.service-mockup {
  width: 100%;
  height: 200px;
  position: relative;
  overflow: hidden;
  display: flex; align-items: center; justify-content: center;
}

/* MOCKUPS SVG placeholders */
.mockup-print { background: linear-gradient(135deg, #0d1b4b 0%, #1a3fa0 100%); }
.mockup-textile { background: linear-gradient(135deg, #2d0b4e 0%, #7c3aed 100%); }
.mockup-perso { background: linear-gradient(135deg, #4a0a2e 0%, #d946ef 100%); }
.mockup-design { background: linear-gradient(135deg, #3d1a00 0%, #f97316 100%); }

.mockup-inner {
  display: flex; align-items: center; justify-content: center;
  width: 100%; height: 100%;
  padding: 1.5rem;
}

.service-info { padding: 1.5rem; }

.service-icon {
  width: 44px; height: 44px;
  border-radius: 12px;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.5rem;
  margin-bottom: 0.75rem;
}

.service-name {
  font-family: 'Syne', sans-serif;
  font-size: 1.2rem;
  font-weight: 700;
  margin-bottom: 0.4rem;
}

.service-desc {
  color: var(--text-muted);
  font-size: 0.88rem;
  line-height: 1.5;
  margin-bottom: 0.75rem;
}

.service-items {
  display: flex; flex-wrap: wrap; gap: 0.4rem;
}

.pill {
  background: rgba(255,255,255,0.06);
  border: 1px solid rgba(255,255,255,0.1);
  color: var(--text-muted);
  padding: 0.25rem 0.7rem;
  border-radius: 50px;
  font-size: 0.75rem;
}

/* BOUTIQUE */
#boutique { background: var(--dark); }

.product-tabs {
  display: flex; gap: 0.5rem; flex-wrap: wrap;
  margin: 2rem 0;
}

.tab-btn {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.1);
  color: var(--text-muted);
  padding: 0.5rem 1.2rem;
  border-radius: 50px;
  font-size: 0.85rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s;
  font-family: 'DM Sans', sans-serif;
}

.tab-btn.active, .tab-btn:hover {
  background: var(--gradient-main);
  border-color: transparent;
  color: #fff;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1.5rem;
}

.product-card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 20px;
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s;
}

.product-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 50px rgba(26,63,160,0.2);
}

.product-img {
  width: 100%;
  height: 180px;
  display: flex; align-items: center; justify-content: center;
  font-size: 4rem;
  position: relative;
  overflow: hidden;
}

.product-details { padding: 1.25rem; }

.product-name {
  font-family: 'Syne', sans-serif;
  font-size: 1.05rem;
  font-weight: 700;
  margin-bottom: 0.3rem;
}

.product-meta {
  font-size: 0.8rem;
  color: var(--text-muted);
  margin-bottom: 0.75rem;
}

.product-price {
  font-family: 'Syne', sans-serif;
  font-size: 1.4rem;
  font-weight: 800;
  color: var(--cyan);
  margin-bottom: 0.75rem;
}

.product-price small {
  font-size: 0.75rem;
  color: var(--text-muted);
  font-weight: 400;
  font-family: 'DM Sans', sans-serif;
}

.product-actions {
  display: flex; gap: 0.5rem;
}

.btn-add-cart {
  flex: 1;
  background: var(--gradient-main);
  border: none;
  color: #fff;
  padding: 0.6rem 1rem;
  border-radius: 50px;
  font-size: 0.85rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.2s;
  font-family: 'DM Sans', sans-serif;
}

.btn-add-cart:hover {
  opacity: 0.9;
  transform: scale(1.02);
}

.btn-quick {
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.1);
  color: var(--text);
  padding: 0.6rem 0.9rem;
  border-radius: 50px;
  font-size: 0.85rem;
  cursor: pointer;
  transition: all 0.2s;
}

.btn-quick:hover {
  background: rgba(255,255,255,0.12);
}

/* PANIER */
#cart-panel {
  position: fixed; right: -420px; top: 0; bottom: 0;
  width: 420px;
  background: #0d1117;
  border-left: 1px solid rgba(255,255,255,0.1);
  z-index: 2000;
  transition: right 0.35s cubic-bezier(.4,0,.2,1);
  display: flex; flex-direction: column;
  overflow: hidden;
}

#cart-panel.open { right: 0; box-shadow: -20px 0 60px rgba(0,0,0,0.5); }

.cart-header {
  padding: 1.5rem;
  border-bottom: 1px solid rgba(255,255,255,0.08);
  display: flex; justify-content: space-between; align-items: center;
}

.cart-title {
  font-family: 'Syne', sans-serif;
  font-size: 1.25rem;
  font-weight: 700;
}

.cart-close {
  background: rgba(255,255,255,0.08);
  border: none;
  color: var(--text);
  width: 36px; height: 36px;
  border-radius: 50%;
  font-size: 1.2rem;
  cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  transition: background 0.2s;
}

.cart-close:hover { background: rgba(255,255,255,0.15); }

.cart-items {
  flex: 1; overflow-y: auto;
  padding: 1.25rem;
}

.cart-item {
  display: flex; gap: 1rem; align-items: start;
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 14px;
  padding: 1rem;
  margin-bottom: 0.75rem;
}

.cart-item-emoji {
  font-size: 2.5rem;
  width: 60px; height: 60px;
  background: rgba(255,255,255,0.05);
  border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
}

.cart-item-name {
  font-weight: 600;
  font-size: 0.9rem;
  margin-bottom: 0.3rem;
}

.cart-item-price { color: var(--cyan); font-size: 0.9rem; }

.cart-qty {
  display: flex; align-items: center; gap: 0.5rem;
  margin-top: 0.5rem;
}

.qty-btn {
  background: rgba(255,255,255,0.1);
  border: none; color: #fff;
  width: 28px; height: 28px;
  border-radius: 50%;
  cursor: pointer;
  font-size: 1rem;
  display: flex; align-items: center; justify-content: center;
  transition: background 0.2s;
}

.qty-btn:hover { background: rgba(255,255,255,0.18); }

.qty-val { min-width: 28px; text-align: center; font-weight: 600; font-size: 0.9rem; }

.remove-item {
  background: none; border: none;
  color: var(--text-muted); cursor: pointer;
  font-size: 1.1rem;
  margin-left: auto;
  transition: color 0.2s;
}

.remove-item:hover { color: #ef4444; }

.cart-footer {
  padding: 1.5rem;
  border-top: 1px solid rgba(255,255,255,0.08);
}

.cart-total-row {
  display: flex; justify-content: space-between; align-items: center;
  margin-bottom: 0.5rem;
}

.cart-total-label { color: var(--text-muted); font-size: 0.9rem; }
.cart-total-val { font-family: 'Syne', sans-serif; font-size: 1.1rem; font-weight: 700; }

.cart-grand {
  font-size: 1.4rem;
  color: var(--cyan);
}

.btn-checkout {
  width: 100%;
  background: var(--gradient-main);
  border: none; color: #fff;
  padding: 1rem;
  border-radius: 14px;
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  margin-top: 1.25rem;
  transition: opacity 0.2s;
  font-family: 'DM Sans', sans-serif;
}

.btn-checkout:hover { opacity: 0.9; }

.cart-badge {
  position: absolute; top: -6px; right: -6px;
  background: var(--orange);
  color: #fff;
  width: 20px; height: 20px;
  border-radius: 50%;
  font-size: 0.72rem;
  font-weight: 700;
  display: flex; align-items: center; justify-content: center;
}

.cart-overlay {
  display: none;
  position: fixed; inset: 0;
  background: rgba(0,0,0,0.6);
  z-index: 1999;
}

.cart-overlay.active { display: block; }

/* UPLOAD COMMANDE */
#commander { background: var(--darker); }

.order-form {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 24px;
  padding: 2.5rem;
  max-width: 700px;
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-label {
  display: block;
  font-size: 0.88rem;
  font-weight: 600;
  color: var(--text-muted);
  letter-spacing: 0.04em;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}

.form-control {
  width: 100%;
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 12px;
  padding: 0.75rem 1rem;
  color: var(--text);
  font-family: 'DM Sans', sans-serif;
  font-size: 0.95rem;
  transition: border-color 0.2s;
  outline: none;
}

.form-control:focus {
  border-color: var(--cyan);
}

.form-control option { background: #111827; }

.upload-zone {
  border: 2px dashed rgba(255,255,255,0.15);
  border-radius: 16px;
  padding: 2.5rem;
  text-align: center;
  cursor: pointer;
  transition: all 0.2s;
  background: rgba(255,255,255,0.02);
}

.upload-zone:hover {
  border-color: var(--cyan);
  background: rgba(0,188,212,0.05);
}

.upload-icon { font-size: 3rem; margin-bottom: 0.75rem; }

.upload-text {
  font-size: 0.95rem;
  color: var(--text-muted);
  margin-bottom: 0.4rem;
}

.upload-formats {
  font-size: 0.8rem;
  color: rgba(255,255,255,0.3);
}

/* PAIEMENT */
#paiement { background: var(--dark); }

.payment-methods {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.25rem;
  margin-top: 2.5rem;
}

.payment-card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 20px;
  padding: 1.75rem;
  text-align: center;
  transition: all 0.3s;
  cursor: pointer;
}

.payment-card:hover {
  transform: translateY(-4px);
  border-color: rgba(255,255,255,0.2);
}

.payment-logo {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.payment-name {
  font-family: 'Syne', sans-serif;
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: 0.25rem;
}

.payment-desc {
  font-size: 0.8rem;
  color: var(--text-muted);
}

/* TEMOIGNAGES */
#temoignages { background: var(--darker); }

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 3rem;
}

.testimonial-card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 20px;
  padding: 1.75rem;
  position: relative;
}

.testimonial-card::before {
  content: '"';
  font-family: 'Syne', sans-serif;
  font-size: 5rem;
  color: rgba(124,58,237,0.2);
  position: absolute;
  top: 0.5rem; left: 1.25rem;
  line-height: 1;
}

.stars {
  color: var(--yellow);
  font-size: 1rem;
  margin-bottom: 1rem;
}

.testimonial-text {
  color: var(--text-muted);
  font-size: 0.92rem;
  line-height: 1.6;
  margin-bottom: 1.25rem;
}

.testimonial-author {
  display: flex; align-items: center; gap: 0.75rem;
}

.author-avatar {
  width: 42px; height: 42px;
  border-radius: 50%;
  background: var(--gradient-main);
  display: flex; align-items: center; justify-content: center;
  font-weight: 700;
  font-size: 1rem;
}

.author-name {
  font-weight: 600;
  font-size: 0.9rem;
}

.author-role {
  font-size: 0.78rem;
  color: var(--text-muted);
}

/* GALERIE */
#galerie { background: var(--dark); }

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1rem;
  margin-top: 2.5rem;
}

.gallery-item {
  border-radius: 16px;
  overflow: hidden;
  cursor: pointer;
  position: relative;
  aspect-ratio: 1;
  display: flex; align-items: center; justify-content: center;
  font-size: 4rem;
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  transition: transform 0.3s;
}

.gallery-item:hover {
  transform: scale(1.03);
}

.gallery-item .gallery-label {
  position: absolute; bottom: 0; left: 0; right: 0;
  background: linear-gradient(0deg, rgba(0,0,0,0.8) 0%, transparent 100%);
  padding: 1rem 0.75rem 0.75rem;
  font-size: 0.8rem;
  font-weight: 600;
  color: #fff;
}

/* CONTACT */
#contact { background: var(--darker); }

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  margin-top: 3rem;
}

.contact-info-item {
  display: flex; gap: 1rem; align-items: start;
  margin-bottom: 1.75rem;
}

.contact-icon {
  width: 48px; height: 48px;
  background: rgba(124,58,237,0.15);
  border: 1px solid rgba(124,58,237,0.3);
  border-radius: 14px;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.4rem;
  flex-shrink: 0;
}

.contact-detail-label {
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-muted);
  margin-bottom: 0.35rem;
}

.contact-detail-val {
  font-size: 0.95rem;
  line-height: 1.5;
}

.map-placeholder {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 20px;
  overflow: hidden;
  height: 320px;
  display: flex; align-items: center; justify-content: center;
  flex-direction: column;
  color: var(--text-muted);
  gap: 0.75rem;
}

.map-placeholder iframe {
  width: 100%; height: 100%;
  border: none;
}

/* MODAL CHECKOUT */
#checkout-modal {
  display: none;
  position: fixed; inset: 0;
  z-index: 3000;
  align-items: center;
  justify-content: center;
}

#checkout-modal.open { display: flex; }

.modal-overlay {
  position: absolute; inset: 0;
  background: rgba(0,0,0,0.7);
}

.modal-box {
  position: relative; z-index: 1;
  background: #0d1117;
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 24px;
  padding: 2.5rem;
  width: 90%; max-width: 540px;
  max-height: 90vh;
  overflow-y: auto;
}

.modal-title {
  font-family: 'Syne', sans-serif;
  font-size: 1.5rem;
  font-weight: 800;
  margin-bottom: 0.5rem;
}

.modal-sub {
  color: var(--text-muted);
  font-size: 0.9rem;
  margin-bottom: 1.75rem;
}

.payment-options {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
  margin-bottom: 1.75rem;
}

.pay-opt {
  background: rgba(255,255,255,0.04);
  border: 2px solid rgba(255,255,255,0.08);
  border-radius: 14px;
  padding: 1rem;
  text-align: center;
  cursor: pointer;
  transition: all 0.2s;
}

.pay-opt:hover, .pay-opt.selected {
  border-color: var(--cyan);
  background: rgba(0,188,212,0.08);
}

.pay-opt-icon { font-size: 2rem; margin-bottom: 0.4rem; }

.pay-opt-name { font-size: 0.85rem; font-weight: 600; }

.phone-input {
  margin-bottom: 1.25rem;
}

/* WHATSAPP FLOAT */
.wa-float {
  position: fixed;
  bottom: 2rem; right: 2rem;
  z-index: 999;
  width: 60px; height: 60px;
  background: #25D366;
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 8px 30px rgba(37,211,102,0.4);
  text-decoration: none;
  font-size: 1.8rem;
  animation: float 3s ease-in-out infinite;
  transition: transform 0.2s;
}

.wa-float:hover {
  transform: scale(1.1);
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-8px); }
}

/* CART BUTTON */
.cart-btn {
  position: relative;
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.12);
  color: #fff;
  width: 42px; height: 42px;
  border-radius: 50%;
  cursor: pointer;
  font-size: 1.2rem;
  display: flex; align-items: center; justify-content: center;
  transition: background 0.2s;
}

.cart-btn:hover { background: rgba(255,255,255,0.14); }

/* FOOTER */
footer {
  background: #060b16;
  padding: 3rem 5% 1.5rem;
  border-top: 1px solid rgba(255,255,255,0.06);
}

.footer-top {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 2rem;
  margin-bottom: 2.5rem;
}

.footer-logo img { height: 48px; margin-bottom: 1rem; }

.footer-desc {
  color: var(--text-muted);
  font-size: 0.88rem;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.footer-socials { display: flex; gap: 0.5rem; }

.social-link {
  width: 36px; height: 36px;
  background: rgba(255,255,255,0.07);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 1rem;
  text-decoration: none;
  transition: background 0.2s;
}

.social-link:hover { background: rgba(255,255,255,0.12); }

.footer-heading {
  font-family: 'Syne', sans-serif;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 1rem;
  color: var(--text);
}

.footer-links {
  list-style: none;
  display: flex; flex-direction: column; gap: 0.6rem;
}

.footer-links a {
  color: var(--text-muted);
  text-decoration: none;
  font-size: 0.88rem;
  transition: color 0.2s;
}

.footer-links a:hover { color: var(--text); }

.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.06);
  padding-top: 1.5rem;
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 1rem;
}

.footer-copy {
  color: var(--text-muted);
  font-size: 0.82rem;
}

/* NOTIFICATION */
.toast {
  position: fixed;
  bottom: 6rem; right: 2rem;
  background: #1a2740;
  border: 1px solid rgba(0,188,212,0.4);
  border-radius: 14px;
  padding: 0.9rem 1.25rem;
  font-size: 0.88rem;
  font-weight: 600;
  color: var(--cyan);
  z-index: 4000;
  transform: translateY(20px);
  opacity: 0;
  transition: all 0.35s;
  pointer-events: none;
}

.toast.show {
  transform: translateY(0);
  opacity: 1;
}

/* ADMIN PANEL */
#admin-panel {
  display: none;
  position: fixed; inset: 0;
  z-index: 5000;
  background: #060b16;
  overflow-y: auto;
}

#admin-panel.open { display: block; }

.admin-nav {
  background: #0d1117;
  padding: 1rem 2rem;
  display: flex; align-items: center; justify-content: space-between;
  border-bottom: 1px solid rgba(255,255,255,0.08);
  position: sticky; top: 0; z-index: 10;
}

.admin-content { padding: 2rem; }

.admin-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.25rem;
  margin-bottom: 2.5rem;
}

.admin-card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 16px;
  padding: 1.5rem;
}

.admin-stat-num {
  font-family: 'Syne', sans-serif;
  font-size: 2.2rem;
  font-weight: 800;
  background: var(--gradient-main);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.admin-stat-label {
  font-size: 0.82rem;
  color: var(--text-muted);
  margin-top: 0.25rem;
}

.admin-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.88rem;
}

.admin-table th {
  text-align: left;
  padding: 0.75rem 1rem;
  background: rgba(255,255,255,0.04);
  border-bottom: 1px solid rgba(255,255,255,0.08);
  font-weight: 600;
  font-size: 0.78rem;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: var(--text-muted);
}

.admin-table td {
  padding: 0.9rem 1rem;
  border-bottom: 1px solid rgba(255,255,255,0.05);
}

.badge-status {
  padding: 0.25rem 0.7rem;
  border-radius: 50px;
  font-size: 0.75rem;
  font-weight: 600;
}

.badge-success { background: rgba(16,185,129,0.15); color: #10b981; }
.badge-pending { background: rgba(245,158,11,0.15); color: #f59e0b; }
.badge-new { background: rgba(0,188,212,0.15); color: var(--cyan); }

/* ANIMATIONS */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-in {
  animation: fadeInUp 0.6s ease forwards;
}

/* RESPONSIVE */
@media (max-width: 1024px) {
  .hero-visual { display: none; }
  .footer-top { grid-template-columns: 1fr 1fr; }
  .contact-grid { grid-template-columns: 1fr; }
}

@media (max-width: 768px) {
  .nav-links, .nav-cta .btn-outline { display: none; }
  .hamburger { display: flex; }
  .hero-stats { gap: 1.5rem; }
  .footer-top { grid-template-columns: 1fr; }
  .payment-options { grid-template-columns: 1fr 1fr; }
  #cart-panel { width: 100%; right: -100%; }
}

@media (max-width: 480px) {
  .hero h1 { font-size: 2.2rem; }
  .hero-stats { flex-wrap: wrap; gap: 1rem; }
  .stat-num { font-size: 1.6rem; }
  .hero-actions { flex-direction: column; }
  .btn-lg { text-align: center; }
}

/* PRODUCT MOCKUPS */
.mock-flyer {
  background: linear-gradient(135deg, #1a3fa0 0%, #0d1b4b 100%);
  width: 120px; height: 155px;
  border-radius: 6px;
  border: 3px solid rgba(255,255,255,0.2);
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  gap: 6px; padding: 10px;
  box-shadow: 8px 8px 20px rgba(0,0,0,0.5);
}

.mock-flyer-line {
  width: 80%; height: 5px;
  background: rgba(255,255,255,0.4);
  border-radius: 3px;
}

.mock-flyer-line.thick {
  height: 8px;
  background: rgba(255,255,255,0.7);
}

.mock-flyer-img {
  width: 70%; height: 45px;
  background: linear-gradient(135deg, var(--cyan), var(--violet));
  border-radius: 4px;
  opacity: 0.8;
}

.mock-tshirt {
  position: relative;
  width: 130px; height: 130px;
}

.mock-polo-shape {
  width: 110px; height: 110px;
  background: linear-gradient(135deg, #1e1b4b 0%, #7c3aed 100%);
  clip-path: polygon(20% 0%, 80% 0%, 100% 25%, 100% 100%, 0% 100%, 0% 25%);
  display: flex; align-items: center; justify-content: center;
  position: relative;
}

.mock-polo-collar {
  position: absolute;
  top: 0; left: 50%; transform: translateX(-50%);
  width: 40px; height: 20px;
  background: #2d1f6e;
  clip-path: polygon(0 0, 100% 0, 80% 100%, 20% 100%);
}

.mock-polo-logo {
  width: 35px; height: 35px;
  background: radial-gradient(circle, #d946ef, #f97316);
  border-radius: 50%;
  margin-top: 15px;
}

.mock-mug {
  width: 90px; height: 90px;
  background: linear-gradient(135deg, #4a0a2e 0%, #d946ef 100%);
  border-radius: 8px 8px 12px 12px;
  position: relative;
  display: flex; align-items: center; justify-content: center;
  box-shadow: 5px 5px 15px rgba(0,0,0,0.4);
}

.mock-mug::after {
  content: '';
  position: absolute; right: -18px; top: 20px;
  width: 16px; height: 30px;
  border: 4px solid rgba(255,255,255,0.4);
  border-left: none;
  border-radius: 0 20px 20px 0;
}

.mock-mug-design {
  width: 45px; height: 45px;
  background: radial-gradient(circle, #fff8, #fff2);
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.5rem;
}

.mock-card-vis {
  width: 140px; height: 85px;
  background: linear-gradient(135deg, #1a3fa0 0%, #7c3aed 100%);
  border-radius: 8px;
  border: 1px solid rgba(255,255,255,0.2);
  padding: 10px;
  display: flex; flex-direction: column; justify-content: space-between;
  box-shadow: 4px 4px 12px rgba(0,0,0,0.5);
}

.mock-card-name {
  font-size: 0.6rem; font-weight: 700; color: #fff; letter-spacing: 0.05em;
}

.mock-card-chip {
  width: 24px; height: 18px;
  background: linear-gradient(135deg, #eab308, #f97316);
  border-radius: 3px;
}

.mock-bottle {
  width: 60px; height: 120px;
  background: linear-gradient(180deg, #00bcd4 0%, #1a3fa0 100%);
  border-radius: 8px 8px 4px 4px;
  position: relative;
  display: flex; align-items: center; justify-content: center;
  box-shadow: 4px 4px 12px rgba(0,0,0,0.4);
}

.mock-bottle::before {
  content: '';
  position: absolute; top: -12px; left: 50%; transform: translateX(-50%);
  width: 20px; height: 14px;
  background: #0a7a8a;
  border-radius: 4px 4px 0 0;
}

.mock-kakemono {
  width: 80px; height: 150px;
  background: linear-gradient(180deg, #1a3fa0 0%, #7c3aed 50%, #d946ef 100%);
  border-radius: 4px;
  border: 2px solid rgba(255,255,255,0.2);
  display: flex; flex-direction: column;
  align-items: center; padding: 12px 8px;
  gap: 6px; box-shadow: 6px 6px 16px rgba(0,0,0,0.4);
}

.mock-sticker {
  width: 100px; height: 100px;
  background: linear-gradient(135deg, #eab308, #f97316);
  border-radius: 16px;
  display: flex; align-items: center; justify-content: center;
  font-size: 2.5rem;
  box-shadow: 4px 4px 12px rgba(0,0,0,0.3);
  transform: rotate(-5deg);
}

.mock-poster {
  width: 105px; height: 148px;
  background: linear-gradient(135deg, #7c3aed 0%, #d946ef 100%);
  border-radius: 6px;
  border: 2px solid rgba(255,255,255,0.2);
  display: flex; flex-direction: column;
  align-items: center; justify-content: flex-start;
  padding: 10px 8px; gap: 5px;
  box-shadow: 8px 8px 20px rgba(0,0,0,0.5);
}

</style>
</head>
<body>

<!-- NAVIGATION -->
<nav id="navbar">
  <a href="#accueil" class="nav-logo">
    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/4gHYSUNDX1BST0ZJTEUAAQEAAAHIAAAAAAQwAABtbnRyUkdCIFhZWiAH4AABAAEAAAAAAABhY3NwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAA9tYAAQAAAADTLQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAlkZXNjAAAA8AAAACRyWFlaAAABFAAAABRnWFlaAAABKAAAABRiWFlaAAABPAAAABR3dHB0AAABUAAAABRyVFJDAAABZAAAAChnVFJDAAABZAAAAChiVFJDAAABZAAAAChjcHJ0AAABjAAAADxtbHVjAAAAAAAAAAEAAAAMZW5VUwAAAAgAAAAcAHMAUgBHAEJYWVogAAAAAAAAb6IAADj1AAADkFhZWiAAAAAAAABimQAAt4UAABjaWFlaIAAAAAAAACSgAAAPhAAAts9YWVogAAAAAAAA9tYAAQAAAADTLXBhcmEAAAAAAAQAAAACZmYAAPKnAAANWQAAE9AAAApbAAAAAAAAAABtbHVjAAAAAAAAAAEAAAAMZW5VUwAAACAAAAAcAEcAbwBvAGcAbABlACAASQBuAGMALgAgADIAMAAxADb/2wBDAAgGBgcGBQgHBwcJCQgKDBQNDAsLDBkSEw8UHRofHh0aHBwgJC4nICIsIxwcKDcpLDAxNDQ0Hyc5PTgyPC4zNDL/2wBDAQkJCQwLDBgNDRgyIRwhMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjL/wAARCAHRBDgDASIAAhEBAxEB/8QAHAABAAIDAQEBAAAAAAAAAAAAAAYHBAUIAwIB/8QAWRAAAQMCAgQGCwsKBQIEBwEBAQACAwQFBhEHEiExE0FRVWGRFBcicXSBkqGx0dIVFjI2QlJUk5SywSMzNTdTYnJzgrMkNMLh8EOiY4OEwwglRVZ14vFEZP/EABsBAQADAQEBAQAAAAAAAAAAAAADBAUCAQYH/8QAOBEAAgIBAgUCBAQFBAIDAQAAAAECAwQREhMUITFRMkEFM2GBInGhsSM0UsHRQmLh8BWRJEPx0v/aAAwDAQACEQMRAD8Av9ERAEREAREQBERAEREAREQBERAEREAREQHnUTxUtPLUTvEcMTC97zua0DMlaHDeMaDEs08NPDUU8kYD2sqGhpkYdzhkTsWDpJuYoMKyU7XZSVjhCOXLefRl41ELJKaB2ErqO5bk+ilOewgnIZ+c+JW6sbdU5v7fuUbsvh3KC7e5b6IiqF4IiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIsK7XGK0Wqpr5vgQsLsvnHiHjOQXqTb0R42ktWVJpLu3uhi6OgjdnDQxHMcWu7f+A8Sy7bRvuOjiogZtnppnTREb82kO2eIkeNQNtTJcb1cKuU6znuGs7lJOZVmYEfqW2oYci3htx5C0Z+hbtsOFjxS9tD53fxMlp/6kye2S4Nutko64HPhog49/j8+a2CguBazsGsrsPyk/kZXmDM/JB3dRB61OljXQ2Ta9jbxbuLUpe/Z/mgiIoiwEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAVR6UsUCWpdZqd/5Gmbr1BB+FIRsb4ht756FYeKL9Fh2xT1zyDIBqwsPy3ncPxPQFzVcaueqie+RxkqKuUuc473Fx3rRwKdW7X2X7lDNt7VL37/kbCzMIomSHfK4vVhYJkylrY89hax3pChVNEI42RjcxoaPEpbg9xbc5mfOgz6nD1rUvj/BaMCM//kp/mbO+mW1YsirqfNrpY2yjpcO5PWMlY9ur4blQxVcBzZIM8uQ8igmM6cuoKKqb8KKXUJ6CM/S1fWE7wKCodA93+Hlydl80nj61j5GjojY/boaGNdwM2dT7S6/csNF+AggEHMHjC/VSN4IiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAITkMzsCKvtKGKHW22ssdDJlX3AariDtih+U7x7R1ruut2SUUczmoR3MgWkTFRv9xe2nkzoonGKnyOx+Xwn+M7ugDlUSpIRPdYW72QN1z3+Jecz2yVeqz83A3IegLYWSH8nNMRte/LPoC+krrUIKC7I+futerm+7NxCzoUhw1+TvUPFrse3/ALc/wWlhbsC29qPB3SkcP2rR17PxXdq1ra+hhRtfMRf1ROLrAKzD1XHlm9rOEb327fWojR5Oh4Rvwoe6PSw7+rYfEVOaYhzdVwzaRkRyjjUHgabbcXwyDMRPdG8fObuPWFixhxKp1M2c38Ftdv2J/hm5cPCaSR2b4xmzpbyeL0ELfquKSaS21zHMdrGE5A/PbxdYPnVhwTMqIGTRnNjxmFkUTbW190b+PZujoz0REU5OEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQGBebvS2K0VNyrHasMDNYjjceIDpJyC5uud4qblWVl9r3f4irJ1ATsjj4gOjLLqUu0m4m98N/FjpZM7dQEvqHNOySQbD1fBHSSq5uMnZ9ZHSDYwnN+XEwcX4LYwqNkd77szcmzfLaux60zT2KHu+FKdc58Q4lJqCHg6KFvGW6x8e1aRsZmlbE3e8ho8alLWjW2DIDYFqxWi0MDNs6HrCzYs2NxieyQb2Oa4eIgrwibkF7OGcbu8Un20MXc9+pYkHcyOHFmVG8SU/BXYVAGTZ2B3jGw+gHxrf00nCMjePlNDusZrxxBSdkWrhQM3051/wCk7D+B8SwqpbLF/wCj6zKr4uO9Pbr/AN+xp43CaihlHwo/yMne3tPVmPEFJcMXEtPYUp2OzLDnx7yPGNviKilqkaKrgHnKOccE48hPwT15dazYi6nkBObHMdkct7SDv74IWPnxePk712ZN8Pu3Vp+66FjIsS3Vra6jbLsDx3MjR8lw3+sdBCy1OmmtUbCeq1CIi9PQiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAoXpJxcMMWAx0z/8A5jVgxwBu9g43+LcOk9ClldW09uoZ6yqkEcELC97jxALnK63qbE1+qsQ1mYhY7UpYidjct3VvPSVaxKeJPV9kV8i3ZHQ1Uw9zaMxyEcO/u5jyHk8Q8+a19qYXtmrXjupjkzoYFjXCSS4VbKRjjrTO7o/NZxlbpjGRsaxgyYwBrR0BbsVrLTx+5k2PSOvu/wBjOtMOvWh53RtLvHuHpUgY3atbZoS2kfMRtkfkO8P9yVtIxtU6MDLnumzIYMgvZq+GjuQvQLmZQj3JlaH61tpSd/BtHVs/BbhobIwseM2uGThyg71orIf/AJTTZ8jvvFbuLPYsC5aSZ9pivWqLfhEIqaY0lZLTkkGNxaD6Ct04isooa0fCeNSbokG/r2FfmJqXUnhqgO5kGo49I3eb0LFs8vCSS24nLhxrx/zG+sehVviUONQpLuVcX+BkSqfZ/wDUbmx3A0dWGPceCfkx+fF8134HvjkUxVfZ6pEpbnqnKRp5CpjaasT0wYXlzmDY473DiPf4j3lj4GTr/Cl9jer7aGwREWoSBERAEREAREQBERAEREARFX+lXEd2w5bbfLaavsZ8szmvPBtfmAM/lAruuDnJRRzKSitWWAi5u7aGMueT9mi9hO2hjLnk/ZovYVnkbPoQ8zE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs0XsJ20MZc8n7NF7CcjZ9BzMTpFFzd20MZc8n7NF7CdtDGXPJ+zRewnI2fQczE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs0XsJ20MZc8n7NF7CcjZ9BzMTpFFzd20MZc8n7NF7CdtDGXPJ+zRewnI2fQczE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs0XsJ20MZc8n7NF7CcjZ9BzMTpFF8sJMbSd5AX0qZYCIql0o4yv+HcSU1Laq808D6Rsjm8Ex2bi94zzc0ncAu663ZLajmc1BastpFzd20MZc8n7NF7CdtDGXPJ+zRewrPI2fQh5mJ0ii5u7aGMueT9mi9hO2hjLnk/ZovYTkbPoOZidIoubu2hjLnk/ZovYTtoYy55P2aL2E5Gz6DmYnSKLm7toYy55P2aL2E7aGMueT9mi9hORs+g5mJ0ii5u7aGMueT9mi9hO2hjLnk/ZovYTkbPoOZidIoubu2hjLnk/ZovYTtoYy55P2aL2E5Gz6DmYnSKLnJmlXGDN9zY/+Knj/BoWbBpjxRD8MUM/8yEj7pCclae8xA6ARUtSacK1uXZtlp5eUwzOZ5iHKS27TJhyqybWRVdE7jLo9dvW3M+ZRyxbY+x0roP3LERa61361XqPhLbcKepGWZEbwXDvt3jxrYqBproyRNPsERF4ehERAEREAREQBERAEREARFGsd4iOGcK1NbE8Nq35Q02YB7s8eR5BmfEvYxcmkjxvRaskqLm7toYy55P2aL2E7aGMueT9mi9hW+Rs+hBzMTpFFzd20MZc8n7NF7CdtDGXPJ+zRewnI2fQczE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs8XsKdaMcfXO93me13urE8ksevTOMbWZFvwm9yBnmNv9JXM8SyEXJnUb4yeha6IiqkwREQBERAEREAREQBFBNKeIbph2x0VRaqrseWSp1Hu1Guzbqk5d0DxhVT20MZc8n7NF7Cs14s7I7kQzujF6M6RRc3dtDGXPJ+zRewnbQxlzyfs0XsLvkbPoc8zE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs0XsJ20MZc8n7NF7CcjZ9BzMTpFFzd20MZc8n7NF7CdtDGXPJ+zRewnI2fQczE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs0XsJ20MZc8n7NF7CcjZ9BzMTpFFzd20MZc8n7NF7CdtDGXPJ+zRewnI2fQczE6RRc3dtDGXPJ+zRewnbQxlzyfs0XsJyNn0HMxOkUXN3bQxlzyfs8XsLoqjkdLQ08jzm98bXOPKSFDbRKrTd7kldin2PdERQkgREQBERAEREAREQBERAEREARFEdIOL2YUsDnQuBuFTnHTMG0g8bsujPrIXUIuclFHMpKK1ZCtKWKH3W4twtbZco4zrVkoOwEcX9Ppy5FWl2rIooxBCNSnhbkByD1neVmSE22heJXF9ZUHXncTmdbib4uPpzUYeDcq8U2ecTe7mPRyeNb1UFVBJdzLnLiSbfYzLNAdWSvlGUk+xgPyWcXWtqATuGZ4gvhm3bkAOILY2qDh7hGD8GPu3eLd58lbhHatDOyLe8jfQwiCGKAbo2hvj4/OvdrcnIAc8yvRo2qRHz1kte56jcvpq+QvaCJ00zIm73nIdCjn21OK1q9ESu0t4O3Uw5W59ZJ/FbmLbktfTta1jGN2taA0eILYMyGWSwbXq2z7THjtgl4Me9wCos0+zN0YEjfFv8xKhQllgqIZofzjHNc3v5qwyzhI3xnc9pbt6Rkq7fmCOVu3qIUFz/APjT+hXzIaXQkvf+xKqoRyTtqYx+RqWCQDoI2hfdnrexKt0Tz3URAz5WHcf+ci87c5s9DNANrqWdwA/ccTl1FY9fGYXxVrQcoe5lA+Uw7+rf1r4zJm67t0fzX/f0N2r8UVInzXBzQ4HMHcV+rVWesEkQhccyBm08oW1X0uLkxyKlZH3/AHO5R2vQIiKweBERAEREAREQBERAFVWnD9D2nwh/3VaqqrTh+h7T4Q/7qsYvzokV3oZSiIi2zPCIiAIiIAiIgCIiAIiIAiIgCIiAIiIDr6L80z+EL6XzF+aZ/CF9L5w1QqI01/G+j8Ab/cer3VEaa/jfR+AN/uPVrD+ciHI9BWyIi2SgEREAREQBERAEREAREQBERAEREB9xSyQStlhkfHI05tew5EHoIU/w3pbvVqeyG6H3SpBsJecpWjodx+PrCr1FHOuE1pJHUZyj2OqrBiS14moeyrZUCQDY+N2x8Z5HDi9C2y5Os95r7Dco6+3TuhnZybnDja4cYXReC8Y0mL7Xw0YbFWRZCop8/gnlHK0rKyMZ1dV2LlVyn0fckyIiqk4REQBERAEREAREQBUJpgxB7pYkZa4X509vbk7LcZXZF3UMh381dGIbxFYLBW3OXIiCMua0/KduaPGSAuVqiolq6mWpneXzSvMj3He5xOZKv4NesnN+xWyZ6LaeaIi1CmEREAREQBZlquU9ou1Lcac5S08gkb05bx3iNnjWGi8aTWjCeh1vb66C526mrqZ2tDURtkYegjNZKq7QziDsq0VFjmfnLSHhYQTvjcdo8TvvBWisG2HDm4mnCW6KYREUZ0EREAREQBERAVjpu+LVu8M/0OVGq8tN3xat3hn+hyo1bGH8pFDI9YREVshCIiAIiIAiIgCIiAIiIAiIgCIiALre3/o2l/ks9AXJC63t/wCjaX+Sz0BZ3xD/AE/ctYvuZKIizS2EREAREQBERAEREAREQBERAY1fXU9soJ62rkEcEDC97jxALne53ybFF/nv9WC2KMllHEdzQNx8XncTyKS6UcVvvd3bhe2y5U0DtaslbuzG8d5u7vnoVf3OoZHC2nhGpGG6rWjiaFrYVG2O+RQyLNz2o1d2uOYfLmSBsYOUr3tlCaOk1X/npDryHp5PEsWhp+zavsl4/IQHKMfOfy+JbloV+qLk97+xSvmorhr7n00ZBSWyUvA0RlcMnzZEfwjd+JWmt1Ga2rbEc9Qd08jib/zYpc1ozAyAG4AcSsmFmXdNqPjJfuW1fbhkvjPaV6Zbep9hbKys1q1zvmRkjxkD8Vqw7kWysr9Wtc3jfGR1EH8FBfrw2T4enGjr5JTBsAKz43ZkBaqKQjYs+B+eSxJo+uqkZxfwcL3n5LSeoKBQRuqJy1vFGXu6ACPxUuu04htFQc+6eAxvfP8AtmtBYYOEFXOfgvyhHpP4KjmS20NeX+3U8sXEyIR8JmXh5+Vymjd/1muYe/vH4raOiD2lrhmCMiCsCKE0txjnaMgS07OUb/StzPHwczsvgk7F8ZmtuOv9L/ft/c28WOkdrNTbZZKWV1OSQ+ndk0njbxH/AJ0qZ08zZ4WyN4xtHIofcInRllZGCXR7Hgb3M4+retnaLg1jwxzwYpNx4s+JdfCM3g3bZemX6MuWU7q90fYkSIi+yKIREQBERAEREAREQBVVpw/Q9p8If91Wqqq04foe0+EP+6rGL86JFd6GUoiItszwiIgCIiAIiIAiIgCIiAIiIAiIgCIiA6+i/NM/hC+l8Rfmmfwhfa+cNUKiNNfxvo/AG/3Hq91RGmv430fgDf7j1aw/nIhyPQVsiItkoBERAEREAREQBERAEREAREQBERAEREAW2w3f6rDV8guVKczGcpI88hIw72n/AJvyK1KLxpSWjCbT1R1vb6+nulvp66lfrwVEYkYegj0rJVYaFrw6qsdZaZHZuo5A+PP5j89nicCf6lZ6wbYcObiacJbophERRnQREQBERAEReNXVQ0NHPV1DwyGBjpJHHiaBmUBUemrEGtJR2CF+xv8AiKjI8e5g9J8YVQrYXy7TXy91lznz16iQvyJ+CNwHiGQ8S163aK+HBRM2yW6TYREUxwEREAREQBERAbzB99dhzFFFccyImv1JgOON2x3Vv74C6jY9r2B7HBzXDMEHMELkBdD6KsQe7WEY6aV+dTbyIH57yz5B6tn9JWdnV9FNFrGn12k5REWaWwiIgCIiAIiICsdN3xat3hn+hyo1Xlpu+LVu8M/0OVGrYw/lIoZHrCIitkIREQBERAEREAREQBERAEREAREQBdb2/wDRtL/JZ6AuSF1vb/0bS/yWegLO+If6fuWsX3MlERZpbCIiAIiIAiIgCIiAIiIAoTpJxm3CtiMVM/8A+Z1YLIANpYON/wCA6e8VKLxdqSx2mouVa/UggbrO5SeIDpJyC5yqrpU4lvVRiW4nZrllLFnsblydDfOSSrWLTxJavsQ3WKETGZF7mUhZK7Wq5jrzuzzyPE3xcfTmtBUufX1RgidkTte75jVlXStcDk3N0jzqsaN5cV9UlN2JAI8w6Rx1pH/Od6uJbmzX8C+5lb9v4339jJgiZFEyKMZMYMmhe+4ZlfjG7FuLHbuyqjh5BnDEfKdxDxb+pT9EjOus0TbNvZ6HsKiBeMppe6f0cgWxX6vxEYdknOTkz4dsWO92TjmvuonZHmAe75BxLC1ySuiPQyWu2rJp5nU9RHM0Zlhzy5RxhYTSshm1ctJrRnibjJNExjlZIxr2HNrgCD0LOp3bFGLTUlp7GdnqnMsPIeMLduq20dM6d2RI2MaflOWNbU4y2n1GNkRnDe/uY9/qzI+KjiBc5pzIHG87AOr0rKpo20lNFTNOZYO7I43HeVqqMFgdcZsy8uLIM/lPPwneIecrMglzO9fNfEchSsVceyL+Inq7Zd5fsbN7gYczvY4FbmqiLoA7jaAVoogJHsj4pJGs/H8FJXZHPkWVwVbvT90v7mxVLpqasND2lrhsK0ZYbdWmmeSYX7Yz6QpBJHwcrm8W8d5YVfSNrqctBylYdZh6VgqDg3CXdGpj2aPR9mbqzV5qoHQyn8vDkHfvDiK2ar6juclJqVgb+UpzqTs4yzj6t6nsM0dRCyaJwdG8ZtI4wvsfheU7qtsvUipl47qnr7M9ERFplQIiIAiIgCIiAKqtOH6HtPhD/uq1VVWnD9D2nwh/3VYxfnRIrvQylERFtmeEREAREQBEXVlhhiOHrYTEzPsWL5I+aFXyL+Dp011Jaq9+pymi684CH9kzyQnAQ/smeSFV5/8A2kvLfU5DRdecBD+yZ5ITgIf2TPJCc/8A7Ry31OQ0XXnAQ/smeSE4CH9kzyQnP/7Ry31OQ0XXnAQ/smeSE4CH9kzyQnP/AO0ct9TkNF15wEP7JnkhOAh/ZM8kJz/+0ct9T9i/NM/hC+0RZxbCojTX8b6PwBv9x6vdURpr+N9H4A3+49WsP5yIcj0FbIiLZKAREQBERAe9FSvrq+npI3Na+eVsTS7cC4gbetWN2kr5zlbut/sqB4f+Mtq8Mh++F1eqOXfOtpRLFFcZp6lGdpK+c5W7rf7KdpK+c5W7rf7KvNFU5y0n5eBRZ0JX3LZcbcT0ueP9K1lw0S4roWF8dPT1gAzPY02Z6nAE+JdDovVm2o8ePA5EqaWoo6h9PVQSQTMOTo5GlrmnpBXkujdI2FKXEGHKipbE0XCkjMsMoG1wG0sPKCM8uQrnJaNF6tjr7lWytwegREU5GEREAREQFi6GKkxYzmhz7majeMukOaR6Cr7XP2h6N0mOg4DZHSyOPe2D8QugVj5vzS9j+gIiKoThERAEREAVa6Y8QdgYfitEL8pq52cmR2iJpzPWcuoqyiQBmTkAuYccX84jxZWVrXa1O13A0/JwbdgPjOZ8atYle+zV9kQ3z2x08kdREWyUAiIgCIiAIiIAiIgCmejHEHuFjCBkr8qWt/w8uZ2Ak9yevId4lQxASCCDkRuK4nBTi4v3PYy2vVHYCKPYIv4xJhSjrnOBqA3gqjokbsPXsPjUhWBKLi2maaeq1QREXh6EREAREQFY6bvi1bvDP9DlRqvLTd8Wrd4Z/ocqNWxh/KRQyPWERFbIQiIgCIiAIujtGEUbtHVqLo2E/ldpH/ivUu4CH9kzyQs+ebtk46dizHH1SepyGi684CH9kzyQnAQ/smeSFzz/APtPeW+pyGi684CH9kzyQnAQ/smeSE5//aOW+pyGi684CH9kzyQnAQ/smeSE5/8A2jlvqchouvOAh/ZM8kJwEP7JnkhOf/2jlvqchrre3/o2l/ks9AXrwEP7Jnkheir5GRxtOnYlqq2ahERViYIiIAiIgCIiAIiIAiKv9KeLxYLIbdSyZV9a0jMHbHHxu753Dx8i7rg5yUUcykorVkG0iYlkxliOOw26fVtlM4mWVp2OLR3b+kAbByk9Kit1qYoohHC3g6eJupGz5rR+PGekrJooBarHrSDKqrWtlkz3sj3sb4/hHxci0Mw90q4wu/y8Q15jy8je+fWt2iCrj0+xlWz3y6nlQwGVxr5hkSCIGn5I43d8rZMaN6+SddxyAA4gNwXsxu4K3CO1aFK2zV6mRRUk1dVRUtO3WlkOTRycpPQAp1HRx0FNHTRDuWDLM73HjJ76/cO2b3Jt3ZM7f8ZVMBII2xs3hvfO8+Jes57oqNT3y6dkZuX0jp7mOd6xKmrERLGbZOM/NSsquDHBxnuzvPItaFOkZyXufpJJzJJJX03evhfbd69PGZDAspgXgwZ5LKjaXODWjMleN6Ii0beiPaPPPMHV1dufIsyDh7vUflHcHEwaz3EbI4+M988ix4InVkzaaButrHyjy/whZlTUxQw9g0jtaIO1pZeOZ/L/AAjiXzXxb4hGpbIdzdwcVtbp9v3PuoqWzyt4NmpDG3UiZ81vrO8r0p3rXNcsqBxLmgbyV8e5OUtWbsJdSS2tvCVsDSPggyfgPQVIVqbJGCx9Vl+c7ln8IW3VnH6py8v/AINSC0ijHqmDUD/m7+8tcXFkgO3LNbhzQ9pa7cdhWkeXNJY74TTkVnZ9Olqmvf8AdF7G6po01yYKC7tmA/IVIyIO7PjW1wtcRR1L7PNJmw5yUrid7Tvb4l43Gn7Ot74h+cb3TDyEKMmaWejbNCSKukdrsA3n5w6vQvMSx02qUTUVSyKdku/b/D/sW2i1liu8V5tcVSwjXIGuOQrZr66E1OKlHsz56cJQk4y7oIiLo5CIiAIiIAqq04foe0+EP+6rVVVacP0PafCH/dVjF+dEiu9DKUREW2Z4REQBERAF1fYfi7bPBIvuBcoK97VpYwzSWiippXVfCQwMjdlDmMw0A8ao5tcpqO1aljHkot6lkooD24cK/PrPqP8AdO3DhX59Z9R/uqHAt/pLXFh5J8igPbhwr8+s+o/3Ttw4V+fWfUf7pwLf6RxYeSfIoD24cK/PrPqP907cOFfn1n1H+6cC3+kcWHknyKA9uHCvz6z6j/dO3DhX59Z9R/unAt/pHFh5J8iitg0hWLElzFvt7qgzlheOEi1RkN+3NSpRyhKL0kjpST6oIiLk9CojTX8b6PwBv9x6vdURpr+N9H4A3+49WsP5yIcj0FbIiLZKAREQBERAbHD/AMZbV4ZD98Lq9coWAgYjtZJyAq4syf4wuqey6b6RF5YWbnptx0LeM+jPZF49l030iLywnZdN9Ii8sLP2vwWdUeyLwNZStGZqYQOUyBau4Yvw7bGF1XeaNuQz1Wyh7vJbmfMvVCT7Ibl5M671MdHZq2pmIEcUD3uz5A0lcmKyMf6TPfDTOtVpZJFb3EcLK/Y6bLaBlxNz28p6OOt1q4dMq4ty9ylfNSfQIiK4QBERAERfrGOke1jGlznHIADMkoC2tCFtc6qul0cMmtY2nYeUk6zvQ3rVyqO4Iw+MNYVpKF7QKgjhajpkdvHi2DxKRLCvnvsckaNUdsEgiIoSQIiIAiIgIbpNxB7hYPnbE/Vqq3/DxZHaAR3R8Tc/GQucVOtK2IPdnFr6WJ+tTW8GBuR2F/yz17P6VBVs4leyv6sz7p7pfkERFaIgiIgC9GwSvhkmbG50UZAe8DY0nPLPv5FeaurBeCm1miyuimYBU3ZplYXfJ1fzXizGfecobrVUtWdwg5vRFKovp7HRyOY9pa9pIc0jaCF8qY4CIiAIiICy9DeIOwb9NZ5n5Q1zdaPM7BK0fiM+oK9VyNR1c1BWwVlO7UmgkbIx3I4HMLqqyXWG+WSjucH5uojD8s/gnjHiOY8Sys6vSW9e5cx56raZ6IiolkIiIAiIgKx03fFq3eGf6HKjVeWm74tW7wz/AEOVGrYw/lIoZHrCIitkIREQBERAdI6Lv1c2nvS/3XqXqIaLv1c2nvS/3XqXrAu+ZL82aVfoQREUZ2EREAREQBERAEREAREQBERAEREAREQBERAYlzuNPabZUV9W/UggYXvP4DpO5c4S1M+McW1NyrszTsPDTNz2NjGxkY7+wdZUy0yYq4WoZh+mk/JQZS1RB3uyza3xDb4xyKLx0xs1hipHt1auf8vU8oJHcN/paeslauHTtjq+7/Yo5Fmr08GpvtxfI+SQkFz3E+PkWBGw0tO2Fvwnd3IeMuK8ZXiqug1jnDBm53SRxdeSyGkvk1nHMlada1evsjPteiS89T3ib3OZUywnYRU3WN1QzWZTtE0rSNmfyWnzHrWuwrZ23CpFTO3/AA0Tsmg/Lf6hxqwrFCIbZLVjfWSukz4y0Ehv4nxqPIt0i0ivFbp/RC4PBkPKtDVziGNzzv3AdK2lZJm85lRatqeyJiW/Absb611RHRGVlS3zZjucXOJJzJOZK/F+IrRAon0F6MG1ebd6yY2ZtL3ODI2/Ce7cF42l3I3Ft6IyIWF51QMz6Fl08b6qVlPSDhNckEj5fLkeJo5VjwU8la8QRNLYiM9UnIyDjLz8lqzJqyKmgdSUTs9YZTTgZa/7reRnpWB8T+KKtOuHc0MTES/HMy56iGhgfR0jw+R4yqKhvyh8xv7vpWvaV4NK9Wr4y6cpy3SNeMtei7GQwrLpo3zzRQR/DkOqMuIcawm7BtPjUlwxSktluD25DLg4s/Sq0noi5jw3zUSUU0bIomsZ8Fo1W94LIC8I9jQAvYK7S/wpGw0fS1NwaG1jv3mB34LbALBrImy10DDs1mOBXOVHdBL6r9en9ybHltnqazW1TsUaubDb7s2dmyGbuh0HjUhlDopCx+xzTkVgXWnFZb3RgZvbtb31R26dTax5KMk32Zg2K4mwX8x5nsOp7to4h84eLerQa5r2hzSC0jMEcapbuq2g4OM/l4zrxHkcOLxqfYGvjbna+Ac7u4h3IO/V5PEfwW3gWOP8NkPxbF1jx13XR/2ZLERFqGAEREAREQBVVpw/Q9p8If8AdVqqqtOH6HtPhD/uqxi/OiRXehlKIiLbM8IiIAiIgCIiAIiIAiIgCIiAIiICe6H/AI+R+DSfgug1z5of+Pkfg0n4LoNZGd837F7H9AREVMnCojTX8b6PwBv9x6vdURpr+N9H4A3+49WsP5yIcj0FbIiLZKAREQBERAERF5oAiImiGoRETQBERegIiIAiL1p6aerqGU9NDJNM85MjjaXOcegBeA8lbOirAj55osR3OIthYdajicPhn9oegcXTt4hnlYK0SGKSK44ka1xHdMoRtGfFrncf4R4+RW41oa0NaAABkAOJZ2TlJrZAtU09d0j9REWcWwiIgCIiALR4uvrcOYYrbjmOFYzVhB45Dsb59veBW8VI6Z8QdlXWmscL846QcLMAd8jhsB7zfvKaiviWKJHbPbHUq973SPc97i5zjmXE5klfKIt0zgiIgCIiA2Fjtct7vlFbYc9aolDCR8kcZ8QzPiXVdPTxUlNFTQMDIomBjGjiaBkAqZ0K2Ph7lWXuVvcU7eAhJ+e7a4+IZD+pXWsnNs3T2+C7jx0jr5OdNKVj9xsZ1EsbMqeuHZDNmzWPwx5WZ8YUKV/6XrH7p4TFfGzOe3v4TZv4N2QcPQf6VQCu4tm+tfQr3R2zCIiskQREQBXHoWxBrRVdgmftZ/iKfM8R2PHXkfGVTi2mHbzLYMQUVzizJgkBc0fKYdjh4wSob6+JW4ndctskzqxF5088VVTRVEDw+KVgexw3OaRmCvRYRpBERAEREBWOm74tW7wz/Q5Uary03fFq3eGf6HKjVsYfykUMj1hERWyEIiIAiIgOhNGt4tdLo/tcNRcqOGVvC6zJJ2tcPyrztBKlfvgsvO9B9pZ61ygiozwlKTlr3LEchpJaHV/vgsvO9B9pZ6098Fl53oPtLPWuUEXPIR8nvMvwdX++Cy870H2lnrT3wWXneg+0s9a5QROQj5HMvwdX++Cy870H2lnrT3wWXneg+0s9a5QROQj5HMvwdX++Cy870H2lnrXrT3e2VcwhprjSTSncyOZrnHxArktTfRN+sGj/AJcv3CuLMJRi5a9jqOQ20tDolERZ5aCIiAIiIAiIgCIiALVYkvcOHbBV3ObI8EzuGH5bzsa3xnJbVUfpfxL2deIrLA/Onou7lyOx0pG7xDzkqfHq4tij7Eds9kdSGWqN98xM6priZWRl1bVOPy8jnl43Fo6163+5Pe6eoe7OR7jt6Ssu0xigw06dwymr5Nfp4JmYb1u1j1KMXifhKlkIOxm098rb101kvyRmpbmonlSN1YXH5T3Zk97d+K2FLCZ5mxg6o3udl8EcZWIzJrGtG8DzrcQMEEQb8t2159A8SsxjtikUb5/icjf2241D3Nt1PGxscuVPC0Da3WOW08e8klWVVxx0lOynj+BEwMb3gMlAsC0vZOIGzFvcUsbps/3j3LfST4lNa6XWcQqV/W1RXscV6QqcvdkavM+qzgwe6k395aB29Z1ylMlfLmdjDqDxf75rAKv1rSJjy6yPxfoC/WMc45AdJ6F9Ql87gykAcScuHLc2j+EfLPm764tuhVHdN6I6jCU3pE+g1kZbrtc97/zcLPhO6egdJWxpKJ1REKmeSJkMZ/Of9KPoaPlO/wCbF9Noaa1teawufO/a6DWzkk6Xu+SOgLGqayWrc3hC0MYMo4mDJkY5APxXzGf8Ylb+CnovJehTCr19WZNTX8JGaela6Km+Vme7lPK8/huCxWleYX21fPybfVnak5Pqe7N692rHYvqSUx6rGgukeQGtAzJJ3AKCS1LNb0M6lppbjWR0UGes/a4j5IVgwQxwxx08WyKJoaOk8q1VgtfuPQZyZGtnydI75o5Atq3JoWZkZEd6gvufR4WM64bpd2ZIdkvdpzCw2uWRC7MkeNW8a9SehYlE9gVgVL875RR57dSRxHRll+KzwtJG/sjFVXKDmymgZCD+84kn0BaDW5xX1X6dTumOrb8J/r0/ufd6g7gVLd4Ia/vcRWoZJk7xqSzsbPC+J257S1RHNzXFrt7Tke+uLalrr5NHEe6Di/Y0Naz3OvMzGfALg9vQDtX5bLkbBiuORmymqfyjR0/Kb/zoWViCMOnpZx8uN0bu+0gjzOWlukTqu0cJEcqilIlYe9vU1Hn3NuCVlSUuzWj/AGL1jkZLG2SNwcxwzaRxhfSiWAb4262WONzhrsaC0funi8R/BS1a8ZblqfG30umx1y9giIuiIIiIAqq04foe0+EP+6rVVVacP0PafCH/AHVYxfnRIrvQylERFtmeEREAREQBERAEREAREQBERAEREBPdD/x8j8Gk/BdBrnzQ/wDHyPwaT8F0GsjO+b9i9j+gIiKmThURpr+N9H4A3+49XuqI01/G+j8Ab/cerWH85EOR6CtkRFslAIiIAiIgCIiAIiIAiIgCIiAIiIAs213e4WSsFXbauSmnAy1mHeOQjcR0FYSLxpNaMalw4Z0zA6lNiKnyO7sunbs77mfiOpWxR1lNcKSOqo5454JBmySN2YIXIykOFcY3PCdcJaSQyUrnZzUrz3Eg/A9I8+5UbsJPrDoyxXkNdJHT6LVYfxDb8S2tlfb5dZh2PYfhRu42uHKtqsxpp6MuJp9UERF4ehERAYd1uMFotVVcKg5Q08bpHdOQ3DpO5cq3Gvnulyqa+pdrTVEjpHnpJzy7yuDTRiDgLfS2GF+T6g8NOB8wHuQe+4Z/0qlVq4Ne2G9+5SyJ6y2+AiIrxXCIiAIilWjux+72M6KF7dangPZE3Jqt3Dxu1R41zOSjFyfsexWr0ReuCLH73sJUNC5urPqcJPy8I7aR4t3iUhRF8/KTk22aaWi0R5VVNFWUk1LOwPhmYY3tPG0jIhcpXq2S2W9Vltmz16aVzMz8ocR8YyPjXWSpPTTY+x7rR3uJvcVLeBmI+e34JPfbs/pVzCs2z2+SDIjrHXwVWiItYpBERAEREBfeiDEHunhl1smfnUW92q3PeYnZlvUcx3gFYq5n0f4g97uLqSokfq00x4CfPdqO4/Ecj4l0wsbLr2Warsy/RPdH8giIqpMEREBWOm74tW7wz/Q5Uary03fFq3eGf6HKjVsYfykUMj1hERWyEIiIAiIgCIiAIiIAiIgCIiAKb6Jv1g0f8uX7hUIU30TfrBo/5cv3Cor/AJUvyO6/WjolERYJpBERAEREAREQBERAarEd4jsNgq7i/ImJncNPynnY0dfmXL9S6puVYSHGSqq5cgSdpc45Z9ZVpaZb659RTWSF/cxASygcb3fBHibrH+oKvsMs18TU0hB1aZsk5/pacv8AuIWvh17KnP3ZRyJazUfBub6+KOo7GgOVPTtEMf8ACwZfhmoG1/ZFU+U8ZzUlvU2rTVDgduodqjFCwyZAbycgrUum2JDDtKRtqOPWPCO5diz81jQkABrdw2Be4KuLX3Mq7q9Sw8AxiO211TxvlbGD0Nbn6XLa1NRqcI/PPVBK12FcqfCULzsMssjz091l+C8K+4wwteHPbuzdmcg0cpPEFSjHdZJsjvs2xjBGicSTm45uO09JWPNUxwSCIh8tQfgwRDNx7/EPGvJ1TNXZNoTwMBORqSwl7/5beTpKlFsw3S2igNZcQ6GJ2wRNOc0zt+Tid3mUWb8Trx1pHqyKnEc9XL/v5mqorRVXFrn1XBsiZ3T4wfyMY5Xu+WejzLYOr4aEcHbc3PyydVvbk7vMb8kefvLyr7hJWkMDWw0zD+Tgj2Nb09J6SsElfJZOVZkS1myZ2KH4az9c7WJJJJO0k7SV+caL9Yxz3HLdxlVuxFo5M+2herG5r6jgKVEsdHHrP2k/BaN7lE5avRFiFT01Z+TTMpojI/xDlKkeFrMRq3ivb3bh/h43Dd+8ek+YLV4dscl3nZcK8f4Rhza39oRxD90ecqbvk13cgG4ciys/MjWuHB6v3PoPhfw9yatmunsZAeSSSdq+tbYsVrl6B25YKk9dWb7hoZTXL3hdlK3pzCw2uWRCfyrf+cSv4ln8SP5ognHoZcszYInSvOTWAuJ7yjeGHOktr62UnhK2Z8235ueQ9C+MZ3N8NsFBTAmprXcDGByZjMryM4oHw00Ls46ZjY8xx5Db+K+pxlvbl7Is0Y74OvvJ/ov8t/oSIvUduzOCr3OAybKA8d/cVuWSiRgc05gjYVr70zWpY5f2b8j3j/vkp5x1R1j/AIbERy9baWlPzZnDrb/stVRvDZy07Q4bjxraXburc08bZA78Fo5CY5A5vEmOupvY8da9p74TuZw9ieooyTwUT9dg5Y3Db+BV3tc17Q5rg5pGYI3Fc9XqQ0txtl0buLuAlPQd3pPUrewPdezrQ+ke7OWjdqd9hzLfxH9Kv19Ohj/GMfWKvXddGShERSnz4REQBVVpw/Q9p8If91Wqqq04foe0+EP+6rGL86JFd6GUoiItszwiIgCIiAIi6Os2BML1FkoJpbLTPkkp43PcQcyS0EneoLr1Vpqu5JXW59jnFF032vsJ8x0vUfWna+wnzHS9R9ar8/DwSctLycyIum+19hPmOl6j607X2E+Y6XqPrTn4eBy0vJzIi6b7X2E+Y6XqPrTtfYT5jpeo+tOfh4HLS8nMiLpvtfYT5jpeo+tO19hPmOl6j605+HgctLyVDog+Pkfg0n4LoNaa24TsNnrBV2+2QU84aW67Ac8jvC3KpZFqtnuRZqg4R0YREUBIFRGmv430fgDf7j1e6ojTX8b6PwBv9x6tYfzkQ5HoK2REWyUAiIgCIiAItjYADiS1gjMGrizB/jC6p7Fp/o8XkBVb8jhNLTuS1VbzkVF112LT/R4vICdi0/0eLyAoOf8AoS8t9TkVF112LT/R4vICGjpiMjTwkdLAnPrwOW+pyKi6nr8JYeubC2rs9G/P5QiDXeUMj51UuPtF4sVJJdrM+SSiZtmgec3RD5wPG3zjp4pasyE3o+hHOiUVqVkiIrhCEREAREQElwTiyfCd9ZUgudRykMqYh8pvKByjePGONdMQyxzwxzRPD45GhzHNOYcDtBC5CV+aH76+54Xkt879aW3yBjc9/Bu2t6iHDvALOzqlpxEWcefXayxERFmlwL5kkZDE+WRwaxgLnOO4AbyvpQHSziD3IwoaGJ+VTcSYhlvEY+GerIf1LuuDnJRRzKW1aspbFV8fiLEtbc3E6kr8omn5MY2NHUOvNaZEW9FKKSRmN6vVhERdAIiIApdgnG7cGircy1tq5qnVBkdNqarRnsHcnjPoURRczgpra+x7GTi9UW528p+YI/tR9lO3lPzBH9qPsqo0UHKVeCTjT8lt9vKfmCP7UfZWmxTpQGKbDLbJ7IyLWc17JRUaxY4HeBq8mY8ar1F7HGri9Ujx2za0bCIisEYREQBERAF0po5xB74MH0skj9aqpv8ADz5naS0bD4xke/mua1YGiTEHuTirsCZ+VNcWiPbuEg2sPj2jxhVcuvfXqu6JqJ7ZfmdAIiLGL4REQFY6bvi1bvDP9DlRqvLTd8Wrd4Z/ocqNWxh/KRQyPWERFbIQiIgCIiAIiIAiIgCIiAIiIApvom/WDR/y5fuFQhTfRN+sGj/ly/cKiv8AlS/I7r9aOiURFgmkEREAREQBERAF5zTMp4JJpXascbS9x5ABmV6KJ6R7kbdg2qDTk+pIgB5M9/mB611CO6Sj5PG9FqUNfbnJesQVVfLnnLI6TI8QOxo8TQF94af/AIu4yD5NJq9cjPUtS1+tE+X5xOXeWwwy/Ke5N+dStPVIF9A1tikjNfVtnhf35W+Y970ham27KfhOPMgLY3450Ew6Wn/uC1lE7Kjib/EfOvdUrVr4ONG6ml5NlA/aSVmNkBK1XChg35L7bK52oWsL9c5MbkSZCd2Q35ecqd2xXUo8GUuhM5sUxwWait9JmTHEGl+W17t51RyZn4R2L7teGK++cHU1x/w5drMg25Od/qPSdg6Fm2PCUNoiFdeWGpukmRjo9bZEOLXI4/3R/up/TxmCHOQgykAOyGQH7rRxAL5/Mz3GO2voiavHjKzT/wBmvt1op7ZqFrWvqtwcB3LByN9fVko7erj2fWHg3EwRZsj6eV3jKkV1qTT26okacpHDg2d92zPqzUNLchkNy+bnY5vqMxqEVVA+DvXzkeRe8UEsz9VjS4nkW0p7cIe6fk5/oUNl0YdypTjTs6+xr4KFz8nSZtHJxlZzaYZZAZDkWwZT6x2DMqPYhxZR2UmkpCypuGeqWjumRHpy3u/dHjVSNs7pbYI1IYaitWZFxrYLVGOEydM8Zsiz4uV3IPSv3D1gmvc5ud1DhSZ9wxwy4YcWXIz0+n5w3hGqqpW3nEmsS467KWTa554jJ+DevkU3km1iNmTRuA4lWysxVJ11PWXu/wDBqYXwt2y32Lp4PYvGqGNAaxoyAHEF8l21eHCdKa6w3Ft6s+jjUorRGS1y9WuWK1y9gdyja0OJRMlhWQx4Yxz3OAAGWZ4uUrFj25AcajWMLvK+SKw27N1TUdw/V3gHi8foV7BqlZYtpDXRK6xVr7/RHhR1wu2IKu9u20tCOBpQ7cXnZmPOepfZlJJJOZO1eDuBo6aK20zgYabMOeP+pJ8p3e4gvlr819xVUqoKCNZQXdLp2X5L/Pf7kis1TrRugcdrdre8sq5d3bKkDfqa3UQfwUdo6ngKuN+ezPI94qQ1LtaimHKxw8ySj0ZRur2WKSIrcjnTMZ84OPoWlmGTnBbOskL59TijiHWST6AFq5yRI7PfmlMTax1otDCucXZlgqovlMbrt74P/wDVucC37sK52uolflFV5Us235TvgnygB4ytU12bJWHc5pafGtDb3OksVwp2uLZIXF8ZG8Ed0MupWX06nuTSrISg/dHT6LUYXvAxBhe3XUZa1TA1zwNwfucPE4ELbqU+EaaejCIiHgVVacP0PafCH/dVqqqtOH6HtPhD/uqxi/OiRXehlKIiLbM8IiIAiIgC6wsPxdtngkX3AuT11fYfi7bPBIvuBZ3xDtH7lrG7s2KIizS2EREAREQBERAEREAREQBURpr+N9H4A3+49XuqI01/G+j8Ab/cerWH85EOR6CtkRFslAIiIAiIgNjh/wCMtq8Mh++F1euUcP8AxltXhkP3wurlmZ/qiW8bswiIs8tBERAF5VFPHVU0tPM0PilYWPaeMEZEL1WoxPfqfDlgqrjO9ocxhETCdr5CO5aPH5s17FNvRHjaS1Zy1PHwNRJFnnqOLc+XI5LzX65xc4ucSSTmSV+L6EywiIvQEREAVi6Ga0wYylpi46lTSvGryuaQ4HqDutV0pfoucW6RrVlx8KD9U9Q3rWqS+h3W9Jo6RREWEaQXNuknEHu/jCpMb9alpP8ADw5HYdU90fG7PxZK7Me4g97mEquqY/VqZRwNPy67uMd4ZnxLmVaODX1c2VcmfaIREWkVAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAL7ilkgmZNE8skjcHMcN4I2gr4RAdU4XvbMRYcormzLWmj/ACjR8l42OHWCtuqX0LYg4Gtq7DM/uZxw8GfzwO6HjGR/pKuhYN9fDscTSrnuimERFEdlY6bvi1bvDP8AQ5Uary03fFq3eGf6HKjVsYfykUMj1hERWyEIiIAiIgJdZtG+IL9aYLnRMpzTz62oXy5HY4tOzvgrO7UGK/2VJ9f/ALK1dF36ubT3pf7r1L1lWZlkZtL2ZcjRFxTOe+1Biv8AZUn1/wDsnagxX+ypPr/9l0Ii452065eBz32oMV/sqT6//ZO1Biv9lSfX/wCy6EROdtHLwOe+1Biv9lSfX/7J2oMV/sqT6/8A2XQiJzto5eBz32oMV/sqT6//AGUmwFo7v+HsW01xr2U4p42Pa4sl1jmWkDYreReSy7JRcX7nqoinqgiIqpMEREAREQBERAFUumy5GOjoqFh7rVfKR0nuW/iraVBaZarh8WNp8/zTYY+vN34qziR1tI7H+EgZbqUrW9C98OyFt2nj/aUrx1FrvwK8Kk5My5FjWufgL7SvzyDnmM95wLfxC2bXo0U4R6Mzbzm6nnZysPXvUdpatrImAnINbmtte6vgxk34TnZBYFpt8THMra1hfHn+Rg45XZ7NnGM9w41FkT0kj2iGsXqbChtlRcI4pXQyScM7Vp6do7qc9A5P+blatpsVJhJrZpCyoxA9mT5Ms46QH5LP3uLP0DYvSz2+TDtD2XUtYb3VNDQd/YrOMDp3Z9PQ1eR7t5OZ8fKsSWbx5NR9K/Uq51jo/BH1P9P+TaWSE1NxM7wSyAa+ZOebzu/E+Jb2R+sVgWJmpa5JON8pHUB6ysvbmsrNv1lp4O8GrbUn7vqae+nNlPFyuc8+LYPxWJS2WWraJJCYYeIkd07vD8VIuAhdMJXsDnsGTSduS/XOc45Nzc4r5zJzpRe2BoVfDlbJ2T7GCKeCkj4KFgaOsnvlYlfV0dpo3VtyqY6ambs1nna48gHGVp8V48t2HXmipIxcbudnAsPcRn94/hv7yrJ0V9xje2CV5r7nJ8CNv5mmb4tgH/Nqs4fw+y6PFue2Hl92X1TBfhijfX3HdyvszbXh2CeGKd2o0tGU83ey+C3z9IUywXgClwzEyvumpUXUjNrBtZB3uU9PUtjhnClvwbS6zSKm6yt/LVLhu/dbyDoWxkqHPcXE5kqHKzIuLoxVpD3fuy7j4O575mXLUOec3H/ZeBl271imUr84RZqrNaNaS0RliRfTXrED19tcjgHEz4355LIB3LAjftGW1eV1vlNY6I1E51pNzI2nunHkHr4lBwZTkoxWrIZQbei7ntfb9FYbeXEh1TJm2JnT6lE7fHPQMkuFU8uudYMwTvjYd56CeLoWFG+epqhd7oA6pePyFORsYOJxHJyDjXq6Z8sjpJHlz3HMuPGvsvhuAsaG6XqNGjFVcNvnu/P0/Lz5Mxj16tkWE16+2v2rT0JXA2Afnkt4KgutBO92pq+Pco0x+3evevuBpbRsPdHMjv7h5z5lzJdCtZS5uMV5MVkgnqJZB8GSo1W9Ibk0fivXENH2HXEtGUcmZHiK+LFBw1fb6b5rgXeLN59CkOLKXhrS+ZozdAdcd7j/AOdC6qhokdTt4WTGHt/1L9iv9YiRzuLPNaq0ENutXTn/AKrNg7xI/FbGZ4jhe7o2LR0smpf6Z3zg9vmzU1kdYmnatNH9S1tB11M1huNne4l9BUazQeJr89g/qa4+NWouf9FNd7m6Vq63FxDKyKVjW8rmkPB6g7rXQC979T4HNhsvkgiIhVCqrTh+h7T4Q/7qtVVVpw/Q9p8If91WMX50SK70MpRERbZnhERAEREAW/ixtiaCFkMV7rGRxtDWtD9gA2ALQIuXFS7o9Ta7Eh9/eKufa36xPf3irn2t+sUeRecOHg93y8kh9/eKufa36xPf3irn2t+sUeROHDwN8vJIff3irn2t+sT394q59rfrFHkThw8DfLySH394q59rfrE9/eKufa36xR5E4cPA3y8kh9/eKufa36xPf3irn2t+sUeROHDwN8vJfeiO9XK9Wm4yXKtmqnxztax0rsyBq7lYqqvQh+hbr4Q37qtRY2SkrWkX6nrBBURpr+N9H4A3+49XuqI01/G+j8Ab/ceu8P5yOcj0FbIiLZKAREQBERAZVsqm0N2o6t7XOZBOyVwbvIa4HZ1K6O3bZObbh1M9pUaihtohbo5HcLJQ7F5du2yc23DqZ7Sdu2yc23DqZ7So1FFyVR3zEy8u3bZObbh1M9pDptsuWy2XAnp1PaVGonJVDmJlv1+nBxYW2+ygO4n1E2YH9IH4qt7/AInu2JqsT3OqMmr8CNo1WM7zfx3rUIpa6K6+sUcSslLuwiIpjgIiIAiIgCnOiSmM+P6aQDMU8Msh6O51f9SgyuPQlZ3NhuN5kbkHkU0Ry5O6d/p6iq+TLbUySlazRbqItbiC8RWGw1tzmyLaeMua0/KduaPGSAsVJt6I0W9OpTGmDEHujiOO1QvzgoG5OyOwyuyJ6hkO/mq4XrU1EtXVTVM7y+aZ5ke48bicyeteS3qoKuCijMnLdJsIiKQ5CIiAIi/Q1xGYBPiXmugPxF9ajvmnqTUd809Sbl5GjPlF9ajvmnqTUd809Sbl5GjPlF9ajvmnqTUd809Sbl5GjPlF9ajvmnqX5qO+aepNyGjPxERegIiIAiIgMy03Kaz3ekuNOfytPIJAM9+W8d4jMeNdV2+uguVup66mdrQ1EbZGHoIzXJCvDQziDsuz1FkmfnLRu4SEHjjcdo8TvvBUM6vWKmvYsY89HtLQREWWXSsdN3xat3hn+hyo1Xlpu+LVu8M/0OVGrYw/lIoZHrCIitkIREQBERAdI6Lv1c2nvS/3XqXqIaLv1c2nvS/3XqXrAu+ZL82aVfoQREUZ2EREAREQBERAEREAREQBERAEREAXNulCUyY8rCTnlUMHUwBdJLmXSO4jHdaDx1R9AV3B9b/L+6I7exHKo71pqiUxPa9pyLXBwPeOa3FTtzK0lWM8wtLI7kFa6HtXSiouRL/zMbdZ3TnxKeaObSKySXFNwaHU9G7UoYjsD5RsBy5GqtaanqLzdaa2UwJkqJAzYugZqOG1WuntFIP8PQsEefznn4R69i+a+OZ7rhw495fsa3w/F3dfBjT1Tp5XyvdrOJyzXm3buWJnkMule0Mm1YmNkbFoZ/xH4Y23JEusQDrPlxiV49Czmw5nctVh2pa58tITk4jhG9OWw/gvXEmIrfh62OqK2Yta7ZHGw93KeRvR0qHInKyekVq2dYlGlaUvY/aiZkMc9RNOyClizMk7zk1oCq7EekWquvCW/DZfS0e6SvfmHvHR83095aS83y5YvkbNcZDT2th/IUkJIDvX0uPiWJBT1NdVU1voYWmaV2pDCwZNHKfWSruL8Jro/i5HV+PZf5Niqptadkelhw/NdLgKC2ROknftlnkGeq3jc7kHRxq5bRZ7dhO3mjoGh9S4Dh6lw7p7u/8AhxLxs9qpcH2ltDA4SV8o16ifLaT/AM2AL5fUZlY+dmzy5bYv8H7l+jHUuqXT9zJfNnnmc++vEyLwMma+ddVFDQ0FDQ9y9A9eOuvrW2r3Q92nu1y9mZk5DasaMF+3cFpLripkDjQ2honqydUyAZtZ6ykKZ2y2wRzscnpE3F5xDS2GABxEtW8fk4Wnae/yBRRrJ56k3O8vElQ4ZxUx+CwcWY5OheUNEy2yGtr5TV3OTusnnMM6T6l4vmfLI573FznHMkr6LC+HwoWr6yLuNif6mZ76l0rzI8lz3b3OO0r6Eo5Vrg9fbZFqaF11JGzbIvVr1r45V6tl2r1IhlWbGOTasK4SmrroqdpOpENZ/f8A+elfr6gU8JlO07mjlKxKZ+pE+Q7ZJDmeVeOOr0PIV6PeS/B8GvVVNY47Im8G3+J2/wAw86k1QxlTDJC7ItkaWnxjJaqwQspbPDG0jhDm+XL554vEMgtkCS4ZcoUsUfO5Ut98pf8AehT9cSxmoTtBIWlDtW6Uj+R+XWCFt7y8C41LRubK8ecrRPOdbTbf+oFLpqfRXT1UfsbGxXEUOmC0VIOQdXRwk/zGhh+8V1MuL5Kww4jgrc/zNdE/P+Fw9S7QXLjtjFfQ+H+ItPJk0ERFyUQqq04foe0+EP8Auq1VVWnD9D2nwh/3VYxfnRIrvQylERFtmeEREAREQBERAEREAREQBERAEREAREQF26EP0LdfCG/dVpqrNCH6FuvhDfuq01iZXzpGhT6EFRGmv430fgDf7j1e6ojTX8b6PwBv9x66w/nI8yPQVsiItkoBERAEREAREQBERAEREAREQBERAEREARF70dHU3CripKSF81RK7VZGwZlxXjegPW12yqvFzp7fRR8JUTv1Wjk5SegDaV1HYbPBYLHSWym+BAzVLsstd28uPfOZUZ0fYCiwpRmqqw2S6ztykcNoib8xv4njU3WRlX8R7Y9kXqatq1fcKntNWIM3Udghfu/xFRkfEwek9SturqoaKjmqqh4ZDCwySOPE0DMlcq327TX2+Vlznz16iQuAJ+C3c1viAA8S9wq909z9jzInpHTya9ERa5SCIiAIiID6jjfLIyONpc95DWtG8k7guqMNWZlgw5Q2xoGtBEA8jjedrj1kqjNFdj92MZwTSNzp6EdkPz3aw2MHXt/pK6JWXnWayUEW8aHRyYyHImQ5ERUC1oMhyJkOREQaDIciZDkREGgyHIvl7GSMcx7Q5rhkQRsIX0iHmhyvimzOw/iavtpBDIpTwZPGw7WnqIWnVwabLH/kL7Ez/wD5piPGWH7w6lT63aLOJWpGdZHbJoIiKY4CIiALe4OvzsOYoorjrEQtfqTgccbtjurf3wFokXMoqSaZ6no9Udftc17Q5pDmkZgjcQv1QfRXiD3awjHTyvzqaAiB+Z2lvyD1bP6SpwsCcHCTi/Y0oy3LVFY6bvi1bvDP9DlRqvLTd8Wrd4Z/ocqNWth/KRSyPWERFbIQiIgCIiA6R0Xfq5tPel/uvUvUQ0Xfq5tPel/uvUvWBd8yX5s0q/QgiIozsIiIAiIgCIiAIiIAiIgCIiAIiIAuaNKEfB46rs9/ZAPWwFdLrnLTNAYcbyyZfneCePIDf9KuYT0m/wAv7ojsXQh1TuWmqRscVuKg5wxu5WhaipAIPStO/qcxRL9D1rD7zcL3IwOZRw6kef7Rx2ejzqzKlhFLKXHM6zcyo1ovphBgMyD4VVXPLu83Z+ClckZkgljy7ot2d8bV+ZfFb3bmT17J6f8Ao+pwIKFKfkj0gy2L4ZrZ7F7vjJIOSxbndqTDlsdX1QEj89WGDPIyv5O8N5K5r3SajBatljIpgouUux7V17p8LU7LlVnWqHAimpg7IvOWWs791V9LUVmJK996vTzIx+yKE7A4Diy4mDzrVRyVmKbvJcLnM6SJmRkOWQPIxo4gtxPPmc8g0ZZBo3NHIF9XhYEcaO6XWb9/7IoUY3EXGa/D7L+55VU4DXPcRmB4gFZOA7EzD1kdf7jH/wDMKpuUTHb2Rnc3LlO8qHYKsAxHidoqG61FSASzDLMOPyWnvnb4lYF6uRrbiWRn/DQdywDjPGfwWN8ZyXOXKwf1l/Zfctwp4tmz29z4kqHzSPlkdm95zcV5a+1eBevwO2rHUUjWVaS6GSHdKay8NdfodtXu0bTIDl9OfFBCaiqlbDTs2lzjlmsSvr6SzUBra+QNb/04/lPPQFEZX1+Jpey7k7sa3sObICdgHK7lPQpsfFlc9ey8kaTm9sTOr79X4kqDRWhjobeMw+XcZB6kg7Fs8JhpAJKg7HTbwO8vCWsZHB2NRs4KDLI5b3d/1LC1lu0UwqjtgjSoxFFfiMpzy4lzjmTtJK/AeleIev0O6VZRd2nvrL6Dl4h2xfWakRy0e7XL0Y8l2/JYwK8ZqjW/JsOzjP4KREckZU8/DyAA5xt2Dp6Vm0Jbr8K/5G4HjPF1LUxuDQspk+zIbgu4QE69Y7USagvDqGfXdm6F5/KNHpClzKhpc14cCzY7Mbst+arSGbpW691zR4Yqw4nWY3goTy64OXVt6l246dTFzcRdJR7kJrZ+GqZpc/hvc7rK1T36tbEeJgc8+JpKypT3K1VdLwdPVy/MhDR33OA9AK7jHodZNuxa+P7GimcX26SQnujLnn1Lt+B5kp4nne5gJ6lw3IdW0Rt43Pz9K7goDrW2lPLCw+YLm7o0j4q6W6WpkIiKEiCqrTh+h7T4Q/7qtVVfpqp56i0WsQQySkTvzDGl2Xc9CnxvmxIrvQyj0WV7mV/0Kp+qd6k9zK/6FU/VO9S2ty8lDRmKiyvcyv8AoVT9U71J7mV/0Kp+qd6k3LyNGYqLK9zK/wChVP1TvUnuZX/Qqn6p3qTcvI0Ziosr3Mr/AKFU/VO9Se5lf9CqfqnepNy8jRmKiyvcyv8AoVT9U71J7mV/0Kp+qd6k3LyNGYqLK9zK/wChVP1TvUnuZX/Qqn6p3qTcvI0Ziosr3Mr/AKFU/VO9Se5lf9CqfqnepNy8jRmKiyvcyv8AoVT9U71J7mV/0Kp+qd6k3LyNGYqLK9zK/wChVP1TvUnuZX/Qqn6p3qTcvI0ZcehD9C3Xwhv3VaarDQrTz09mugnhkiJqGkB7S3PuelWesXJ+bI0KfQgqI01/G+j8Ab/cer3VHaZqSpqMWUboaeaRooWgljCRnrv5F1hvS1HN/oKwRZXuZX/Qqn6p3qT3Mr/oVT9U71LY3LyUdGYqLK9zK/6FU/VO9Se5lf8AQqn6p3qTcvI0Ziosr3Mr/oVT9U71J7mV/wBCqfqnepNy8jRmKiyvcyv+hVP1TvUnuZX/AEKp+qd6k3LyNGYqLK9zK/6FU/VO9Se5lf8AQqn6p3qTcvI0Ziosr3Mr/oVT9U71J7mV/wBCqfqnepNy8jRmKiyxa7gd1BVHvQu9S948PXuX83Z7g/8Ahpnn8E3R8jRmtRSGnwJiqpy1LFWjP9pHqfeyW6o9EOK6rLhYaWkB/bTg5eTrLh3Vx7s9Vcn2RBEVyW3QhE0tddLw94446aPV/wC52foU5suBcOWFzZKO2xmdu6ab8o/PlBO7xZKCebXHt1JY48n3KRw1o4v2InNk4A0VGd9RUNIzH7rd7vR0q7cK4JtOE6fKkj4WqcMpKqQZvd0D5o6B481JEVC3JnZ0fRFmFMYBERVyUrbTFiD3Pw9FaIX5T17vymW8RNyJ6zkO9mqIUtx1W1+I8WVlYykqXU7DwNP+SdlwbdgO7jOZ8ajnuZX/AEKp+qd6ltY0Y11pa9TPtblLUxUWV7mV/wBCqfqnepPcyv8AoVT9U71KfcvJHozFRZXuZX/Qqn6p3qT3Mr/oVT9U71JuXkaMxUWV7mV/0Kp+qd6lm2jDtwut4pKAUtRHw8rWF5jIDQTtPiGZRzilrqFFsurRFY/cvCXZ0jcp7g/hTnv4MbGD0n+pT9eVNTxUlLFTQMDIomBjGjiaBkAvVYNk3OTk/c0ox2xSCIi4OgiIgCIiAIiIDUYoszcQYar7YQNeaI8GTxPG1p6wFyw9jo3uY9pa5pIcDvBXXy550l4ZqLdjKplpKWV9NWDshpjYSA4/CGz94E+MK/g2aNwZVyYapSRBUWV7mV/0Kp+qd6k9zK/6FU/VO9S0ty8lXRmKiyvcyv8AoVT9U71J7mV/0Kp+qd6k3LyNGYqLK9zK/wChVP1TvUnuZX/Qqn6p3qTcvI0ZKtF+IPcPGEEcr9Wlrv8ADyZnYCT3B69neJXRi5KFuuDSCKKpBG0ERO2eZdMYPvEt8wvRVlQx7KrU4Odr2kHXbsJy6d/jWbnQWqmi3jyem1kO03fFq3eGf6HKjVe2miCaow5b2wxSSuFXmQxpcR3DuRUn7mV/0Kp+qd6lYw2lUiK9PeYqLK9zK/6FU/VO9Se5lf8AQqn6p3qVrcvJDozFRZXuZX/Qqn6p3qT3Mr/oVT9U71JuXkaMxUWV7mV/0Kp+qd6k9zK/6FU/VO9Sbl5GjOh9F36ubT3pf7r1L1EtGUUkOjy1Ryscx44XNrhkR+VfxKWrCu+ZL82aNfoQREUZ2EREAREQBERAEREAREQBERAEREAVFaeaXUulvrMtj4QzP+Fx9oK9VVmnOg7IwtSVQGZhmczym5/6Ap8Z6WI8kuhSJOtRR9GYWvkZm8d9ZlI7hKAj5rs+teEjdq2Z9YpnKRa+jlo7XtKB8ismafKKkjjqnMd9Q7RZXdkWK7WrfJTVIqGjj1Xjb5wetSuaUDuc9q/KviNbhm2xfl/r1PqMF7qkaq6VlHbaaauqX8HTxjWfy94cpJ2BUliC+VeIrq6qlBAPcQQN2iNuewd/lPGtxjrEYvd1FJTPzoaQkNI3Sv43d7iH+609gpxNdRK74MDdfLp3Dz+hfT/CsDgQVs1+J/oQX2PKtVMX010/5JHBTNt1DHRtyzbteRxuO9Y1Q7JusTsAWTK7N+S8oqc1twpqQZ5TTMjOXIXAeta05KMdX7GzYoxjtj2RZuHKU4ZwFHJ8GtuBEpI3gu3dTVitdq5ZLa4ina6sipm7I4IxkOk/7ALS63Svh4KVut0u8nr/AIO8OvbXufd9T218ygcvIOX6HL1xLeh6621fNyutHh+39m1u152Qw8b3L8qaumtFBJca12Uce5nG53EB0qBUstRie7vu9wP5KM5RR/JblxeJT42Lxnul6V+v0Klk3Kaqh3ZsoGVN4rHXi9POzbFDxRjiyHKvSprHzu1R3MTfgsHF/uvirquFIYzZG3d09KxdZa8YrRJLRF6CjUtInsXprLx19m9NZTJHfFPfW2L91l4hy+tYLtEkbeh7tcvRr81jt27ljy1wB1ISCdxfxDvcqkitSSV0Yx1kZVRU6p4Jh7o7zyLzadixIzvPLtJXsHbFNGBUjc5PcZLXr1a/IrFa7YvtrlYhEuV2bl1M6OTLjXhdK90kMVID3LHF5HSRsXzwojjdI74Ldq1jpC9znO+ETmV20tCrlyitF7nzK/uVH7xMW0TGcdTKXf0t7kecuW6qdeRoihBMjzqtA5So/fy03ttMw/k6drYW9OQ2nxnNEuqR818Utaqen5GDWbI4YWjj2BdzwxiGCOIbmNDR4guJbdTe6WLLTQN3zVUMPjc8D8V26oL3+M+ck9WERFCchERAMhyJkOREQDIciZDkREAyHImQ5ERAMhyJkOREQDIciZDkREAyHImQ5ERAMhyJkOREQDIciZDkREAyHImQ5ERAEREAREQDIciZDkREAyHImQ5ERAMhyJkOREQDIciZDkREAyHImQ5ERAMhyJkOREQDIIiIAiIgCIiAIiIAiIgGQ5EyHIiIBkORMhyIiAZDkTIciIgGQ5EREAREQBERAEREAREQBERAEyREAyHImQ5ERAMhyJkOREQDIciZDkREAyHIiIgCZBEQDIciZDkREAyHImQ5ERAMhyJkOREQBERAEREAREQBERAEREAREQBERAEREAREQBRPSVQ9n4DuTQM3QtbMO80jP/tzUsXhXUrK6gqKST83PE6N3ecMj6V1CW2Sl4Bx5bSWulhO/IjLpBX05ubivyrjfbr3MyQarmPzcOQjY4eYrImZqyHLdvB6Fux7aeDyPY9sN4g96WLqWveT2HUt4CpA+aTv8Ww+JTnSJe22eyvZTSgz135OFzD/ANMgFzx4iAO+qwukHD25+zuoyHjxb/MtXU19VV0tNDUzvlZTMMcOu7PUaTnqjozWBn/CYXZcMjx3+vj9S9j5Mq4Sgvc8GkDYApDhyIMo5p+OSTV8Q/8A6o2DkN6lVmGrZoulzj5yrk12ND4Ytb9fCf8Aj+5mOd+Uz6CszDuT8XWtpGf+Ja7qBK1xP5QZrNsT+BxTa5c8v8Q1uZ6QR+KqZafAnp4f7GvY9UT+5Sme6Vb92UpZl/Ds/BYS96rPs6rB/byfeK8F87VXpBL6F+rpBL6I/M1l0zIoaSSvq3iKCMEgu3HLee8POVjwxOnqGQtORecieQcZ6lFMfX7h6ltkpH5U1P8AntU7HHib3h6UWM7bFXH37/REOVdw46LuaDEF8qMRXFjY2ubTh2rBGTvzPwj0lb9zGUFDFSRbABl3+U+MqM2WES3iDPczN58QW8qZeEmc7PoC2ZVxhpXHsiHD/DCVr7t6H4Xr84ReWsvwnaiiTObPUvTXK+I43yE5DYN5K8pq6iphk6bhpPmRbfPuXSXg836LWT0MxjiSAAv2aogpR+XkDXcTBtcfEtHPeKmYFsIFOz9z4XX6ljRtzOsSS47yTtKmjS33InmLtBam0mrZaruW5xRfNB2nvlfbCA0ABYkZyXuwnLerEa0jjiOT1kzLY5ewdsWKw9K9mnYu1EmjPoZDHL1bmTsWMwr5mqdUGJh7o7HEcXQu0tCzC5RWrP2pn13cGzaxm88pXjnsX40ZN6FuLVbuFLaiZvcDaxvKeVNCtKcptyYt1J2LRzXGobqljC5oPyQOPvqtxI6sub53bi4v2qd45uvYluZbon5TVPdPy4mDi8ZUCDhBTSO+U7YF7Hq9fB858UvUpqpe3UlmiaiF00r2YObrMjmdOejUY5wPWAuv1zh/8ONndPiK63hw7ilphAzMfKkdnmO8GHyl0eqUnq9TICLXX65Gz2CvuQa1zqaB8jWu3OcBsB75yVQdu68c1UPW/wBakronYtYkc7Iw6MvBFR/buvHNVD1v9adu68c1UPW/1qTk7fBzx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/AFp27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v8AWnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/wBacnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/AFp27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v8AWnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvH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iIc/hJCOJx2dQW1YxsbA1jQ1o3ADIBWsPEy1dxr5/YhvupcOHXH7kaxR/mYP4Sv3DMUcpquEja/LVy1hnlvW4rrVT3B7HTGQFoyGqQPwX1QWyC3cJwJedfLPWOe7P1rnkLH8Q5hpbf8AjQ95mHLcJd/+Twulqiq6QiGNjJm7W6oAz6FFqKqkt9Y2VoILTk5p4xxhTxayqsVHVVDpn8I1zt4YQB6F1n/DpWTjdj9JI8xspRi4W9UzPgmZUQsljdmxwzBUXxN+kWfyh6SpFRUMdBEY4nyOYTnk855d5eVbaKavmEszpA4N1e5IH4KfNouycXZp+LoR49kKrt3sRu13c21kjRCJNcg562WXmWf76XfRB9Z/ssv3tUPz5vKHqX772qH583lD1LPqxviVUFCDWiLM7cScnKSepix4nc+RrexANYgZ8J/st3W/5Gf+W70LXtw5RMeHB02YOY7oepbSWMSxPjdnquBByWliQytklkPVvsVbnTquEV806rgeQ5qQe+l30QfWf7LM97VD8+byh6k97VD8+byh6lkY+B8Qx9eG0tS7bk41um/XoYfvpd9EH1n+y2dquZuTJSYhHqED4Weea8Pe1Q/Pm8oepZtDbobe14hLyHkE6xz3LRxYZ6tTua2lW54zg+GuposT/wCbh/gPpX3hmKOXsrhI2Py1MtYA5b1t661U9wka+Z0gLRkNUgfgvqgtsFu4TgS86+Wesc92frUSwLP/ACHMNLb/AMaHfMw5bhLv/wAmPdbVHVUh4GNjJmbW6oAz6FGKGrkt9Y2VoOw5PaeMcYU7WsqbFR1VQ6Z3CNc7eGEAehdZ/wAOlOyN2P0kjzGyoxi67eqZnwzMqIWyxuzY4Zgr0WNRUMdBEYonyOYTnk855d5ZK1q3JwW9aP3KctNXt7BERdnIREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQH/2Q==" alt="EBAF Business Center">
  </a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#boutique">Boutique</a></li>
    <li><a href="#commander">Commander</a></li>
    <li><a href="#temoignages">Avis</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="nav-cta">
    <button class="btn-outline" onclick="toggleAdmin()">⚙️ Admin</button>
    <button class="cart-btn" onclick="toggleCart()">
      🛒
      <span class="cart-badge" id="cart-count">0</span>
    </button>
    <a href="#boutique" class="btn-primary">Commander</a>
  </div>
  <button class="hamburger" onclick="toggleMenu()" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
</nav>

<!-- HERO -->
<section id="accueil" class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-content animate-in">
    <div class="hero-badge">🏆 N°1 Impression à Abidjan</div>
    <h1>EBAF<br><span>Business</span><br>Center</h1>
    <p class="hero-sub">Votre partenaire en impression, broderie et personnalisation de qualité premium à Abidjan.</p>
    <p class="hero-slogan">IMPRIMER • BRODER • CRÉER</p>
    <div class="hero-actions">
      <a href="#boutique" class="btn-primary btn-lg">🛒 Commander maintenant</a>
      <a href="#commander" class="btn-outline btn-lg">📋 Demander un devis</a>
      <a href="https://wa.me/2250704423114?text=Bonjour%20EBAF%20Business%20Center%2C%20je%20souhaite%20obtenir%20des%20informations%20sur%20vos%20services." class="btn-wa btn-lg" target="_blank">💬 WhatsApp</a>
    </div>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-num">500+</div>
        <div class="stat-label">Clients satisfaits</div>
      </div>
      <div class="stat">
        <div class="stat-num">15+</div>
        <div class="stat-label">Services offerts</div>
      </div>
      <div class="stat">
        <div class="stat-num">24h</div>
        <div class="stat-label">Délai express</div>
      </div>
    </div>
  </div>
  <div class="hero-visual">
    <div class="hero-logo-display">
      <img src="data:image/jpeg;base64,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u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/wBacnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/AFp27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v8AWnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvH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iIc/hJCOJx2dQW1YxsbA1jQ1o3ADIBWsPEy1dxr5/YhvupcOHXH7kaxR/mYP4Sv3DMUcpquEja/LVy1hnlvW4rrVT3B7HTGQFoyGqQPwX1QWyC3cJwJedfLPWOe7P1rnkLH8Q5hpbf8AjQ95mHLcJd/+Twulqiq6QiGNjJm7W6oAz6FFqKqkt9Y2VoILTk5p4xxhTxayqsVHVVDpn8I1zt4YQB6F1n/DpWTjdj9JI8xspRi4W9UzPgmZUQsljdmxwzBUXxN+kWfyh6SpFRUMdBEY4nyOYTnk855d5eVbaKavmEszpA4N1e5IH4KfNouycXZp+LoR49kKrt3sRu13c21kjRCJNcg562WXmWf76XfRB9Z/ssv3tUPz5vKHqX772qH583lD1LPqxviVUFCDWiLM7cScnKSepix4nc+RrexANYgZ8J/st3W/5Gf+W70LXtw5RMeHB02YOY7oepbSWMSxPjdnquBByWliQytklkPVvsVbnTquEV806rgeQ5qQe+l30QfWf7LM97VD8+byh6k97VD8+byh6lkY+B8Qx9eG0tS7bk41um/XoYfvpd9EH1n+y2dquZuTJSYhHqED4Weea8Pe1Q/Pm8oepZtDbobe14hLyHkE6xz3LRxYZ6tTua2lW54zg+GuposT/wCbh/gPpX3hmKOXsrhI2Py1MtYA5b1t661U9wka+Z0gLRkNUgfgvqgtsFu4TgS86+Wesc92frUSwLP/ACHMNLb/AMaHfMw5bhLv/wAmPdbVHVUh4GNjJmbW6oAz6FGKGrkt9Y2VoOw5PaeMcYU7WsqbFR1VQ6Z3CNc7eGEAehdZ/wAOlOyN2P0kjzGyoxi67eqZnwzMqIWyxuzY4Zgr0WNRUMdBEYonyOYTnk855d5ZK1q3JwW9aP3KctNXt7BERdnIREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQH/2Q==" alt="EBAF Business Center Logo">
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="section-label">Ce que nous faisons</div>
  <h2 class="section-title">Nos <span>Services</span></h2>
  <p class="section-sub">Des solutions d'impression et de personnalisation haut de gamme pour particuliers et entreprises.</p>
  
  <div class="services-grid">
    <!-- Impression -->
    <div class="service-card" onclick="location.href='#boutique'">
      <div class="service-mockup mockup-print">
        <div class="mockup-inner" style="gap:1.5rem;">
          <div class="mock-flyer">
            <div class="mock-flyer-img"></div>
            <div class="mock-flyer-line thick"></div>
            <div class="mock-flyer-line"></div>
            <div class="mock-flyer-line"></div>
          </div>
          <div style="display:flex;flex-direction:column;gap:10px;">
            <div class="mock-card-vis">
              <div class="mock-card-chip"></div>
              <div class="mock-card-name">EBAF BUSINESS CENTER</div>
            </div>
            <div style="width:80px;height:55px;background:linear-gradient(135deg,#d946ef,#f97316);border-radius:6px;border:2px solid rgba(255,255,255,0.2);display:flex;align-items:center;justify-content:center;font-size:0.6rem;color:#fff;font-weight:700;letter-spacing:0.05em;">AFFICHE A4</div>
          </div>
        </div>
      </div>
      <div class="service-info">
        <div class="service-icon" style="background:rgba(26,63,160,0.2);">🖨️</div>
        <div class="service-name">Impression</div>
        <div class="service-desc">Flyers, affiches, cartes de visite et bien plus avec une qualité professionnelle.</div>
        <div class="service-items">
          <span class="pill">Flyers</span>
          <span class="pill">Affiches A4/A3</span>
          <span class="pill">Cartes de visite</span>
          <span class="pill">Kakémono</span>
        </div>
      </div>
    </div>

    <!-- Textile -->
    <div class="service-card" onclick="location.href='#boutique'">
      <div class="service-mockup mockup-textile">
        <div class="mockup-inner" style="gap:1.5rem;">
          <div class="mock-tshirt">
            <div class="mock-polo-shape">
              <div class="mock-polo-collar"></div>
              <div class="mock-polo-logo"></div>
            </div>
          </div>
          <div style="display:flex;flex-direction:column;gap:8px;align-items:center;">
            <div style="font-size:0.65rem;color:rgba(255,255,255,0.7);font-weight:700;letter-spacing:0.05em;text-align:center;">T-SHIRT DTF</div>
            <div style="width:70px;height:70px;background:linear-gradient(135deg,#7c3aed,#d946ef);clip-path:polygon(20% 0%, 80% 0%, 100% 25%, 100% 100%, 0% 100%, 0% 25%);display:flex;align-items:center;justify-content:center;"></div>
            <div style="font-size:0.65rem;color:rgba(255,255,255,0.7);font-weight:700;letter-spacing:0.05em;">BRODÉ</div>
          </div>
        </div>
      </div>
      <div class="service-info">
        <div class="service-icon" style="background:rgba(124,58,237,0.2);">👕</div>
        <div class="service-name">Textile</div>
        <div class="service-desc">T-shirts et polos personnalisés par impression DTF ou broderie professionnelle.</div>
        <div class="service-items">
          <span class="pill">T-shirt DTF</span>
          <span class="pill">T-shirt brodé</span>
          <span class="pill">Polo brodé</span>
        </div>
      </div>
    </div>

    <!-- Personnalisation -->
    <div class="service-card" onclick="location.href='#boutique'">
      <div class="service-mockup mockup-perso">
        <div class="mockup-inner" style="gap:1.5rem;">
          <div class="mock-mug">
            <div class="mock-mug-design">☕</div>
          </div>
          <div style="display:flex;flex-direction:column;gap:12px;align-items:center;">
            <div class="mock-bottle"></div>
            <div class="mock-sticker" style="width:70px;height:70px;border-radius:12px;font-size:1.5rem;">⭐</div>
          </div>
        </div>
      </div>
      <div class="service-info">
        <div class="service-icon" style="background:rgba(217,70,239,0.2);">🎁</div>
        <div class="service-name">Personnalisation</div>
        <div class="service-desc">Tasses, bouteilles et cadeaux d'entreprise à votre image pour marquer les esprits.</div>
        <div class="service-items">
          <span class="pill">Tasses</span>
          <span class="pill">Bouteilles</span>
          <span class="pill">Pack cadeau</span>
        </div>
      </div>
    </div>

    <!-- Design -->
    <div class="service-card" onclick="location.href='#boutique'">
      <div class="service-mockup mockup-design">
        <div class="mockup-inner" style="gap:1rem;">
          <div style="display:flex;flex-direction:column;gap:8px;">
            <div style="width:80px;height:80px;background:radial-gradient(circle at 40% 40%, #eab308, #f97316, #d946ef);border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:2rem;box-shadow:4px 4px 12px rgba(0,0,0,0.4);">✦</div>
            <div style="font-size:0.6rem;color:rgba(255,255,255,0.7);font-weight:700;letter-spacing:0.08em;text-align:center;">LOGO</div>
          </div>
          <div style="display:flex;flex-direction:column;gap:8px;">
            <div class="mock-poster">
              <div style="width:100%;height:40px;background:rgba(255,255,255,0.15);border-radius:3px;"></div>
              <div style="width:80%;height:4px;background:rgba(255,255,255,0.5);border-radius:2px;"></div>
              <div style="width:60%;height:3px;background:rgba(255,255,255,0.3);border-radius:2px;"></div>
              <div style="width:70%;height:3px;background:rgba(255,255,255,0.3);border-radius:2px;"></div>
            </div>
          </div>
        </div>
      </div>
      <div class="service-info">
        <div class="service-icon" style="background:rgba(249,115,22,0.2);">🎨</div>
        <div class="service-name">Création Graphique</div>
        <div class="service-desc">Logos, flyers, affiches et visuels réseaux sociaux réalisés par nos designers.</div>
        <div class="service-items">
          <span class="pill">Logos</span>
          <span class="pill">Flyers</span>
          <span class="pill">Affiches</span>
          <span class="pill">Réseaux sociaux</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- BOUTIQUE -->
<section id="boutique">
  <div class="section-label">Boutique en ligne</div>
  <h2 class="section-title">Nos <span>Produits</span></h2>
  <p class="section-sub">Commandez directement en ligne. Livraison ou retrait en boutique à Riviera Palmeraie.</p>
  
  <div class="product-tabs">
    <button class="tab-btn active" onclick="filterProducts('all',this)">Tout voir</button>
    <button class="tab-btn" onclick="filterProducts('impression',this)">Impression</button>
    <button class="tab-btn" onclick="filterProducts('textile',this)">Textile</button>
    <button class="tab-btn" onclick="filterProducts('perso',this)">Personnalisation</button>
    <button class="tab-btn" onclick="filterProducts('design',this)">Design</button>
  </div>

  <div class="products-grid" id="products-grid">
    <!-- Flyers -->
    <div class="product-card" data-cat="impression">
      <div class="product-img" style="background:linear-gradient(135deg,#0d1b4b,#1a3fa0);">
        <div class="mock-flyer" style="transform:rotate(-3deg);">
          <div class="mock-flyer-img"></div>
          <div class="mock-flyer-line thick"></div>
          <div class="mock-flyer-line"></div>
          <div class="mock-flyer-line"></div>
        </div>
        <div class="mock-flyer" style="transform:rotate(5deg);margin-left:-20px;margin-top:15px;">
          <div class="mock-flyer-img" style="background:linear-gradient(135deg,#f97316,#eab308);"></div>
          <div class="mock-flyer-line thick"></div>
          <div class="mock-flyer-line"></div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Flyers</div>
        <div class="product-meta">Format A5 · Recto/Verso · Qualité premium</div>
        <div class="product-price">10 000 <small>FCFA / 200 pcs</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Flyers (200 pcs)', 10000, '📄')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Flyers')">💬</button>
        </div>
      </div>
    </div>

    <!-- Affiche A4 -->
    <div class="product-card" data-cat="impression">
      <div class="product-img" style="background:linear-gradient(135deg,#2d0b4e,#7c3aed);">
        <div class="mock-poster" style="width:120px;height:165px;">
          <div style="width:100%;height:55px;background:linear-gradient(135deg,rgba(255,255,255,0.25),rgba(255,255,255,0.1));border-radius:4px;"></div>
          <div style="width:85%;height:5px;background:rgba(255,255,255,0.6);border-radius:2px;"></div>
          <div style="width:65%;height:4px;background:rgba(255,255,255,0.35);border-radius:2px;"></div>
          <div style="width:75%;height:4px;background:rgba(255,255,255,0.35);border-radius:2px;"></div>
          <div style="width:85%;height:4px;background:rgba(255,255,255,0.35);border-radius:2px;"></div>
          <div style="width:50%;height:20px;background:rgba(249,115,22,0.6);border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:0.55rem;color:#fff;font-weight:700;">A4</div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Affiche A4</div>
        <div class="product-meta">21×29.7cm · Haute résolution · Papier glacé</div>
        <div class="product-price">18 000 <small>FCFA / 200 pcs</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Affiches A4 (200 pcs)', 18000, '🖼️')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Affiche A4')">💬</button>
        </div>
      </div>
    </div>

    <!-- Affiche A3 -->
    <div class="product-card" data-cat="impression">
      <div class="product-img" style="background:linear-gradient(135deg,#3d1a00,#f97316);">
        <div class="mock-poster" style="width:130px;height:175px;background:linear-gradient(135deg,#f97316,#eab308);">
          <div style="width:100%;height:65px;background:rgba(255,255,255,0.2);border-radius:4px;"></div>
          <div style="width:85%;height:5px;background:rgba(255,255,255,0.7);border-radius:2px;"></div>
          <div style="width:65%;height:4px;background:rgba(255,255,255,0.4);border-radius:2px;"></div>
          <div style="width:75%;height:4px;background:rgba(255,255,255,0.4);border-radius:2px;"></div>
          <div style="width:50%;height:20px;background:rgba(26,63,160,0.6);border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:0.55rem;color:#fff;font-weight:700;">A3</div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Affiche A3</div>
        <div class="product-meta">29.7×42cm · Grand format · Papier premium</div>
        <div class="product-price">25 000 <small>FCFA / 200 pcs</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Affiches A3 (200 pcs)', 25000, '🖼️')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Affiche A3')">💬</button>
        </div>
      </div>
    </div>

    <!-- Cartes de visite -->
    <div class="product-card" data-cat="impression">
      <div class="product-img" style="background:linear-gradient(135deg,#0a0a2e,#1a3fa0);">
        <div style="display:flex;flex-direction:column;gap:-5px;transform:rotate(-10deg);">
          <div class="mock-card-vis" style="transform:translateY(0) rotate(3deg);"></div>
          <div class="mock-card-vis" style="transform:translateY(-65px) rotate(-2deg);background:linear-gradient(135deg,#7c3aed,#d946ef);"></div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Cartes de visite</div>
        <div class="product-meta">85×55mm · Recto/Verso · Pelliculage mat ou brillant</div>
        <div class="product-price">7 500 <small>FCFA / 200 pcs</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Cartes de visite (200 pcs)', 7500, '💼')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Carte de visite')">💬</button>
        </div>
      </div>
    </div>

    <!-- Kakemono -->
    <div class="product-card" data-cat="impression">
      <div class="product-img" style="background:linear-gradient(135deg,#0d1b4b,#1a3fa0);">
        <div style="display:flex;gap:1rem;align-items:center;">
          <div class="mock-kakemono">
            <div style="width:50px;height:25px;background:rgba(255,255,255,0.2);border-radius:3px;"></div>
            <div style="width:40%;height:4px;background:rgba(255,255,255,0.5);border-radius:2px;"></div>
            <div style="width:60%;height:3px;background:rgba(255,255,255,0.3);border-radius:2px;"></div>
            <div style="width:50%;height:3px;background:rgba(255,255,255,0.3);border-radius:2px;"></div>
          </div>
          <div style="color:rgba(255,255,255,0.6);font-size:0.7rem;font-weight:700;letter-spacing:0.1em;writing-mode:vertical-lr;transform:rotate(180deg);">85×200 cm</div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Kakémono</div>
        <div class="product-meta">85×200cm · Roll-up · Pied inclus</div>
        <div class="product-price">40 000 <small>FCFA / pièce</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Kakémono 85×200cm', 40000, '📋')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Kakémono')">💬</button>
        </div>
      </div>
    </div>

    <!-- Sticker -->
    <div class="product-card" data-cat="impression">
      <div class="product-img" style="background:linear-gradient(135deg,#2d1a00,#eab308);">
        <div style="display:flex;flex-wrap:wrap;gap:8px;padding:1rem;justify-content:center;">
          <div class="mock-sticker" style="width:75px;height:75px;font-size:2rem;">⭐</div>
          <div class="mock-sticker" style="width:65px;height:55px;background:linear-gradient(135deg,#1a3fa0,#00bcd4);border-radius:8px;font-size:1.8rem;transform:rotate(3deg);">✦</div>
          <div class="mock-sticker" style="width:55px;height:65px;background:linear-gradient(135deg,#d946ef,#7c3aed);font-size:1.5rem;transform:rotate(-8deg);">★</div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Stickers</div>
        <div class="product-meta">Formes variées · Vinyle haute qualité · Résistant</div>
        <div class="product-price">1 500 <small>FCFA / feuille</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Stickers (1 feuille)', 1500, '⭐')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Sticker')">💬</button>
        </div>
      </div>
    </div>

    <!-- T-shirt DTF -->
    <div class="product-card" data-cat="textile">
      <div class="product-img" style="background:linear-gradient(135deg,#1e1b4b,#7c3aed);">
        <div style="position:relative;width:120px;height:140px;display:flex;align-items:center;justify-content:center;">
          <div style="width:110px;height:120px;background:linear-gradient(180deg,#fff1 0%,#fff0 100%);clip-path:polygon(18% 0%,82% 0%,100% 20%,95% 100%,5% 100%,0% 20%);display:flex;align-items:center;justify-content:center;background:#2d235e;">
            <div style="width:40px;height:40px;background:radial-gradient(circle,#f97316,#d946ef);border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:1.2rem;">✦</div>
          </div>
          <div style="position:absolute;top:0;left:50%;transform:translateX(-50%);width:36px;height:22px;background:#1a1040;clip-path:polygon(0 0,100% 0,85% 100%,15% 100%);"></div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">T-shirt DTF</div>
        <div class="product-meta">Impression directe sur tissu · Toutes couleurs</div>
        <div class="product-price">3 500 <small>FCFA / pièce</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('T-shirt DTF', 3500, '👕')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('T-shirt DTF')">💬</button>
        </div>
      </div>
    </div>

    <!-- T-shirt brodé -->
    <div class="product-card" data-cat="textile">
      <div class="product-img" style="background:linear-gradient(135deg,#0a2e1a,#16a34a);">
        <div style="position:relative;width:120px;height:140px;display:flex;align-items:center;justify-content:center;">
          <div style="width:110px;height:120px;clip-path:polygon(18% 0%,82% 0%,100% 20%,95% 100%,5% 100%,0% 20%);background:#134e23;display:flex;align-items:center;justify-content:center;">
            <div style="width:45px;height:20px;background:rgba(255,255,255,0.2);border-radius:4px;border:1px solid rgba(255,255,255,0.4);display:flex;align-items:center;justify-content:center;font-size:0.5rem;color:#fff;font-weight:700;letter-spacing:0.05em;">BRODÉ</div>
          </div>
          <div style="position:absolute;top:0;left:50%;transform:translateX(-50%);width:36px;height:22px;background:#0a3015;clip-path:polygon(0 0,100% 0,85% 100%,15% 100%);"></div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">T-shirt brodé logo</div>
        <div class="product-meta">Broderie haute définition · Finition premium</div>
        <div class="product-price">4 000 <small>FCFA / pièce</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('T-shirt brodé logo', 4000, '🪡')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('T-shirt brodé')">💬</button>
        </div>
      </div>
    </div>

    <!-- Polo brodé -->
    <div class="product-card" data-cat="textile">
      <div class="product-img" style="background:linear-gradient(135deg,#1e1b4b,#312e81);">
        <div style="position:relative;width:120px;height:140px;display:flex;align-items:center;justify-content:center;">
          <div style="width:115px;height:125px;background:#252060;clip-path:polygon(18% 0%,82% 0%,100% 18%,96% 100%,4% 100%,0% 18%);display:flex;align-items:flex-start;justify-content:center;padding-top:30px;">
            <div style="width:35px;height:35px;background:radial-gradient(circle,#eab308,#f97316);border-radius:50%;"></div>
          </div>
          <div style="position:absolute;top:0;left:50%;transform:translateX(-50%);width:38px;height:28px;background:#1a1755;clip-path:polygon(0 0,100% 0,80% 100%,20% 100%);border:1px solid rgba(255,255,255,0.1);"></div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Polo brodé logo</div>
        <div class="product-meta">Logo avant · Poignets brodés · Tissu polo coton</div>
        <div class="product-price">5 000 <small>FCFA / pièce</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Polo brodé logo avant', 5000, '🥼')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Polo brodé')">💬</button>
        </div>
      </div>
    </div>

    <!-- Tasse -->
    <div class="product-card" data-cat="perso">
      <div class="product-img" style="background:linear-gradient(135deg,#4a0a2e,#d946ef);">
        <div style="display:flex;gap:1rem;align-items:center;">
          <div class="mock-mug" style="width:100px;height:100px;">
            <div class="mock-mug-design" style="width:55px;height:55px;">☕</div>
          </div>
          <div class="mock-mug" style="width:85px;height:90px;background:linear-gradient(135deg,#1a3fa0,#00bcd4);">
            <div class="mock-mug-design" style="width:48px;height:48px;font-size:1.3rem;">★</div>
          </div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Tasse personnalisée</div>
        <div class="product-meta">Céramique · Impression HD · Lave-vaisselle safe</div>
        <div class="product-price">5 000 <small>FCFA / pièce</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Tasse personnalisée', 5000, '☕')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Tasse')">💬</button>
        </div>
      </div>
    </div>

    <!-- Bouteille -->
    <div class="product-card" data-cat="perso">
      <div class="product-img" style="background:linear-gradient(135deg,#063040,#00bcd4);">
        <div style="display:flex;gap:1.5rem;align-items:center;">
          <div class="mock-bottle" style="width:65px;height:130px;"></div>
          <div class="mock-bottle" style="width:55px;height:110px;background:linear-gradient(180deg,#d946ef,#7c3aed);"></div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Bouteille personnalisée</div>
        <div class="product-meta">Inox ou plastique · Impression 360° · Étanche</div>
        <div class="product-price">5 000 <small>FCFA / pièce</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Bouteille personnalisée', 5000, '🍶')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Bouteille')">💬</button>
        </div>
      </div>
    </div>

    <!-- Pack Cadeau -->
    <div class="product-card" data-cat="perso">
      <div class="product-img" style="background:linear-gradient(135deg,#2d1a00,#f97316);">
        <div style="display:flex;gap:0.75rem;align-items:center;padding:1rem;">
          <div class="mock-mug" style="width:70px;height:70px;background:linear-gradient(135deg,#f97316,#eab308);">
            <div class="mock-mug-design" style="width:40px;height:40px;font-size:1.1rem;">🎁</div>
          </div>
          <div style="display:flex;flex-direction:column;gap:8px;">
            <div style="width:14px;height:80px;background:linear-gradient(180deg,#1a3fa0,#00bcd4);border-radius:4px;"></div>
          </div>
          <div style="display:flex;flex-direction:column;gap:6px;">
            <div style="width:55px;height:42px;background:linear-gradient(135deg,#7c3aed,#d946ef);border-radius:6px;border:1px solid rgba(255,255,255,0.2);"></div>
          </div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Pack Cadeau Entreprise</div>
        <div class="product-meta">Tasse + Stylo + Carnet · Coffret premium</div>
        <div class="product-price">10 000 <small>FCFA / pack</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Pack Cadeau Entreprise', 10000, '🎁')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Pack Cadeau')">💬</button>
        </div>
      </div>
    </div>

    <!-- Conception graphique -->
    <div class="product-card" data-cat="design">
      <div class="product-img" style="background:linear-gradient(135deg,#1a0a00,#f97316);">
        <div style="display:flex;gap:1rem;align-items:center;padding:1rem;">
          <div style="width:80px;height:80px;background:conic-gradient(from 0deg, #1a3fa0, #7c3aed, #d946ef, #f97316, #eab308, #1a3fa0);border-radius:50%;display:flex;align-items:center;justify-content:center;">
            <div style="width:55px;height:55px;background:#1a0a00;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.8rem;">✦</div>
          </div>
          <div style="display:flex;flex-direction:column;gap:6px;">
            <div style="width:75px;height:30px;background:linear-gradient(135deg,#1a3fa0,#00bcd4);border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:0.55rem;color:#fff;font-weight:700;letter-spacing:0.05em;">LOGO DESIGN</div>
            <div style="width:65px;height:25px;background:linear-gradient(135deg,#7c3aed,#d946ef);border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:0.55rem;color:#fff;font-weight:700;letter-spacing:0.05em;">FLYER</div>
            <div style="width:55px;height:25px;background:linear-gradient(135deg,#f97316,#eab308);border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:0.55rem;color:#fff;font-weight:700;letter-spacing:0.05em;">RÉSEAUX</div>
          </div>
        </div>
      </div>
      <div class="product-details">
        <div class="product-name">Conception graphique</div>
        <div class="product-meta">Logo, flyer, affiche, visuels réseaux sociaux</div>
        <div class="product-price">5 000 <small>FCFA / création</small></div>
        <div class="product-actions">
          <button class="btn-add-cart" onclick="addToCart('Conception graphique', 5000, '🎨')">🛒 Ajouter</button>
          <button class="btn-quick" onclick="quickOrder('Conception graphique')">💬</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- COMMANDER / UPLOAD -->
<section id="commander">
  <div style="display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:start;">
    <div>
      <div class="section-label">Commande personnalisée</div>
      <h2 class="section-title">Envoyez votre <span>fichier</span></h2>
      <p class="section-sub" style="margin-bottom:2rem;">Téléchargez vos fichiers, précisez vos besoins et nous vous répondons en moins de 2h.</p>
      
      <div style="display:flex;flex-direction:column;gap:1.25rem;margin-bottom:2rem;">
        <div style="display:flex;gap:1rem;align-items:start;">
          <div style="width:44px;height:44px;background:rgba(0,188,212,0.15);border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:1.3rem;flex-shrink:0;">📁</div>
          <div>
            <div style="font-weight:600;margin-bottom:0.25rem;">Formats acceptés</div>
            <div style="color:var(--text-muted);font-size:0.88rem;">PNG, JPG, PDF, AI, PSD</div>
          </div>
        </div>
        <div style="display:flex;gap:1rem;align-items:start;">
          <div style="width:44px;height:44px;background:rgba(124,58,237,0.15);border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:1.3rem;flex-shrink:0;">⚡</div>
          <div>
            <div style="font-weight:600;margin-bottom:0.25rem;">Réponse rapide</div>
            <div style="color:var(--text-muted);font-size:0.88rem;">Devis en moins de 2 heures</div>
          </div>
        </div>
        <div style="display:flex;gap:1rem;align-items:start;">
          <div style="width:44px;height:44px;background:rgba(249,115,22,0.15);border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:1.3rem;flex-shrink:0;">🚚</div>
          <div>
            <div style="font-weight:600;margin-bottom:0.25rem;">Livraison disponible</div>
            <div style="color:var(--text-muted);font-size:0.88rem;">Abidjan et environs</div>
          </div>
        </div>
      </div>
    </div>
    
    <div class="order-form">
      <div class="form-group">
        <label class="form-label">Nom complet *</label>
        <input type="text" class="form-control" placeholder="Jean Kouassi" id="order-name">
      </div>
      <div class="form-group">
        <label class="form-label">Téléphone / WhatsApp *</label>
        <input type="tel" class="form-control" placeholder="07 XX XX XX XX" id="order-phone">
      </div>
      <div class="form-group">
        <label class="form-label">Produit souhaité</label>
        <select class="form-control" id="order-product">
          <option>-- Sélectionner un produit --</option>
          <option>Flyers (200 pcs) - 10 000 FCFA</option>
          <option>Affiches A4 (200 pcs) - 18 000 FCFA</option>
          <option>Affiches A3 (200 pcs) - 25 000 FCFA</option>
          <option>Cartes de visite (200 pcs) - 7 500 FCFA</option>
          <option>Kakémono 85×200cm - 40 000 FCFA</option>
          <option>T-shirt DTF - 3 500 FCFA</option>
          <option>T-shirt brodé logo - 4 000 FCFA</option>
          <option>Broderie logo seule - 500 FCFA</option>
          <option>Tasse personnalisée - 5 000 FCFA</option>
          <option>Bouteille personnalisée - 5 000 FCFA</option>
          <option>Sticker - 1 500 FCFA</option>
          <option>Polo brodé logo avant - 5 000 FCFA</option>
          <option>Polo brodé texte + logo - 6 500 FCFA</option>
          <option>Pack Cadeau Entreprise - 10 000 FCFA</option>
          <option>Conception graphique - 5 000 FCFA</option>
        </select>
      </div>
      <div class="form-group">
        <label class="form-label">Quantité</label>
        <input type="number" class="form-control" placeholder="200" min="1" id="order-qty">
      </div>
      <div class="form-group">
        <label class="form-label">Votre fichier (logo, image, PDF...)</label>
        <div class="upload-zone" onclick="document.getElementById('file-input').click()">
          <div class="upload-icon">📎</div>
          <div class="upload-text" id="upload-text">Cliquez pour importer votre fichier</div>
          <div class="upload-formats">PNG · JPG · PDF · AI · PSD · Max 50MB</div>
        </div>
        <input type="file" id="file-input" style="display:none" accept=".png,.jpg,.jpeg,.pdf,.ai,.psd" onchange="handleFileUpload(this)">
      </div>
      <div class="form-group">
        <label class="form-label">Instructions spéciales</label>
        <textarea class="form-control" rows="3" placeholder="Couleurs, taille, précisions..." id="order-notes"></textarea>
      </div>
      <button class="btn-primary" style="width:100%;padding:0.9rem;font-size:1rem;border-radius:12px;" onclick="submitOrder()">
        📤 Envoyer ma commande
      </button>
    </div>
  </div>
</section>

<!-- PAIEMENT -->
<section id="paiement">
  <div class="section-label">Paiement sécurisé</div>
  <h2 class="section-title">Payez en toute <span>confiance</span></h2>
  <p class="section-sub">Plusieurs moyens de paiement disponibles, adaptés à la Côte d'Ivoire.</p>
  
  <div class="payment-methods">
    <div class="payment-card" style="border-color:rgba(255,100,0,0.3);background:rgba(255,100,0,0.05);">
      <div class="payment-logo">🟠</div>
      <div class="payment-name">Orange Money</div>
      <div class="payment-desc">Paiement instantané via votre compte Orange Money CI</div>
    </div>
    <div class="payment-card" style="border-color:rgba(0,188,212,0.3);background:rgba(0,188,212,0.05);">
      <div class="payment-logo">🌊</div>
      <div class="payment-name">Wave</div>
      <div class="payment-desc">Transfert rapide et sans frais via l'application Wave</div>
    </div>
    <div class="payment-card" style="border-color:rgba(124,58,237,0.3);background:rgba(124,58,237,0.05);">
      <div class="payment-logo">📱</div>
      <div class="payment-name">MTN Mobile Money</div>
      <div class="payment-desc">Disponible via CinetPay pour tous les opérateurs</div>
    </div>
    <div class="payment-card" style="border-color:rgba(26,63,160,0.3);background:rgba(26,63,160,0.05);">
      <div class="payment-logo">💳</div>
      <div class="payment-name">Carte bancaire</div>
      <div class="payment-desc">Visa, Mastercard · Paiement 3D Secure via CinetPay</div>
    </div>
    <div class="payment-card" style="border-color:rgba(234,179,8,0.3);background:rgba(234,179,8,0.05);">
      <div class="payment-logo">📲</div>
      <div class="payment-name">QR Code</div>
      <div class="payment-desc">Scannez et payez directement depuis votre smartphone</div>
    </div>
  </div>
  
  <div style="text-align:center;margin-top:2rem;color:var(--text-muted);font-size:0.85rem;">
    🔒 Paiements sécurisés SSL · Architecture CinetPay / PayDunya / FedaPay prête
  </div>
</section>

<!-- TEMOIGNAGES -->
<section id="temoignages">
  <div class="section-label">Ils nous font confiance</div>
  <h2 class="section-title">Ce que disent nos <span>clients</span></h2>
  
  <div class="testimonials-grid">
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">Qualité exceptionnelle pour nos flyers d'événement. EBAF a livré à temps et le rendu était vraiment professionnel. Je recommande vivement !</p>
      <div class="testimonial-author">
        <div class="author-avatar">AK</div>
        <div>
          <div class="author-name">Ama Konan</div>
          <div class="author-role">Organisatrice d'événements · Abidjan</div>
        </div>
      </div>
    </div>
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">Nos polos brodés avec le logo de l'entreprise sont magnifiques. La broderie est propre, les couleurs sont fidèles. L'équipe est très réactive sur WhatsApp.</p>
      <div class="testimonial-author">
        <div class="author-avatar">JM</div>
        <div>
          <div class="author-name">Jean-Michel Brou</div>
          <div class="author-role">Directeur commercial · Cocody</div>
        </div>
      </div>
    </div>
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">Les tasses personnalisées pour notre séminaire étaient parfaites. Rapide, professionnel, prix compétitif. EBAF est notre partenaire impression depuis 2 ans.</p>
      <div class="testimonial-author">
        <div class="author-avatar">FD</div>
        <div>
          <div class="author-name">Fatima Diallo</div>
          <div class="author-role">Responsable RH · Plateau</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GALERIE -->
<section id="galerie">
  <div class="section-label">Portfolio</div>
  <h2 class="section-title">Notre <span>Galerie</span></h2>
  
  <div class="gallery-grid">
    <div class="gallery-item" style="background:linear-gradient(135deg,#0d1b4b,#1a3fa0);">
      <div class="mock-flyer" style="transform:rotate(-5deg)scale(1.2);">
        <div class="mock-flyer-img"></div>
        <div class="mock-flyer-line thick"></div>
        <div class="mock-flyer-line"></div>
      </div>
      <div class="gallery-label">Flyers promotionnels</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#1e1b4b,#7c3aed);">
      <div style="font-size:4.5rem;">👕</div>
      <div class="gallery-label">T-shirts personnalisés</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#0a2e1a,#16a34a);">
      <div style="font-size:4.5rem;">🥼</div>
      <div class="gallery-label">Polos brodés</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#4a0a2e,#d946ef);">
      <div class="mock-mug" style="width:100px;height:100px;transform:scale(1.1);">
        <div class="mock-mug-design" style="width:60px;height:60px;font-size:1.8rem;">☕</div>
      </div>
      <div class="gallery-label">Tasses personnalisées</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#0a0a2e,#1a3fa0);">
      <div class="mock-card-vis" style="transform:scale(1.4)rotate(-8deg)"></div>
      <div class="gallery-label">Cartes de visite</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#2d1a00,#eab308);">
      <div class="mock-sticker" style="width:110px;height:110px;font-size:3rem;transform:rotate(-8deg);">⭐</div>
      <div class="gallery-label">Stickers vinyle</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#063040,#00bcd4);">
      <div class="mock-bottle" style="width:70px;height:140px;"></div>
      <div class="gallery-label">Bouteilles personnalisées</div>
    </div>
    <div class="gallery-item" style="background:linear-gradient(135deg,#0d1b4b,#1a3fa0);">
      <div class="mock-kakemono" style="width:90px;height:170px;">
        <div style="width:60px;height:35px;background:rgba(255,255,255,0.2);border-radius:3px;"></div>
        <div style="width:40%;height:4px;background:rgba(255,255,255,0.5);border-radius:2px;"></div>
        <div style="width:60%;height:3px;background:rgba(255,255,255,0.3);border-radius:2px;"></div>
      </div>
      <div class="gallery-label">Kakémonos Roll-up</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label">Nous trouver</div>
  <h2 class="section-title">Contactez- <span>nous</span></h2>
  
  <div class="contact-grid">
    <div>
      <div class="contact-info-item">
        <div class="contact-icon">📍</div>
        <div>
          <div class="contact-detail-label">Adresse</div>
          <div class="contact-detail-val">Riviera Palmeraie, Derrière la SODECI<br>Non loin de chez SAMER, Immeuble KOLO<br>Rue I129-12 · Abidjan, Côte d'Ivoire</div>
        </div>
      </div>
      <div class="contact-info-item">
        <div class="contact-icon">📞</div>
        <div>
          <div class="contact-detail-label">Téléphone</div>
          <div class="contact-detail-val"><a href="tel:+2250704423114" style="color:var(--cyan);text-decoration:none;">07 04 42 31 14</a></div>
        </div>
      </div>
      <div class="contact-info-item">
        <div class="contact-icon">💬</div>
        <div>
          <div class="contact-detail-label">WhatsApp</div>
          <div class="contact-detail-val"><a href="https://wa.me/2250704423114?text=Bonjour%20EBAF%20Business%20Center%2C%20je%20souhaite%20obtenir%20des%20informations%20sur%20vos%20services." target="_blank" style="color:#25D366;text-decoration:none;">07 04 42 31 14</a></div>
        </div>
      </div>
      <div class="contact-info-item">
        <div class="contact-icon">✉️</div>
        <div>
          <div class="contact-detail-label">Email</div>
          <div class="contact-detail-val"><a href="mailto:contact@ebafbusinesscenter.com" style="color:var(--cyan);text-decoration:none;">contact@ebafbusinesscenter.com</a></div>
        </div>
      </div>
      <div class="contact-info-item">
        <div class="contact-icon">🕐</div>
        <div>
          <div class="contact-detail-label">Horaires</div>
          <div class="contact-detail-val">Lun - Sam : 08h00 – 19h00<br>Dimanche : Sur rendez-vous</div>
        </div>
      </div>
    </div>
    
    <div class="map-placeholder">
      <iframe 
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3972.2!2d-3.9563!3d5.3764!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNcKwMjInMzUuMCJOIDPCsDU3JzIyLjciVw!5e0!3m2!1sfr!2sci!4v1"
        allowfullscreen="" loading="lazy"
        style="filter:invert(90%) hue-rotate(180deg);">
      </iframe>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div>
      <div class="footer-logo">
        <img src="data:image/jpeg;base64,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u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/wBacnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/AFp27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v8AWnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvH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iIc/hJCOJx2dQW1YxsbA1jQ1o3ADIBWsPEy1dxr5/YhvupcOHXH7kaxR/mYP4Sv3DMUcpquEja/LVy1hnlvW4rrVT3B7HTGQFoyGqQPwX1QWyC3cJwJedfLPWOe7P1rnkLH8Q5hpbf8AjQ95mHLcJd/+Twulqiq6QiGNjJm7W6oAz6FFqKqkt9Y2VoILTk5p4xxhTxayqsVHVVDpn8I1zt4YQB6F1n/DpWTjdj9JI8xspRi4W9UzPgmZUQsljdmxwzBUXxN+kWfyh6SpFRUMdBEY4nyOYTnk855d5eVbaKavmEszpA4N1e5IH4KfNouycXZp+LoR49kKrt3sRu13c21kjRCJNcg562WXmWf76XfRB9Z/ssv3tUPz5vKHqX772qH583lD1LPqxviVUFCDWiLM7cScnKSepix4nc+RrexANYgZ8J/st3W/5Gf+W70LXtw5RMeHB02YOY7oepbSWMSxPjdnquBByWliQytklkPVvsVbnTquEV806rgeQ5qQe+l30QfWf7LM97VD8+byh6k97VD8+byh6lkY+B8Qx9eG0tS7bk41um/XoYfvpd9EH1n+y2dquZuTJSYhHqED4Weea8Pe1Q/Pm8oepZtDbobe14hLyHkE6xz3LRxYZ6tTua2lW54zg+GuposT/wCbh/gPpX3hmKOXsrhI2Py1MtYA5b1t661U9wka+Z0gLRkNUgfgvqgtsFu4TgS86+Wesc92frUSwLP/ACHMNLb/AMaHfMw5bhLv/wAmPdbVHVUh4GNjJmbW6oAz6FGKGrkt9Y2VoOw5PaeMcYU7WsqbFR1VQ6Z3CNc7eGEAehdZ/wAOlOyN2P0kjzGyoxi67eqZnwzMqIWyxuzY4Zgr0WNRUMdBEYonyOYTnk855d5ZK1q3JwW9aP3KctNXt7BERdnIREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQH/2Q==" alt="EBAF Business Center">
      </div>
      <p class="footer-desc">Votre partenaire en impression, broderie et personnalisation premium à Abidjan. Qualité professionnelle, délais respectés.</p>
      <div class="footer-socials">
        <a href="https://wa.me/2250704423114" class="social-link" target="_blank">💬</a>
        <a href="mailto:contact@ebafbusinesscenter.com" class="social-link">✉️</a>
        <a href="tel:+2250704423114" class="social-link">📞</a>
      </div>
    </div>
    <div>
      <div class="footer-heading">Services</div>
      <ul class="footer-links">
        <li><a href="#services">Impression</a></li>
        <li><a href="#services">Broderie</a></li>
        <li><a href="#services">Personnalisation</a></li>
        <li><a href="#services">Création graphique</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-heading">Produits</div>
      <ul class="footer-links">
        <li><a href="#boutique">Flyers & Affiches</a></li>
        <li><a href="#boutique">T-shirts & Polos</a></li>
        <li><a href="#boutique">Tasses & Bouteilles</a></li>
        <li><a href="#boutique">Cartes de visite</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-heading">Informations</div>
      <ul class="footer-links">
        <li><a href="#commander">Commander</a></li>
        <li><a href="#paiement">Paiement</a></li>
        <li><a href="#contact">Contact</a></li>
        <li><a href="#temoignages">Avis clients</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <div class="footer-copy">© 2025 EBAF Business Center · Abidjan, Côte d'Ivoire · Tous droits réservés</div>
    <div class="footer-copy">Impression · Broderie · Personnalisation</div>
  </div>
</footer>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/2250704423114?text=Bonjour%20EBAF%20Business%20Center%2C%20je%20souhaite%20obtenir%20des%20informations%20sur%20vos%20services." class="wa-float" target="_blank" title="Contacter sur WhatsApp">💬</a>

<!-- PANIER PANEL -->
<div class="cart-overlay" id="cart-overlay" onclick="toggleCart()"></div>
<div id="cart-panel">
  <div class="cart-header">
    <div class="cart-title">🛒 Mon Panier</div>
    <button class="cart-close" onclick="toggleCart()">✕</button>
  </div>
  <div class="cart-items" id="cart-items-container">
    <div style="text-align:center;padding:3rem;color:var(--text-muted);">
      <div style="font-size:3rem;margin-bottom:1rem;">🛍️</div>
      <div>Votre panier est vide</div>
    </div>
  </div>
  <div class="cart-footer">
    <div class="cart-total-row">
      <span class="cart-total-label">Sous-total</span>
      <span class="cart-total-val" id="cart-subtotal">0 FCFA</span>
    </div>
    <div class="cart-total-row">
      <span class="cart-total-label">TVA (18%)</span>
      <span class="cart-total-val" id="cart-tva">0 FCFA</span>
    </div>
    <div class="cart-total-row" style="border-top:1px solid rgba(255,255,255,0.08);padding-top:0.75rem;margin-top:0.75rem;">
      <span style="font-weight:700;">TOTAL</span>
      <span class="cart-total-val cart-grand" id="cart-total">0 FCFA</span>
    </div>
    <button class="btn-checkout" onclick="openCheckout()">💳 Procéder au paiement</button>
    <a href="https://wa.me/2250704423114?text=Bonjour%20EBAF%2C%20je%20souhaite%20commander." target="_blank" style="display:block;text-align:center;margin-top:0.75rem;color:#25D366;font-size:0.88rem;text-decoration:none;">💬 Commander via WhatsApp</a>
  </div>
</div>

<!-- CHECKOUT MODAL -->
<div id="checkout-modal">
  <div class="modal-overlay" onclick="closeCheckout()"></div>
  <div class="modal-box">
    <div class="modal-title">💳 Paiement</div>
    <div class="modal-sub" id="checkout-amount-display">Total : 0 FCFA</div>
    
    <div style="font-size:0.82rem;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:var(--text-muted);margin-bottom:0.75rem;">Choisir votre mode de paiement</div>
    
    <div class="payment-options">
      <div class="pay-opt" onclick="selectPayment(this,'orange')">
        <div class="pay-opt-icon">🟠</div>
        <div class="pay-opt-name">Orange Money</div>
      </div>
      <div class="pay-opt" onclick="selectPayment(this,'wave')">
        <div class="pay-opt-icon">🌊</div>
        <div class="pay-opt-name">Wave</div>
      </div>
      <div class="pay-opt" onclick="selectPayment(this,'mtn')">
        <div class="pay-opt-icon">📱</div>
        <div class="pay-opt-name">MTN MoMo</div>
      </div>
      <div class="pay-opt" onclick="selectPayment(this,'card')">
        <div class="pay-opt-icon">💳</div>
        <div class="pay-opt-name">Carte bancaire</div>
      </div>
    </div>
    
    <div class="phone-input">
      <label class="form-label">Numéro de téléphone</label>
      <input type="tel" class="form-control" placeholder="07 XX XX XX XX" id="pay-phone">
    </div>
    
    <div class="form-group">
      <label class="form-label">Votre nom</label>
      <input type="text" class="form-control" placeholder="Nom complet" id="pay-name">
    </div>
    
    <button class="btn-checkout" onclick="processPayment()">✅ Confirmer le paiement</button>
    <button onclick="closeCheckout()" style="width:100%;background:none;border:none;color:var(--text-muted);padding:0.75rem;cursor:pointer;font-family:'DM Sans',sans-serif;margin-top:0.5rem;">Annuler</button>
  </div>
</div>

<!-- TOAST NOTIFICATION -->
<div class="toast" id="toast"></div>

<!-- ADMIN PANEL -->
<div id="admin-panel">
  <div class="admin-nav">
    <div style="display:flex;align-items:center;gap:1rem;">
      <img src="data:image/jpeg;base64,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u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/wBacnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/AFp27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v8AWnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v9adu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/wBadu68c1UPW/1pydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/AFpydvgceBeCKj+3deOaqHrf607d145qoet/rTk7fA48C8EVH9u68c1UPW/1p27rxzVQ9b/WnJ2+Bx4F4IqP7d145qoet/rTt3Xjmqh63+tOTt8DjwLwRUf27rxzVQ9b/WnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvHNVD1v8AWnbuvHNVD1v9acnb4HHgXgio/t3Xjmqh63+tO3deOaqHrf605O3wOPAvBFR/buvH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iIc/hJCOJx2dQW1YxsbA1jQ1o3ADIBWsPEy1dxr5/YhvupcOHXH7kaxR/mYP4Sv3DMUcpquEja/LVy1hnlvW4rrVT3B7HTGQFoyGqQPwX1QWyC3cJwJedfLPWOe7P1rnkLH8Q5hpbf8AjQ95mHLcJd/+Twulqiq6QiGNjJm7W6oAz6FFqKqkt9Y2VoILTk5p4xxhTxayqsVHVVDpn8I1zt4YQB6F1n/DpWTjdj9JI8xspRi4W9UzPgmZUQsljdmxwzBUXxN+kWfyh6SpFRUMdBEY4nyOYTnk855d5eVbaKavmEszpA4N1e5IH4KfNouycXZp+LoR49kKrt3sRu13c21kjRCJNcg562WXmWf76XfRB9Z/ssv3tUPz5vKHqX772qH583lD1LPqxviVUFCDWiLM7cScnKSepix4nc+RrexANYgZ8J/st3W/5Gf+W70LXtw5RMeHB02YOY7oepbSWMSxPjdnquBByWliQytklkPVvsVbnTquEV806rgeQ5qQe+l30QfWf7LM97VD8+byh6k97VD8+byh6lkY+B8Qx9eG0tS7bk41um/XoYfvpd9EH1n+y2dquZuTJSYhHqED4Weea8Pe1Q/Pm8oepZtDbobe14hLyHkE6xz3LRxYZ6tTua2lW54zg+GuposT/wCbh/gPpX3hmKOXsrhI2Py1MtYA5b1t661U9wka+Z0gLRkNUgfgvqgtsFu4TgS86+Wesc92frUSwLP/ACHMNLb/AMaHfMw5bhLv/wAmPdbVHVUh4GNjJmbW6oAz6FGKGrkt9Y2VoOw5PaeMcYU7WsqbFR1VQ6Z3CNc7eGEAehdZ/wAOlOyN2P0kjzGyoxi67eqZnwzMqIWyxuzY4Zgr0WNRUMdBEYonyOYTnk855d5ZK1q3JwW9aP3KctNXt7BERdnIREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQH/2Q==" alt="EBAF" style="height:40px;">
      <span style="font-family:'Syne',sans-serif;font-weight:700;">Tableau de bord Admin</span>
    </div>
    <button class="btn-outline" onclick="toggleAdmin()">✕ Fermer</button>
  </div>
  <div class="admin-content">
    <div class="admin-grid">
      <div class="admin-card">
        <div class="admin-stat-num" id="admin-orders-count">12</div>
        <div class="admin-stat-label">Commandes reçues</div>
      </div>
      <div class="admin-card">
        <div class="admin-stat-num">235 500</div>
        <div class="admin-stat-label">FCFA encaissés</div>
      </div>
      <div class="admin-card">
        <div class="admin-stat-num">8</div>
        <div class="admin-stat-label">Clients actifs</div>
      </div>
      <div class="admin-card">
        <div class="admin-stat-num">3</div>
        <div class="admin-stat-label">En cours</div>
      </div>
    </div>
    
    <h3 style="font-family:'Syne',sans-serif;margin-bottom:1rem;">Dernières commandes</h3>
    <div style="background:var(--card-bg);border:1px solid var(--card-border);border-radius:16px;overflow:auto;">
      <table class="admin-table">
        <thead>
          <tr>
            <th>#</th>
            <th>Client</th>
            <th>Produit</th>
            <th>Montant</th>
            <th>Paiement</th>
            <th>Statut</th>
          </tr>
        </thead>
        <tbody id="admin-orders-body">
          <tr>
            <td>#001</td>
            <td>Ama Konan</td>
            <td>Flyers 200 pcs</td>
            <td>10 000 FCFA</td>
            <td>Orange Money</td>
            <td><span class="badge-status badge-success">Payé</span></td>
          </tr>
          <tr>
            <td>#002</td>
            <td>Jean Brou</td>
            <td>Polo brodé x5</td>
            <td>25 000 FCFA</td>
            <td>Wave</td>
            <td><span class="badge-status badge-pending">En cours</span></td>
          </tr>
          <tr>
            <td>#003</td>
            <td>Fatima D.</td>
            <td>Tasses x10</td>
            <td>50 000 FCFA</td>
            <td>Carte bancaire</td>
            <td><span class="badge-status badge-new">Nouveau</span></td>
          </tr>
        </tbody>
      </table>
    </div>
    
    <div style="display:flex;gap:1rem;margin-top:1.5rem;flex-wrap:wrap;">
      <button class="btn-primary" onclick="exportData('excel')">📊 Export Excel</button>
      <button class="btn-primary" onclick="exportData('pdf')">📄 Export PDF</button>
    </div>
  </div>
</div>

<script>
// ===== CART STATE =====
let cart = [];
let selectedPayment = '';

function addToCart(name, price, emoji) {
  const existing = cart.find(i => i.name === name);
  if (existing) {
    existing.qty++;
  } else {
    cart.push({ name, price, emoji, qty: 1 });
  }
  updateCartUI();
  showToast('✅ ' + name + ' ajouté au panier !');
}

function removeFromCart(index) {
  cart.splice(index, 1);
  updateCartUI();
}

function updateQty(index, delta) {
  cart[index].qty += delta;
  if (cart[index].qty <= 0) cart.splice(index, 1);
  updateCartUI();
}

function updateCartUI() {
  const count = cart.reduce((s, i) => s + i.qty, 0);
  document.getElementById('cart-count').textContent = count;
  
  const subtotal = cart.reduce((s, i) => s + i.price * i.qty, 0);
  const tva = Math.round(subtotal * 0.18);
  const total = subtotal + tva;
  
  document.getElementById('cart-subtotal').textContent = subtotal.toLocaleString() + ' FCFA';
  document.getElementById('cart-tva').textContent = tva.toLocaleString() + ' FCFA';
  document.getElementById('cart-total').textContent = total.toLocaleString() + ' FCFA';
  
  const container = document.getElementById('cart-items-container');
  if (cart.length === 0) {
    container.innerHTML = '<div style="text-align:center;padding:3rem;color:var(--text-muted);"><div style="font-size:3rem;margin-bottom:1rem;">🛍️</div><div>Votre panier est vide</div></div>';
    return;
  }
  
  container.innerHTML = cart.map((item, i) => `
    <div class="cart-item">
      <div class="cart-item-emoji">${item.emoji}</div>
      <div style="flex:1;">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">${(item.price * item.qty).toLocaleString()} FCFA</div>
        <div class="cart-qty">
          <button class="qty-btn" onclick="updateQty(${i}, -1)">−</button>
          <span class="qty-val">${item.qty}</span>
          <button class="qty-btn" onclick="updateQty(${i}, 1)">+</button>
        </div>
      </div>
      <button class="remove-item" onclick="removeFromCart(${i})">🗑️</button>
    </div>
  `).join('');
}

function toggleCart() {
  document.getElementById('cart-panel').classList.toggle('open');
  document.getElementById('cart-overlay').classList.toggle('active');
}

// ===== CHECKOUT =====
function openCheckout() {
  if (cart.length === 0) { showToast('⚠️ Votre panier est vide !'); return; }
  const subtotal = cart.reduce((s, i) => s + i.price * i.qty, 0);
  const total = subtotal + Math.round(subtotal * 0.18);
  document.getElementById('checkout-amount-display').textContent = 'Total à payer : ' + total.toLocaleString() + ' FCFA';
  document.getElementById('checkout-modal').classList.add('open');
  toggleCart();
}

function closeCheckout() {
  document.getElementById('checkout-modal').classList.remove('open');
}

function selectPayment(el, method) {
  document.querySelectorAll('.pay-opt').forEach(o => o.classList.remove('selected'));
  el.classList.add('selected');
  selectedPayment = method;
}

function processPayment() {
  const phone = document.getElementById('pay-phone').value;
  const name = document.getElementById('pay-name').value;
  if (!selectedPayment) { showToast('⚠️ Choisissez un mode de paiement'); return; }
  if (!phone || !name) { showToast('⚠️ Remplissez tous les champs'); return; }
  
  closeCheckout();
  cart = [];
  updateCartUI();
  
  const methods = {orange:'Orange Money', wave:'Wave', mtn:'MTN MoMo', card:'Carte bancaire'};
  showToast('✅ Commande confirmée ! Paiement ' + methods[selectedPayment] + ' en cours de traitement.');
  
  // Update admin
  const count = parseInt(document.getElementById('admin-orders-count').textContent) + 1;
  document.getElementById('admin-orders-count').textContent = count;
  
  const row = document.createElement('tr');
  row.innerHTML = `<td>#00${count}</td><td>${name}</td><td>Commande en ligne</td><td>—</td><td>${methods[selectedPayment]}</td><td><span class="badge-status badge-new">Nouveau</span></td>`;
  document.getElementById('admin-orders-body').prepend(row);
}

// ===== ORDER FORM =====
function handleFileUpload(input) {
  if (input.files.length > 0) {
    const file = input.files[0];
    document.getElementById('upload-text').textContent = '✅ ' + file.name + ' (' + (file.size/1024).toFixed(0) + ' KB)';
  }
}

function submitOrder() {
  const name = document.getElementById('order-name').value;
  const phone = document.getElementById('order-phone').value;
  const product = document.getElementById('order-product').value;
  
  if (!name || !phone) { showToast('⚠️ Remplissez les champs obligatoires'); return; }
  if (product === '-- Sélectionner un produit --') { showToast('⚠️ Sélectionnez un produit'); return; }
  
  const msg = `Bonjour EBAF Business Center !%0A%0AJe souhaite commander :%0A- Produit : ${encodeURIComponent(product)}%0A- Nom : ${encodeURIComponent(name)}%0A- Téléphone : ${encodeURIComponent(phone)}`;
  window.open('https://wa.me/2250704423114?text=' + msg, '_blank');
  showToast('✅ Redirection WhatsApp...');
}

function quickOrder(product) {
  const msg = `Bonjour EBAF Business Center, je souhaite commander : ${product}`;
  window.open('https://wa.me/2250704423114?text=' + encodeURIComponent(msg), '_blank');
}

// ===== FILTERS =====
function filterProducts(cat, btn) {
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  
  document.querySelectorAll('.product-card').forEach(card => {
    if (cat === 'all' || card.dataset.cat === cat) {
      card.style.display = '';
    } else {
      card.style.display = 'none';
    }
  });
}

// ===== ADMIN =====
function toggleAdmin() {
  document.getElementById('admin-panel').classList.toggle('open');
}

function exportData(type) {
  showToast('📥 Export ' + type.toUpperCase() + ' en cours...');
}

// ===== TOAST =====
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 3500);
}

// ===== MOBILE MENU =====
function toggleMenu() {
  const nav = document.querySelector('.nav-links');
  if (nav.style.display === 'flex') {
    nav.style.display = '';
  } else {
    nav.style.cssText = 'display:flex;flex-direction:column;position:fixed;top:72px;left:0;right:0;background:#0a0f1e;padding:1.5rem 5%;border-bottom:1px solid rgba(255,255,255,0.08);z-index:999;gap:1.5rem;';
  }
}

// ===== SCROLL ANIMATIONS =====
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.style.opacity = '1';
      e.target.style.transform = 'translateY(0)';
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.service-card, .product-card, .testimonial-card, .payment-card, .gallery-item').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(24px)';
  el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
  observer.observe(el);
});

// NAV SCROLL
window.addEventListener('scroll', () => {
  const nav = document.getElementById('navbar');
  if (window.scrollY > 50) {
    nav.style.background = 'rgba(10,15,30,0.98)';
  } else {
    nav.style.background = 'rgba(10,15,30,0.92)';
  }
});
</script>
</body>
</html>
