# Dubai AI Platform — Edit Guide
## Files Overview
- `index.html` — Complete platform (all HTML, CSS, JS in one file)

---

## 🎨 COLORS — Change Brand Colors
Find at top of `<style>` tag:
```css
--gold: #C9A96A;       /* Main gold accent */
--gold-light: #E8C98A; /* Lighter gold */
--bg: #0B0B0B;         /* Page background */
--card: #151515;       /* Card background */
```

---

## 🏢 COMPANY NAME
Search & replace: `Dubai Luxury Real Estate` → Your agency name
Search & replace: `Dubai Luxury RE · AI` → Your short brand

---

## 💰 PRICING — Change Plans
Search for `AED 3,000`, `AED 6,000`, `AED 12,000`
Edit the feature list `<li>` items under each plan.
Plan names: Search `STARTER`, `GROWTH`, `ELITE`

---

## 🗺️ MAP LEADS — Customize Lead Data
In the `<script>` section, find:
```js
const dubaiLocations = [ ... ]  // Add/remove areas
const buyerNames = [ ... ]       // Change demo names
const propTypes = [ ... ]        // Change property types
const budgets = [ ... ]          // Change budget ranges
const sources = [ ... ]          // Change lead sources
```

Lead spawn timing (currently 5–8 seconds):
```js
const delay = 5000 + Math.random() * 3000;
```
Change `5000` = minimum ms, `3000` = random add-on ms.

---

## 📞 AI CALL SCRIPT — Edit Conversation
Find `const script = [` inside `openAICallModal()`:
```js
{ role: 'ai',   text: "Hello Ahmed..." },
{ role: 'user', text: "I'm looking for..." },
```
Edit `text:` values to change what AI and customer say.

---

## 💬 WHATSAPP SCRIPT — Edit Messages
Find `const waScript = [`:
```js
{ type: 'r', text: "...", time: '10:42 AM' },  // r = received (customer)
{ type: 's', text: "...", time: '10:42 AM' },  // s = sent (AI)
```

---

## 📊 ANALYTICS — Change Numbers
Find the 4 metric cards in `#analytics` section:
- `184` → leads this month
- `160` → AI calls handled
- `42`  → viewings booked
- `11`  → deals closed

Chart data — find `new Chart(document.getElementById('leadChart'` etc.
Edit the `data: [4,8,12,9,16,14,20]` arrays.

---

## 🏗️ PIPELINE STAGES — Change Columns
Find `const pipelineStages = [`:
```js
{ title: 'New Lead', count: 8, color: '#3B82F6' },
```
Change `title`, `count`, and `color` per stage.

---

## 🖼️ HERO BACKGROUND IMAGE
Find in CSS:
```css
url('https://images.unsplash.com/photo-1546412414-e1885259563a?w=1800&q=80')
```
Replace with your own image URL or local file path.

---

## 📋 CRM FIELDS — Change Auto-Fill Labels
Find in HTML `id="crm-panel"`, the `.crm-label` divs:
- LEAD NAME, BUDGET, LOCATION, PROPERTY TYPE, VIEWING DATE, LEAD SOURCE, STATUS

---

## 🚀 DEPLOYING
1. Open `index.html` directly in any browser — no server needed
2. For hosting: upload to any static host (Netlify, Vercel, GitHub Pages)
3. Just drag the single `index.html` file
