# F1 Race Results Web App

A public-facing web application to view Formula 1 race results with driver and constructor information.

## Features

- **Browse Race Results**: View F1 race results with driver names, constructor names, and finishing positions
- **Filter by Season**: Filter results by F1 season/year
- **Search**: Search for specific drivers or races
- **Race Details**: Click any race result to see full details including lap counts and times
- **Responsive Design**: Works on desktop and mobile devices

## Tech Stack

- React 18 (via CDN)
- HTML5 & CSS3
- Papa Parse for CSV parsing
- GitHub Pages for hosting

## Local Development

Simply open `index.html` in your web browser to run the app locally. The app loads CSV files from the `public/` directory.

### Requirements
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No build process or dependencies needed

## Project Structure

```
.
├── index.html                # Main application file
├── public/                   # CSV data files
│   ├── results.csv
│   ├── drivers.csv
│   ├── constructors.csv
│   ├── races.csv
│   └── ...other data files
├── .github/
│   └── workflows/
│       └── deploy.yml        # GitHub Pages deployment workflow
└── README.md
```

## Data Structure

The app combines three main CSV files:
- **results.csv**: Race results with driverId, constructorId, raceId, position, points
- **drivers.csv**: Driver information with driverId, forename, surname
- **constructors.csv**: Constructor information with constructorId, name
- **races.csv**: Race information with raceId, name, year, date

## Deployment to GitHub Pages

### Setup Instructions

1. **Create a GitHub Repository**
   - Go to [GitHub.com](https://github.com)
   - Create a new repository named `f1-results-app` (or your desired name)

2. **Push Code to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: F1 Race Results app"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/f1-results-app.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository settings
   - Navigate to "Pages" section (under Code and automation)
   - Select "Deploy from a branch"
   - Choose `gh-pages` branch and root directory
   - Save

4. **Automatic Deployment**
   - The GitHub Actions workflow will automatically:
     - Trigger on every push to `main` branch
     - Deploy the files to the `gh-pages` branch
     - Make your site available at `https://YOUR_USERNAME.github.io/f1-results-app/`

### Updating the App

To update the app:
1. Make changes to the files locally
2. Commit and push to GitHub: `git push origin main`
3. GitHub Actions will automatically deploy the changes
4. Your site will update within 1-2 minutes

## Usage

1. **Filtering**: Use the season dropdown to filter results by year
2. **Search**: 
   - Type a driver name in the "Search Driver" field (e.g., "Lewis Hamilton")
   - Type a race name in the "Search Race" field (e.g., "Monaco Grand Prix")
3. **View Details**: Click any race result row to see the full race results with all drivers, constructors, laps, and times
4. **Reset**: Click "Reset" to clear all filters and search terms

## Notes

- The app loads all CSV data at startup for fast searching and filtering
- No backend server required - everything runs in the browser
- Data is not stored; the page must be refreshed to reload data
- Compatible with older styles of CSV data formatting (handles \N and null values)

## License

This project uses F1 historical race data for educational purposes.
