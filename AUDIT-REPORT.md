# Website Audit Report: Healing Waters for Dignity
**URL:** https://www.healingwatersfordignity.org
**Date:** 2026-03-20
**Auditor:** Claude Code

---

## Executive Summary

Healing Waters, Inc. is a 501(c)(3) nonprofit providing mobile showers and support services to homeless individuals in Banning, CA. The current website is built on **GoDaddy Website Builder** and serves as a basic informational presence. While the content is heartfelt and the mission is clear, the site has significant issues in design quality, performance, accessibility, and donor conversion that limit its effectiveness as a fundraising and outreach tool.

**Overall Grade: C-**

---

## 1. Design & Visual Quality

### Strengths
- Clean logo with clear brand identity ("Love - Dignity - Hope")
- Teal accent color is distinctive and appropriate
- Professional photos of team and locations

### Issues
| Issue | Severity | Details |
|-------|----------|---------|
| Generic template feel | High | GoDaddy builder produces cookie-cutter layouts that undermine credibility |
| Inconsistent spacing | Medium | Sections have wildly different padding — some cramped, some overly spacious |
| No visual hierarchy | High | All content sections look the same — no differentiation between hero, mission, schedule, team |
| Typography is flat | Medium | League Spartan used everywhere with no weight/size variation to create hierarchy |
| Hero section weak | High | Logo + text side-by-side with no emotional impact — first impression is corporate, not compassionate |
| "The Power of A Shower" section | Medium | Good concept but text overlaid on shower photo has readability issues |
| Director photos inconsistent | Low | Different crops, sizes, and aspect ratios for team member photos |
| Footer/donation section | High | Dark background with parallax image is visually cluttered; PayPal button feels afterthought |

### Color Palette Assessment
- **Background:** `rgb(22, 22, 22)` (nav), white (sections), `rgb(246, 246, 246)` (alternating)
- **Accent:** `rgb(0, 200, 197)` teal — good choice, underutilized
- **Text:** Dark grays — adequate but inconsistent across sections
- **Verdict:** Palette is fine but applied without design system discipline

---

## 2. Content & Information Architecture

### Site Structure (3 pages)
1. **Home** — Everything is here (mission, schedule, history, team, donations)
2. **Services** — Sparse; mostly shower/bathroom stock photos
3. **Contact Us** — Form + phone numbers + donate CTA

### Issues
| Issue | Severity | Details |
|-------|----------|---------|
| Single-page dump | High | Home page is a wall of content — ~2500+ words with no clear user journey |
| Services page is hollow | High | Stock photos of bathrooms, minimal unique content |
| No impact data | High | No statistics, testimonials, or success stories to build donor confidence |
| No volunteer signup | Medium | "Become a volunteer" is mentioned but there's no dedicated path |
| Schedule buried | Medium | Critical operational info is far down the page |
| Typo: "consulation" | Low | Should be "consultation" in wellness clinic description |
| No social media links | Medium | No Facebook, Instagram, or other social presence linked |
| No newsletter/email capture | Medium | Missed opportunity for ongoing engagement |

---

## 3. Performance

### Observations
- **Platform:** GoDaddy Website Builder (heavy framework overhead)
- **Images:** Multiple high-res photos served without optimization; lazy-loading via base64 GIF placeholders
- **Scripts:** Service worker registered, visitor tracking via UUID, marketing attribution (gclid, fbclid)
- **Fonts:** League Spartan loaded from wsimg.com CDN
- **Estimated load time:** Slow — GoDaddy builder ships significant JavaScript/CSS bloat

### Issues
| Issue | Severity | Details |
|-------|----------|---------|
| No image optimization | High | Full-resolution photos served to all devices |
| GoDaddy framework bloat | High | Excessive CSS/JS for a 3-page informational site |
| No caching headers visible | Medium | Platform-managed, limited control |
| No WebP/AVIF format usage | Medium | Modern formats would cut image weight 30-50% |

---

## 4. Accessibility (WCAG 2.1)

