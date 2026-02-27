# Build: Scandic IT Spare Parts Inventory Portal

## What to build
A single-page web app (index.html) — an online spare parts inventory for Dell Latitude laptops that Scandic IT can share with customers via a login link.

## Design requirements
- Match Scandic IT's website style (scandic-it.com): clean, modern, professional
- Dark header/hero area, white content sections, subtle shadows
- Colors: dark navy/charcoal (#1a1a2e or similar), green accent (#2ecc71 or similar for Scandic's sustainability angle), white backgrounds
- Clean sans-serif font (Inter or system fonts)
- Mobile responsive
- Professional enough to share with enterprise clients

## Features

### 1. Login wall
- Simple password input (like pipeline.returna.com)
- Password stored as SHA-256 hash in the code
- Default password: "scandic2026"
- Scandic IT logo/branding on login

### 2. Dashboard overview
- Total parts in inventory
- Models covered (7)
- Cross-compatibility highlights
- Quick stats cards

### 3. Inventory table
- Filter by model (5410, 5420, 5430, 5440, 5450, 3420, 3430)
- Filter by part category (Battery, Screen, Keyboard, SSD, RAM, System Board, etc.)
- Search functionality
- Columns: Part Category, Description, Compatible Models, Dell P/N, Stock Priority, Notes
- Sort by any column
- Cross-compatibility highlighted (parts that work across multiple models shown with a badge)

### 4. Model comparison view
- Select 2+ models to see which parts they share
- Visual matrix showing compatibility

### 5. System Board reference
- Dedicated section showing all motherboard variants with CPU specs
- Clear warning about non-interchangeable boards

## Data
All data comes from spare-parts-inventory.md in this directory. Parse it and embed as JSON in the HTML.

Here's the structured data to embed:

### System Boards
| Model | CPU | Dell P/N | Board ID |
|-------|-----|----------|----------|
| 5410 | i7-10610U | 67VJ9 | LA-J372P |
| 5420 | i7-1185G7 | 772C9 | LA-K491P |
| 5430 | i7-1255U | 3G0RF | LA-L591P |
| 5430 | i7-1265U | 4X33N | LA-L591P |
| 5440 | i7-1365U | TKYC0 | LA-M401P |
| 3420 | i5-1145G7 | 3GP42 | Cybory-L15 |
| 3430 | i5-1235U | TBD | TBD |

### Parts inventory (embed all from the markdown file)

## Technical
- Single index.html file (all CSS/JS inline)
- No build tools, no frameworks — vanilla HTML/CSS/JS
- Host on GitHub Pages
- Must work offline after initial load

## Branding
- Title: "Scandic IT — Spare Parts Portal"
- Subtitle: "Dell Latitude Parts Inventory & Compatibility"
- Footer: "© 2026 Scandic IT — Tarmvej 8, 9220 Aalborg Øst, Denmark"
- No Scandic IT logo file available — use text logo styled nicely
