# Family Table

A family-friendly weekly meal planner. One static page (`index.html`), no build step.

## Deploy to Vercel
1. Vercel dashboard > Add New > Project > import this repo.
2. Framework Preset: **Other**. Leave Build Command and Output Directory empty. Root Directory: `./`.
3. Deploy.

## Data
Dishes, household and weekly plans live in Supabase (tables `ft_dishes`, `ft_meal_ideas`, `ft_household`, `ft_weeks`). The first visit copies the starter dishes into the tables. If Supabase can't be reached, the app falls back to browser storage.

The project URL and publishable key are set at the top of the `cloud.js` section inside `index.html` (`SB_URL`, `SB_KEY`). The publishable key is meant to be public. Never put a secret or service-role key in this file.

The tables allow anyone with the site link to read and edit, so share the link only with family.

Optional: put dish photos in `images/`.
