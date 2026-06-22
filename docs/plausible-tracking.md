# Plausible Tracking

The production site `industry.tum-blockchain.com` loads the self-hosted Plausible tracker from the shared TBC Plausible instance:

```html
<script
	defer
	data-domain="industry.tum-blockchain.com"
	src="https://plausible.rbg.tum-blockchain.com/js/script.js"
></script>
```

The script is installed in `src/app.html` so it is present on every SvelteKit page.

Verify locally after a build by inspecting the generated HTML or by checking the deployed page source for `plausible.rbg.tum-blockchain.com/js/script.js`.
