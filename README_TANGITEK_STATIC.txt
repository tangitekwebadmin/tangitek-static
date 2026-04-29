TangiTek static site conversion

Converted PHP template pages to static HTML for Azure Static Web Apps.

Notes:
- Common PHP header/sidebar/footer content was rendered into each HTML page.
- Internal tangitek.com links were normalized to root-relative paths and converted from .php to .html.
- Existing /images, /downloads, and /w3c subfolder references are preserved as root-relative paths. Copy those folders into this deployment root before deploying if they are not already included.
- report-to-eco.html contains a form that still posts to mail.php. Static Web Apps will not execute mail.php; replace with a form service or Azure Function if that form must work.
- contactus.html has a static timestamp rendered at conversion time because the original PHP displayed the current server date/time.

Deploy the contents of this folder, not the folder itself, to Azure Static Web Apps.
