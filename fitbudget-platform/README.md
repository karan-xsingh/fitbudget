# FitBudget

**Build muscle. Spend smarter.** FitBudget is a responsive, zero-backend-cost starter web app for affordable Indian meal planning, nutrition logging, workouts, and simple progress tracking.

## What's included

- Overview dashboard with calories, protein, estimated food spending, and workout status.
- Food diary with common Indian foods, portion multipliers, meal categories, macros, and estimated cost.
- Budget-first meal ideas with vegetarian / egg / chicken filters and cost/protein comparisons.
- Beginner bodyweight / backpack workout templates with completion tracking.
- Seven-day activity view, weekly insights, and optional weight check-ins.
- Editable profile and estimated calorie/protein starting targets.
- Responsive layout for desktop and mobile.
- Local persistence through browser `localStorage`; no account or API key required.

## Run locally

No build tools are required.

1. Download or clone this repository.
2. Open `index.html` in a browser, or run a local static server from this folder:

   ```bash
   python -m http.server 5500
   ```

3. Visit `http://localhost:5500`.

## Deploy to GitHub and Vercel

### GitHub

1. Create a new empty repository on GitHub.
2. Extract this project folder.
3. In a terminal inside the extracted folder, run:

   ```bash
   git init
   git add .
   git commit -m "Build FitBudget starter platform"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   git push -u origin main
   ```

4. Replace the placeholder remote URL with your repository URL.

### Vercel

1. Sign in to Vercel and choose **Add New → Project**.
2. Import the GitHub repository.
3. Framework preset: **Other** (static site).
4. Build command: leave blank.
5. Output directory: `.` (project root).
6. Deploy.

`vercel.json` is included for clean static deployment. You can also use Vercel's CLI if installed: `vercel` from this folder.

## Important limitations — read before sharing publicly

- This version is a **front-end MVP**, not a production multi-user service. Data is stored only in the current browser/device. It will not sync across devices, and clearing browser data can remove it.
- There is no cloud database, account system, password recovery, admin dashboard, or server-side authorization yet.
- Food nutrition and prices are approximate reference estimates. Verify serving sizes and update prices to match your region. Unknown custom foods are added with zero nutrition rather than invented values.
- Calorie/protein targets are rough general estimates, not medical advice. The app is not suitable for medical nutrition therapy.
- Workout templates are general beginner examples; users should adapt exercises to their ability and stop if they experience pain.
- Free hosting/provider limits and terms can change.

## Before a real startup launch

1. Interview target users and test repeat use.
2. Validate the nutrition database and price assumptions with local sources.
3. Add a secure backend and database (for example, Supabase) before implementing user accounts or cross-device sync.
4. Add automated tests, error handling, data export/deletion, privacy disclosures, and accessibility checks.
5. Get qualified review for health-related recommendations and avoid medical claims.

## Customization

- `index.html`: page structure and copy.
- `styles.css`: visual design and responsive layouts.
- `app.js`: food catalog, meal ideas, target estimates, interactions, and local storage.

To add foods, update the `foodCatalog` array near the top of `app.js`. Values are per the reference serving listed in `serving`; prices are estimates in INR per serving.

## Immersive UI update

The current interface includes CSS-built floating dumbbells and kettlebell artwork on the dashboard, a floating food-orbit scene in Meal Planner, and an interactive exercise motion lab in Workouts. Tap Squat, Bicep curl, Push-up, or Deadlift to switch the animated visual study. These are stylized CSS animations, not recorded videos or biomechanically accurate exercise demonstrations.

A creator bio appears at the bottom of the app. Open **Your profile** and edit **Your Builder Profile** to change the displayed name, role, and bio. The creator details are saved with the app's browser-local profile state.

### Motion and accessibility

The UI respects `prefers-reduced-motion` and reduces animations when a visitor has that operating-system preference enabled. The exercise animation is for visual interest only; it should not be treated as form coaching.
