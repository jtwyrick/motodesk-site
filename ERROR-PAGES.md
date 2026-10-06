# Error-page assets (routing not enabled)

404.html and500.html use the app's service-ticket style with new jokes.
They are standalone static documents, with no runtime dependency, form, or JS.
The home button returns to gettorquebench.com, not the shop app.

Current Render static service: srv-dahipjtg1s2s73bckiq0, root publish directory.
Dashboard redirects/rewrites had no rules at the read-only inspection.
Render documentation does not establish a native custom404 or500 fallback:
https://render.com/docs/static-sites
https://render.com/docs/redirects-rewrites

Uploading these files alone is NOT proof that unknown URLs or provider failures
will show them. No catch-all rewrite is added: it can turn missing paths into
200 soft404s. Confirm actual host support/status before activating a fallback.
500.html is a reviewed design asset until an actual host error hook is verified.
DNS and full provider outages cannot be replaced by a file on that same host.
