# QuantOmics Website

Website for the **NSERC CREATE in AI-Driven Quantum Sensing and Genomics for Precision Therapeutics (QuantOmics)** program.

Built with [Hugo Blox](https://hugoblox.com/) (Research Group template) and deployed on [Netlify](https://netlify.com) with continuous deployment. Content is managed via [Decap CMS](https://decapcms.org/) — a browser-based admin panel that requires no Git or terminal knowledge.

---

## One-Time Deployment Setup

### Step 1 — Push to GitHub

```bash
cd Quantomics
git init
git add .
git commit -m "Initial QuantOmics site scaffold"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/quantomics-website.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username or organization.

### Step 2 — Connect to Netlify

1. Log in to [netlify.com](https://netlify.com) → **Add new site** → **Import an existing project**
2. Connect to GitHub and select your `quantomics-website` repository
3. Build settings are auto-detected from `netlify.toml`:
   - **Build command:** `hugo mod download && hugo --gc --minify`
   - **Publish directory:** `public`
4. Click **Deploy site**

> After the first deploy succeeds, update `baseURL` in `config/_default/hugo.yaml` to your actual Netlify URL (e.g., `https://quantomics.netlify.app/`) and push.

### Step 3 — Enable Netlify Identity & Git Gateway (for CMS)

1. In your Netlify dashboard → **Site configuration** → **Identity** → **Enable Identity**
2. Under **Identity** → **Services** → **Git Gateway** → **Enable Git Gateway**
3. Under **Identity** → **Registration** → set to **Invite only** (recommended)
4. Under **Identity** → **Invite users** → invite your program coordinator's email

### Step 4 — Coordinator Accepts Invite & Accesses CMS

1. Coordinator receives an email from Netlify Identity
2. They follow the link to set their password
3. They visit `https://your-site.netlify.app/admin/` to access the CMS
4. Done — they can now edit all site content entirely through the browser

---

## Continuous Deployment

Any commit pushed to the `main` branch on GitHub automatically triggers a Netlify rebuild. Changes made through the CMS admin panel create commits to `main` and trigger rebuilds automatically.

**Typical publish time: 2–4 minutes after a commit.**

---

## Site Structure

```
Quantomics/
├── config/_default/
│   ├── hugo.yaml          # Main Hugo config (title, modules, outputs)
│   ├── params.yaml        # Theme params (colors, contact info, social)
│   └── menus.yaml         # Navigation menu
├── content/
│   ├── _index.md          # Homepage (hero, streams, stats, team, news)
│   ├── about/_index.md    # Program overview page
│   ├── training/_index.md # Training program details
│   ├── apply/_index.md    # How to apply
│   ├── partners/_index.md # Partner organizations
│   ├── people/_index.md   # Team directory page
│   ├── authors/           # Individual team member profiles
│   │   ├── naimul-khan/
│   │   ├── brenda-andrews/
│   │   ├── jacques-corbeil/
│   │   ├── stefania-impellizzeri/
│   │   ├── sara-mahshid/
│   │   ├── shayan-rayan/
│   │   ├── harry-ruda/
│   │   ├── amber-simpson/
│   │   ├── brett-trost/
│   │   └── virgilio-valente/
│   ├── project/           # Research streams
│   │   ├── stream-1-quantum-biosensing/
│   │   ├── stream-2-genomics-integration/
│   │   └── stream-3-ai-therapeutics/
│   ├── post/              # News & blog posts
│   └── event/             # Events
├── static/
│   ├── admin/
│   │   ├── index.html     # Decap CMS entry point
│   │   └── config.yml     # CMS collection definitions
│   └── uploads/           # Media uploaded via CMS
├── assets/media/          # Site media (logos, team photos)
├── netlify.toml           # Netlify build config
└── go.mod                 # Hugo module dependencies
```

---

## Adding/Updating Content

### Via the CMS (recommended for coordinators)

1. Go to `https://your-site.netlify.app/admin/`
2. Log in with Netlify Identity credentials
3. Choose a collection: **News Posts**, **Events**, **Team Members**, **Research Streams**, or **Pages**
4. Create or edit entries — changes are committed to GitHub and trigger an automatic rebuild

### Via Git (for developers)

Edit the relevant Markdown files in `content/` and push to `main`.

---

## Adding Team Photos

Team member profile photos should be named `avatar.jpg` (or `.png`) and placed in the author's content directory:

```
content/authors/naimul-khan/avatar.jpg
```

Upload via the CMS (**Team Members** → select person → photo field) or commit directly to the repository.

---

## Customizing the Site

| What to change | Where |
|----------------|-------|
| Site title, base URL | `config/_default/hugo.yaml` |
| Contact info, social links | `config/_default/params.yaml` |
| Navigation menu | `config/_default/menus.yaml` |
| Homepage sections | `content/_index.md` |
| Color theme | `config/_default/params.yaml` → `appearance.theme_day` |
| Team members | `content/authors/*/` |
| Research streams | `content/project/*/` |
| News posts | `content/post/*/` |
| Events | `content/event/*/` |

---

## Local Development

Prerequisites: [Hugo Extended](https://gohugo.io/installation/) v0.119+ and [Go](https://golang.org/) v1.21+

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/quantomics-website.git
cd quantomics-website

# Download Hugo modules
hugo mod download

# Start local dev server
hugo server

# Visit http://localhost:1313
```

To use the CMS locally, run `npx decap-server` in a separate terminal (requires Node.js), then visit `http://localhost:1313/admin/`.

---

## Support

- **Hugo Blox docs:** https://docs.hugoblox.com/
- **Decap CMS docs:** https://decapcms.org/docs/
- **Netlify docs:** https://docs.netlify.com/
- **Program contact:** quantomics@torontomu.ca
