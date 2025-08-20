# Toni-sales-page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Oracle Boxing - Master Sparring Under Pressure</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html, body {
            overflow-x: hidden;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #000;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
            color: white;
            padding: 80px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="boxing-gloves" x="0" y="0" width="50" height="50" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="2" fill="%23ff4444" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23boxing-gloves)"/></svg>');
            animation: float 20s ease-in-out infinite;
            z-index: 1;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        @keyframes float {
            0%, 100% { transform: translate(-50%, -50%) rotate(0deg); }
            50% { transform: translate(-48%, -52%) rotate(180deg); }
        }
        
        .preheader {
            color: #ff4444;
            font-weight: bold;
            font-size: 1.1rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        .main-headline {
            font-size: 3.5rem;
            font-weight: bold;
            margin-bottom: 25px;
            line-height: 1.2;
        }
        
        .subheader {
            font-size: 1.4rem;
            margin-bottom: 40px;
            color: #ddd;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .vsl-container {
            margin: 40px 0;
            position: relative;
            text-align: center;
        }
        
        .vsl-thumbnail {
            width: 400px;
            height: 225px;
            background: linear-gradient(45deg, #2d2d2d, #1a1a1a);
            border-radius: 15px;
            position: relative;
            cursor: pointer;
            border: 3px solid #ff4444;
            transition: all 0.3s ease;
            display: inline-block;
        }
        
        .vsl-thumbnail:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 40px rgba(255, 68, 68, 0.3);
        }
        
        .play-button {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 80px;
            height: 80px;
            background: #ff4444;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: translate(-50%, -50%) scale(1); }
            50% { transform: translate(-50%, -50%) scale(1.1); }
            100% { transform: translate(-50%, -50%) scale(1); }
        }
        
        .cta-primary {
            background: linear-gradient(45deg, #ff4444, #cc3333);
            color: white;
            padding: 20px 50px;
            font-size: 1.3rem;
            font-weight: bold;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            margin: 20px 0;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .cta-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(255, 68, 68, 0.4);
        }
        
        /* Section Styles */
        .section {
            padding: 80px 0;
        }
        
        .section-dark {
            background: #111;
            color: white;
        }
        
        .section-light {
            background: #f8f8f8;
            color: #333;
        }
        
        .section-headline {
            font-size: 2.8rem;
            font-weight: bold;
            margin-bottom: 30px;
            text-align: center;
            line-height: 1.2;
        }
        
        .section-content {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            text-align: left;
        }
        
        .section-content p {
            margin-bottom: 20px;
        }
        
        .highlight {
            color: #ff4444;
            font-weight: bold;
        }
        
        .emphasis {
            background: #ff4444;
            color: white;
            padding: 2px 8px;
            border-radius: 4px;
        }
        
        /* Problem Section */
        .problem-visual {
            background: linear-gradient(135deg, #2d1b1b, #1a1a1a);
            padding: 40px;
            border-radius: 15px;
            margin: 40px 0;
            border-left: 5px solid #ff4444;
        }
        
        /* Solution Bullets */
        .solution-bullets {
            list-style: none;
            margin: 40px 0;
        }
        
        .solution-bullets li {
            margin-bottom: 25px;
            padding: 20px;
            background: rgba(255, 68, 68, 0.1);
            border-radius: 10px;
            border-left: 4px solid #ff4444;
        }
        
        .bullet-feature {
            font-weight: bold;
            color: #ff4444;
            font-size: 1.1rem;
        }
        
        .bullet-benefit {
            margin: 10px 0;
            font-style: italic;
        }
        
        /* Offer Section */
        .offer-container {
            background: linear-gradient(135deg, #1a1a1a, #2d2d2d);
            padding: 60px 40px;
            border-radius: 20px;
            margin: 40px 0;
            text-align: center;
            border: 2px solid #ff4444;
        }
        
        .price-container {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 40px 0;
            flex-wrap: wrap;
        }
        
        .price-option {
            background: #2d2d2d;
            padding: 30px;
            border-radius: 15px;
            flex: 1;
            min-width: 300px;
            max-width: 400px;
            border: 2px solid transparent;
            transition: all 0.3s ease;
        }
        
        .price-option:hover {
            border-color: #ff4444;
            transform: translateY(-5px);
        }
        
        .price-option.featured {
            border-color: #ff4444;
            transform: scale(1.05);
        }
        
        .price {
            font-size: 3rem;
            font-weight: bold;
            color: #ff4444;
            margin: 20px 0;
        }
        
        .price-description {
            font-size: 1.1rem;
            margin-bottom: 20px;
        }
        
        /* FAQ Section */
        .faq-item {
            margin-bottom: 30px;
            background: #f8f8f8;
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid #ff4444;
        }
        
        .faq-question {
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #333;
        }
        
        .faq-answer {
            color: #666;
            line-height: 1.6;
        }
        
        /* Responsive Design */
        @media (max-width: 1024px) {
            .main-headline {
                font-size: 3rem;
            }
            
            .section-headline {
                font-size: 2.4rem;
            }
            
            .vsl-thumbnail {
                width: 350px;
                height: 197px;
            }
        }
        
        @media (max-width: 768px) {
            .hero {
                padding: 60px 0;
            }
            
            .main-headline {
                font-size: 2.5rem;
            }
            
            .section-headline {
                font-size: 2rem;
            }
            
            .subheader {
                font-size: 1.2rem;
            }
            
            .vsl-thumbnail {
                width: 100%;
                max-width: 300px;
                height: 169px;
            }
            
            .cta-primary {
                padding: 15px 30px;
                font-size: 1.1rem;
            }
            
            .price-container {
                flex-direction: column;
                align-items: center;
            }
            
            .section-content {
                font-size: 1.1rem;
            }
        }
        
        /* Animation Classes */
        .fade-in {
            animation: fadeIn 0.8s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .boxing-accent {
            position: relative;
        }
        
        .boxing-accent::after {
            content: '🥊';
            position: absolute;
            right: -30px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.5rem;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(-50%); }
            40% { transform: translateY(-70%); }
            60% { transform: translateY(-65%); }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content fade-in">
                <div class="preheader">For Serious Boxers Who Train Hard But Struggle in Live Sparring</div>
                
                <h1 class="main-headline">
                    Go From <span class="highlight">Drill Perfect</span> to <span class="highlight">Sparring Lethal</span><br>
                    in Just 90 Days
                </h1>
                
                <p class="subheader">
                    Finally perform with calm precision under pressure... without losing your form when speed and chaos hit
                </p>
                
                <div class="vsl-container">
                    <div class="vsl-thumbnail">
                        <div class="play-button">▶</div>
                    </div>
                </div>
                
                <a href="#offer" class="cta-primary">Get Started - $497</a>
            </div>
        </div>
    </section>

    <!-- Problem Section -->
    <section class="section section-dark">
        <div class="container">
            <h2 class="section-headline">You Look Like a Champion in Practice...</h2>
            
            <div class="section-content">
                <p>Your form is crisp on the heavy bag.</p>
                
                <p>Your footwork flows smooth as silk during pad work.</p>
                
                <p>Your combinations land with surgical precision... when nobody's throwing back.</p>
                
                <div class="problem-visual">
                    <p><strong>But the moment you step into live sparring...</strong></p>
                    
                    <p>Your perfect technique crumbles.</p>
                    
                    <p>Your mind goes blank under pressure.</p>
                    
                    <p>And that smooth fighter you see in the mirror? <span class="emphasis">Gone.</span></p>
                </div>
                
                <p>You've spent months drilling the same combinations...</p>
                
                <p>You've invested hundreds in personal training sessions...</p>
                
                <p>You've watched every YouTube tutorial promising to make you "unstoppable"...</p>
                
                <p>Yet when the gloves come up and someone's actually trying to hit you back, you freeze.</p>
                
                <p>Because here's the brutal truth most coaches won't tell you:</p>
                
                <p><span class="highlight">Speed steals your form and pressure steals your mind.</span></p>
                
                <p>And if you don't fix this gap between practice and performance...</p>
                
                <p>You'll stay stuck in that frustrating cycle of looking good in drills but getting exposed in sparring.</p>
                
                <p>Until now.</p>
            </div>
        </div>
    </section>

    <!-- Origin Story Section -->
    <section class="section section-light">
        <div class="container">
            <h2 class="section-headline">The Night Everything Changed</h2>
            
            <div class="section-content">
                <p>Three years ago, I was exactly where you are now.</p>
                
                <p>Sharp in the gym. Sloppy in sparring.</p>
                
                <p>I'd land clean combinations on the pads, then get tagged by shots I should have seen coming in live rounds.</p>
                
                <p>My coach kept saying "just relax and let it flow"...</p>
                
                <p>But how do you relax when someone's throwing leather at your face?</p>
                
                <p>Then came the fight that humbled me completely.</p>
                
                <p>Local smoker. Nothing fancy. But I got picked apart by a guy whose technique looked rough compared to mine.</p>
                
                <p>He wasn't faster. He wasn't stronger.</p>
                
                <p><span class="highlight">But he could think and adapt while I was still trying to remember my combinations.</span></p>
                
                <p>That's when I realized the problem wasn't my technique...</p>
                
                <p>It was my <em>approach</em> to learning boxing.</p>
                
                <p>Traditional training teaches you what to do. It doesn't teach you <em>why</em> it works or <em>when</em> to use it.</p>
                
                <p>So when chaos hits, you have no foundation to fall back on.</p>
                
                <p>I spent the next 18 months deconstructing boxing down to its core principles...</p>
                
                <p>Building an operating system for mind, body, strategy, and conditioning that works under pressure.</p>
                
                <p>And the results were immediate.</p>
            </div>
        </div>
    </section>

    <!-- Solution Section -->
    <section class="section section-dark">
        <div class="container">
            <h2 class="section-headline">The Oracle Method: Boxing From First Principles</h2>
            
            <div class="section-content">
                <p>Forget memorizing 47 different combinations.</p>
                
                <p>Forget drilling the same patterns until your muscle memory takes over.</p>
                
                <p>The Oracle Method builds something deeper:</p>
                
                <p><span class="highlight">Cause-and-effect thinking that adapts in real time.</span></p>
                
                <p>Instead of learning "what to do," you learn the <em>why</em> behind every movement.</p>
                
                <p>So when your opponent does something unexpected...</p>
                
                <p>When the pace picks up beyond your comfort zone...</p>
                
                <p>When pressure starts clouding your judgment...</p>
                
                <p><span class="emphasis">Your foundation stays solid.</span></p>
                
                <ul class="solution-bullets">
                    <li>
                        <div class="bullet-feature">Mind System:</div>
                        <div class="bullet-benefit">Mental frameworks that keep you calm and calculating when chaos erupts around you</div>
                        <div>So you think three moves ahead instead of reacting to what just happened</div>
                    </li>
                    
                    <li>
                        <div class="bullet-feature">Body System:</div>
                        <div class="bullet-benefit">Movement principles that flow naturally from any position or situation</div>
                        <div>So your technique stays crisp even when you're off-balance or surprised</div>
                    </li>
                    
                    <li>
                        <div class="bullet-feature">Strategy System:</div>
                        <div class="bullet-benefit">Pattern recognition that reads opponents like an open book</div>
                        <div>So you spot openings and weaknesses others miss completely</div>
                    </li>
                    
                    <li>
                        <div class="bullet-feature">Engine System:</div>
                        <div class="bullet-benefit">Conditioning protocols that build the gas tank for sustained performance</div>
                        <div>So you're still sharp in round 8 while others are fading</div>
                    </li>
                </ul>
                
                <p>This isn't theory.</p>
                
                <p>In the last 12 months, Oracle Method fighters have:</p>
                
                <p>• Won 23 amateur titles across 4 weight classes</p>
                <p>• Improved sparring performance in an average of 6 weeks</p>
                <p>• Built unshakeable confidence that carries outside the gym</p>
                
                <p>Because when you understand the <em>principles</em> instead of just the techniques...</p>
                
                <p>Everything changes.</p>
            </div>
        </div>
    </section>

    <!-- Product Introduction Section -->
    <section class="section section-light">
        <div class="container">
            <h2 class="section-headline">Introducing Oracle Boxing Elite</h2>
            
            <div class="section-content">
                <p>This isn't another drill-heavy course that leaves you confused in live scenarios.</p>
                
                <p>Oracle Boxing Elite is a complete operating system for fighters who want to perform under pressure.</p>
                
                <p><span class="boxing-accent"><strong>"Boxing From First Principles" Foundation Course</strong></span> (12+ hours)</p>
                <p>The mental framework that turns reactive fighters into strategic ones. You'll understand the <em>why</em> behind every movement, so you can adapt instead of just repeat.</p>
                
                <p><span class="boxing-accent"><strong>"The Boxing Roadmap" 20-Week Program</strong></span></p>
                <p>Week-by-week progression that builds your skills systematically. No guesswork. No wasted training. Just steady improvement you can measure.</p>
                
                <p><span class="boxing-accent"><strong>Daily Live Group Coaching</strong></span></p>
                <p>Jump on live calls where I break down technique, answer questions, and help you work through sticking points in real time.</p>
                
                <p><span class="boxing-accent"><strong>Oracle AI Assistant</strong></span></p>
                <p>24/7 access to personalized training advice, workout planning, and technique troubleshooting. Like having a coach in your pocket.</p>
                
                <p><span class="boxing-accent"><strong>Weekly Video Feedback</strong></span></p>
                <p>Submit your training footage and get detailed analysis on what's working and what needs adjustment.</p>
                
                <p><span class="boxing-accent"><strong>Private Community Access</strong></span></p>
                <p>Connect with serious fighters who push each other to improve. Share victories, troubleshoot challenges, stay motivated.</p>
                
                <p>Compare this to hiring a top-level boxing coach:</p>
                
                <p>Private sessions run $150-300 per hour...</p>
                
                <p>You'd need 40+ sessions just to cover what's in the foundation course...</p>
                
                <p>That's $6,000-12,000 before you factor in ongoing coaching and support.</p>
                
                <p>But you won't pay anywhere close to that.</p>
            </div>
        </div>
    </section>

    <!-- Offer Section -->
    <section class="section section-dark" id="offer">
        <div class="container">
            <h2 class="section-headline">Your Path to Sparring Mastery</h2>
            
            <div class="offer-container">
                <p style="font-size: 1.3rem; margin-bottom: 40px;">Everything you need to go from drill-perfect to sparring-lethal...</p>
                
                <div class="price-container">
                    <div class="price-option">
                        <h3>6-Month Elite</h3>
                        <div class="price">$497</div>
                        <div class="price-description">
                            • Lifetime access to all courses<br>
                            • 6 months live coaching<br>
                            • Oracle AI assistant<br>
                            • Video feedback<br>
                            • Private community<br>
                            • Auto-renews at $97/month
                        </div>
                        <a href="#" class="cta-primary">Get Started - $497</a>
                    </div>
                    
                    <div class="price-option featured">
                        <h3>12-Month Elite (Best Value)</h3>
                        <div class="price">$797</div>
                        <div class="price-description">
                            • Everything in 6-month<br>
                            • <strong>12 months live coaching</strong><br>
                            • <strong>Save $466</strong><br>
                            • Priority video feedback<br>
                            • Bonus sparring masterclass<br>
                            • Auto-renews at $97/month
                        </div>
                        <a href="#" class="cta-primary">Get Started - $797</a>
                    </div>
                </div>
                
                <p style="margin-top: 40px; font-size: 1.1rem;">
                    <strong>100% Money-Back Guarantee:</strong> If you don't see improvement in your sparring within 60 days, I'll refund every penny. No questions asked.
                </p>
                
                <p style="color: #ff4444; font-weight: bold; margin-top: 20px;">
                    Only 50 spots available this month. When they're gone, the waitlist opens.
                </p>
                
                <a href="#" class="cta-primary" style="margin-top: 30px; font-size: 1.4rem;">
                    Claim Your Spot Now
                </a>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="section section-light">
        <div class="container">
            <h2 class="section-headline">Questions? We've Got Answers</h2>
            
            <div class="faq-item">
                <div class="faq-question">I'm already training at a good gym. Do I still need this?</div>
                <div class="faq-answer">
                    Good gyms teach technique. Great gyms teach application. But most gyms don't teach the mental frameworks that keep you calm under pressure. Oracle Method fills that gap, making your existing training more effective.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">What if I'm too busy for daily coaching calls?</div>
                <div class="faq-answer">
                    Every session is recorded. You can catch up whenever it fits your schedule. Plus, the Oracle AI assistant gives you 24/7 access to coaching insights without waiting for the next live call.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">I'm not ready for serious sparring yet. Is this too advanced?</div>
                <div class="faq-answer">
                    Perfect timing. The earlier you learn proper fundamentals, the faster you'll progress. The 20-week roadmap starts with basics and builds systematically. You'll be ready for sparring with confidence, not fear.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">Can I really improve without in-person coaching?</div>
                <div class="faq-answer">
                    Video feedback is incredibly effective for technique correction. Plus, the mental frameworks and strategic thinking we teach translate immediately to your gym training. Many members see improvements within their first week.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">What if this doesn't work for my fighting style?</div>
                <div class="faq-answer">
                    The Oracle Method isn't about changing your style – it's about making your natural style more effective under pressure. Whether you're a boxer-puncher, pressure fighter, or counter-puncher, these principles enhance what you already do.
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 60px;">
                <p style="font-size: 1.3rem; margin-bottom: 30px;">
                    Stop getting exposed in sparring. Start performing with the precision and confidence you've been training for.
                </p>
                <a href="#offer" class="cta-primary">Transform Your Sparring Today</a>
            </div>
        </div>
    </section>

    <script>
        // Add smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
