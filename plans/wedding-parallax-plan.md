# Wedding Invitation Webpage - Parallax Design Plan

## Priority Focus - Location Navigation

> **IMPORTANT:** The primary purpose of this website is for guests to quickly find and navigate to the ceremony location. All design decisions prioritize easy location access.

### Design Priority
1. **Ceremony Location** - Most prominent after hero section
2. **Google Maps Integration** - Large, clearly visible buttons
3. **Quick Access** - Minimal scrolling to reach map links
4. **Visual Confirmation** - Clear venue names and addresses

---

## Wedding Details (From User)

> **IMPORTANT:** Primary focus is helping guests find locations easily. Google Maps buttons must be prominent and easily accessible.
| Field | Value |
|-------|-------|
| **Bride** | Sabitha |
| **Groom** | Shiva |
| **Wedding Date** | May 25, 2026 (Monday) |
| **Ceremony Time** | 5:30 AM - 7:00 AM (IST) |
| **Wedding Venue** | Eshwaran Temple, Rasipuram |
| **Reception Date** | May 26, 2026 (Tuesday) |
| **Reception Time** | 11:00 AM - 3:00 PM (IST) |
| **Reception Venue** | Kongu Thirumana Maaligai, Vaiyappamalai |
| **Bride's Home** | Bride's Residence |

---

## Page Structure (Parallax Sections)

```mermaid
graph TB
    A[Hero Section<br/>Names & "Save the Date"] --> B[Couple Caricature<br/>Parallax Image]
    B --> C[ Wedding Ceremony<br/>Temple Location & Map]
    C --> D[Reception<br/>Maaligai Location & Map]
    D --> E[Bride's Home<br/>Residence Location & Map]
    E --> F[Footer<br/>Love Message]
    
    style A fill:#7b1e2b,color:#fff
    style B fill:#b76e79,color:#fff
    style C fill:#fff,color:#333
    style D fill:#fff,color:#333
    style E fill:#fff,color:#333
    style F fill:#7b1e2b,color:#fff
```

---

## UI/UX Specifications

### Color Palette
| Purpose | Color | Hex |
|---------|-------|-----|
| Primary (Deep Maroon) | Wedding elegance | `#7b1e2b` |
| Secondary (Rose) | Accent color | `#b76e79` |
| Background Light | Cream gradient start | `#fff7ef` |
| Background Dark | Cream gradient end | `#ffe9dc` |
| Text Primary | Dark brown | `#4a3728` |
| Text Accent | Maroon | `#7b1e2b` |
| Gold Accent | Decorative | `#d4af37` |

### Typography
- **Headings:** Playfair Display (serif) - elegant, classic wedding feel
- **Body:** Poppins (sans-serif) - clean, readable
- **Decorative:** Unicode symbols (lamps, flowers, ornaments)

### Layout Structure

#### 1. Hero Section (Parallax)
- Full viewport height (100vh)
- Background: Layered decorative pattern with floating elements
- Centered: Couple names "Shiva ❤️ Sabitha"
- Subtitle: "We're Getting Married"
- Date prominently displayed
- Animated scroll indicator

#### 2. Couple Caricature Section (Parallax)
- Background: Soft gradient with floating flower petals
- Caricature image (existing `caricature.png`)
- Decorative border/frame effect
- Floating ornament animations

#### 3. Wedding Ceremony Section
- White card with subtle shadow
- Temple name with icon
- Full address
- Date & Time (5:30 AM - 7:00 AM IST)
- Google Maps button (link confirmed)
- Decorative divider

#### 4. Reception Section
- Same card style as ceremony
- Venue name with icon
- **Date & Time: May 26, 2026 (Tuesday) 11:00 AM - 3:00 PM**
- Address
- Google Maps button
- Festive decorations

#### 5. Bride's Home Section
- Same card style
- "Bride's Residence" label
- Google Maps button

#### 6. Footer
- "With Love" message
- Couple initials or decorative element
- Bottom lamps decoration

---

## Interactive Features

### Parallax Effects
- Hero background moves at 0.5x scroll speed
- Caricature section background at 0.3x speed
- Floating decorative elements at varying speeds

### Animations
- Fade-in on scroll for each section
- Button hover: scale + shadow enhancement
- Text reveal animations on page load
- Floating elements continuous animation
- Smooth scroll behavior between sections

### Buttons
- Gradient background matching theme
- Hover state: slight lift and shadow
- Active state: pressed effect
- Opens Google Maps in new tab

---

## Responsive Breakpoints

| Breakpoint | Width | Adjustments |
|------------|-------|-------------|
| Desktop | > 1024px | Full layout, large typography |
| Tablet | 768px - 1024px | Adjusted spacing, medium fonts |
| Mobile | < 768px | Stacked layout, compact sections, full-width buttons |

---

## Technical Implementation

### Structure
- Single HTML file with embedded CSS and JavaScript
- External fonts from Google Fonts
- Existing caricature.png preserved
- No external dependencies (pure CSS parallax)

### CSS Features Used
- `background-attachment: fixed` for parallax
- CSS animations (@keyframes)
- Flexbox/Grid for layout
- CSS custom properties for theming
- Media queries for responsiveness

### JavaScript
- Intersection Observer for scroll animations
- Smooth scroll behavior
- Optional: parallax calculations for enhanced effect

---

## File Structure
```
WeddingAndReceptionAddress/
├── index.html        (new parallax version)
├── caricature.png    (existing - unchanged)
├── README.md         (existing)
```

---

## Implementation Tasks

1. [ ] Create hero section with parallax background
2. [ ] Add couple names and save the date
3. [ ] Implement caricature section with floating elements
4. [ ] Create wedding ceremony card with all details
5. [ ] Create reception card with all details
6. [ ] Create Bride's Home card
7. [ ] Add footer section
8. [ ] Implement parallax CSS effects
9. [ ] Add scroll animations
10. [ ] Style buttons with hover effects
11. [ ] Ensure mobile responsiveness
12. [ ] Test all Google Maps links work

---

## Acceptance Criteria

- [ ] Page loads with smooth animations
- [ ] Parallax effect visible on scroll
- [ ] All wedding details correctly displayed
- [ ] Google Maps buttons functional
- [ ] Mobile responsive (looks good on phone)
- [ ] Elegant, wedding-appropriate aesthetic
- [ ] Caricature image displays properly
- [ ] No horizontal scrolling on any device
- [ ] All fonts load correctly
