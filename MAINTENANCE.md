# Static maintenance page (not enabled)

maintenance.html is standalone: no app, database, session, scripts or images.
Fonts are optional. Its back button points to the app; no deadline or claim
about saved data is made.

For APP planned maintenance, publish this on the separate marketing static site,
verify its real URL returns200 and this content, then use that URL as the app's
Render Maintenance Mode custom URI. This is separate from deploying this file.
Paid web services only. Render returns503 to public traffic, while private/SSH
access remains. Do not point at torquebench.app while that app is in maintenance.
If the custom URL errors, Render passes that error through rather than its
standard page. No settings changes or toggle are included here.

https://render.com/docs/maintenance-mode

For MARKETING maintenance, this page is only an asset until a serving/routing
choice is approved. Static services do not use the paid web-service maintenance
toggle. A file on this service cannot cover this service being wholly unavailable,
DNS failure or a Render-wide outage. Automatic outage fallback would need a
separate edge/hosting design; do not claim this deployment supplies that.

Validate status/content on the exact deployed URL before using it. If any setup
fails, stop and report it, no silent retry/rollback/fallback. Disabling an app's
maintenance toggle is a separate approved restore-public-traffic action.
