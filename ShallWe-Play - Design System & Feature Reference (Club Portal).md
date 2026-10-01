# **Design System & Feature Reference**

# **ShallWe-Play Club Admin Portal**

---

# **1\. Executive Overview & Platform Architecture**

The ShallWe-Play Club Admin Portal (audited live at https://test.app.shallwe-play.com/booking-rules/?tab=booking) serves as an authoritative desktop-first workspace for sport venue administrators, operation managers, and front-desk personnel.

# **Header, Canvas & Navigation Structure**

The portal platform architecture comprises the following core interface regions:

* **Top Navigation Header (Fixed Height: 64px, White Surface, \#E2E8F0 Border):**  
  * **Tenant Selector:** Displays the active tenant name ("PayoutTest") along with brand identity elements.  
  * Horizontal Navigation Menu: Primary module bar containing top-level navigation items: Booking, Membership, Finance, Settings ∨ (dropdown), and Review.  
  * Right Header Utility Actions: Features a notifications bell trigger, a language switcher control, and a user avatar badge complete with an active green online status dot.  
* Main Canvas & Application Container:  
  * **Background & Sizing:** Formatted with a \#F8F9FA canvas background hosting a 1200px max-width centered container.  
* Footer Region:  
  * **Minimal Copyright Footer:** Centered bottom block using muted text styling (\#8C98A4).

# **Platform Architecture Specifications**

| Layout Region | Dimensions & Styling | Component Details |
| :---- | :---- | :---- |
| **Top Header** | `64px height, #FFFFFF surface, #E2E8F0 border` | Tenant "PayoutTest", Navigation (Booking, Membership, Finance, Settings ∨, Review), Right Actions (Notifications bell, Language switcher, User avatar \+ green dot) |
| **Main Canvas Container** | `1200px max-width, centered, #F8F9FA bg` | Hosts page module viewports, card grids, tables, and settings tabs |
| **Footer Block** | `#8C98A4 text color` | Minimal copyright notice |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

---

# **2\. Complete Feature Catalogue & Module Inventory**

# **2.1 Booking Management (/booking-rules/)**

* Purpose & Navigation: Core venue schedule and rules management split across four sub-navigation tabs:  
  * Tab 1: Booking Rules (?tab=booking): Operational hours, slot intervals, advance booking windows, and usage limits.  
  * Tab 2: Pricing & Cancellation (?tab=pricing): Dynamic tier rates (Peak, Off-Peak), court rate overrides, refund percentages, and cancellation timeframes.  
  * Tab 3: Manage Assets (?tab=assets): Infrastructure inventory for courts, fields, and facilities status management.  
  * Tab 4: Equipment (?tab=equipment): Rental item tracking, stock counts, check-in/out logs, and availability counters.  
* User Flows & Patterns: Tab-based sub-navigation, multi-step rule builders, step list visualizers, conflict banners, drawer sheets, and toggle triggers.

# **2.2 Membership (/membership/)**

* Purpose & Capabilities: Club member directory, pass subscriptions, access permissions, and account management.  
* Components & Flows: Package cards display, \+ Add Member trigger, \+ New Package trigger, and the Complete Rules modal.  
* **Patterns & Controls:** Filterable data tables, plan tier pills, status badges, avatar displays, and slide-over member profile drawers.

# **2.3 Finance (/finance/)**

* Purpose & Modules: Revenue reporting, transaction ledgers, bank settlements, and billing configurations structured across four sub-views:  
  * Earnings: KPI summary cards and revenue trend analytics.  
  * Monthly Statement: High-density accounting ledgers with CSV export capabilities.  
  * Bank Payout: Bank account parameters, payout schedules, and settlement history logs.  
  * Billings & Plans: Portal subscription tier details, invoicing history, and payment methods.  
* Key Patterns: Metric summary cards, date-range pickers, right-aligned monetary values (€ formatted to 2 decimal places), and status pills.

# **2.4 Settings (/settings/)**

* Purpose & Sub-modules: System setup, user administration, and operational policy configurations across sub-paths:  
  * Availability (/availability/): Venue operating hours, recurring availability grids, and blackout date overrides.  
  * Sports Rules: Sport-specific booking configurations, court dimension settings, and game play parameters.  
  * Manage Users (/manage-user/): Staff directory, account invitations, and active user profile toggles.  
  * Roles & Permissions (/role-permissions/): Permission matrix, custom role definitions, and access controls.  
  * Coaches: Instructor directory, rostering schedules, and lesson assignment links.

# **2.5 Review (/review/)**

* Purpose & Sections: Customer feedback management and quality monitoring across two sub-sections:  
  * Club Review: Overall venue ratings, service feedback, and management response threads.  
  * Asset Review: Court-specific quality reports, maintenance feedback, and condition ratings.  
* Patterns & Controls: Star rating indicators, expandable review feeds, reply drawers, and flag content modals.

# **2.6 Common Module Operational States**

* Active State: Populated tables/grids, interactive controls, real-time counters, active status badges.  
* Empty State: Centered prompt graphics (40px icon in \#94A3B8 inside a 48px \#F1F5F9 circle), explanatory subtitle, and clear primary CTA trigger.  
* Error State: Red warning banners (\#FFEBEE background, \#E53935 text), inline form field error messages, and retry/reset action buttons.

---

# **3\. Global Design System Tokens (Exact Live Audit)**

# **3.1 Color Tokens**

| Token Name | Hex Code | Application / Role |
| :---- | :---- | :---- |
| `color-primary` | `#0080FF` | Primary CTA, active tabs, focus rings, toggles |
| `color-primary-hover` | `#0066CC` | Deep Blue hover state for primary buttons |
| `color-header-ice` | `#E8F4FD` | Brand Surface / Card Header Ice Blue background strip |
| `color-success-fill` | `#E8F8F0` | Success status badge background fill |
| `color-success-text` | `#27AE60` | Success status badge label and border color |
| `color-warning-fill` | `#FDF2E9` | Warning alert / badge background fill |
| `color-warning-text` | `#E67E22` | Warning text label color |
| `color-warning-border` | `#FFE0B2` | Warning container border color |
| `color-danger-fill` | `#FFEBEE` | Destructive action / error background fill |
| `color-danger-text` | `#E53935` | Destructive button text, error messages, out-of-order labels |
| `color-bg-canvas` | `#F8F9FA` | Main canvas background |
| `color-bg-surface` | `#FFFFFF` | Card body, modal, header, and panel white background surface |
| `color-border-neutral` | `#E2E8F0` | Card borders, header divider lines, table row borders |
| `color-border-input` | `#D0D5DD` | Form input borders, neutral cancel button border |
| `color-text-primary` | `#1E293B` | Primary headings, title text, body main text |
| `color-text-secondary` | `#475569` | Secondary labels, descriptions, table header text |
| `color-text-muted` | `#8C98A4` | Footer copy, placeholders, disabled text states |

# **3.2 Typography Scale**

Primary Font Family: Inter, sans-serif across all UI components.

| Typography Level | Size (px) | Font Weight | Line Height | Target Color | Token Token |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **H1 (Page Titles)** | 24px | Bold (700) | 1.20 | \#1E293B | `font-h1` |
| **H2 (Section Titles)** | 18px | SemiBold (600) | 1.25 | \#1E293B | `font-h2` |
| **H3 (Card Headers)** | 16px | SemiBold (600) | 1.25 | \#1E293B | `font-h3` |
| **Body (Normal Text)** | 14px | Regular (400) | 1.40 | \#1E293B | `font-body` |
| **Body SemiBold** | 14px | SemiBold (600) | 1.40 | \#1E293B | `font-body-semibold` |
| **Inset Label** | 12px | Medium (500) | 1.00 | \#475569 | `font-label-inset` |
| **Caption** | 12px | Regular (400) | 1.30 | \#8C98A4 | `font-caption` |
|  |  |  |  |  |  |

# **3.3 Spacing & Grid System**

All layouts and containers align to the following audited grid and spacing standards:

| Layout Metric | Audited Standard Value | Application Scope |
| :---- | :---- | :---- |
| `canvas-max-width` | 1200px | Centered global page viewport container |
| `card-padding` | 16px / 24px | Internal surface card and panel padding |
| `form-row-gap` | 16px | Vertical spacing between consecutive form rows |
| `column-gap` | 20px | Horizontal separation between grid columns and fields |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

# **3.4 Border Radii Tokens**

| Component Group | Radius Specification | Audited Application |
| :---- | :---- | :---- |
| `Buttons` | 6px – 8px | Primary CTA, Secondary outline, and Cancel action triggers |
| `Inputs & Dropdowns` | 8px | Inset-label text inputs, select dropdown menus, pickers |
| `Cards & Modals` | 12px | Surface cards, dialog modals, slide-over sheet containers |
| `Status Pills` | 9999px | Pill badges, active status indicators, toggle tracks |
|  |  |  |

# 

---

# **4\. Standardized Component Library**

# **4.1 Buttons**

Buttons follow exact visual hierarchy rules across all portal screens:

Primary CTA:       \[  Confirm Booking  \]  \--\> Solid Primary Blue (\#0080FF), White Text (\#FFFFFF)

Secondary Outline: \[  View Details \-\> \]  \--\> Outline 1px Primary Blue (\#0080FF), Blue Text (\#0080FF)

## **Button Hierarchy Specifications**

| Button Type | Background Fill | Text Color | Border Style | Usage Rule |
| :---- | :---- | :---- | :---- | :---- |
| **Primary CTA** | `#0080FF` | `#FFFFFF` | None | Main call-to-action trigger per section/modal. Limited to 1 per view. |
| **Secondary Outline** | `#FFFFFF` | `#0080FF` | 1px solid \#0080FF | Secondary actions, filter triggers, export actions. |
| **Neutral Cancel** | `#FFFFFF` | `#1E293B` | 1px solid \#D0D5DD | Modal cancel buttons, dismiss triggers (remediating legacy pink/orange \#FFF0ED). |
| **Destructive** | `#FFEBEE` | `#E53935` | None | Destructive deletions, asset removals, rule cancellations. |

* **Do:** Enforce Title Case across all button labels (e.g., `Save Settings`).  
* Don't: Use ALL CAPS on modal button labels (e.g., remediate SAVE SETTINGS to Save Settings).  
* Don't: Place multiple solid Primary CTA buttons in the same modal or card group.

# **4.2 Inset-Label Form Fields**

Single-line input fields adopt the Inset-Label structure where the uppercase text label breaks and resides directly inside the top field border.

\+--- COURT NAME \---------------------------+

| Center Court 1                           |

\+------------------------------------------+

## **Field Tokens & Specifications**

* Border & Radius: 1px solid \#D0D5DD border with 8px radius.  
* Label Styling: 12px Medium (500), Uppercase, \#475569 color breaking top border.  
* Value Text Styling: 14px Regular (400), \#1E293B color.  
* Focus State: 1px solid \#0080FF border with active focus ring.

# **4.3 Toggle Switches**

Interactive controls for instantaneous setting switches (e.g., Active/Inactive, Online/Offline).

* **Track Dimensions:** 44px x 24px pill shape (9999px radius).  
  * Off State Track: \#E2E8F0 fill with white circular thumb thumbed left.  
  * Active On State Track: Solid Primary Blue (\#0080FF) fill with white circular thumb transitioned right.

# **4.4 Cards & Surface Containers**

Cards group information into structured surface containers:

* **Header Strip:** Ice Blue surface strip (\#E8F4FD) housing card title (16px SemiBold \#1E293B) and a 3-dot action menu trigger (⋮).  
* Body Surface: White surface (\#FFFFFF) with 16px/24px internal padding.  
* Container Border & Radius: 1px solid \#E2E8F0 border with 12px rounded corner radius.

# **4.5 Status Badges**

Compact status pills (9999px radius) providing immediate operational feedback:

| Status Type | Background Fill | Text Color | Border Style | Sample Value |
| :---- | :---- | :---- | :---- | :---- |
| **Success / Active** | `#E8F8F0` | `#27AE60` | None | Active / Confirmed |
| **Warning / Pending** | `#FDF2E9` | `#E67E22` | 1px solid \#FFE0B2 | Pending / In Review |
| **Danger / Out of Order** | `#FFEBEE` | `#E53935` | None | Inactive / Out of Order |
| **Neutral / Draft** | `#F8F9FA` | `#475569` | 1px solid \#E2E8F0 | Draft / Archived |

# **4.6 Alert Banners & Empty States**

Feedback banners and empty state views follow exact live audit parameters:

* **Alert Banner Specs:**  
  * *Warning Banner:* \#FDF2E9 fill, 1px solid \#FFE0B2 border, \#E67E22 text.  
  * Error Banner: \#FFEBEE fill, \#E53935 text.  
* Empty State Component Specs:  
  * *Graphic Element:* 40px icon rendered in \#8C98A4 placed inside a 48px \#F8F9FA circular container.  
  * Copy & Action: 16px SemiBold title (\#1E293B), 14px Regular subtitle (\#475569), and an optional Primary CTA button below.

---

# **5\. Standard Page Templates & Layout Skeletons**

# **Template A: Multi-Step Configuration Layout**

* Application: Booking rules builder, multi-tiered pricing schedules, onboarding flows.  
* Skeleton Structure:  
  * **Header:** Title, Subtitle, Step indicator bar, Save draft button.  
  * Body Split Container: Left-hand step progression list; right-hand inset-label form panel (1200px container width).  
  * Footer Action Bar: Right-aligned Neutral Cancel button and Primary CTA button (\#0080FF).

# **Template B: Directory / Card Grid Layout**

* Application: Manage Assets directory, Equipment catalogue, Membership package cards.  
* Skeleton Structure:  
  * **Control Header:** Title, search input, filter dropdown triggers, view toggles, Primary CTA (+ Add Asset / \+ New Package).  
  * Card Grid: Responsive grid (20px column gap) of surface cards featuring Ice Blue header strips (\#E8F4FD) and 3-dot action menus (⋮).

# **Template C: Tabular Management Layout**

* Application: Member directory, Monthly Statement ledgers, Earnings, Review logs.  
* Skeleton Structure:  
  * **Summary Bar:** Metric summary cards displaying key totals, earnings, or active subscriber counts.  
  * Action Bar: Inset-label search input, date range pickers, Secondary Outline Export CSV button, and Primary CTA (+ Add Member).  
  * Data Table: Full-width table with \#E2E8F0 borders, uppercase 12px header text (\#475569), status badges, and right-aligned € prices (formatted to 2 decimal places).

# **Template D: Modal Flow Layout**

* Application: Complete Rules modal, quick asset edits, check-in drawers, review reply dialogs.  
* Skeleton Structure:  
  * **Overlay Container:** 12px rounded corner modal surface over a dark backdrop.  
  * Header: Modal title (18px SemiBold \#1E293B) and close trigger (X).  
  * Body: Inset-label form fields (16px row gap) and toggle switches.  
  * Footer Action Pair: Right-aligned Neutral Cancel button (1px \#D0D5DD border, Title Case) and Primary CTA button (\#0080FF solid, Title Case).

---

# **6\. Consistency Audit & Remediation Matrix**

This matrix identifies live portal interface discrepancies and mandates exact design system corrections:

| Interface Domain | Live Interface Discrepancy Found | Mandated Standardized Correction |
| :---- | :---- | :---- |
| **Sub-navigation Pattern** | Inconsistent sub-navigation controls across modules (mixing multi-step wizard bars, horizontal tabs, and segmented pills). | Standardize module sub-navigation to clean horizontal sub-navigation tabs anchored by the Primary Blue (\#0080FF) active underline indicator. |
| **Cancel Button Paradigm** | Legacy pink/orange tint (\#FFF0ED) used for modal cancel buttons across several settings dialogs. | Remediate all cancel actions to the Neutral Cancel button standard (1px \#D0D5DD border, \#FFFFFF background, \#1E293B text). |
| **Button Label Casing** | UPPERCASE text casing used on modal submit buttons (e.g., SAVE SETTINGS, CANCEL). | Enforce strict Title Case on all button labels across modals and pages (e.g., Save Settings, Cancel). Reserve UPPERCASE exclusively for Inset Field Labels. |
| **Price Formatting** | Inconsistent currency symbols and decimal precisions across pricing tables and finance logs. | Standardize all financial amounts and court rate displays to exactly 2 decimal places with the € currency symbol (e.g., €25.00). |
|  |  |  |
|  |  |  |
|  |  |  |

---

# **7\. Wireframe Production Guidelines**

# **7.1 Component Selection Hierarchy**

When assembling wireframes for new admin sub-features, select controls strictly in this order:1. Navigation Shell \--\> Wrap in 64px Header (PayoutTest, Booking, Membership, Finance, Settings, Review)

2\. Page Template    \--\> Select Template A, B, C, or D based on task requirements

3\. Container        \--\> Apply Ice Blue header cards (\#E8F4FD header strip, 12px radius, \#E2E8F0 border)

4\. Form Inputs      \--\> Deploy Inset-Label Fields (12px uppercase label, 8px radius, \#D0D5DD border)

5\. Action Triggers  \--\> Insert Primary CTA (\#0080FF solid), Secondary Outline (\#0080FF border), or Neutral Cancel (1px \#D0D5DD)

# **7.2 'Closest Existing Feature' Lookup Table**

Map planned administrative sub-features directly to live platform layout patterns:

| Planned New Feature | Map Layout & Pattern To | Recommended Template |
| :---- | :---- | :---- |
| **Coach & Instructor Rostering** | **Settings \-\> Coaches** (Staff list \+ schedule grid) | Template C (Tabular Management Layout) |
| **Automation Light & Power Rules** | **Booking Management \-\> Booking Rules** (Time window overrides & rule matrix) | Template A (Multi-Step Configuration Layout) |
| **Locker Rental Management** | **Booking Management \-\> Equipment** (Stock counters & check-in drawer) | Template B (Directory / Card Grid Layout) |
| **Promotion & Discount Engine** | **Booking Management \-\> Pricing & Cancellation** (Tier rates & overrides) | Template A (Multi-Step Configuration Layout) |
| **Court Incident Reporting** | **Review \-\> Asset Review** (Feed list \+ reply modal flow) | Template D (Modal Flow Layout) |

# **7.3 8-Point Authoring Checklist**

Verify compliance against these 8 structural audit rules before completing screen specs:

- [ ] **Viewport Container:** Layout resides in the 1200px centered container over a \#F8F9FA background.  
- [ ] Header Integration: Top bar retains 64px height with tenant "PayoutTest" and active navigation item highlight.  
- [ ] Typography Token Compliance: Inter font used exclusively (H1 24px, H2 18px, H3 16px, Body 14px, Inset Label 12px).  
- [ ] Inset-Label Precision: All text fields deploy inset labels breaking top \#D0D5DD borders with 8px radius.  
- [ ] Exact Color Fidelity: Strictly use Primary Blue \#0080FF, Ice Blue \#E8F4FD, and defined status colors (\#27AE60, \#E67E22, \#E53935).  
- [ ] Button Casing & Paradigms: All buttons strictly use Title Case. Modal cancels use Neutral 1px \#D0D5DD outline.  
- [ ] Price Formatting Standardization: All monetary displays format to 2 decimal places with € symbol.  
- [ ] Remediation Check: Screen avoids legacy sub-navigation discrepancies and pink cancel buttons.

# **7.4 Reusable Wireframe Prompt Template**

Use this standardized text prompt template when generating wireframes for new portal screens:\#\#\# UI/UX Wireframe Specification \-- ShallWe-Play Portal

\*\*Module Name:\*\* \[Insert Module Name & URL Path\]

\*\*Target Template:\*\* Template \[A/B/C/D\] (\[Template Name\])

\*\*Primary User Goal:\*\* \[Insert Goal\]  
\*\*1. Global Header & Container Specs:\*\*

\* Header: 64px White Header (\#E2E8F0 border, tenant "PayoutTest", nav bar, user avatar with green dot)

\* Canvas: 1200px centered container on \#F8F9FA canvas background

\* Sub-Navigation: Horizontal tabs with Primary Blue (\#0080FF) active underline indicator

\* Page Title: \[Insert Title\] (font-h1, 24px Bold Inter, \#1E293B)  
\*\*2. Interface Component Layout:\*\*

\* Surface Containers: Cards with Ice Blue header strip (\#E8F4FD), 3-dot action menu (⋮), 12px radius, \#E2E8F0 border

\* Inputs & Controls: Inset-label fields (12px uppercase label, 8px radius, \#D0D5DD border), 44x24 pill toggle switches (\#0080FF active)

\* Status Badges: Pill badges (Active \#E8F8F0/\#27AE60, Pending \#FDF2E9/\#E67E22, Danger \#FFEBEE/\#E53935)  
\*\*3. Action Triggers & Pricing:\*\*

\* Primary Action: \[Insert CTA Label\] (\#0080FF solid button, Title Case)

\* Cancel Action: Neutral Cancel button (1px \#D0D5DD border, Title Case)

\* Monetary Values: Formatted to 2 decimal places with € symbol  
