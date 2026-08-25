Ekodeck Deck Planner v1.0.23


DEPLOYMENT
1. Upload index.html and the entire assets folder together.
2. Keep the relative folder structure unchanged.
3. Set window.EKODECK_SEND_PLAN_ENDPOINT near the top of index.html to your deployed Cloudflare Worker URL.
4. worker.js is included for reference/update if required. Existing SendGrid secrets and Browser Run binding remain unchanged.

PLANNER MODES
- Customer DIY: enabled and clickable from the first screen.
- Advanced User: opens the existing professional deck-shape selector and tools.

IMPORTANT
Do not upload or reference any old core_decoded development file. It is not required by this build.

v1.0.10 NOTE - PDF ATTACHMENT NAME
The attachment filename is controlled by worker.js. Deploy the included worker.js to Cloudflare if you want customer and internal attachments to be named "Ekodeck Plan.pdf". Existing SendGrid secrets and Browser Run binding names do not change.

v1.0.19 NOTE - STEP 10 LIVE METRICS
Breaker-board plan cycling now recalculates total boards and overall waste for the selected breaker layout, and Step 11/PDF use the same selected-plan figures.


v1.0.20 EMAIL UPDATE:
Redeploy worker.js in Cloudflare to activate the new branded customer email, inline Ekodeck logo, links and Support Team signature. No SendGrid secrets need to change.


v1.0.21 ENDPOINT:
The planner is preconfigured to send to https://ekodeck-plan-email.gavelkane.workers.dev/ . No manual endpoint edit is required.


v1.0.22: Step 10 now recalculates stock-board quantity and waste from the actual selected breaker-board bay layout. The preconfigured Worker endpoint and branded email remain unchanged.

v1.0.23 DIY PDF EXPORT UPDATE:
- Page 1 plan legend now includes: "*Note : Breaker boards are regular decking boards.*"
- Page 2 legend uses "Standard QuickFix Clip" and "Locking QuickFix Clip".
- Standard clip symbols in the rendered QuickFix drawing are horizontal.
- Breaker-board subframe supports render as clear ladder framing, matching the picture-frame ladder style.
- The duplicate Material Summary page has been removed. The Product & Price Summary is now Page 4 of 4.
- This update is in index.html only; worker.js does not require a redeploy for these PDF layout changes if the existing v1.0.22 worker is already deployed.
