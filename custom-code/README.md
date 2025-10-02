# 🔴 **Pathway 2 — Custom Code Powered Site (Astro / Hugo / Jekyll)**

This pathway is for members who want to **focus on content and presentation first**, while still being able to extend with **custom styles, components, and animations** later.
Your site becomes a **living portfolio and blog**, powered by Markdown for content management.
We'll rely on **LLM guidance** to scaffold templates, configure themes, and gradually add interactivity if desired.


## ✅ Week 1: Build Your LinkedIn Profile

### 🖼️ Profile Picture

* [ ] Upload a professional headshot (plain background, good lighting, natural smile).
* [ ] If you don’t have one, generate with an AI headshot tool (ensure it looks realistic).
* [ ] (Optional) Go and get a headshot taken from a professional studio.


### 🏷️ Headline & Tagline

* [ ] Brainstorm 3–5 headline options.
* [ ] Use this prompt to generate recruiter-friendly headlines:

```
Act as a professional career coach and LinkedIn expert. I want to create a compelling LinkedIn headline and tagline.

Here is my information:
- Target Role/Industry: [e.g., Junior Full-Stack Developer, UX/UI Designer for FinTech, Data Analyst]
- My Top 3-5 Skills: [e.g., React, Node.js, SQL, Figma, User Research, Python, Pandas]
- My Core Professional Interest: [e.g., building scalable web applications, creating intuitive user interfaces, deriving insights from complex datasets]
- A unique quality about me: [e.g., "I'm passionate about clean code," "I love solving complex user problems," "I have a background in finance which gives me unique domain knowledge"]

Based on this, generate 5 different LinkedIn headline options for me. The headlines should be concise (under 220 characters), include relevant keywords for my target industry, and highlight my key value proposition.
```


### 📖 About Section

* [ ] Draft a 150–250 word summary (who you are, skills, achievements, aspirations).
* [ ] Use this prompt to create/refine:

```
Act as a professional LinkedIn summary writer. I want to create a concise, engaging, and professional About section.

Here is my information:
- Current Role/Background: [e.g., MSc in Data Science, 2 years experience as a Business Analyst]
- Skills/Expertise: [e.g., Python, SQL, Tableau, Machine Learning, NLP]
- Achievements (in STAR format if possible): [e.g., automated reporting system saving 15 hours/week, built churn prediction model with 85% accuracy]
- Career Aspirations: [e.g., becoming a Machine Learning Engineer in the healthcare sector]

Please generate 2–3 versions of an About section (150–250 words) that highlight my skills, experience, and aspirations in a way that is recruiter-friendly, engaging, and authentic.
```


### 💼 Experience Section

* [ ] For each role/project, write 3–5 bullet points in STAR format.
* [ ] Use this prompt for achievement-oriented bullets:

```
Act as a professional resume writer. I need to write a compelling, achievement-oriented bullet point for my experience section using the STAR method.

Here is the information for one of my achievements:
- My Role: [e.g., Software Development Intern]
- The Company: [e.g., Tech Solutions Inc.]
- The Situation: [e.g., The customer support team was manually spending hours each week answering the same basic questions from users.]
- The Task: [e.g., I was tasked with developing a solution to automate responses to frequently asked questions to save the team time.]
- The Action I Took: [e.g., I designed, built, and deployed a simple chatbot for the company's main website using JavaScript and the Dialogflow API. I integrated it with their existing knowledge base.]
- The Result: [e.g., The chatbot successfully handled an estimated 40% of incoming user queries, which saved the support team approximately 8 hours of work per week. It also improved user response time.]

Please generate 3 variations of a concise, professional bullet point for my LinkedIn profile based on this information. Start the bullet point with an action verb.
```


### 🛠️ Skills & Endorsements

* [ ] Add 10–15 relevant skills (Python, SQL, ML, Deep Learning, Generative AI, etc.).
* [ ] Reorder to show top 3–5 first.
* [ ] Ask 1–2 peers to endorse your top skills.


### 🌟 Extras (Optional but Valuable)

* [ ] Customize LinkedIn URL (e.g., linkedin.com/in/firstname-lastname).
* [ ] Add featured links (GitHub, portfolio, blog, projects).
* [ ] Request at least one recommendation (peer, mentor, or manager).


**End of Week 1 Goal:** A polished, keyword-optimized LinkedIn profile with a professional photo, headline, About section, STAR-based experience bullets, and skills that reflect your career goals.

