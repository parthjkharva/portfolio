<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Parth Kharva - Power Systems Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0066cc;
            --primary-dark: #004c99;
            --secondary: #2d3e50;
            --light: #f5f7fa;
            --gray: #e0e0e0;
            --dark: #333;
            --accent: #ffb400;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 100px 40px;
            text-align: center;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .profile-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }
        
        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            background-color: var(--primary-dark);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 64px;
        }
        
        .profile-text h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .title {
            font-size: 1.2rem;
            font-weight: 400;
            margin-bottom: 15px;
        }
        
        .contact-info {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 20px;
        }
        
        .contact-info a {
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s;
        }
        
        .contact-info a:hover {
            color: var(--accent);
        }
        
        section {
            padding: 60px 0;
        }
        
        section:nth-child(even) {
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2rem;
            color: var(--secondary);
            display: inline-block;
        }
        
        .section-title h2:after {
            content: '';
            display: block;
            width: 50%;
            height: 3px;
            background-color: var(--primary);
            margin: 10px auto 0;
        }
        
        .about-content {
            display: flex;
            gap: 40px;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .skill-category {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }
        
        .skill-category h3 {
            margin-bottom: 15px;
            color: var(--primary);
            border-bottom: 2px solid var(--gray);
            padding-bottom: 10px;
        }
        
        .skill-list {
            list-style: none;
        }
        
        .skill-list li {
            margin-bottom: 8px;
            display: flex;
            align-items: center;
        }
        
        .skill-list li:before {
            content: '▹';
            color: var(--primary);
            margin-right: 10px;
        }
        
        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 3px;
            background-color: var(--primary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1.5px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: white;
            border: 3px solid var(--primary);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }
        
        .timeline-item:nth-child(odd)::after {
            right: -13px;
        }
        
        .timeline-item:nth-child(even)::after {
            left: -13px;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            position: relative;
            border-radius: 6px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }
        
        .timeline-content h3 {
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .timeline-content h4 {
            color: var(--secondary);
            margin-bottom: 15px;
            font-weight: 500;
        }
        
        .timeline-content .date {
            font-style: italic;
            color: var(--primary-dark);
            margin-bottom: 10px;
            display: block;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-image {
            height: 160px;
            background-color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 48px;
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            color: var(--secondary);
            margin-bottom: 10px;
        }
        
        .project-date {
            font-size: 0.9rem;
            color: var(--primary-dark);
            margin-bottom: 10px;
            display: block;
        }
        
        .certifications {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }
        
        .certification {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            flex: 1;
            min-width: 250px;
            max-width: 400px;
            text-align: center;
        }
        
        .certification i {
            font-size: 48px;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        footer {
            background-color: var(--secondary);
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent);
        }
        
        .footer-contact {
            margin-top: 20px;
        }
        
        .footer-contact a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
            transition: color 0.3s;
        }
        
        .footer-contact a:hover {
            color: var(--accent);
        }
        
        .copyright {
            margin-top: 20px;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive */
        @media screen and (max-width: 768px) {
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item::after {
                left: 18px;
            }
            
            .timeline-item:nth-child(odd)::after {
                left: 18px;
                right: auto;
            }
            
            .about-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="profile-container">
                <div class="profile-image">
                    <i class="fas fa-user"></i>
                </div>
                <div class="profile-text">
                    <h1>Parth Kharva</h1>
                    <p class="title">Power Systems Engineer</p>
                    <p>Fullerton, CA, USA (willing to relocate)</p>
                    <div class="contact-info">
                        <a href="tel:+17148370943"><i class="fas fa-phone"></i> +1 (714) 837-0943</a>
                        <a href="mailto:parthkharva3.14@gmail.com"><i class="fas fa-envelope"></i> parthkharva3.14@gmail.com</a>
                        <a href="https://www.linkedin.com/in/parthkharva" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>Aspiring Power Systems Engineer with 5+ years of experience in electrical system design, transmission studies, and renewable energy integration. Seeking to leverage expertise in HV transmission, system modeling, and interconnection studies to contribute to the energy industry's mission of delivering clean energy projects with technical excellence and innovation.</p>
                    <p>Currently pursuing my Master's degree in Electrical Engineering with a focus on power systems, I am passionate about improving grid reliability and integrating sustainable energy solutions.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>Technical Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Power Systems</h3>
                    <ul class="skill-list">
                        <li>HV Transmission & Substation Design</li>
                        <li>Load Flow, Short Circuit Analysis</li>
                        <li>Stability Studies & Contingency Analysis</li>
                        <li>Interconnection Processes & Risk Assessment</li>
                        <li>Synchrophasor Applications</li>
                        <li>State Estimation</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Software & Tools</h3>
                    <ul class="skill-list">
                        <li>ETAP</li>
                        <li>PowerWorld Simulator</li>
                        <li>HOMER Energy</li>
                        <li>MATLAB/Simulink</li>
                        <li>AutoCAD</li>
                        <li>LabVIEW</li>
                        <li>ANSYS Maxwell</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Engineering Domains</h3>
                    <ul class="skill-list">
                        <li>Renewable Energy Integration</li>
                        <li>Grid Stability & Protection</li>
                        <li>Smart Grid Technology</li>
                        <li>Dynamic Modeling</li>
                        <li>Technical Documentation</li>
                        <li>Cross-Functional Team Collaboration</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <div class="section-title">
                <h2>Work Experience</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Research Assistant</h3>
                        <h4>California State University, Fullerton</h4>
                        <span class="date">Jan 2025 - Present</span>
                        <ul>
                            <li>Conduct power system modeling and renewable integration studies for McCarthy Hall's microgrid project</li>
                            <li>Validate grid stability strategies, perform contingency analysis, and optimize solar and energy storage systems</li>
                            <li>Develop dynamic models for load flow and fault analysis, aligning with CAISO and interconnection best practices</li>
                        </ul>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Associate Electrical Engineer</h3>
                        <h4>Natraj Enterprise, Vadodara, Gujarat</h4>
                        <span class="date">Jun 2022 - Jun 2023</span>
                        <ul>
                            <li>Designed and optimized electric motor control systems using MATLAB/Simulink and ANSYS Maxwell</li>
                            <li>Performed torque-speed analysis, thermal evaluation, and root cause failure analysis (RCFA)</li>
                            <li>Collaborated with embedded and mechanical teams to integrate electrical subsystems</li>
                            <li>Supported control system validation aligned with industrial standards</li>
                        </ul>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Junior Electrical Engineer</h3>
                        <h4>Natraj Enterprise, Vadodara, Gujarat</h4>
                        <span class="date">Nov 2020 - Jun 2022</span>
                        <ul>
                            <li>Designed detailed schematics for control circuits using AutoCAD Electrical</li>
                            <li>Conducted prototype trials, validated control algorithms in LabVIEW and MATLAB</li>
                            <li>Assisted in PLC system integration for motor systems, optimizing I/O wiring and configuration</li>
                        </ul>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Graduate Engineer Trainee</h3>
                        <h4>Sangam Enterprise, Vadodara, Gujarat</h4>
                        <span class="date">Aug 2019 - Oct 2020</span>
                        <ul>
                            <li>Supported control system design for switchgear installations</li>
                            <li>Collaborated on relay setting adjustments, basic protection schemes, and UPS system design</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="education">
        <div class="container">
            <div class="section-title">
                <h2>Education</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Master of Science in Electrical Engineering</h3>
                        <h4>California State University, Fullerton</h4>
                        <span class="date">Expected Graduation: May 2025</span>
                        <p><strong>Relevant Coursework:</strong> Power System Analysis, Smart Grid Technology, Renewable Energy Integration, Machine Learning in Power Systems, Digital Signal Processing (DSP), Microcontrollers & Embedded Systems</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Bachelor of Science in Electrical Engineering</h3>
                        <h4>Charusat University, Anand, Gujarat</h4>
                        <span class="date">April 2019</span>
                        <p><strong>Relevant Coursework:</strong> Embedded Systems Design, Power Electronics, Signal Processing & Control Systems, High-Speed PCB Design</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2>Technical Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image">
                        <i class="fas fa-solar-panel"></i>
                    </div>
                    <div class="project-info">
                        <h3>Hybrid Renewable System Design</h3>
                        <span class="project-date">Jan 2025 - Present</span>
                        <p>Modeled and optimized a hybrid energy system using HOMER Energy, achieving 40% carbon emission reduction while maintaining 95% load demand coverage. Integration of solar, wind, and hydrogen technologies.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <div class="project-info">
                        <h3>Power System Fault Analysis</h3>
                        <span class="project-date">May 2024 - Aug 2024</span>
                        <p>Developed and simulated a 5-bus system using PowerWorld Simulator; executed fault analysis and contingency planning, increasing system resilience by 25%.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">
                        <i class="fas fa-cogs"></i>
                    </div>
                    <div class="project-info">
                        <h3>Electromagnetic Analysis of Induction Motor</h3>
                        <span class="project-date">Jan 2019 - Apr 2019</span>
                        <p>Performed electromagnetic field and thermal behavior analysis using AutoCAD and ANSYS, applying inverter designs for solar energy applications.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="internships">
        <div class="container">
            <div class="section-title">
                <h2>Internships</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Indian Oil Corp. LTD (IOCL)</h3>
                        <span class="date">May 2015 - Jun 2015</span>
                        <ul>
                            <li>Practical experience in gas power plant operations and synchronous motor systems</li>
                            <li>Skilled in industrial power distribution and system management</li>
                        </ul>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Gujarat State Electricity LTD (GSECL)</h3>
                        <span class="date">Nov 2014 - Dec 2014</span>
                        <ul>
                            <li>Trained in UPS systems, switchgear, and relay engineering with hands-on experience</li>
                            <li>Knowledgeable in power system protection, including fault analysis, relay coordination, and system reliability</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="certifications">
        <div class="container">
            <div class="section-title">
                <h2>Certifications</h2>
            </div>
            <div class="certifications">
                <div class="certification">
                    <i class="fas fa-certificate"></i>
                    <h3>FE Electrical & Computer Certification</h3>
                    <p>Ongoing</p>
                </div>
                <div class="certification">
                    <i class="fas fa-certificate"></i>
                    <h3>ETAP Power System Modeling</h3>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <h3>Parth Kharva</h3>
                <p>Power Systems Engineer</p>
                <div class="social-links">
                    <a href="https://www.linkedin.com/in/parthkharva" target="_blank"><i class="fab fa-linkedin"></i></a>
                    <a href="mailto:parthkharva3.14@gmail.com"><i class="fas fa-envelope"></i></a>
                </div>
                <div class="footer-contact">
                    <a href="tel:+17148370943"><i class="fas fa-phone"></i> +1 (714) 837-0943</a>
                    <a href="mailto:parthkharva3.14@gmail.com"><i class="fas fa-envelope"></i> parthkharva3.14@gmail.com</a>
                </div>
                <p class="copyright">&copy; 2025 Parth Kharva. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Add smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
