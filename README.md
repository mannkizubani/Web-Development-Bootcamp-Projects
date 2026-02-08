# Personal Website — Pages

- index.html — Home page
- consultation.html — Consultation details and booking form
- podcast.html — Podcast episode listing
- blog.html — Blog page (attempts to fetch posts from live blog)
- contact.html — Contact form and map placeholder
- assets/css/style.css — Main stylesheet
- assets/js/main.js — Mobile menu, form handlers, and blog fetch logic
- assets/images/hero-placeholder.svg — Simple illustration placeholder

**Two Approaches for Quick WordPress integration:**

- Option A (quick): Create Pages in WordPress and use the Custom HTML block to paste the HTML content for each page. Add the CSS to Appearance → Customize → Additional CSS, and enqueue the JS with a plugin that injects scripts into the footer.
- Option B (theme): Add the CSS and JS to your theme or child theme and create page templates for each layout. For the Blog page, the provided script attempts to fetch and parse https://whereispillmythoughts.com/blog/ — this will fail if the blog blocks cross-origin requests. Use a server-side proxy or expose a JSON endpoint if needed.
- Forms: The included forms are client-side only. To receive submissions in WordPress, replace the form action with an endpoint (WP REST API, Contact Form 7, or another plugin) or use a form plugin and embed its markup.