| Issue | Level | Details |
|-------|-------|---------|
| Missing alt text | A (Fail) | Multiple images lack alt attributes, including the logo |
| Color contrast: white on teal | AA (Fail) | `rgb(0, 200, 197)` on white/dark backgrounds doesn't consistently meet 4.5:1 |
| No skip-to-content link | A (Fail) | Keyboard users must tab through entire nav on every page |
| Form labels unclear | A (Fail) | Contact form fields may lack proper label associations |
| No ARIA landmarks | A (Fail) | Template-based layout uses divs instead of semantic HTML |
| No focus indicators visible | AA (Fail) | Link/button focus states suppressed or absent |
| Text in images | AA (Fail) | "The Power of A Shower" text baked into image overlay without alt |

---

## 5. SEO

| Factor | Status | Notes |
|--------|--------|-------|
| Title tag | OK | "Healing Waters - Mobile Showers, Nonprofit, For the Homeless" |
| Meta description | Missing | No meta description tag detected |
| Heading hierarchy | Poor | H2 used for org name, inconsistent H3 usage |
| Open Graph tags | Missing | No social sharing metadata |
| Structured data | Missing | No Schema.org markup for NonprofitOrganization |
| Sitemap | Unknown | GoDaddy may auto-generate |
| Mobile-responsive | OK | Responsive breakpoints present |

---

## 6. Donor Conversion

| Issue | Severity | Details |
|-------|----------|---------|
| PayPal-only donations | High | No direct credit card processing; PayPal friction loses donors |
| No donation amounts suggested | High | No "Give $25 / $50 / $100" options — blank PayPal redirect |
| No impact framing | High | "$25 = 5 hot showers" type messaging is absent |
| CTA buried at bottom | High | Donate button only appears after scrolling entire page |
| No recurring donation option | Medium | Monthly giving not promoted |
| No tax receipt mention | Medium | Donors want to know they'll get a receipt |

---

## 7. Mobile Experience

- Navigation collapses to hamburger menu — functional
- Content is responsive but sections are very long on mobile
- Images scale but aren't optimized for mobile bandwidth
- PayPal button is accessible on mobile
- Overall: **Passable but not optimized**

---

## 8. Security & Technical

| Item | Status |
|------|--------|
| HTTPS | Yes (via GoDaddy) |
| Cookie consent | Present |
| reCAPTCHA on contact form | Yes |
| Service worker | Registered |
| Visitor tracking | UUID-based, marketing attribution params |

---

## Recommendations Summary

### Critical (Must Fix)
1. **Redesign with modern, emotional storytelling** — Lead with impact, not org chart
2. **Add impact metrics and testimonials** — Build donor confidence
3. **Improve donation UX** — Suggested amounts, impact framing, sticky CTA
4. **Fix all accessibility failures** — Alt text, contrast, keyboard nav, semantic HTML
5. **Add meta description and Open Graph tags** — Basic SEO

### Important (Should Fix)
6. **Optimize images** — WebP format, responsive srcset, proper sizing
7. **Move off GoDaddy builder** — Static site would be faster, cheaper, more maintainable
8. **Add volunteer signup path** — Dedicated form or section
9. **Create proper Services page** — Real content, not stock photos
10. **Add social media integration** — Link to and embed social content

### Nice to Have
11. Add newsletter signup (Mailchimp or similar)
12. Add Google Maps embed for locations
13. Add event calendar or upcoming dates
14. Blog/news section for updates
15. Annual report or impact report download

---

## Conclusion

The Healing Waters website communicates its mission but fails to convert that mission into action. The GoDaddy template creates a generic presentation that doesn't match the deeply personal, community-driven nature of the organization. A purpose-built redesign focused on emotional storytelling, clear donation paths, and accessibility compliance would significantly improve the site's effectiveness as a fundraising and volunteer recruitment tool.

The recommended approach is a complete frontend rebuild as a static site (HTML/CSS/JS) deployable to GitHub Pages — fast, free hosting with full design control.
