# nova-winter-fashion-emailer
Color system
-------------------
Cream #F7F2E9 is the main background.
Beige #E3D9C6 is used for the quote strip.
Soft brown #8A6E55 is used for the discount banner and the small accent labels.
Charcoal #2E2A27 is used for text, the primary button, the top bar and the footer.
Muted greys and tans are used for secondary text and struck-through prices.


Typography
------------------
Role	Style
Logo	Georgia, 26px, letter-spacing: 9px (wide tracking gives the luxury look)
Headline	Georgia italic, 54px/58px, font-weight: normal
Body/subheads	Georgia, 16–18px, with generous line-height (about 1.6)
Prices, small labels	Helvetica/Arial for contrast with the serif

Structure: nested tables
--------------------------
The layout follows this pattern:

Outer table (100% width, beige background)
 └─ td (centers everything)
     └─ Ghost table for Outlook (600px)
         └─ Container table (600px max, cream background)
              └─ tr per section: top bar, logo, hero, copy, CTA, banner, grid, quote, footer
              
Each section is its own <tr>, which makes it easy to reorder or remove blocks.
The outer table's full-width beige background is what you see on either side of the email on desktop.
Every table has role="presentation" so screen readers don't announce it as a data table.
Outlook ghost table: <!--[if mso]><table width="600">...<![endif]--> wraps the container. Outlook ignores max-width, so this forces a 600px width there while other clients use the flexible table.
