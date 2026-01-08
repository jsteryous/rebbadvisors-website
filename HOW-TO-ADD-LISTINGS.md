# How to Add New Listings - QUICK GUIDE

## Step 1: Open listings.html in VS Code

## Step 2: Find the "LISTING TEMPLATE" comment (around line 295)

## Step 3: Copy this entire block (from `<div class="listing-card"...` to its closing `</div>`)

```html
<div class="listing-card" data-industry="service" data-price="750000" data-location="sc">
    <span class="status-badge new">New Listing</span>
    <div class="listing-header">
        <div class="listing-id">Listing #2025-001</div>
        <h3 class="listing-title">Established HVAC Service Company</h3>
        <div class="listing-location">Greenville, SC</div>
    </div>
    <div class="listing-details">
        <div class="detail-row">
            <span class="detail-label">Asking Price</span>
            <span class="detail-value price-highlight">$750,000</span>
        </div>
        <div class="detail-row">
            <span class="detail-label">Annual Revenue</span>
            <span class="detail-value">$1.2M</span>
        </div>
        <div class="detail-row">
            <span class="detail-label">Cash Flow</span>
            <span class="detail-value">$285K</span>
        </div>
        <div class="detail-row">
            <span class="detail-label">Established</span>
            <span class="detail-value">2008</span>
        </div>
    </div>
    <div class="listing-description">
        Well-established HVAC service and installation company serving residential and commercial clients. Strong recurring maintenance contracts, experienced team of 8 technicians, excellent reputation in the community.
    </div>
    <div class="listing-footer">
        <button class="inquiry-btn" onclick="inquire('2025-001')">Request Information</button>
    </div>
</div>
```

## Step 4: Paste it right after the last listing (before the `</div>` that closes `listings-grid`)

## Step 5: Update these fields:

### A) Top line attributes (for filtering):
- `data-industry="service"` → Options: retail, service, manufacturing, technology, hospitality, healthcare
- `data-price="750000"` → Numbers only, no commas
- `data-location="sc"` → Options: sc, nc, ga

### B) Status badge (optional):
- Remove entire `<span class="status-badge new">New Listing</span>` line if not needed
- Or change to: `<span class="status-badge pending">Under LOI</span>`

### C) Content to update:
- `Listing #2025-001` → Your listing number
- `Established HVAC Service Company` → Business name/type
- `Greenville, SC` → Location
- `$750,000` → Asking price
- `$1.2M` → Annual revenue
- `$285K` → Cash flow
- `2008` → Year established
- Description paragraph → Your description
- `onclick="inquire('2025-001')` → Match your listing number

## Step 6: Save the file

## Step 7: Push to GitHub

```powershell
git add listings.html
git commit -m "Add new listing #2025-XXX"
git push
```

Render will auto-deploy in 1-2 minutes!

---

## Tips:

- Keep descriptions to 2-3 sentences max
- Always use consistent formatting for prices ($XXXk or $X.XM)
- Remove status badge for regular listings
- To remove a listing: just delete the entire `<div class="listing-card">...</div>` block
- To update a listing: just edit the values directly

## Common Industries:
- retail
- service
- manufacturing
- technology
- hospitality
- healthcare

## Common Locations:
- sc (South Carolina)
- nc (North Carolina)
- ga (Georgia)

Add more options in the filter dropdowns if needed (lines 310-345 in listings.html)
