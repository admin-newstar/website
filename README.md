NewStar Ventures — Static Site

Single-file static website. No build step, no dependencies, no external requests.

Files





index.html — the entire site (HTML, CSS, JS inline)



README.md — this file

Publish on GitHub Pages





Create a new repository on GitHub (e.g. newstar-ventures).



Upload index.html to the root of the repo (Add file → Upload files, then commit).



Go to Settings → Pages.



Under Source, choose Deploy from a branch; set branch to main and folder to / (root). Save.



Wait ~1 minute. The site goes live at https://<your-username>.github.io/<repo-name>/.



Custom domain (newstar.ventures)





In Settings → Pages → Custom domain, enter www.newstar.ventures and save. This creates a CNAME file in the repo.



At your domain registrar, add a CNAME record: www → <your-username>.github.io



For the apex domain, add four A records pointing to:

185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153



Back in Settings → Pages, tick Enforce HTTPS once the certificate is issued.



Editing

Everything lives in index.html:





Contact details — search for 623 and admin@newstar.ventures (they appear in the contact cards, the footer, and the form script).



Accent color — change --accent near the top of the <style> block.



Copy — each section is labeled with an HTML comment (<!-- ===== FOCUS ===== -->, etc.).



Contact form

The form composes an email in the visitor's mail client via mailto: — nothing to host or pay for, which is why it works on GitHub Pages. If you'd rather receive submissions directly in your inbox, swap it for a free form endpoint (Formspree, Getform, Web3Forms): replace the <form id="contactForm" ...> tag with <form action="https://formspree.io/f/YOUR_ID" method="POST"> and delete the form-submit block in the <script>.