## ✅ **Week 2 — Plan, Build & Deploy**

**Goal:** Plan your content, set up your development environment, scaffold the Astro + Markdown project, build your sections, and deploy live.

### **To-Do Checklist**

* [ ] Install **Node.js**, **npm**, and **Git**
* [ ] Create and clone a **GitHub repo**
* [ ] Set up **VS Code** with helpful extensions
* [ ] Scaffold Astro project (via LLM prompt)
* [ ] Generate and paste **Markdown copy** (via LLM prompt)
* [ ] Add **project images** to `/public/images/`
* [ ] Run site locally with `npm run dev`
* [ ] Iterate on styling/layout until satisfied
* [ ] Push project to GitHub
* [ ] Connect repo to Vercel / Netlify / GitHub Pages
* [ ] Deploy and get live URL
* [ ] Add optional **custom domain**
* [ ] Test navigation anchors
* [ ] Share link on LinkedIn with a short announcement


### **Setup Environment**

* [ ] Install **Node.js** (LTS version) and **npm** from [nodejs.org](https://nodejs.org/).
* [ ] Verify installation with `node -v` and `npm -v`.
* [ ] Install **Git** from [git-scm.com](https://git-scm.com/).
* [ ] Configure Git:

  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  ```
* [ ] Create a **GitHub account** (if you don’t already have one).
* [ ] Create a new **GitHub repo** for your portfolio project.
* [ ] Clone the repo locally:

  ```bash
  git clone <your-repo-url>
  cd <repo-name>
  ```
* [ ] Install **VS Code**. Recommended extensions: **Astro**, **Markdown All in One**.
* [ ] (Optional) Install **VS Code Live Server** for quick previews of static HTML.


### **Get Inspiration**

Have a look at free portfolio themes from the [Astro Themes website](https://astro.build/themes/3/?search=&categories%5B%5D=portfolio&price%5B%5D=free) for inspiration. You can download the files from any portfolio you like and just make changes to the markdown files to add in your information.

Or you can choose to build your own custom template using the prompts below. Be sure to change the styling and information to how you want your website to look like.


### **Step A — Prompt to Build the Astro + Markdown Project (Template/Files)**

```
You are an expert Astro starter generator. Create a **single-page portfolio** starter that uses **Astro + MDX** with content in Markdown and a minimal black-and-white theme.

### Requirements
- Stack: Astro + @astrojs/mdx, no Tailwind, plain CSS.
- Single page only: `src/pages/index.mdx` with sections: Hero, About, Skills, Experience, Projects, Contact.
- Components: `src/components/ProjectCard.astro` for project cards.
- Layout: `src/layouts/BaseLayout.astro`.
- Styles: `src/styles/global.css` (black & white, pills for skills inside the Hero; responsive grid for projects; smooth scroll; sticky nav).
- Assets folder: `public/images/` (use placeholder names).
- Keep CSS simple and readable using CSS variables.
- Provide a file tree and the content for every file as fenced code blocks.
- Include setup instructions (`npm` commands) and a note on where to edit copy.

### User Inputs
Theme options:
- Base fonts: [e.g., system-ui]
- Accent style: [underline links | bordered buttons]
- Project grid columns (desktop): [2 | 3]
- Section spacing (rem): [3.2]
- Card border style: [1px solid #111]

### Output Format
1. File tree  
2. `package.json`  
3. `astro.config.mjs`  
4. `src/styles/global.css`  
5. `src/layouts/BaseLayout.astro`  
6. `src/components/ProjectCard.astro`  
7. `src/pages/index.mdx` with placeholder text and anchor IDs (#about, #skills, #experience, #projects, #contact)  
8. `public/images/placeholder.png` (describe placeholder, no binary)  
9. Setup steps (`npm i`, `npm run dev`)  
10. Where to edit content  
```


### **Step B — Prompt to Generate All Portfolio Copy as Markdown**

````
You are a portfolio content writer. Produce **final Markdown** for a one-page Astro site and per-project Markdown entries.

### Inputs
[Hero]
- Name: <your name>
- Role/Title: <e.g., Data Scientist • AI Engineer>
- Tagline (1 line): <...>
- CTA text + anchor link: <e.g., View Projects → #projects>

[About]
- Short bio (3–5 sentences)
- Highlights (3 bullets)

[Skills]
- 10–15 skills as a bulleted list

[Experience]
- Up to 3 roles. For each: title, company, dates, 3–5 impact bullets

[Projects]
- 3–4 projects. For each: title, summary, stack, links (repo/demo), image filename (e.g., `/images/p1.png`)

[Contact]
- Email, GitHub, LinkedIn (and optional Calendly)

### Output
1) `index.mdx` content (sections: Hero, About, Skills, Experience, Projects, Contact)  
2) Per-project Markdown blocks with frontmatter:  
```yaml
---
title: "<Project Title>"
summary: "<2–3 sentence summary>"
stack: ["Python","FastAPI","Docker"]
links: { repo: "https://...", demo: "https://..." }
thumbnail: "/images/<filename>.png"
---
````

3. Checklist of images to prepare under `/public/images/`

````


### **Step C — Drop Files In & Preview**
1. Create the project from Step A’s output (or copy files into your repo).  
2. Paste all Markdown from Step B into `src/pages/index.mdx` (and add images under `public/images/`).  
3. Run:  
   ```bash
   npm install
   npm run dev
````

Visit `http://localhost:4321`.


### **Step D — Iterate on Styling & Layout**

Keep tweaking your website alongside an LLM until you are satisfied with your website.


### **Deploy & Share**

### **Deploy Options**

* **GitHub Pages** (works with Astro builds).
* **Vercel** (seamless for Astro).
* **Netlify** (works for Hugo/Jekyll/Astro).

**Steps:**

1. Push code to GitHub.
2. Connect repo to chosen platform.
3. Configure build settings (Astro → `npm run build`, output: `dist`).
4. Deploy and get live URL (e.g., `yoursite.vercel.app`).


### **Custom Domain**

After purchasing a domain (e.g., from **Namecheap**, **Cloudflare**, or **Google Domains**), point it to your hosting provider.

#### **On Vercel**

1. In Vercel dashboard → **Settings → Domains**.
2. Add your custom domain.
3. Add DNS records at your registrar:

   * `A` record → `76.76.21.21`
   * Or `CNAME` record → `cname.vercel-dns.com`
4. Wait for propagation (up to 24 hrs).

#### **On Netlify**

1. In Netlify dashboard → **Site Settings → Domain Management**.
2. Add your domain.
3. Update DNS at your registrar:

   * Point nameservers to Netlify (preferred).
   * Or add `CNAME` pointing to `<yoursite>.netlify.app`.
4. SSL is auto-provisioned.

#### **On GitHub Pages**

1. Repo → **Settings → Pages → Custom Domain**.
2. Enter your domain.
3. Add DNS records at your registrar:

   * `A` records:

     * 185.199.108.153
     * 185.199.109.153
     * 185.199.110.153
     * 185.199.111.153
   * Or `CNAME` → `<username>.github.io`
4. GitHub auto-provisions SSL.


### **Navigation QA**

* [ ] Navbar anchors scroll correctly.

### **Sharing**

* Record a Loom walkthrough.
* Post link on LinkedIn with a short write-up.
* Ask peers for feedback.

**Prompt Template – LinkedIn Post**

```
Act as a LinkedIn content creator. Write a short announcement for my new Markdown-powered portfolio site.
Include:
- My role/skills
- Purpose of the site
- Call-to-action
Keep under 200 words.
```

## 📦 **Submission Checklist (Markdown Path)**

* [ ] **Week 2 complete**: Environment set up, project scaffolded, content added, styling applied, images present, site runs locally, and deployed live.
* [ ] **Repo link**: GitHub repository with `src/` and `public/`.
* [ ] **Live URL**: Deployed site with optional custom domain.
* [ ] **Screenshots**: Hero, About, Skills, Experience, Projects, Contact (desktop + mobile).
* [ ] **README** updated with framework choice, theme notes, and next steps.
Keep under 200 words.
```


## 📦 **Submission Checklist (Markdown Path)**

* [ ] **Week 2 complete**: Environment set up, project scaffolded, content added, styling applied, images present, site runs locally.
* [ ] **Repo link**: GitHub repository with `src/` and `public/`.
* [ ] **Screenshots**: Hero, About, Skills, Experience, Projects, Contact (desktop + mobile).
* [ ] **Week 3 deployed**: Live URL + optional custom domain.
* [ ] **README** updated with framework choice, theme notes, and next steps.

