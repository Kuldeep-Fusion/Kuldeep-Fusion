from pathlib import Path
import shutil, zipfile, os

base = Path("/mnt/data/kuldeep-github-profile")
assets = base / "assets"
assets.mkdir(parents=True, exist_ok=True)

banner_src = Path("/mnt/data/ultra_wide_cinematic_dark_green_black_tech_banne.png")
banner_dst = assets / "profile-banner.png"
shutil.copy2(banner_src, banner_dst)

readme = r'''<!--
  GitHub Profile README
  Repository name must match your GitHub username: Kuldeep-Fusion
  Keep profile-banner.png inside the assets/ folder.
-->

<div align="center">
  <img src="assets/profile-banner.png" alt="Kuldeep Kumar — Full-Stack Developer" width="100%" />

  <h1>Hey, I'm Kuldeep Kumar 👋</h1>
  <h3>Full-Stack Developer · Tech Creator · Problem Solver</h3>
  <p>Building modern, scalable and AI-powered web applications.</p>

  <p>
    <a href="https://kuldeep-zeta.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-Visit-16a34a?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
    <a href="https://github.com/Kuldeep-Fusion"><img src="https://img.shields.io/badge/GitHub-Follow-111827?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
    <a href="https://ats-checker-free.vercel.app/"><img src="https://img.shields.io/badge/Live_Project-ATS_Checker-0ea5e9?style=for-the-badge&logo=vercel&logoColor=white" alt="ATS Resume Checker" /></a>
  </p>
</div>

---

## 👨‍💻 About Me

- 💻 Full-Stack Developer focused on building useful, responsive web applications.
- ⚛️ Working with **React, Next.js, Node.js, Express.js and MongoDB**.
- ✨ Interested in AI-powered products, clean UI, performance and scalable backend systems.
- 🚀 Currently sharpening my skills in **MERN, Next.js, system design and AI integrations**.
- 🤝 Open to collaborating on interesting web and open-source projects.

---

## 🧰 Tech Stack

<div align="center">
  <img src="https://skillicons.dev/icons?i=html,css,js,ts,react,nextjs,tailwind,bootstrap,nodejs,express,mongodb,firebase,git,github,figma,vite&perline=8" alt="Technology stack" />
</div>

---

## 📌 Featured Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>💬 Chat Application</h3>
      <p>Real-time chat experience with Socket.IO, authentication, friend requests, notifications and AI chat.</p>
      <p><strong>Built with:</strong> Next.js · Node.js · MongoDB · Socket.IO</p>
      <!-- Replace # with the public repository URL when ready. -->
      <a href="https://github.com/Kuldeep-Fusion">View on GitHub ↗</a>
    </td>
    <td width="50%" valign="top">
      <h3>🌐 Portfolio v2</h3>
      <p>Personal portfolio showcasing projects, skills and development experience with a modern responsive interface.</p>
      <p><strong>Built with:</strong> React · Tailwind CSS · Framer Motion</p>
      <a href="https://github.com/Kuldeep-Fusion/Portfolio-v2">Source Code ↗</a> ·
      <a href="https://kuldeep-zeta.vercel.app/">Live Demo ↗</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🎬 MovieFlex</h3>
      <p>Movie discovery application with search, filters, trending titles and detailed movie information.</p>
      <p><strong>Built with:</strong> React · TMDB API · Tailwind CSS</p>
      <a href="https://github.com/Kuldeep-Fusion">Explore repositories ↗</a>
    </td>
    <td width="50%" valign="top">
      <h3>📄 ATS Resume Checker</h3>
      <p>AI-powered resume checker that analyzes resumes, provides a match score and suggests improvements.</p>
      <p><strong>Built with:</strong> Next.js · Gemini API · Tailwind CSS</p>
      <a href="https://ats-checker-free.vercel.app/">Live Demo ↗</a>
    </td>
  </tr>
</table>

---

## 📊 GitHub Statistics

<div align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=Kuldeep-Fusion&show_icons=true&theme=transparent&hide_border=true&title_color=22c55e&icon_color=22c55e&text_color=c9d1d9&rank_icon=github" alt="Kuldeep's GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kuldeep-Fusion&layout=compact&theme=transparent&hide_border=true&title_color=22c55e&text_color=c9d1d9&langs_count=6" alt="Most used languages" />
</div>

<div align="center">
  <img width="70%" src="https://github-readme-streak-stats.herokuapp.com?user=Kuldeep-Fusion&theme=transparent&hide_border=true&ring=22c55e&fire=22c55e&currStreakLabel=22c55e&sideLabels=c9d1d9&dates=8b949e" alt="GitHub contribution streak" />
</div>

---

## 🗓️ Contribution Activity

<div align="center">
  <img src="https://ghchart.rshah.org/22c55e/Kuldeep-Fusion" alt="Kuldeep's GitHub contribution graph" width="100%" />
</div>

---

## 🤝 Connect With Me

<div align="center">
  <a href="https://github.com/Kuldeep-Fusion"><img src="https://img.shields.io/badge/GitHub-111827?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="https://kuldeep-zeta.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-16a34a?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn — add your profile URL" /></a>
</div>

<div align="center">
  <p><i>“Great products are built with curiosity, consistency and a lot of problem-solving.”</i></p>
  <img src="https://komarev.com/ghpvc/?username=Kuldeep-Fusion&style=flat&color=16a34a" alt="Profile views" />
</div>
'''
readme_path = base / "README.md"
readme_path.write_text(readme, encoding="utf-8")

# Also provide the README separately for easy copy/paste.
standalone_readme = Path("/mnt/data/README-Kuldeep-GitHub-Profile.md")
standalone_readme.write_text(readme, encoding="utf-8")

# Bundle README + banner into a ready-to-upload folder archive.
zip_path = Path("/mnt/data/Kuldeep-GitHub-Profile-README.zip")
with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as zf:
    zf.write(readme_path, "README.md")
    zf.write(banner_dst, "assets/profile-banner.png")

print("Created:")
print(readme_path)
print(standalone_readme)
print(banner_dst)
print(zip_path)
