---
# Homepage
type: landing

sections:

  ##############################################
  ## HERO BANNER
  ##############################################
  - block: hero
    id: home
    content:
      title: |
        QuantOmics
      image:
        filename: hero-bg.jpg
      text: |-
        **NSERC CREATE** in AI-Driven Quantum Sensing and Genomics for Precision Therapeutics

        Training Canada's next generation of interdisciplinary leaders at the convergence of **quantum biosensing**, **computational genomics**, and **artificial intelligence** — from sensor to clinic.
      cta:
        label: Apply Now
        url: apply/
        icon_pack: fas
        icon: graduation-cap
      cta_alt:
        label: Explore the Program
        url: about/
      cta_note:
        label: 'A consortium of 6 universities · 11 co-applicants · 93 trainees'
    design:
      background:
        gradient_end: '#1565C0'
        gradient_start: '#0D3B8C'
        text_color_light: true

  ##############################################
  ## ABOUT STRIP
  ##############################################
  - block: markdown
    id: about
    content:
      title: What is QuantOmics?
      subtitle: ''
      text: |-
        The NSERC CREATE in **AI-Driven Quantum Sensing and Genomics for Precision Therapeutics (QuantOmics)** is Canada's first integrated training pipeline bridging quantum nanotechnology, genomic data science, and AI-driven medicine.

        A consortium of **six research-intensive universities** — Toronto Metropolitan University, McGill, Queen's, Université Laval, University of Saskatchewan, and University of Toronto — together with a cross-sectoral network of **industry and clinical partners**, will train **93 highly qualified personnel** over six years to be fluent across all three domains.

        Our driving philosophy: a QuantOmics graduate can speak the language of hardware engineers, molecular biologists, and AI developers simultaneously — making them invaluable as integrators and leaders in Canada's emerging quantum-biomedical economy.
    design:
      columns: '1'

  ##############################################
  ## THREE RESEARCH STREAMS
  ##############################################
  - block: features
    id: streams
    content:
      title: Three Interconnected Research Streams
      subtitle: 'An integrated pipeline — from molecule to medicine'
      items:
        - name: 'Stream 1: Quantum Probe Design & Fabrication'
          description: >
            Engineering next-generation quantum biosensors using NV-center diamond probes,
            quantum-dot nanoparticles, spin-based magnetometry, and CMOS/MEMS integration.
            Trainees build ultra-sensitive devices capable of detecting biomarkers at the attomolar level.
          icon: atom
          icon_pack: fas
        - name: 'Stream 2: Genomics Signal Integration'
          description: >
            Converting raw quantum sensor data into high-fidelity multi-omic datasets.
            Trainees build computational pipelines fusing nanopore sequencing, methylation maps,
            EHR features, and multi-omic data using reproducible workflow tools.
          icon: dna
          icon_pack: fas
        - name: 'Stream 3: AI-Powered Therapeutic Design'
          description: >
            Building predictive AI models to guide rational design of next-generation personalized
            therapeutics and vaccines. Projects span generative AI for drug design,
            neoantigen prediction, and multimodal fusion for cancer diagnostics.
          icon: brain
          icon_pack: fas
    design:
      columns: '3'

  ##############################################
  ## KEY STATISTICS
  ##############################################
  - block: markdown
    content:
      title: ''
      text: |-
        <div class="qo-stats">
          <div class="qo-stat"><div class="qo-stat-num">93</div><div>Trainees over 6 years<br><small>(UG · MSc · PhD · PDF)</small></div></div>
          <div class="qo-stat"><div class="qo-stat-num">6</div><div>Partner universities<br><small>across Canada</small></div></div>
          <div class="qo-stat"><div class="qo-stat-num">11</div><div>Co-applicants including<br><small>5 Canada Research Chairs</small></div></div>
          <div class="qo-stat"><div class="qo-stat-num">8</div><div>Industry &amp; clinical<br><small>partner organizations</small></div></div>
        </div>
    design:
      columns: '1'

  ##############################################
  ## TRAINING HIGHLIGHTS
  ##############################################
  - block: markdown
    id: training-highlights
    content:
      title: A Unique Training Experience
      subtitle: 'Going far beyond a traditional graduate degree'
      text: |-
        QuantOmics equips trainees with technical depth **and** professional breadth through a suite of purpose-built learning experiences:

        | Component | Description |
        |-----------|-------------|
        | 🔬 **5 Specialized Courses** | From quantum nanotechnology to responsible AI, building a shared cross-disciplinary vocabulary |
        | 🧪 **Multimodal-Omics Bootcamp** | 3-week intensive: building full sensor-to-insight analysis pipelines |
        | 🤝 **Mentorship Trio** | Every graduate trainee paired with a primary supervisor, cross-stream co-supervisor, and industry advisor |
        | 🏭 **Industry & Lab Internships** | Mandatory mobility placements (6–8 weeks) at partner labs or companies |
        | 🏆 **Annual Vaccine Design Challenge** | Interdisciplinary team hackathon solving real vaccine design problems |
        | 🎓 **Symposiums & Job Fairs** | Triennial national symposium with concurrent job fair and recruiter networking |

        [Explore the Full Training Program →](training/)
    design:
      columns: '1'

  ##############################################
  ## FEATURED TEAM
  ##############################################
  - block: people
    id: people
    content:
      title: Research Team
      subtitle: 'Faculty from across Canada'
      user_groups:
        - Principal Investigator
        - Co-Applicants
    design:
      show_interests: false
      show_role: true
      show_social: true
      columns: '5'

  ##############################################
  ## RECENT NEWS
  ##############################################
  - block: collection
    id: news
    content:
      title: Latest News & Updates
      subtitle: ''
      text: ''
      count: 3
      filters:
        folders:
          - post
        featured_only: false
    design:
      view: card
      columns: '3'

  ##############################################
  ## UPCOMING EVENTS
  ##############################################
  - block: collection
    id: events
    content:
      title: Upcoming Events
      subtitle: ''
      count: 3
      filters:
        folders:
          - event
    design:
      view: compact
      columns: '1'

  ##############################################
  ## PARTNER UNIVERSITIES
  ##############################################
  - block: markdown
    id: partners
    content:
      title: Our University Consortium
      subtitle: ''
      text: |-
        QuantOmics brings together world-class researchers from six Canadian universities:

        **Toronto Metropolitan University** · **McGill University** · **Queen's University** · **Université Laval** · **University of Saskatchewan** · **University of Toronto**

        Supported by a cross-sectoral network of industry and clinical partners including **C2MI**, **Epiloid Biotech**, **Terry Fox Research Institute**, **Ontario Genomics**, **Klick Health**, **Alimentiv**, **Novavax**, and others.

        [View All Partners →](partners/)
    design:
      columns: '1'

  ##############################################
  ## CONTACT
  ##############################################
  - block: contact
    id: contact
    content:
      title: Contact Us
      subtitle: ''
      text: |-
        Have questions about the program, applications, or partnership opportunities?
        We'd love to hear from you.
      email: quantomics@torontomu.ca
      phone: '+1 416-979-5000'
      address:
        street: 350 Victoria Street
        city: Toronto
        region: ON
        postcode: 'M5B 2K3'
        country: Canada
        country_code: CA
      directions: 'Kerr Hall, Toronto Metropolitan University'
      office_hours:
        - 'Monday–Friday, 9:00 AM – 5:00 PM ET'
      autolink: true
      coordinates:
        latitude: '43.6578'
        longitude: '-79.3789'
    design:
      columns: '2'
---
