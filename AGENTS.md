# Senebridge website

Canonical source repository: https://github.com/sbworkstation/SBwebsite
Production domain: https://senebridge.com
Hosting: ChatGPT Sites. Reuse the exact project_id in .openai/hosting.json; never create a replacement Site for an update.

## Routine website requests

- Read these instructions and the current repository before making changes.
- The page is a buildless static site in dist/index.html. Keep the implementation simple; no framework or database is required.
- Use GitHub as the canonical source. Save all source changes there before publishing. Use the connected GitHub tools if local GitHub write authentication is unavailable.
- For a deployment, fetch the resulting GitHub commit into the local checkout, push that exact source commit to the existing Sites source repository using a short-lived credential, package the static assets using the installed Sites skill, save the version and deploy it.
- Always follow the available Sites building and hosting skills. Discover the currently installed skill path rather than hard-coding a plugin version.
- A user request to deploy or publish authorizes publishing the requested change to the existing public website. A request for a draft or preview alone does not authorize replacing production.
- Verify the deployment succeeds and that https://senebridge.com returns the requested content over HTTPS. Report an unresolved DNS or deployment failure plainly.
- Preserve Northwest domain registration, nameservers, and all Zoho email records. Routine page updates need no DNS changes.
- Never commit credentials, tokens, passwords, local environment files, or customer data. Only dist is served publicly; source documentation stays outside dist.
- Keep changes focused on the user's request. Do not add forms, tracking, dependencies, paid services, or application features without a need in the request.

## Recovery

For a rollback, inspect Sites version history and restore a known working saved version when requested. Keep GitHub aligned with the version intended to remain current. Never delete the Site or change domain ownership to fix a deployment.
