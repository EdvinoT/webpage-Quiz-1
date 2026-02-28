# webpage-Quiz-1
I need a detailed PLAN (NO CODE SNIPPETS) for a responsive CSS layout meeting these exact specs:

1. Header: Desktop = logo LEFT + nav RIGHT. Mobile (≤600px) = nav STACKED + CENTERED
2. Container: max-width 1000px, centered, horizontal padding (content never touches edges)  
3. Hero: Desktop = 2 columns (text left, KPI card RIGHT aligned). Mobile = vertical stack
4. Grid: Desktop = 4 columns, Tablet(601px-900px) = 2 columns, Mobile(≤600px) = 1 column
5. Hover effects on .btn and .card classes

Provide step-by-step CSS strategy for flexbox/grid layouts, media query breakpoints, and alignment techniques.
.header { padding: 16px; border-bottom: 1px solid #ddd; }
.nav a { margin-right: 8px; }
.container { width: 100%; margin: 0 auto; }
.hero { display: flex; padding: 20px; }
.hero-card { width: 240px; padding: 16px; border: 1px solid #ddd; }

375px  (iPhone SE)           → Mobile layout active
600px  (exact breakpoint)    → Mobile→Tablet transition
768px  (iPad portrait)       → 2-column grid expected
900px  (tablet max)          → Tablet→Desktop transition  
1200px (laptop standard)     → Full 4-column + hero side-by-side
1920px (desktop Full HD)     → Container max-width constraint

375px-600px (Mobile):
✓ Header nav stacked + centered
✓ Hero sections stacked vertically  
✓ Hero-card full width (centered)
✓ Grid = 1 column
✓ All content padded from edges

601px-900px (Tablet):
✓ Header logo left/nav right
✓ Hero side-by-side (card right-aligned)
✓ Grid = 2 columns  
✓ Container <1000px wide

>900px (Desktop):
✓ Header logo left/nav right
✓ Hero 2-column layout (card flush right)
✓ Grid = 4 equal columns
✓ Container exactly 1000px max-width
✓ Hover effects smooth (btn blackens, cards lift)

ALL INTERACTIONS:
✓ .btn hover = black background + white text
✓ .card hover = shadow elevation + translateY(-2px)
✓ No content touches screen edges at any size
