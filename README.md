<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PrimeGrade Solutions | Excellence, Integrity, Precision</title>
    <style>
        :root { 
            --primary: #0f172a; 
            --secondary: #1e293b; 
            --accent: #22c55e; 
            --gold: #fbbf24; 
            --light: #f8fafc; 
            --white: #ffffff;
        }
        
        body { font-family: 'Segoe UI', sans-serif; margin: 0; padding: 0; background-color: var(--light); color: #333; line-height: 1.6; }
        
        /* --- 1. HERO SECTION (UPDATED) --- */
        .header { 
            background: linear-gradient(135deg, var(--primary), var(--secondary)); 
            color: white; 
            padding: 50px 20px; 
            text-align: center; 
            border-bottom: 5px solid var(--gold); 
        }
        .logo-img { width: 90px; height: 90px; background-color: white; border-radius: 50%; padding: 5px; object-fit: contain; border: 3px solid var(--gold); margin-bottom: 15px; box-shadow: 0 0 15px rgba(251, 191, 36, 0.5); }
        .brand { font-size: 32px; font-weight: 800; letter-spacing: 1px; margin: 5px 0; }
        .tagline { color: var(--gold); font-size: 14px; font-weight: 600; text-transform: uppercase; letter-spacing: 3px; margin-bottom: 10px; }
        .hero-sub { max-width: 600px; margin: 10px auto; font-size: 18px; color: #cbd5e1; }

        /* --- CONTAINER & CARDS --- */
        .container { max-width: 800px; margin: -40px auto 40px auto; padding: 20px; }
        
        .card { 
            background: var(--white); 
            border-radius: 12px; 
            padding: 30px; 
            box-shadow: 0 10px 30px -5px rgba(0, 0, 0, 0.08); 
            margin-bottom: 30px; 
            border-top: 1px solid #f1f5f9;
        }
        
        h2 { color: var(--primary); border-left: 5px solid var(--gold); padding-left: 15px; margin-top: 0; font-size: 24px; }
        h3 { color: var(--secondary); margin-top: 0; }
        
        /* --- 2. FORM STYLING (POLISHED) --- */
        .form-group { margin-bottom: 20px; }
        label { display: block; font-weight: 700; margin-bottom: 8px; color: var(--secondary); font-size: 14px; text-transform: uppercase; }
        
        select, input[type="text"] { 
            width: 100%; 
            padding: 15px; /* Bigger touch area */
            border: 1px solid #cbd5e1; 
            border-radius: 8px; /* Rounded corners */
            font-size: 16px; 
            background: #fff; 
            box-sizing: border-box; 
            transition: 0.3s;
        }
        
        select:focus, input:focus {
            border-color: var(--gold);
            outline: none;
            box-shadow: 0 0 0 3px rgba(251, 191, 36, 0.2);
        }

        .wa-btn { 
            background: linear-gradient(to right, #16a34a, #22c55e); 
            color: white; 
            width: 100%; 
            padding: 18px; 
            border: none; 
            border-radius: 50px; /* Pill shape button */
            font-size: 18px; 
            font-weight: bold; 
            cursor: pointer; 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            text-decoration: none; 
            box-shadow: 0 4px 15px rgba(34, 197, 94, 0.4);
            transition: transform 0.2s;
        }
        .wa-btn:hover { transform: translateY(-2px); }
        
        /* --- 3. TESTIMONIALS (GRID CARDS) --- */
        .testimonial-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; margin-top: 20px; }
        .testimonial-box { 
            background: #f8fafc; 
            padding: 20px; 
            border-radius: 10px; 
            border-left: 4px solid var(--gold);
            font-size: 15px;
        }

        /* --- 4. SUBJECT PILLS (SEO LIST) --- */
        .subject-container { margin-top: 15px; }
        .subject-pill {
            display: inline-block;
            background: #e2e8f0;
            color: var(--primary);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 13px;
            margin: 4px;
            font-weight: 600;
        }

        /* --- 5. PORTFOLIO / SAMPLES --- */
        .portfolio-scroller {
            display: flex;
            gap: 15px;
            overflow-x: auto;
            padding-bottom: 10px;
        }
        .portfolio-item {
            min-width: 200px;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            overflow: hidden;
        }
        .portfolio-placeholder {
            height: 120px;
            background: #cbd5e1;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #64748b;
            font-size: 12px;
        }
        
        /* --- 6. PAYMENT LOGOS (FIXED SIZE) --- */
        .payment-row { display: flex; justify-content: center; align-items: center; gap: 20px; margin-bottom: 10px; flex-wrap: wrap; }
        .pay-icon { 
            height: 40px; /* Equal height for all */
            width: auto; 
            object-fit: contain; 
            filter: grayscale(100%); 
            opacity: 0.7; 
            transition: 0.3s; 
        }
        .pay-icon:hover { filter: grayscale(0%); opacity: 1; transform: scale(1.05); }

        /* --- 7. FAQ (ACCORDION) --- */
        details { margin-bottom: 10px; border-bottom: 1px solid #eee; padding-bottom: 10px; }
        summary { font-weight: bold; cursor: pointer; color: var(--primary); list-style: none; }
        summary::-webkit-details-marker { display: none; } /* Hide default arrow */
        summary::after { content: "+"; float: right; font-weight: bold; }
        details[open] summary::after { content: "-"; }
        .faq-ans { margin-top: 10px; font-size: 14px; color: #475569; }

        /* FOOTER */
        .footer { text-align: center; color: #64748b; font-size: 13px; padding: 40px 20px; border-top: 1px solid #e2e8f0; margin-top: 40px; background: white; }
        .disclaimer { font-size: 11px; color: #94a3b8; max-width: 600px; margin: 20px auto; line-height: 1.5; }
    </style>
</head>
<body>

    <!-- HERO SECTION -->
    <div class="header">
        <img src="https://cdn-icons-png.flaticon.com/512/3135/3135810.png" alt="Logo" class="logo-img">
        <div class="tagline">Excellence • Integrity • Precision</div>
        <div class="brand">PRIMEGRADE SOLUTIONS</div>
        <div class="hero-sub">Zambia's leading academic consultancy. We bridge the gap between complex engineering concepts and distinction.</div>
    </div>

    <div class="container">
        
        <!-- NEW: SAMPLE WORK / PORTFOLIO -->
        <div class="card">
            <h2>Recent Successful Projects</h2>
            <p style="font-size: 14px; color: #64748b; margin-bottom: 15px;">A glimpse of our distinction-level work:</p>
            <div class="portfolio-scroller">
                <!-- Sample 1 -->
                <div class="portfolio-item">
                    <div class="portfolio-placeholder">⚡ Circuit Diagram</div>
                    <div style="padding: 10px;">
                        <div style="font-weight:bold; font-size:14px;">Circuit Analysis</div>
                        <div style="font-size:12px; color:#16a34a;">UNZA | Distinction</div>
                    </div>
                </div>
                <!-- Sample 2 -->
                <div class="portfolio-item">
                    <div class="portfolio-placeholder">📄 Research PDF</div>
                    <div style="padding: 10px;">
                        <div style="font-weight:bold; font-size:14px;">Thesis Proposal</div>
                        <div style="font-size:12px; color:#16a34a;">CBU | Approved</div>
                    </div>
                </div>
                <!-- Sample 3 -->
                <div class="portfolio-item">
                    <div class="portfolio-placeholder">📐 Math Calc</div>
                    <div style="padding: 10px;">
                        <div style="font-weight:bold; font-size:14px;">Calculus III</div>
                        <div style="font-size:12px; color:#16a34a;">Step-by-Step</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- NEW: DETAILED SUBJECT LIST -->
        <div class="card">
            <h2>Modules We Cover</h2>
            <div class="subject-container">
                <span class="subject-pill">🧮 Calculus I-III</span>
                <span class="subject-pill">⚡ Circuit Theory</span>
                <span class="subject-pill">🏗️ Structural Analysis</span>
                <span class="subject-pill">🌊 Fluid Mechanics</span>
                <span class="subject-pill">💾 MATLAB / CAD</span>
                <span class="subject-pill">📝 Academic Writing</span>
                <span class="subject-pill">🎓 Research Methods</span>
                <span class="subject-pill">💼 CV Design</span>
            </div>
        </div>

        <!-- ORDER FORM -->
        <div class="card" style="border-top: 4px solid var(--accent);">
            <h2>Start Your Order</h2>
            <p style="text-align: center; color: #64748b; margin-bottom: 25px;">Fill in the details to get an instant quote.</p>

            <div class="form-group">
                <label>Service Required</label>
                <select id="service">
                    <option value="Engineering Calculation">⚙️ Engineering / Math Calculation</option>
                    <option value="Academic Assignment">📝 Academic Assignment (Essay/Report)</option>
                    <option value="Research/Thesis Support">🎓 Research Proposal or Thesis</option>
                    <option value="CV/Resume Design">💼 Professional CV / Resume Design</option>
                    <option value="Homework Q&A">🔓 Homework Q&A (Chegg/CourseHero)</option>
                </select>
            </div>

            <div class="form-group">
                <label>Urgency Level</label>
                <select id="urgency">
                    <option value="Standard (3-5 Days)">📅 Standard (3-5 Days)</option>
                    <option value="Priority (24-48 Hours)">🔥 Priority (24-48 Hours)</option>
                    <option value="CRITICAL (ASAP - Today)">🚨 CRITICAL (ASAP - Today)</option>
                </select>
            </div>

            <div class="form-group">
                <label>Topic / Module (Optional)</label>
                <input type="text" id="topic" placeholder="e.g. Thermodynamics, Linear Algebra...">
            </div>

            <button class="wa-btn" onclick="sendToWhatsApp()">
                <span style="margin-right: 10px; font-size: 24px;"></span> 
                Send Inquiry via WhatsApp
            </button>
            <p style="text-align: center; font-size: 12px; color: #94a3b8; margin-top: 10px;">⚡ You will be redirected to WhatsApp to chat with an agent.</p>
        </div>

        <!-- TESTIMONIALS (UPDATED LAYOUT) -->
        <div class="card">
            <h2>Trusted by Students</h2>
            <div class="testimonial-grid">
                <div class="testimonial-box">
                    <div style="color: var(--gold); font-size: 20px;">★★★★★</div>
                    <p>"Saved my semester! The circuit analysis breakdown was clear and the steps helped me study."</p>
                    <div style="font-weight: bold; font-size: 13px; color: var(--primary);">— 4th Year Student, CBU</div>
                </div>
                <div class="testimonial-box">
                    <div style="color: var(--gold); font-size: 20px;">★★★★★</div>
                    <p>"Fastest CV service I've used. I got the internship interview within a week."</p>
                    <div style="font-weight: bold; font-size: 13px; color: var(--primary);">— Graduate, UNZA</div>
                </div>
            </div>
        </div>

        <!-- FAQ (UPDATED) -->
        <div class="card">
            <h2>Frequently Asked Questions</h2>
            
            <details>
                <summary>Is my information confidential?</summary>
                <div class="faq-ans">Yes, 100%. We value your privacy and never share client data with third parties or universities. Your data is deleted after service delivery.</div>
            </details>

            <details>
                <summary>Is the work Plagiarism-Free?</summary>
                <div class="faq-ans">Absolutely. We provide a <strong>FREE Turnitin report</strong> with every major writing assignment. We have a zero-tolerance policy for AI-generated text.</div>
            </details>

            <details>
                <summary>How do I make payment?</summary>
                <div class="faq-ans">We accept Mobile Money (MTN, Airtel, Zamtel) for local clients and PayPal/Payoneer for international clients. A 50% deposit is required to start.</div>
            </details>
        </div>

        <!-- PAYMENT LOGOS (RESIZED) -->
        <div class="card" style="text-align: center;">
            <h3>💳 Secure Payment Options</h3>
            <div class="payment-row">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/MTN_Logo.svg/200px-MTN_Logo.svg.png" alt="MTN" class="pay-icon">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/Airtel_Logo.svg/200px-Airtel_Logo.svg.png" alt="Airtel" class="pay-icon">
                <!-- Zamtel Custom Badge -->
                <div class="pay-icon" style="display:flex; align-items:center; justify-content:center; background:#009639; color:white; font-weight:bold; width:80px; font-size:11px; border-radius: 4px;">ZAMTEL</div>
            </div>
            <div class="payment-row">
                <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal" class="pay-icon">
                <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/Payoneer_logo.svg" alt="Payoneer" class="pay-icon">
            </div>
        </div>

    </div>

    <!-- FOOTER WITH LEGAL DISCLAIMER -->
    <div class="footer">
        <h3 style="color: var(--primary); margin:0;">PRIMEGRADE SOLUTIONS</h3>
        <p>Excellence. Integrity. Precision.</p>
        
        <div class="disclaimer">
            <strong>Disclaimer:</strong> PrimeGrade Solutions provides academic consulting, tutoring, and sample research services. All materials provided are to be used for research and reference purposes only. We do not encourage academic dishonesty or plagiarism.
        </div>
        
        <p>© 2026 PrimeGrade Solutions. Lusaka, Zambia.</p>
    </div>

    <script>
        function sendToWhatsApp() {
            var service = document.getElementById("service").value;
            var urgency = document.getElementById("urgency").value;
            var topic = document.getElementById("topic").value;
            
            // CHECK: Is this the correct number?
            var phone = "260951036866"; 
            
            var text = "*New Inquiry for PrimeGrade* %0a%0a📌 *Service:* " + service + "%0a⏰ *Urgency:* " + urgency + "%0a";
            if(topic) { text += "📚 *Topic:* " + topic + "%0a"; }
            text += "%0a_Hello, I would like a quote for this work. Is an expert available?_";
            
            window.open("https://wa.me/" + phone + "?text=" + text, '_blank');
        }
    </script>
</body>
</html>
